# Jupyter: History and Internals

This are my notes from Jupyter’s Architecture Unpacked (with Afshin Darian & Sylvain Corlay) from channel Developer Voices (Kris Jenkins)
https://www.youtube.com/watch?v=_-zhMzwpSOQ

## Origin of the Name

Jupyter came from the IPython project. When they started working on language-agnostic features, they wanted to remove "Python" from the name. They named it after the three biggest languages they were targeting at the time: **Ju**lia, **Pyt**hon, and **R** → **Ju-Pyt-R**.

## Jupyter's Purpose and Users

Jupyter is the frontend to analytical tools in the ecosystem and a way of sharing exploratory analysis. It's used for:
- Sending notebook files
- Generating dashboards with low code
- Providing a REPL interface with richer output
- Education
- Exploratory coding
- Multiple programming languages

**Key user demographic**: People who write code but aren't software developers—scientists, educators, mathematicians, physicists. They write scientific code, not applications for the general public. Jupyter lowers the overhead so they can jump straight into what they're good at.

The project was named in 2014 when it wasn't clear which analytical language would dominate. While Python became the largest community, Jupyter remains committed to its language-agnostic architecture.

## Jupyter for Communication

Jupyter Notebooks serve as a communication medium. You can send them by email or deploy via Binder.

**Prime example**: LIGO project used Jupyter Notebooks to publish all data processing and signal processing work related to detecting gravitational waves. This allowed others to:
- Run the analysis
- See exactly what was done
- Tweak and verify results

Instead of sharing static PDFs or CSVs, sharing the actual notebook means analysis and its answers are in the same place. Jupyter natively understands LaTeX snippets inside cells for equations.

## Adoption in Finance

Jupyter is very popular in financial institutions—banks and funds. Often as many people have Jupyter open as have spreadsheet software. Users typically have backgrounds in mathematics, finance, or physics, not necessarily software engineering.

Hedge funds support Jupyter because quantitative analysts use it to drive buying/selling decisions. Finance firms recruit people already trained on these tools.

## Jupyter Architecture: How It Works

When you hit Shift+Enter to run a cell:
1. A message is sent to the backend server
2. The kernel executes your code
3. A message is sent back to the frontend for display

This follows a well-defined, language-agnostic protocol. The frontend doesn't know what language the kernel is executing.

### Communication Protocol

- The protocol uses **ZeroMQ** (open-source)
- Provides a language-agnostic way to communicate with a process
- Fast and allows servers/kernels in any language
- Both sides just need to agree on the messaging protocol

**WebSocket connection**: The frontend communicates with the Jupyter backend over WebSockets, which then talks to the kernel via ZeroMQ channels.

### Kernel Architecture

- 60+ language kernels available
- The kernel is responsible for executing code
- It's completely agnostic to the frontend (notebook, console, etc.)
- Kernels follow the same lifecycle, mediated by a server

## Building a New Kernel

To implement a new language kernel, you need to:
1. Implement multiple message types
2. Handle message signing
3. Implement concurrency requirements
4. Process messages while code is running

**Xeus project**: A C++ implementation of the protocol that helps create kernels. You override a few language-specific methods. Most kernels embed the language interpreter (Python, R) in a C++ process.

### Message Types

- **Control messages**: Kernel lifecycle (shut down, restart) and debug messages
- **Execution requests**: Main channel for running code
- **Inspect requests**: Getting docstrings and class information

The kernel must be multi-threaded or have concurrency to:
- Process control messages while code runs
- Handle stop/interrupt messages

### LSP (Language Server Protocol)

