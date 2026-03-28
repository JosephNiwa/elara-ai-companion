Elara – Local AI Companion

Overview

Elara is a locally hosted AI companion built using Ollama, Godot, and Obsidian. She maintains a persistent personality, retrieves long-term memory, and runs entirely offline.

Tech Stack
Ollama (qwen2.5:32b)
Python (memory bridge server)
Godot 4 (frontend + interaction)
Obsidian (memory storage)

Architecture
Model Layer
Custom Ollama model with personality defined in a Modelfile

Memory Layer
Python server (memory_bridge.py)
Reads Obsidian vault
Injects relevant context into prompts

Interface Layer
Godot (ElaraBrain.gd)
Handles interaction and UI

Features
Persistent personality (no drift)
Memory retrieval from Obsidian
Session-based conversation memory
Manual memory saving ("remember that...")
Automatic journaling system
Fully local AI system

How It Runs

python3 memory_bridge.py &
ollama serve &
# Run Godot scene

What I learned
Integrating AI models with external memory systems
Context injection for better responses
Structuring multi-layer systems (AI + backend + frontend)
Managing state and persistence

Future Improvements
Animation system (AnimationTree)
Idle behaviors
Presence detection
Jellyfin integration
Notification system