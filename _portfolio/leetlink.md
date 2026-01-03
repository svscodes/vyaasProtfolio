---
title: "LeetLink - Live Chrome Extension"
excerpt: "A published Chrome Extension that automatically syncs LeetCode submissions to GitHub. <br/><img src='/images/leetlink_screenshot.png'>"
collection: portfolio
---

**LeetLink** is a browser extension designed to help developers build their portfolios automatically. It intercepts successful code submissions on LeetCode and commits them to a GitHub repository in real-time.

### ⚙️ Technical Challenges Solved
1.  **Bypassing "Isolated World" Security:** Chrome extensions cannot access page variables (like the Monaco Editor instance) directly. I architected a **DOM-injection bridge** that injects a script into the page context to extract code and communicates back via `window.postMessage`.

2.  **Stateless Authentication (Manifest V3):**
    Since Manifest V3 Service Workers terminate when idle, I implemented a stateless auth flow using the **Chrome Storage API** to securely retrieve credentials on-demand for every API call.

3.  **Serverless Sync:**
    The extension communicates directly with the **GitHub REST API** from the client side, handling file versioning (SHA checks) and directory creation without a backend server.

**[Download on Chrome Web Store](https://chromewebstore.google.com/detail/oklfkajedlajipjbbdbcjcohhhgelnih?utm_source=item-share-cb)** | **[View Source Code](YOUR_GITHUB_REPO_LINK)**
