### SOP: High-Level Gemini CLI State Management

---

## 1. Initialize the "System Image"
Before starting a sprint, define the global constraints and dependencies to ensure the model adheres to your specific architectural patterns and style guides.

* **Configure Environment Variables:** Use `/init` to generate a project-specific manifest that acts as a `.env` for the AI.
    * `/init` — *Generates a `GEMINI.md` file in the root directory to store persistent system prompts and coding standards.*
* **Load Dependencies:** Import relevant boilerplate, API documentation, or existing modules into the active buffer.
    * `/read [filename]` — *Serializes the contents of a local file and appends it to the active context array.*
* **Tag a "Golden Master":** Create a clean snapshot of this initial state so you can "reboot" to a known-good configuration.
    * `/chat save baseline` — *Saves the current state of the context ledger as a named, immutable checkpoint.*

## 2. Implement "Logical Branching"
Avoid "monolithic chat threads" where unrelated features bleed into the same context; instead, fork the conversation for every new ticket or refactor.

* **Checkout from Baseline:** When moving from "Auth Module" to "Database Schema," revert to the clean baseline to avoid cross-contamination.
    * `/chat resume baseline` — *Swaps the current active session log with the data stored in the specified checkpoint.*
* **Commit Feature Milestones:** Once a specific logic or unit test passes, save that state as a new version.
    * `/chat save feature-complete-v1` — *Captures the entire reasoning path and variable state of the current sub-task.*
* **Inspect the Ledger:** Periodically audit your "heads" to ensure your active thread aligns with your current Git branch.
    * `/chat list` — *Returns a list of all manually saved session forks present in the local project cache.*

## 3. Optimize "Context Memory Management"
Every prompt effectively "uploads" the entire session history; manage this "weight" to prevent latency and memory leaks in the AI's logic.

* **Monitor Buffer Weight:** Regularly check the telemetry of your session to identify when the AI's "RAM" is nearing its limit.
    * `/stats` — *Displays the current token usage, total message objects, and the physical size of the JSON state file.*
* **Garbage Collect via Compression:** If a thread is long but the conclusions are vital, refactor the history into a dense summary.
    * `/compress` — *Triggers a summarization of the history and purges the verbose logs to minimize token overhead.*
* **Rollback Faulty Logic:** If the AI produces a "buggy" response or hallucinates, don't patch it with more text—revert the state.
    * `/undo` — *Deletes the most recent prompt-response object from the JSON ledger to prevent logic pollution.*

---