LSP provides static analysis of the workspace:
- Inline warnings
- Auto-complete suggestions
- Treats code as text (doesn't execute it)

LSP and kernel complement each other:
- Kernel provides runtime information
- LSP provides static analysis
- Both can provide auto-complete suggestions

### LLM Integration

Jupyter AI allows LLM suggestions. LLMs are standalone services and not part of the kernel. There are proposals to expand the kernel protocol with a new channel for AI/machine clients.

## Security Concerns

The core feature of Jupyter is arbitrary code execution as a service. You cannot assume any limiting to code that will be run.

**Attack scenarios**:
- Cloud provider protecting itself from users
- Protecting users from each other (with sharing features)
- Collaborators in the same document

**Mitigations**:
- Cloud services treat user code as hostile by default
- Isolated Docker environments
- VMs (mybinder.org spins up a VM per user)
- WASM-based execution in the browser (no filesystem to destroy)
- Rich content display may run JavaScript—must be isolated

## Execution Model

- Jupyter is essentially "REPL as a service"
- One execution thread unless you create your own threads
- Control threads exist for debugging and monitoring

**Concurrent execution**: The notebook runs code sequentially. You can write threaded code or use libraries like Dask. There are projects that detect independent cells and run them in parallel, but this hasn't landed in core Jupyter and is language-specific.

**Reconnection**: Jupyter clients can reconnect to kernels after page refresh. If you close your laptop and come back, the connection re-establishes and streaming output continues. Long-running jobs (27+ hours) are still being worked on.

---

## Jupyter as an Application Framework (Beyond Notebooks)

### Evolution

Jupyter has evolved from:
1. IPython → improved Python wrapper
2. Kernel-client architecture → language agnostic
3. Notebook → became very popular
4. Jupyter Lab → more feature-full, closer to an IDE

### Jupyter Lab as a Framework

Jupyter Lab provides primitives that aren't specific to IDEs:
- Tiled window layout
- Theming and configurable keyboard shortcuts
- Internationalization
- Extensibility with plugins
- Dependency injection system
- Command palette
- File browser
- Status bar
- Drag-and-droppable tabs
- Menu system

**Goal**: Provide a rich application framework for desktop-like experiences in the browser, competing with tools like Qt for C++ desktop apps.

### Real-Time Collaboration

Jupyter provides RTC building blocks using **YJS** (CRDT library):
- Conflict-free Replicated Data Types
- Supports text, number arrays, matrices, booleans
- Can represent JSON-like documents
- History browser for tracking changes

**Challenges**:
- CRDTs don't handle schema constraints well (e.g., "notebook must have at least one cell")
- Constraints that bind data from different parts of the document are problematic
- Better to use flatter data formats than typical XML/JSON schemas

**Undo behavior** = "last thing I did" (per user), not "last thing that happened"

**Git integration**: RTC history and Git history aren't unified yet. Separate plugins exist.

### Example Applications Built with Jupyter Framework

**Jupyter CAD**: Web-based FreeCAD-like application with real-time collaboration
- Reuses Jupyter Lab components (command palette, file browser, status bar, theming)
- Essentially a Jupyter Lab extension that handles CAD files

**Jupyter GIS**: Collaborative web-based interface for QGIS workflows
- Built with funding from ESA (European Space Agency)
- Targeted at Earth observation, sharing satellite data from Copernicus

### Documentation & Maturity

**Challenge**: Jupyter is a tall stack with varying maturity levels

**Deployment distributions** (like JupyterHub):
- "The Littlest JupyterHub" → single machine with Unix authentication
- "Zero-to-JupyterHub" → Kubernetes-based deployments
- mybinder.org → spins up VMs for users

**State of RTC**: 
- Isolated in separate package (moves faster than core Jupyter Lab)
- Harder API to learn
- One engineer built Jupyter CAD's first version alone
- Requires understanding constraints of CRDTs

**Getting Started**:
- Visit jupyterlab.readthedocs.io
- Check example applications in Jupyter Lab GitHub repo
- Look at extension and API documentation

**Use Cases**:
- Not for product websites
- Good for desktop-like internal enterprise applications
- Excellent for applications needing scripting in multiple languages
- Perfect for collaborative tools (analysts, scientists, engineers)
- Can embed any scripting language via kernels
- WASM-based languages can get a REPL working in ~3 hours

**Target sweet spot**: Applications where you want to run programming/scripting languages within the application (like FreeCAD's Python console, but more feature-full with full Jupyter notebook experience).
