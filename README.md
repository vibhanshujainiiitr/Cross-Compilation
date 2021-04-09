## Compiler Options
These  are the command line options to change the default operations while executing a certain program. These are highly case-sensitive. They didn’t help in compiling your program though help in controlling different aspects of the application. 
These are helpful in the things are code generation, optimization, controlling the name location and type of output file, and many more.

- o flag<br>
```gcc main.cpp```<br>
This will create an executable file a.out<br>
```gcc main.cpp -o main```<br>
This will produce output file as main<br>

- Assembly Output<br>
```gcc -S main.c > main.s```<br>
Produces only the file which contains assembly output<br>

- Machine level Output<br>
```gcc -C main.c```<br>
Produces only the file which contains machine level code as output<br>

- Object file<br>
```gcc main.c -o main.o```<br>
It will come to produce the output as main.o object file<br>


## Compiler Frontend
A compiler basically turns the code into an intermediate stage which is between the machine level instructions and the high level instructions. <br>
There are several frontends of compilers which basically convert the code into an intermediate level from where it will be converted to machine level instructions which are converted with the backend. The backends are basically the intermediate between the frontend and machine level code. There are several backends like x86 and MIPS CPU. <br>
Every time we just need to rewrite the front, and we can use the same backend if we are on the same machine.<br>
<br>
For example, suppose we are running a c program in GCC with MIPS CPU, this means there is a frontend which converts the c code to intermediate level, now the backend will convert this code to MIPS instructions.<br>
Now if we want to run Java, then we can compile using GCC, but we will need a new frontend which accepts Java and converts it to an intermediate level from where it can convert to MIPS instructions using the same backend.<br>
<br>
Frontend supported by GNU Compiler Collection<br>
- C
- C++
- Objective-C
- Java
- Fortan
- Ada

Frontend supported by LLVM
- C and C++
- Go
- Haskell
- Rust 
- Ruby 
- Javascript
- Fortan
And many more

## Compiling for different architecture

- x86_64<br>
```
$ gcc helloworld.c -o helloworld-x86_64

$ file helloworld-x86_64
helloworld-x86_64: ELF 64-bit LSB shared object, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=d0c90e797106a0a6d6f8f72cf428638c1b1bc790, for GNU/Linux 3.2.0, not stripped
```
- 32 bit ARM
```
$ arm-linux-gnueabi-gcc helloworld.c -o helloworld-arm -static

$ file helloworld-arm
helloworld-arm: ELF 32-bit LSB executable, ARM, EABI5 version 1 (SYSV), statically linked, BuildID[sha1]=ae974c9365d4d28bd07cd770b8580ef8314a50f9, for GNU/Linux 3.2.0, not stripped
```
- 64 bit ARM
```
$ aarch64-linux-gnu-gcc helloworld.c -o helloworld-aarch64 -static

$ file helloworld-aarch64
helloworld-aarch64: ELF 64-bit LSB executable, ARM aarch64, version 1 (GNU/Linux), statically linked, BuildID[sha1]=c8e1ce459df806249e2e40bbb80d26a0cc8a8543, for GNU/Linux 3.7.0, not stripped
```
- MIPS
```
$ mips-linux-gnu-gcc helloworld.c -o helloworld-mips -static

$ file helloworld-mips
helloworld-mips: ELF 32-bit MSB executable, MIPS, MIPS32 rel2 version 1 (SYSV), statically linked, BuildID[sha1]=e7a5d8790f9e45365027c8d0dff1529c93a39f48, for GNU/Linux 3.2.0, not stripped
```

- Alpha
```
$ alpha-linux-gnu-gcc helloworld.c -o helloworld-alpha -static

$ file helloworld-alpha
helloworld-alpha: ELF 64-bit LSB executable, Alpha (unofficial), version 1 (SYSV), statically linked, BuildID[sha1]=9b14d1c75e0e51e004296ab037427a5ffcf48ad9, for GNU/Linux 3.2.0, not stripped
```

- Sparc
```
$ sparc64-linux-gnu-gcc helloworld.c -o helloworld-sparc -static

$ file helloworld-sparc
helloworld-sparc: ELF 64-bit MSB executable, SPARC V9, Sun UltraSPARC1 Extensions Required, relaxed memory ordering, version 1 (SYSV), statically linked, BuildID[sha1]=8ed0vibhanshu@LAPTOP-DDGIF99C:~$
```
