all releases
# 🧠 AI Translator Rule List  
[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)

This project contains a rule-based AI translation system that manages reversible language transformations and developer command control.

---

## ⚙️ Commands Overview
here are the commands
| Command | Function |
|----------|-----------|
| **`/lang4 <language>`** | Adds a new language to the system. |
| **`/lang4 remove <language>`** | Removes a language from the system. |
| **`/lang4 list`** | Lists all currently known languages. |
| **`/lang4 to <language>`** | Sets the active “translate to” language. |
| **`/lang4 amount`** | Shows the number of languages currently loaded. |

---

### 💬 Translation Control Commands

| Command | Function |
|----------|-----------|
| **`talk in English`** | (Triggers Rule 11) Temporarily disables translation output and uses normal English. |
| **Any command starting with `/lang4`** | Affects how translation is managed or displayed. |

--
release 5 and up
## ⚙️ release 5+ new Commands Overview
Explanation Toggle (/explain)
This command gives the user control over an "English Explanation" section in the AI's output.

Default Behavior: The explanation section is on (shown).

Turning Off: Typing /explain=0 hides the explanation for a cleaner, more concise output.

Turning On: Typing /explain=1 re-enables the explanation section.

System Version (/version)
This is a simple informational command used to check the AI's current operational status.

Function: When the user types /version, the AI reports its current software or update file.

Purpose: It allows users or developers to confirm exactly which version of the system is running.

Example Output: The rule provides the specific format: "Currently running on 'Release 5' (release-V5.txt)".

Reset Language (/resetlang)
This command is for managing the language setting the user may have previously chosen.

Function: Typing /resetlang clears the currently active language that was set by a previous command (like /lang4 to).

Effect: After the command, the AI reverts to a specific startup state where it must follow Rule 4 (which instructs it to ask the user to select a language). It essentially removes the saved language preference.

release 6 amd up
This project contains a rule-based AI translation system. Release 6 introduces a dedicated Modding System, allowing users to install custom tools without risking the core system stability.

🆕 What's New in Release 6?
The Mod Zone (Rules 31-40): A reserved block of rules specifically for user-created mods, debug tools, and custom scripts.
Mod Installer (/install): A new developer command to easily write code into the Mod Zone.
Mod Manager (/mods): A command to list all currently active mods.
Holiday Cleanup: The system has been reset from the holiday events (Thanksgiving/Christmas), returning Rule 26 to a placeholder state.
⚙️ Official Rule Roadmap
The system rules are now strictly partitioned to prevent conflicts:

Rule Range	Purpose	Status
1 - 30	Core Systems	Protected (Translation logic, Holiday events, Kernel)
31 - 40	The Mod Zone	Open (Reserved for User Mods & Custom Rules)
41 - 98	Expansion	Open (Available for future core features)
99 - ∞	Achievements	Protected (Persistent user achievements)
🛠️ Command Reference
Modding Commands (New!)
Command	Function
/install <slot> <text>	(Rule 42) Installs a custom rule into a specific slot (31-40 only).
/mods	(Rule 41) Lists all currently installed mods in the Mod Zone.
/debug	(Rule 31 Mod) Optional: Displays a raw system diagnostic if the Debug Mod is installed.
