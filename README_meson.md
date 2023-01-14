# Onethinx Core MAC OS-X dependencies pack

## How to setup Visual Studio Code with the Onethinx Core dependencies pack
 The instructions on how to update are way down below.

## 1. Download prerequisites
- **VS Code**
    - [Download Visual Studio Code](https://code.visualstudio.com/download)
- **Onethinx Dependencies Pack**
    - [Download the Onethinx dependencies pack for Mac OS](https://github.com/onethinx/VSCode_OnethinxPack_macOS/archive/refs/heads/main.zip)
## 2. Install VS Code, extensions & meson/ninja
  - Install VS Code.
  - Install extensions:
    - C/C++ IntelliSense, debugging (microsoft)
    - Cortex-Debug GDB support (marus25)
    - Meson Build (mrmomo)
    - Power Tools (e.GO Mobile)
    - Tasks (actboy168)
    - optional: ARM Assembly Support For Visual Studio Code (dan-c-underwood)
    - optional: Output Colorizer (IBM)
  - Install meson & ninja:
    - sudo port install meson (using MacPorts)
    - sudo port install ninja (using MacPorts)
## 3. Install the Onethinx Dependencies Pack
  - Unzip the pack archive to your local harddisk (eg: /Applications/VSCode_OnethinxPack_macOS).
     - Hint: you might want to remove '-main' at the end of the folder name.
  - If you're on Catalina (macOS 10.15) or later:
    - If the file ~.zprofile doesn't exist, create it: Terminal >> `cd ~ && touch .zprofile`
    - Open ~.zprofile: Terminal >> `cd ~ && open -e .zprofile`
  - If you're on Mojave (macOS 10.14) or earlier:
    - If the file ~.bash_profile doesn't exist, create it: Terminal >> `cd ~ && touch .bash_profile`
    - Open ~.bash_profile: Terminal >> `cd ~ && open -e .bash_profile` 
  - Add this to the end of the file (make sure you enter the correct path for ONETHINX_PACK_LOC) and save:
    ```
    # Loading environment variables for the Onethinx Pack
    export ONETHINX_PACK_LOC="/locationOfYour/VSCode_OnethinxPack_macOS"
    source "$ONETHINX_PACK_LOC/variables.env"
    ```
  - Restart your machine (or log-out and log-in) to reload the environment variables.
## 4. Check
  - If CMake, Make and the compiler is correctly installed by typing the following into your terminal or terminal window of VS Code.
    - `make -v`
    - `cmake --version`
    - `arm-none-eabi-gcc -v`
  - If you have not done this yet, download the [Hello World Project](https://github.com/onethinx/HelloWorld)
    - You should be able to build and debug this project. If you experience issues, [your feedback is appreciated.](https://github.com/onethinx/VSCode_OnethinxPack_macOS/issues)
## 5. Remind
  - After changing the device configuration (or project file structure) to use
    - Clean Reconfigure
    - Clean Rebuild
       in order to build the image properly  
  - To delete the contents of the build folder
    - if you copied the project including build folder from another location / machine
    - when build fails.
    
## How to update
  - Download the [latest Onethinx Dependencies Pack](https://github.com/onethinx/VSCode_OnethinxPack_macOS/archive/refs/heads/main.zip)
  - Delete the contents of the Dependencies Pack folder from you harddisk
  - Unpack the contents of the archive to the Dependencies Pack folder
  - Make sure the correct path is set in the environment variables (see step 3)
  - Restart your machine (or log-out and log-in) to reload the environment variables.
