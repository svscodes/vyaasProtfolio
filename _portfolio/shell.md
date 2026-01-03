---
title: "Shell (Node.js)"
excerpt: "A custom shell implementation to understand OS internals. <br/><img src='/images/shell_screenshot.png'>"
collection: portfolio
---

**Tech Stack:** Node.js, JavaScript, OS Modules

##Shell

## The "Why"
I've used Bash and Zsh for years, but I realized I treated them like black boxes. I wanted to understand the lifecycle of a command from keystroke to execution.

## Core Features
1.  **REPL:** Implemented a Read-Eval-Print Loop that persists history and handles user input.
2.  **Built-in Commands:** * `cd`: You cannot execute `cd` as a child process because it would only change the directory for that child, not the shell. I had to implement this as a native built-in that manipulates `process.chdir()`.
    * `pwd`, `echo`, `type`.
3.  **External Execution:** Uses `child_process` to spawn binaries found in the user's `$PATH`.

## The Hardest Part: Parsing
Handling a command like `echo "Hello World" > output.txt` looks simple, but parsing it is tricky.
* I wrote a custom tokenizer to handle:
    * **Quotes:** Preserving spaces inside `" "`.
    * **Escapes:** Handling `\` correctly.
    * **Redirection:** Detecting `>` and `>>`, creating file streams, and piping `stdout` to them instead of the console.

[View Source Code](YOUR_GITHUB_REPO_LINK)
