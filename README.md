# Wavedump-Compile-Tutorial
This tutorial will help you how compile CAEN wavedump package and you can do customized modification. Really thanks for the helps from Matteo from CAEN Support Division.I hope this tutorial will help the people who is fresh about C package compiling.

## Detailed procedure is following:
Install Visual Studio, the following operation is under visual studio software
0. open the Wavedump project in the C:\Program Files\CAEN\Digitizers\WaveDump\build folder.
1.	Open the project proprieties window and select Debug x64 configuration
2.	In C/C++ -> General -> Additional Include Directories add C:\Program Files\CAEN\Digitizers\WaveDump\compile\inc
3.	In Linker -> General -> Additional Library Directories add C:\Program Files\CAEN\Digitizers\WaveDump\compile\lib\x64
4.	In Linker -> Input -> Additional Dependencies check if the CAENComm.lib and the CAENDigitizer.lib are present

## I take some snapshoots for the demostration:
1. ![image](https://github.com/jack595/Wavedump-Compile-Tutorial/assets/31855564/243acdd8-93ae-4d88-8233-104ef08528aa)
2. ![image](https://github.com/jack595/Wavedump-Compile-Tutorial/assets/31855564/3fde3aa0-642b-48fb-a1f2-546edcc04340)
3. ![image](https://github.com/jack595/Wavedump-Compile-Tutorial/assets/31855564/5b6913e6-1d9b-4c8f-abbc-68f42a0cb287)
4. Here is an extra amend for the include header. We don't need to list the specific path and only to list the file name. Because we have added the dependency in linker.
![image](https://github.com/jack595/Wavedump-Compile-Tutorial/assets/31855564/3b17ebd9-fada-4290-9dd9-3af9422a3e77)
5. Compile the package![image](https://github.com/jack595/Wavedump-Compile-Tutorial/assets/31855564/416f4636-ee28-4e32-ad18-fdfcd62d9980)
6. After compiling, the exe and dependency can be found in folder "Debug"
![image](https://github.com/jack595/Wavedump-Compile-Tutorial/assets/31855564/f57d273e-4efd-4c19-8d1c-5db21946c78c)







