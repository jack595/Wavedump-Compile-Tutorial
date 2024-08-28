# Wavedump-Compile-Tutorial
This tutorial will show you how to compile the CAEN wavedump package and how to do customized modifications. Really, thanks for the help from Matteo from the CAEN Support Division.I hope this tutorial will help people who are new to C package compilation.

## The detailed procedure is the following:
Install Visual Studio, The following operation is under visual studio software
0. Open the Wavedump project in the C:\Program Files\CAEN\Digitizers\WaveDump\build folder.
1.	Open the project proprieties window and select Debug x64 configuration
2.	In C/C++ -> General -> Additional Include Directories add C:\Program Files\CAEN\Digitizers\WaveDump\compile\inc
3.	In Linker -> General -> Additional Library Directories add C:\Program Files\CAEN\Digitizers\WaveDump\compile\lib\x64
4.	In Linker -> Input -> Additional Dependencies check if the CAENComm.lib and the CAENDigitizer.lib are present

## I take some snapshoots for the demostration:
1. ![image](https://github.com/jack595/Wavedump-Compile-Tutorial/assets/31855564/243acdd8-93ae-4d88-8233-104ef08528aa)
2. Adding Properties(Step 2)
   ![image](https://github.com/jack595/Wavedump-Compile-Tutorial/assets/31855564/3fde3aa0-642b-48fb-a1f2-546edcc04340)
   ![image](https://github.com/jack595/Wavedump-Compile-Tutorial/assets/31855564/5b6913e6-1d9b-4c8f-abbc-68f42a0cb287)
4. Adding Linker(Step 3 and 4):
   ![Adding Linker](https://github.com/user-attachments/assets/0827d637-3434-428d-8c3b-8786eb7414f0)
6. **Attention!!!Cannot be Omitted** Here is an extra amend for the include header. We don't need to list the specific path and only to list the file name. Because we have added the dependency in linker.
![image](https://github.com/jack595/Wavedump-Compile-Tutorial/assets/31855564/3b17ebd9-fada-4290-9dd9-3af9422a3e77)
7. Compile the package![image](https://github.com/jack595/Wavedump-Compile-Tutorial/assets/31855564/416f4636-ee28-4e32-ad18-fdfcd62d9980)
8. After compiling, the exe and dependency can be found in folder "Debug"
![image](https://github.com/jack595/Wavedump-Compile-Tutorial/assets/31855564/f57d273e-4efd-4c19-8d1c-5db21946c78c)
9. Get the released version by switch the compile mode
![GetReleaseVersion](https://github.com/jack595/Wavedump-Compile-Tutorial/assets/31855564/f28dcbf9-ceaa-46b7-853c-9b21601660c5)
10. Copy the files from the folder C:\Program Files\CAEN\Digitizers\WaveDump\compile\bin\x64 to the released files
![ReplaceFiles](https://github.com/jack595/Wavedump-Compile-Tutorial/assets/31855564/2a42131a-772b-4892-bd01-14399c343473)
11. For example, replace the files in this folder, and it will work
![Snipaste_2023-11-28_23-59-36](https://github.com/jack595/Wavedump-Compile-Tutorial/assets/31855564/74cdb5fa-ef27-4cbb-a5bc-200c21decc05)

* The released version in the `released` folder is modified by me. I just added an option to change the saving path of wavedump and showing the total event number instantly. You need to add one line like `PATH D:/Data/` in WaveDumpConfig.txt. Follow the step 8 and 9. And things will be done well.
![Snipaste_2023-11-29_00-08-09](https://github.com/jack595/Wavedump-Compile-Tutorial/assets/31855564/2f656651-e36e-4a91-93fc-4c87badfc969)






