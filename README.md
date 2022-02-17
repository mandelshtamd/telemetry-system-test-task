### Test task for the project `Telemetry System with Azul`

#### Task
Java program’s behavior may vary depending on the order of the classpath arguments in the command line that launches it.

#### Solution description
The simplest way to demonstrate that the order of the classpath arguments is important is when we choose 
main class via -classpath arguments.

1. Run `gradlew assemble` to compile .class files and build .jar file
2. In the case when we specify the Main class in the first package as the first argument, 
   we will see one behavior  
Example: `java -cp build/libs/telemetry-system-test-task-1.0-SNAPSHOT.jar first.Main second.Main`  
Output: `First hello world`  
3. In the case when we specify the Main class in the second package as the first argument,
   we will see another behavior  
Example: `java -cp build/libs/telemetry-system-test-task-1.0-SNAPSHOT.jar second.Main first.Main`  
Output: `Second hello world`

