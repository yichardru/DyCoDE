# Dynamic Companion Dialogue Engine (DyCoDE)

I have no idea why I made this, probably cuz I got bored and played too much dating sims, anyway...
DyCoDE is a modular frontend/backend system for building emotionally reactive, AI-powered NPC dialogue.

---

## ✨ Overview

DyCoDE aims to replace static dialogue trees with dynamic, memory-driven interactions.  
Using lightweight LLMs (1B–3B parameters) and persistent emotional states (trust, respect, fear, betrayal),  
NPCs can evolve their behavior and conversation tone naturally over time based on player actions.

DyCoDE supports dynamic voice responses via real-time TTS fallback, maintains long-term companion memory profiles and is built with performance optimizations suitable for consumer hardware.

*(This is a high-level overview — much more happens under the hood, including token management, emotional decay, major event tracking, and system prompt construction.)*

---

## ⚙️ Key Features

- **Memory-Based Relationship Evolution**  
  Track Trust, Respect, Fear, Betrayal, Affection, and adjust NPC dialogue accordingly.

- **Dynamic Dialogue Generation Using Lightweight LLMs**  
  1B–3B parameter models used for fast, responsive, memory-aware conversation generation.

- **Integrated TTS (Text-to-Speech) Fallback**  
  Optional dynamic voice generation for dialogue responses, with caching and failover.

- **Persistent NPC Memory System**  
  NPCs remember player interactions over time, shaping moods and emotional context dynamically.

- **Frontend/Backend Modular Architecture**  
  Separate modules for Dialogue Management, AI Inference, Postprocessing, TTS Handling, and Memory Management.

---

## 🚀 Performance Notes

- DyCoDE is designed around **small token budgets per conversation** (e.g., 256 input tokens, 30–60 output tokens).
- Transformer inference behaves **approximately linear (O(n))** with respect to sequence length for fixed-size models.
- On an **RTX 3060 (12GB)** running 4-bit quantized models:
- Estimated generation time for 30–60 tokens = **~200–500ms**.
- NPC replies remain responsive enough for real-time gameplay, matching normal human dialogue pacing.

---

## 📚 Project Status

This is currently a **high-level system architecture** — not a full working prototype (yet).  

I am not a professional software developer — if you are interested, pls help.

---
