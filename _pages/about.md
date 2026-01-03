---
permalink: /
title: "About Me"
excerpt: "Backend Engineer, Tool Builder, and 9.56 GPA Defender."
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Hello! I’m **S Vyaas Sundar**.

I am a final-year Computer Science & Business Systems student at **SRM Institute of Science and Technology**, currently holding a **9.56/10 GPA**. 

While I pride myself on academic rigor, I am an engineer at heart. My philosophy is simple: **if you have to do it twice, automate it.** I specialize in **Backend Engineering**, **System Internals**, and **Developer Tooling**. I don't just write code to pass exams; I build tools to solve actual problems (usually problems I caused for myself).

---

## 🛠 Engineering Highlights

I believe the best way to understand how something works is to break it—and then (hopefully) put it back together.

### 🚀 **[LeetLink (Chrome Extension)](https://chromewebstore.google.com/detail/oklfkajedlajipjbbdbcjcohhhgelnih?utm_source=item-share-cb)**
* **The Mission:** Manually syncing LeetCode solutions to GitHub was ruining my flow state. I needed a way to automate my portfolio.
* **The Engineering:** I built a **Manifest V3** extension that intercepts successful submissions and pushes them to GitHub via their REST API. 
* **The Gritty Details:**
  * **Security Bypass:** Chrome's "Isolated World" policy prevents extensions from reading page variables (like the Monaco Editor state). I architected a **script-injection bridge** that injects a script into the DOM context to steal the code and passes it back via `window.postMessage`.
  * **Stateless Auth:** Since Manifest V3 kills background service workers when idle, I couldn't store variables in memory. I implemented a robust auth flow using `chrome.storage.local` to persist tokens securely.

### 🐚 **Unix Shell (Built from Scratch)**
* **The Mission:** I wanted to understand what actually happens when I type `ls -la`.
* **The Engineering:** Instead of reading about it, I wrote a Unix-like shell in **Node.js**.
* **The Gritty Details:**
  * **Process Management:** I didn't just use `exec()`. I handled **process forking** and implemented standard IO piping.
  * **Parsing Logic:** Writing the parser to handle quotes (`" "`), escape characters (`\`), and output redirection (`>`) gave me a newfound respect for Regex and state machines.
  * **Built-ins:** Implemented `cd` manually (because you can't change the parent process's directory from a child process!).

### 🤖 **FoodPicker AI**
* **The Mission:** Solving the eternal group chat debate: *"Where should we eat?"*
* **The Engineering:** Trained a **PyTorch** NLP model on a custom dataset of local restaurants and user preferences.
* **The Gritty Details:**
  * **NLP Pipeline:** Used **NLTK** for tokenization and stemming to break down conversational queries ("I want something spicy" vs "Spicy food near me").
  * **Model:** Implemented a Feed-Forward Neural Network (Bag of Words approach) to classify intent with **90% accuracy** on our test set.
  * **Result:** It now automates our decision-making (and takes 100% of the blame if the food is bad).

### 💱 **Global Currency Converter**
* **The Mission:** I needed financial data faster than Google could load.
* **The Engineering:** A Python-based tool integrating the Free Currency Converter API.
* **The Gritty Details:**
  * **Latency Optimization:** Achieved **<60ms response times** by implementing aggressive local caching for frequent currency pairs.
  * **Scale:** Handles conversion logic for **918 currencies** concurrently.

---

## 💻 Technical Arsenal

* **Languages:** Python (Primary), JavaScript (ES6+), SQL.
* **Frameworks:** FastAPI, Node.js, Express.js, PyTorch.
* **Core Concepts:** System Design, Data Structures & Algorithms, REST APIs, OS Internals.
* **Tools:** Git/GitHub, Docker, Chrome Extension API, Postman.
* **Databases:** PostgreSQL, MongoDB.

[📄 Download My Resume](/files/Vyaas_Sundar_Resume.pdf){: .btn .btn--primary .btn--large}
