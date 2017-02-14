Step 1:
=====================================================================================

forbeb@forbebW541 /cygdrive/c/users/forbeb/Desktop/CMAKE2/Step1
$ cmake ../step01                                                                            [
-- The C compiler identification is GNU 4.8.4
-- The CXX compiler identification is GNU 4.8.4
-- Check for working C compiler: /usr/bin/cc
-- Check for working C compiler: /usr/bin/cc -- works
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Check for working CXX compiler: /usr/bin/c++
-- Check for working CXX compiler: /usr/bin/c++ -- works
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Configuring done
-- Generating done
-- Build files have been written to: /cygdrive/c/users/forbeb/Desktop/CMAKE2/Step1/
forbeb@forbebW541 /cygdrive/c/users/forbeb/Desktop/CMAKE2/Step1 $ make                                                           
Scanning dependencies of target Tutorial
[100%] Building CXX object CMakeFiles/Tutorial.dir/tutorial.cxx.o
Linking CXX executable Tutorial
[100%] Built target Tutorial
bears:build/ (master✗) $ ./Tutorial 169                                                                           
The square root of 169 is 13
bears:build/ (master✗) $ 
=====================================================================================

Step 2:
=====================================================================================
forbeb@forbebW541 /cygdrive/c/users/forbeb/Desktop/CMAKE2/Step2/MathFunctions
$ cmake ..
CMake Warning at /usr/share/cmake-3.6.2/Modules/Platform/CYGWIN.cmake:15 (message):
  CMake no longer defines WIN32 on Cygwin!

  (1) If you are just trying to build this project, ignore this warning or
  quiet it by setting CMAKE_LEGACY_CYGWIN_WIN32=0 in your environment or in
  the CMake cache.  If later configuration or build errors occur then this
  project may have been written under the assumption that Cygwin is WIN32.
  In that case, set CMAKE_LEGACY_CYGWIN_WIN32=1 instead.

  (2) If you are developing this project, add the line

    set(CMAKE_LEGACY_CYGWIN_WIN32 0) # Remove when CMake >= 2.8.4 is required

  at the top of your top-level CMakeLists.txt file or set the minimum
  required version of CMake to 2.8.4 or higher.  Then teach your project to
  build on Cygwin without WIN32.
Call Stack (most recent call first):
  /usr/share/cmake-3.6.2/Modules/CMakeSystemSpecificInformation.cmake:36 (include)
  CMakeLists.txt:2 (project)


-- Configuring done
-- Generating done
-- Build files have been written to: /cygdrive/c/users/forbeb/Desktop/CMAKE2/Step2/MathFunctions

forbeb@forbebW541 /cygdrive/c/users/forbeb/Desktop/CMAKE2/Step2/MathFunctions
$ make
Scanning dependencies of target MathFunctions
[ 25%] Building CXX object MathFunctions/CMakeFiles/MathFunctions.dir/mysqrt.cxx.o
[ 50%] Linking CXX static library libMathFunctions.a
[ 50%] Built target MathFunctions
Scanning dependencies of target Tutorial
[ 75%] Linking CXX executable Tutorial.exe
[100%] Built target Tutorial

forbeb@forbebW541 /cygdrive/c/users/forbeb/Desktop/CMAKE2/Step2/MathFunctions
$ ./Tutorial 169
Computing sqrt of 169 to be 85
Computing sqrt of 169 to be 43.4941
Computing sqrt of 169 to be 23.6899
Computing sqrt of 169 to be 15.4119
Computing sqrt of 169 to be 13.1887
Computing sqrt of 169 to be 13.0014
Computing sqrt of 169 to be 13
Computing sqrt of 169 to be 13
Computing sqrt of 169 to be 13
Computing sqrt of 169 to be 13
The square root of 169 is 13

=====================================================================================

Step 3:
=====================================================================================
forbeb@forbebW541 /cygdrive/c/users/forbeb/Desktop/CMAKE2/Step3/MathFunctions
$ cmake ..
-- The C compiler identification is GNU 5.4.0
-- The CXX compiler identification is GNU 5.4.0
CMake Warning at /usr/share/cmake-3.6.2/Modules/Platform/CYGWIN.cmake:15 (message):
  CMake no longer defines WIN32 on Cygwin!

  (1) If you are just trying to build this project, ignore this warning or
  quiet it by setting CMAKE_LEGACY_CYGWIN_WIN32=0 in your environment or in
  the CMake cache.  If later configuration or build errors occur then this
  project may have been written under the assumption that Cygwin is WIN32.
  In that case, set CMAKE_LEGACY_CYGWIN_WIN32=1 instead.

  (2) If you are developing this project, add the line

    set(CMAKE_LEGACY_CYGWIN_WIN32 0) # Remove when CMake >= 2.8.4 is required

  at the top of your top-level CMakeLists.txt file or set the minimum
  required version of CMake to 2.8.4 or higher.  Then teach your project to
  build on Cygwin without WIN32.
Call Stack (most recent call first):
  /usr/share/cmake-3.6.2/Modules/CMakeSystemSpecificInformation.cmake:36 (include)
  CMakeLists.txt:2 (project)


-- Check for working C compiler: /usr/bin/cc
-- Check for working C compiler: /usr/bin/cc -- works
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /usr/bin/c++.exe
-- Check for working CXX compiler: /usr/bin/c++.exe -- works
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Configuring done
-- Generating done
-- Build files have been written to: /cygdrive/c/users/forbeb/Desktop/CMAKE2/Step3/MathFunctions

forbeb@forbebW541 /cygdrive/c/users/forbeb/Desktop/CMAKE2/Step3/MathFunctions
$ make
Scanning dependencies of target Tutorial
[ 50%] Building CXX object CMakeFiles/Tutorial.dir/tutorial.cxx.o
[100%] Linking CXX executable Tutorial.exe
[100%] Built target Tutorial

forbeb@forbebW541 /cygdrive/c/users/forbeb/Desktop/CMAKE2/Step3/MathFunctions
$ ^C

forbeb@forbebW541 /cygdrive/c/users/forbeb/Desktop/CMAKE2/Step3/MathFunctions
$ ctest
Test project /cygdrive/c/users/forbeb/Desktop/CMAKE2/Step3/MathFunctions
    Start 1: TutorialRuns
1/5 Test #1: TutorialRuns .....................   Passed    0.09 sec
    Start 2: TutorialComp25
2/5 Test #2: TutorialComp25 ...................   Passed    0.08 sec
    Start 3: TutorialNegative
3/5 Test #3: TutorialNegative .................***Failed  Required regular expression not found.Regex=[-25 is 0
]  0.08 sec
    Start 4: TutorialSmall
