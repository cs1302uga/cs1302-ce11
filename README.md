# cs1302-ce11 Title 

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
package cs1302.list;

import cs1302.listadt.StringList;

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
   ```
                   /----------------\       /----------------\
   example ------->| str -> "Hello" |   /-->| str -> "World" |
                   | next ----------|--/    | next = null    |
                   \----------------/       \----------------/
   ```
  
   
1. In your notes, write your expected output for the four `System.out.println` statements in the code based 
   on your diagram created in the previous step. 
   
1. Make sure you are in the `cs1302-ce11` directory. Write the exact command to:
   1. Compile `Driver.java` specifying `bin` as the default package location for your compiled code.
   1. Run `cs1302.list.Driver`.

1. Write the output from the program in your notes. If your expected output does not match the output from the 
   program execution, repeat the last three steps using a new piece of paper.
   
**CHECKPOINT**

1. In `Driver.java`, add a method to print the string value of the third `StringList.Node` in the list. Your
   method should take a single `StringList.Node` parameter representing the starting node. The method must
   begin with the starting node and traverse the `next` links to print the third node.
   
1. In your notes, write down the expected output of calling your new method from `main` passing with 
   the preexisting `StringList.Node` references (`end`, `node`, and `n`) as the actual parameters.

1. From the `main` method of `Driver.java`, make three separate calls to your new method using `end`, `node`,
   and `n` as the actual parameters.
   
1. Compile and run your `Driver` program. 

1. Write the output from the program in your notes. If your expected output does not match the output from the 
   program execution, indicate the reason(s) in your notes.
   
1. Your `Driver` program likely threw an unchecked exception when you ran it. Update your code to handle this 
   type of error instead of crashing. In your notes, explain how you handled it and why you handled it this way.

**CHECKPOINT**

1. 

1.

**CHECKPOINT**
