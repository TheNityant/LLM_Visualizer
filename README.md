LLM Visualizer
An interactive platform for exploring LLM internals, model layers, tensors, and token-level computation.

The project is built around one idea: language models become much easier to understand when their internal structure can be inspected visually instead of treated as a black box.
<p align="center">
  <img
    src="docs/media/llm-visualizer-demo.gif"
    width="100%"
    alt="LLM Visualizer interactive demo"
  />
</p>

<p align="center">
  <sub>
    Interactive architecture, tensor, layer, projection, walkthrough, and debugger views.
  </sub>
</p>

What it explores
LLM Visualizer provides an interactive workspace for inspecting different parts of a language model and understanding how information moves through it.

The current interface demonstrates areas including:
- Model architecture — inspect the structure of the loaded model and move through individual layers.
- Layer visualization — explore transformer blocks and their position inside the network.
- Tensor inspection — browse model tensors, tensor groups, shapes, and related metadata.
- Projection views — visualize selected components and transformations spatially.
- Normalization and MLP internals — inspect intermediate operations and associated mathematical expressions.
- Attention internals — explore attention-related tensors and projections.
- Model walkthrough — move through model components in a more guided, chapter-like flow.
- Debugger workspace — inspect captured tensor information and internal model state.
Why this project exists
Most LLM tooling focuses on either using models or measuring their outputs.

LLM Visualizer approaches the problem from the opposite direction:
What is actually happening inside the model?

Instead of reducing a transformer to a diagram in a textbook, the goal is to make its architecture, tensors, layers, and intermediate computation something that can be actively explored.

This project is part of a broader effort to connect:

LLM theory → model files → tensors → computation → visual understanding
Demo
Interactive preview
The animated preview above is a condensed tour of the application.

For a more complete walkthrough, keep the full demo video alongside the repository:
docs/media/llm-visualizer-full-demo.mp4
You can link it from the README with:
[▶ View the full walkthrough](docs/media/llm-visualizer-full-demo.mp4)
The GIF is intended for immediate visual context. The MP4 preserves the detail needed to inspect the full interface.
Interface areas
Architecture
Explore the model as a sequence of transformer layers rather than a single opaque file.

The architecture view is designed to make it easier to understand:
- where a layer exists in the model,
- how deep it is,
- which component is currently selected,
- and how different transformer stages relate to one another.
Tensor Grid
Inspect tensors associated with the loaded model using a structured grid.

This makes it easier to move from:
model
  ↓
layer
  ↓
component
  ↓
tensor
without manually digging through raw model metadata.
Mathematical context
Selected model operations can be paired with their mathematical representation so that the visual interface is not separated from the underlying computation.

Examples include normalization, projection, MLP, and attention-related operations.
Walkthrough
The walkthrough view organizes model internals into a more guided exploration path.

This is intended to bridge the gap between:
- reading about transformer architecture,
- inspecting an actual model,
- and understanding how the corresponding tensors fit together.
Debugger
The debugger workspace provides a place to inspect captured internal information during model exploration.

The long-term goal is to make this useful for investigating intermediate activations, layer behavior, and other model-level diagnostics.
Project direction
LLM Visualizer is being developed toward a broader LLM engineering and learning environment, with areas such as:
- GGUF model loading and inspection,
- tensor-level exploration,
- layer and component visualization,
- token-level computation views,
- attention inspection,
- model walkthroughs,
- debugger-style internal inspection,
- and integration with an understanding-first LLM engineering notebook.
The project is intentionally evolving beyond a static architecture diagram into an interactive environment for learning, inspecting, and experimenting with language models.
Related project
LLM Engineering Notebook
The visualizer is closely related to the LLM Engineering Notebook.

The notebook focuses on structured understanding of LLM architecture and engineering, while LLM Visualizer provides the interactive visual layer for many of the same concepts.

Together, the direction is:
Theory
  ↓
Engineering notes
  ↓
Model inspection
  ↓
Interactive visualization
  ↓
Experiments
Status
This project is under active development.

The current build already demonstrates the core visual exploration workflow, while additional model-inspection and debugging capabilities are being developed progressively.
<div align="center">

Understand what's happening underneath. Then build with it.
</div>