4/5 Test #4: TutorialSmall ....................   Passed    0.08 sec
    Start 5: TutorialUsage
5/5 Test #5: TutorialUsage ....................   Passed    0.08 sec

80% tests passed, 1 tests failed out of 5

Total Test time (real) =   0.46 sec

The following tests FAILED:
          3 - TutorialNegative (Failed)
Errors while running CTest

=====================================================================================

Step 4:
=====================================================================================
forbeb@forbebW541 /cygdrive/c/users/forbeb/Desktop/CMAKE2/Step4/MathFunctions
$ cmake ..
-- The C compiler identification is GNU 5.4.0
-- The CXX compiler identification is GNU 5.4.0
CMake Warning at /usr/share/cmake-3.6.2/Modules/Platform/CYGWIN.cmake:15 (message):
  CMake no longer defines WIN32 on Cygwin!

  (1) If you are just trying to build this project, ignore this warning or
  quiet it by setting CMAKE_LEGACY_CYGWIN_WIN32=0 in your environment or in
  the CMake cache.  If later configuration or build errors occur then this
  project may have been written under the assumption that Cygwin is WIN32.
  In that case, set CMAKE_LEGACY_CYGWIN_WIN32=1 instead.

  (2) If you are developing this project, add the line

    set(CMAKE_LEGACY_CYGWIN_WIN32 0) # Remove when CMake >= 2.8.4 is required

  at the top of your top-level CMakeLists.txt file or set the minimum
  required version of CMake to 2.8.4 or higher.  Then teach your project to
  build on Cygwin without WIN32.
