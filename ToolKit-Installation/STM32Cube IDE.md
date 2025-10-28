# ⚙️ STM32CubeIDE – Installation & Setup Guide
---

## 🧭 What is STM32CubeIDE?

**STM32CubeIDE** is an **all-in-one development tool** provided by **STMicroelectronics** for programming **STM32 microcontrollers**.

It combines:
- 🧠 **Code editing** (C/C++ based)
- 🧩 **Project configuration** (Pinout, peripherals, clock setup)
- 🔍 **Code generation**
- 🧰 **Debugging and flashing support**
- 🖥️ **Integration with STM32CubeMX**

In short — it’s the **main tool** you’ll use for **Embedded C programming** on STM32 boards like:
- STM32F103 (Blue Pill)
- STM32F4 Discovery
- STM32 Nucleo Boards, etc.

---

## 💡 Why Use STM32CubeIDE?

| Feature | Description |
|----------|--------------|
| 🧩 Integrated Toolchain | Combines STM32CubeMX + Eclipse + GCC toolchain |
| 🧠 Auto Code Generation | Generates initialization code automatically |
| ⚡ Easy Debugging | Real-time debugging using ST-Link |
| 🎯 Device Configuration | Graphical interface to configure pins and peripherals |
| 🌍 Cross-Platform | Works on Windows, macOS, and Linux |
| 💬 Free & Official | Provided by STMicroelectronics (no license required) |

---

## 🧰 Prerequisites

Before installing, make sure you have:
- 💻 A PC running **Windows 10/11**, **macOS**, or **Ubuntu/Linux**
- 🌐 Stable internet connection
- 📦 At least **2 GB free disk space**
- 🪫 **Administrator privileges** for installation

---

## 🪜 Step-by-Step Installation Guide

### 🥇 Step 1: Download STM32CubeIDE

1. Visit the official STMicroelectronics download page:  
   👉 [https://www.st.com/en/development-tools/stm32cubeide.html](https://www.st.com/en/development-tools/stm32cubeide.html)

2. Scroll down and click **“Get Software”**.
3. You’ll need to **create or log in** to your ST account.
4. After logging in, download the version that matches your **operating system**.

---

### 🥈 Step 2: Install STM32CubeIDE

#### 🪟 On Windows:
1. Run the downloaded `.exe` installer.  
2. Accept the license agreement.  
3. Choose installation directory (default is fine).  
4. Keep all default options checked (like ST-Link drivers).  
5. Click **Install** and wait — it may take a few minutes.

#### 🐧 On Linux:
```bash
# Example for Ubuntu/Debian
cd ~/Downloads
chmod +x st-stm32cubeide_x.x.x_amd64.sh
sudo ./st-stm32cubeide_x.x.x_amd64.sh
```
Follow the on-screen instructions to complete installation.

#### 🍏 On macOS:

1. Open the downloaded .dmg file.
2. Drag and drop STM32CubeIDE into the Applications folder.
3. Launch it from Launchpad.

---

### 🥉 Step 3: Launch the IDE
1. Open STM32CubeIDE
2. Choose a workspace (this is where your projects will be stored)

💡 Example:

`C:\STM32_Projects\` (Windows)

`~/STM32_Workspace/` (Mac/Linux)

---

## 💻 Writing Your First C Program ("Hello World")

Now that STM32CubeIDE is ready, let’s run your first C program just like in a regular C IDE.

### 🧩 Step 1: Create a New Project

1. Go to File → New → C Project
2. In the pop-up window:
   * Project Name: HelloWorld
   * Project Type: Empty Project
   * Toolchain: Ac6 STM32 MCU GCC (or default GCC if available)
3. Click Finish

### 🧠 Step 2: Create a New C Source File

1. Right-click your project name in the Project Explorer
2. Select New → Source File
3. Name it: main.c
4. Click Finish

### 🧾 Step 3: Write the Code

Copy and paste the following C program:
```c
#include <stdio.h>

int main(void) {
    printf("Hello, World! Welcome to STM32CubeIDE.\n");
    return 0;
}
```

### 🧱 Step 4: Build the Project

1. Click the 🧱 Build (hammer) icon on the toolbar
or press Ctrl + B

If the build is successful, you’ll see:

`
Build Finished (took 0s.123ms)
`

### ▶️ Step 5: Run the Program

1. Click Run → Run Configurations…
2. Select C/C++ Application → New Configuration
3. Under Project, select your project (HelloWorld)
4. Under C/C++ Application, choose main.c
5. Click Run

### 🖥️ Step 6: View Output

At the bottom of your screen, open the Console tab.
You should see:

`
Hello, World! Welcome to STM32CubeIDE.
`

---
