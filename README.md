# Windows CE ARM Bughunting
Various scripts and programs that support my Windows CE 4.2/6.0 exploit development and fuzzing efforts

Current Files:

HarnessHandler.cpp
- A harness to facilitate the remote fuzzing of Windows CE 4.2 programs using Peach Community Edition
- Facilitates hook/injection based file format fuzzing
- Acts as both the remote file recipient and remote monitor for Peach fuzzer
- Can easily be adapted to other network based fuzzers

ImageFuzz.cpp
- An example of the harness described in HarnessHAndler.cpp
- Puts thread into kernel mode and fuzzes LoadKernelLibrary function

HarnessAgentExample.xml
- Example Peach fuzzer description that works with the harness
- Current state model based off of ImageFuzz.cpp

DebugTest.cpp
- Example of debugging a process, waiting a few seconds for a crash, and terminating the process

KeyPressTest.cpp
- Tests the ability to click a link in an Internet Explorer window generated by the program

html3.xml
- A basic HTML template for peach fuzzer
- Based off of example.com
