#### JDK
It provide an environment to develop and run Java programs
Its a package that includes:
- Development Tools
- JRE (A Runtime environment the executes the program)
- A compiler (javac)
- Archiver (jar)
- Docs Generator (javadoc)
- Interpreter / Loader

[[Architecture of Java#^bRUI4I7Vv_4ybLKwycor7|JDK Structure]]

#### JRE
It only runs the program
It is an installation package that provides runtime environment to only a single program
It consists of:
- Deployment Technologies
- User Interface Tools
- Integration Libraries
- Base Libraries
- JVM (Java Virtual Machine)

#### Class Loader ([[Architecture of Java#^hERMly5isHqn1WZDTOa65|JVM Working]])
1. Loading
   - Binary code of the .class file is basically an object in the heap memory, because **[[Memory Management|Objects of Classes are created in Heap Memory]]**.
2. Linking
   - JVM verifies the .class file and allocates the memory to the variables and stuffs used in program.
   - It also replaces symbolic references to direct references. (Basically replacing variables with its values and function calls with the function).
3. Initialization
   - Static Variables are assigned with their values and static block

> [!NOTE] Note
>JVM also contains Stack and Heap memory allocations

#### JVM Execution
Interpreter
- Line-by-line execution of code.
- Basically means one methods is called many times for executions which make the things inefficient.
JIT
- Methods that are repeated, are sent to JIT that directly shares the machine code, so re-interpretation of code is not required. 
- This make things more efficient


[[Architecture of Java#^hERMly5isHqn1WZDTOa65|JVM Working]]