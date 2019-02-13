# cs1302-ce11 Title TBD

> Roses are red. 
> Violets are blue. 
> `error: ';' expected` in `Driver.java` on line `142`.

This class exercise explores how to TBD.
It also revists how to commit and view changes to a local Git repository.

## Prerequisite Knowledge

* Inheritance and polymorphism in Java.
* UML Class Diagrams

## Questions

In your notes, clearly answer the following questions. These instructions assume that you are 
logged into the Nike server. 

**NOTE:** If a step requires you to enter in a command, please provide in your notes the full 
command that you typed to make the related action happen. If context is necessary (e.g., the 
command depends on your present working directory), then please note that context as well.

### Getting Started

1. Use Git to clone the repository for this exercise onto Nike into a subdirectory called `cs1302-ce11`:

   ```
   $ git clone --depth 1 https://github.com/cs1302uga/cs1302-ce11.git
   ```

1. Change into the `cs1302-ce11` directory that was just created and look around. There should be
   almost nothing there! That's okay. Use the following to download the JAR file that accompanies your
   `cs1302-listadt` project:
   
   ```
   $ wget https://github.com/cs1302uga/cs1302-listadt/raw/master/listadt.jar
   ```
   
   **NOTE:** This is a separate download. When you followed (or follow) the instructions provided
   in the project description for how to download the project, you will automatically get a copy of
   the JAR file that you can use with the project.

1. Create a `Driver` program using the code below. Make sure you place the file in the proper directory
   within `src`.

```java
package cs1302.listadt;

public class Driver {

    public static void main(String[] args) {

        StringList.Node node = new StringList.Node();
        node.setStr("Susan");
        node.setNext(new StringList.Node("Sally"));
        node.getNext().setNext(new StringList.Node("Barry"));

        StringList.Node end = new StringList.Node("Supa Mike", node);
        StringList.Node n = node.getNext();
        n.setNext(new StringList.Node("Simon"));

        System.out.println(end.getNext());           // Output 1
        System.out.println(node.getNext().getStr()); // Output 2
        System.out.println(n.getNext().getNext());   // Output 3
        System.out.println(n.getNext().getStr());    // Output 4

    } // main
} // Driver
```

1. For each line in the program, draw a diagram that illustrates any nodes that have been created along with 
   their associated string values and next references. Since `next` is a reference, you would either need to 
   denote it as `null` or draw an arrow to the object it references. Redraw the entire picture after each line.
   Reference variables that are not contained in Node objects should be included in the diagram. Although the 
   associated string is also a reference, you may draw it within the node. Number each step in your notes.
   
   Example:
  
   
1. In your notes, write your expected output    
**CHECKPOINT**

1. 

1. 

**CHECKPOINT**

1. 

1.

