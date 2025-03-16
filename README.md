# CZ4031
In this project, since we are using C++, you need to ensure that your IDE provides support for C++. 

1. Since we are using visual studio code, we installed the extension for C++ in the marketplace to enable cross-platform development.

2. Besides making sure our IDE is able to read C++, we need to make sure that we have installed a compiler. C++ is a compiled language meaning your program's source code must be translated (compiled) before it can be run on your computer. VS Code is first and foremost an editor, and relies on command-line tools to do much of the development workflow. The C/C++ extension does not include a C++ compiler or debugger. You will need to install these tools or use those already installed on your computer. To check if you have a compiler installed, refer to this document: https://code.visualstudio.com/docs/languages/cpp.

3. We will install Mingw-w64 via MSYS2, which provides up-to-date native builds of GCC, Mingw-w64, and other helpful C++ tools and libraries. You can download the latest installer from the MSYS2 page or use this the link found in this document: https://code.visualstudio.com/docs/languages/cpp to the installer. 

4. Add the MinGW Compiler to your path. 
Add the path to your Mingw-w64 bin folder to the Windows PATH environment variable by using the following steps: 
   1. In the Windows search bar, type 'settings' to open your Windows Settings.
   2. Search for Edit environment variables for your account.
   3. Choose the Path variable in your User variables and then select Edit.
   4. Select New and add the Mingw-w64 destination folder path, with \mingw64\bin appended, to the system path. The exact path depends on which version of Mingw-w64 you have installed and where you installed it. If you used the settings above to install Mingw-w64, then ### add this to the path: C:\msys64\mingw64\bin.
   5. Select OK to save the updated PATH. You will need to reopen any console windows for the new PATH location to be available.

5. Check your MinGW installation. 
   To check that your Mingw-w64 tools are correctly installed and available, open a new Command Prompt and type:

 ```
 gcc -version
 g++ --version
 gdb --version
```
6. If you don't see the expected output or g++ or gdb is not a recognized command, make sure your PATH entry matches the Mingw-w64 binary location where the compiler tools are located. If the compilers do not exist at that PATH entry, make sure you followed the instructions on the MSYS2 website to install Mingw-w64

7. Lastly, compile and run main.cpp.

-------------------------------------------------------------------
NOTES: 
Current blkSize settings is at 200Bytes. If want to run at blkSize = 500Bytes, can change the following:
1. At main.cpp, comment out line 31 and uncomment line 32, then
2. At Storage.cpp, comment out line 8 and uncomment line 7. 
Save both file and recompile the code.

