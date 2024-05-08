# Basic Shellcode Tester, Debugger, and PE-File Wrapper
This program serves as a versatile tool for handling shellcode, offering functionalities for testing, debugging, and generating executable PE files. Whether your shellcode is 32-bit or 64-bit, this tool can handle it, providing flexibility for various scenarios.

## Features:
Execution and Debugging: Load and execute shellcode directly, or debug it for troubleshooting.
PE File Generation: Create executable PE files based on your shellcode, simplifying testing and analysis with standard reverse engineering tools.
## Usage:
Executing Shellcode From a File
Required Argument: Provide the path to the file containing your shellcode using the -f argument.
Optional Arguments:
-pause: Pause the program before executing the shellcode, allowing for attachment of a debugger and setting breakpoints.
-ep: Adjust the entry point by X bytes, useful for shellcode starting execution anywhere within the binary blob.
-bp: Insert a breakpoint before the shellcode, facilitating debugging. Avoid using this if not running under a debugger to prevent crashes.
## Producing a PE File
Use the -pe argument to generate a PE file encapsulating your shellcode.
Optional Arguments:
-ep: Define an offset from the beginning of the .text section to adjust the entry point in the PE file.
-64: Generate a 64-bit PE file, suitable for 64-bit shellcode.
The resulting PE file can be analyzed with common reverse engineering tools like IDA Pro, Ghidra, or debuggers such as x32dbg and WinDbg.
