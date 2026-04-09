# Semantic Vision MVP: Technical Demo

This repository contains a demonstration of the **Semantic Vision** middleware, an AI-powered accessibility layer designed to restore usability to DeFi protocols for blind and visually impaired users.

## Demo Overview
**Use Case:** Real-time ARIA labeling on the **Aave v3** protocol.

### Step-by-Step Walkthrough

1. **Backend Initialization**: Launching the local Semantic Vision server (Python) to handle DOM analysis and LLM inference coordination.
2. **Environment Setup**: Clearing the local JSON cache via `curl` to demonstrate a "cold start" and launching a secure browser environment.
3. **Baseline Check (NVDA)**: Using the NVDA screen reader to identify "unlabeled" interactive elements within the Aave v3 interface that are currently inaccessible.
4. **Activation**: Triggering the extension via hotkey (`Alt + Shift + A`).
5. **AI Processing**: The system identifies unlabeled clusters and processes them via LLM inference to generate context-aware labels.
6. **Live Injection**: Successfully injecting **8 new ARIA labels** into the live DOM without any page reloads or code changes from the protocol side.
7. **Verification**: Re-scanning the Elements List with NVDA to confirm that previously "unlabeled" buttons are now correctly announced and fully navigable.

## Technical Highlights
* **Zero-Code Integration**: Works on top of existing UIs.
* **Low Latency**: Optimized through a local JSON-based caching mechanism.
* **Context Awareness**: Generates labels based on surrounding DOM structure, not just button text.

---
*For more information, visit the [Project Website](https://wislaw.github.io/Semantic-Vision-Public/)*