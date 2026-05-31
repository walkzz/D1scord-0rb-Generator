# Custom Discord Game Status & Orb Automator

A lightweight toolkit that allows you to generate a standalone dummy executable (`.exe`) for **any** game. It fools Discord into thinking the game is active, letting you earn Discord orbs or customize your active status without wasting CPU or RAM on running the actual game.

## Features
* **Completely Customizable:** Name the executable after any game you want to complete the quest.
* **Lightweight Background Process:** Completely resource-free.
* **Standalone Output:** Once generated, the `.exe` can be moved anywhere and launched with a simple double-click—no terminal required to run it.

---

## Prerequisites

To bundle the application yourself, you only need one tool installed on your system:
* **Node.js (LTS version recommended):** [Download Node.js](https://nodejs.org/)

*Note: You do **not** need a code editor like VS Code. Standard Windows PowerShell is all you'll use.*

---

## Step-by-Step Setup & Build Guide

### 1. Download the Project Files
Download the files from this repository (specifically ensuring you have `index.js` and `package.json` if applicable) and place them into a folder on your computer (e.g., `C:\Users\[USER]\Desktop`).

### 2. Open PowerShell in Your Folder
1. Open the folder where your files are located.
2. Hold `Shift` and **Right-Click** an empty space inside the folder.
3. Select **"Open PowerShell window here"** (or "Open in Terminal").

### 3. Install Dependencies & Generate Your Custom Game Executable
In the PowerShell window that pops up, you need to install the project dependencies first. Type this command and press **Enter**:

```powershell
npm install
```

### 4. Generate Your Custom Game Executable
In the PowerShell window that pops up, type the following command.
```powershell
npx pkg index.js --targets node18-win-x64 --output YOUR-GAME-NAME.exe
```
> **Important:** Replace `[YOUR-GAME-NAME]` with the exact name of the game Discord looks for (e.g., `GenshinImpact.exe`, `wwm.exe`, etc.).

NOTE: Some applications(e.g., Where Winds Meet) uses different executable - `wwm.exe`. You can find most of the executables in the file named `discord-executables.txt`, as with their folder directories where the exe file must be launched from.

### Troubleshooting
### 1. Error: "running scripts is disabled on this system"
If you see a red error in PowerShell when typing `npm install`, copy and paste this command into PowerShell, hit **Enter**, and try again:
```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```
2. If it asks for confirmation, type Y and press Enter.
3. Run `npm install` again.

##  How to Run It
Once your custom `.exe` is generated, follow these steps:

* **Double-click** your newly created `.exe` file.
* A **command prompt terminal** will open, starting the game process in the background.
* **Discord** will instantly detect it and display that you are playing the game.
* **To turn it off:** Simply close the terminal window once the orb quest has been completed.

---
### Step by step with screenshots
1. Here, we'll use the game **Where Winds Meet** as an example. Click on the quest and select the desktop version <br />
   <img width="532" height="340" alt="Screenshot 2026-05-31 163035" src="https://github.com/user-attachments/assets/55f2f3a2-6353-4982-869d-87729252b553" />
2. Go to your folder where the index.js and package.json files are located(should be on your desktop) and open the terminal. <br />
   <img width="476" height="441" alt="Screenshot 2026-05-31 163157" src="https://github.com/user-attachments/assets/ca975da6-78c5-4aa2-93c4-7afefeadb696" />
3. Inside the terminal, run the following command and press **Enter** to create the executable: <br />
   <img width="1104" height="338" alt="Screenshot 2026-05-31 163536" src="https://github.com/user-attachments/assets/54c50f35-3099-4f34-810c-3bb32a74aa07" />
4. Once done, launch the application named **wwm.exe** <br />
5. Discord should now recognize the application in the background and the quest timer will begin. Once the quest is over, close the terminal manually or use **CTRL + C** to terminate. <br />
   <img width="351" height="163" alt="Screenshot 2026-05-31 163643" src="https://github.com/user-attachments/assets/360fb428-177d-4a95-988f-a8b0632baeb0" />

### FAQ
## 1. Will I get banned for using this service?
- Technically, no. You will only be rate-limited because Discord will notice an unusual behaviour from your account, standard spam protection these days, you know.
## 2. How many times can I use this program to earn orbs in a day?
- Do not go over 3 times per day. Discord will rate-limit you and you will have to wait a day or two to reset.
## 3. Can I use my earned orbs to gift my friends, especially what they have in their wishlist?
- No, you cannot gift orbs to your friends.
## 4. Is this service free?
- The service is completely free and I do not need your well-earned money.

##  Disclaimer
This utility is for educational and personal use and I do not enforce spamming behavior or other scripts beyond this program. Use this program at your own risk; you can stop at any time.
