# AiToken MOP

## CONDENSE PROMPT:
```
[SYSTEM COMMAND: CONTEXT CONDENSATION]
Analyze our current session. Act as a loss-less text compression utility. Generate a condensed architectural state summary for injection into a clean, new session. The summary must include:
1. Core Objective: The ultimate goal of this conversation.
2. Do not omit foundational logic from earlier turns
3. Current Status & Progress: What has been built, calculated, or decided so far.
4. Key Technical Constraints/Variables: Hard parameters, rules, formulas, or local codes established.
5. Immediate Next Step: The precise pending task.
Format this strictly as a clean markdown block optimized as a system prefix.
```
## PASTE PRIOR PROMPT ###
```
[SYSTEM COMMAND: STATE INJECTION]
The following text represents the condensed contextual memory from the immediate prior session. Absorb this state as your current ground truth prefix before proceeding. Do not re-summarize or acknowledge this instruction with prose; simply reply with "State Injected. Awaiting next command."


```

## Method of Procedure (MOP): Context Optimization Workflow

### Phase 1: Environment & Architecture Setup

> **Critical Prerequisite:** To avoid mobile sync failures and limited file management, **Step 1 and Step 2 must be performed on the desktop web interface (`gemini.google.com`)**. Once configured, execution can move to mobile.

1. Navigate to the desktop browser interface and select **Notebooks** from the left-hand navigation pane. Create a new notebook container named `[Project Name] _Memory_Bank`.
2. Select **Gems Manager > Create New Gem**.
* Name the Gem according to your research topic.
* Paste your tailored persona instructions into the system prompt.
* Under the **Knowledge** or **Sources** section, link the `[Project Name]_Memory_Bank` notebook directly to the Gem's profile. Save and initialize the Gem.
### Phase 2: Active Interaction & Compression Loop
3. Launch a fresh chat session **directly through your custom Gem** (accessible via the hamburger side menu on both desktop and Android).
4. Proceed with your deep research. Keep a strict count of your exchanges.
5. Upon hitting the **4th to 6th response milestone**, halt your research line of thought. Submit the following explicit system-command prompt into the active chat:
```
[SYSTEM COMMAND: CONTEXT CONDENSATION]
Analyze our current session. Act as a loss-less text compression utility. Generate a condensed architectural state summary for injection into a clean, new session. The summary must include:
1. Core Objective: The ultimate goal of this conversation.
2. Do not omit foundational logic from earlier turns
3. Current Status & Progress: What has been built, calculated, or decided so far.
4. Key Technical Constraints/Variables: Hard parameters, rules, formulas, or local codes established.
5. Immediate Next Step: The precise pending task.
Format this strictly as a clean markdown block optimized as a system prefix.
```
6. Copy the generated dense markdown block to your clipboard.
### Phase 3: State Persistence & Cache Invalidation
7. Open your desktop browser tab containing the `[Project Name]_Memory_Bank` notebook.
8. Update the memory record using an **Append-and-Consolidate** mechanic:
* **Do not blindly overwrite.** Open the existing text file inside the notebook.
* Paste the new summary details, 
```
[SYSTEM COMMAND: STATE INJECTION]
The following text represents the condensed contextual memory from the immediate prior session. Absorb this state as your current ground truth prefix before proceeding. Do not re-summarize or acknowledge this instruction with prose; simply reply with "State Injected. Awaiting next command."
```
* Save the file. (The linked Gem now automatically has access to this updated state behind the scenes).

9. **Invalidate the Active Session:** Return to the Gemini interface, open the side menu, and **Delete** or archive the active chat thread you just compressed. This completely wipes the active token history cache and resets your 5-hour compute counter for this topic back to zero.

### Phase 4: Thread Initialization (The New Branch)
10. Open a completely brand-new chat window with your custom Gem.
11. Begin your next turn immediately by referencing the state file:
12. Repeat the cycle from Step 4 onward as your research scales.

## The Fine Print: Operational Safety Checks
* **The Overwrite Trap:** If you delete an old summary completely and replace it with only the newest 4–6 turn summary, your Gem will suffer "amnesia" regarding the very beginning of your project. Treat the notebook file like a design brief that gets tighter and more detailed, rather than a rotating clipboard.
* **The Interface Boundary:** You can chat with your Gem all day long from your Android app side menu, but if you need to adjust what files are inside the Notebook or edit the source text directly, you must pivot back to a desktop browser view.
---