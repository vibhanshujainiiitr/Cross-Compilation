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