Call Stack (most recent call first):
  /usr/share/cmake-3.6.2/Modules/CMakeSystemSpecificInformation.cmake:36 (include)
  CMakeLists.txt:2 (project)


-- Check for working C compiler: /usr/bin/cc
-- Check for working C compiler: /usr/bin/cc -- works
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /usr/bin/c++.exe
-- Check for working CXX compiler: /usr/bin/c++.exe -- works
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Looking for log
-- Looking for log - found
-- Looking for exp
-- Looking for exp - found
-- Configuring done
-- Generating done
-- Build files have been written to: /cygdrive/c/users/forbeb/Desktop/CMAKE2/Step4/MathFunctions

forbeb@forbebW541 /cygdrive/c/users/forbeb/Desktop/CMAKE2/Step4/MathFunctions
$ make
Scanning dependencies of target Tutorial
[ 50%] Building CXX object CMakeFiles/Tutorial.dir/tutorial.cxx.o
[100%] Linking CXX executable Tutorial.exe
[100%] Built target Tutorial

forbeb@forbebW541 /cygdrive/c/users/forbeb/Desktop/CMAKE2/Step4/MathFunctions
$ ./Tutorial 169
The square root of 169 is 13

=====================================================================================

Step 5:
=====================================================================================
forbeb@forbebW541 /cygdrive/c/users/forbeb/Desktop/CMAKE2/Step5/build
$ cmake ..
-- The C compiler identification is GNU 5.4.0
-- The CXX compiler identification is GNU 5.4.0
CMake Warning at /usr/share/cmake-3.6.2/Modules/Platform/CYGWIN.cmake:15 (message):
  CMake no longer defines WIN32 on Cygwin!

  (1) If you are just trying to build this project, ignore this warning or
  quiet it by setting CMAKE_LEGACY_CYGWIN_WIN32=0 in your environment or in
  the CMake cache.  If later configuration or build errors occur then this
  project may have been written under the assumption that Cygwin is WIN32.
  In that case, set CMAKE_LEGACY_CYGWIN_WIN32=1 instead.

  (2) If you are developing this project, add the line

    set(CMAKE_LEGACY_CYGWIN_WIN32 0) # Remove when CMake >= 2.8.4 is required

  at the top of your top-level CMakeLists.txt file or set the minimum
  required version of CMake to 2.8.4 or higher.  Then teach your project to
  build on Cygwin without WIN32.
Call Stack (most recent call first):
  /usr/share/cmake-3.6.2/Modules/CMakeSystemSpecificInformation.cmake:36 (include)
  CMakeLists.txt:2 (project)


-- Check for working C compiler: /usr/bin/cc
-- Check for working C compiler: /usr/bin/cc -- works
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /usr/bin/c++.exe
-- Check for working CXX compiler: /usr/bin/c++.exe -- works
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Looking for log
-- Looking for log - found
-- Looking for exp
-- Looking for exp - found
-- Configuring done
-- Generating done
-- Build files have been written to: /cygdrive/c/users/forbeb/Desktop/CMAKE2/Step5/build

forbeb@forbebW541 /cygdrive/c/users/forbeb/Desktop/CMAKE2/Step5/build
$ make
Scanning dependencies of target Tutorial
[ 50%] Building CXX object CMakeFiles/Tutorial.dir/tutorial.cxx.o
[100%] Linking CXX executable Tutorial.exe
[100%] Built target Tutorial

forbeb@forbebW541 /cygdrive/c/users/forbeb/Desktop/CMAKE2/Step5/build
$ ./Tutorial 169
The square root of 169 is 13
