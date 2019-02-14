# cs1302-ce11 Lovable Linked Lists 

> Roses are red. 
> Violets are blue. 
> `error: ';' expected` in `Driver.java` on line `142`.

This class exercise explores how to work with linked lists.

## Prerequisite Knowledge

* Reference variables.
* [`StringList.Node` API Documentation](http://cobweb.cs.uga.edu/~mec/cs1302/listadt-api/cs1302/listadt/StringList.Node.html)

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

1. For convenience, here is a link to the 
   [`StringList.Node` API Documentation](http://cobweb.cs.uga.edu/~mec/cs1302/listadt-api/cs1302/listadt/StringList.Node.html).
   What is the FQN of the _package_ that contains `StringList.Node`?

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

            System.out.println(end.getNext());           
            System.out.println(node.getNext().getStr()); 
            System.out.println(n.getNext().getNext());   
            System.out.println(n.getNext().getStr());    

        } // main
        
    } // Driver
    ```

1. For each line in the program, draw a diagram that illustrates any nodes that have been created along with 
   their associated string values and next references. Since `next` is a reference, you would either need to 
   denote it as `null` or draw an arrow to the object it references. Redraw the entire picture after each line.
   Although the associated string is also a reference, you may draw it within the node. Number each step in 
   your notes. Reference variables that are not contained in node objects should also be included in the 
   diagram. 
   
   Example:
   ```
                   /----------------\       /----------------\
   example ------->| str -> "Hello" |   /-->| str -> "World" |
                   | next ----------|--/    | next = null    |
                   \----------------/       \----------------/
   ```
  
   
1. In your notes, write your expected output for the four `System.out.println` statements in the code based 
   on the diagram you created in the previous step. 
   
1. Make sure you are in the `cs1302-ce11` directory. Write the exact command to:
   1. Compile `Driver.java` specifying `bin` as the default package location for your compiled code.
   1. Run `cs1302.list.Driver`.
   
   **NOTE:** This program depends depends on two different sets of compiled code, the compiled code you placed
   into `bin` and the compiled code in the JAR file. You will need to place the default package for both 
   compiled code locations on the class path in order to run your program.

1. Write the output from the program in your notes. If your expected output does not match the output from the 
   program execution, repeat the last three steps using a new piece of paper.
   
**CHECKPOINT**

1. In `Driver.java`, add a method to print the string value of the third `StringList.Node` in the list. Your
   method should take a single `StringList.Node` parameter representing the starting node. The method must
   begin with the starting node and traverse the `next` links to print the third node.
   
1. In your notes, write down the expected output of calling your new method from `main` passing in 
   the preexisting `StringList.Node` references (`end`, `node`, and `n`) as the actual parameters.

1. From the `main` method of `Driver.java`, make three separate calls to your new method using `end`, `node`,
   and `n` as the actual parameters.
   
1. Compile and run your `Driver` program. 

1. Write the output from the program in your notes. If your expected output does not match the output from the 
   program execution, indicate the reason(s) in your notes.
   
1. Your `Driver` program likely threw an unchecked exception when you ran it. Update your code to handle this 
   type of error instead of crashing. In your notes, explain how you handled it and why you handled it this way.

**CHECKPOINT**

1. In `Driver.java`, add a method to insert a `StringList.Node` into the third position in the list. It should 
   shift the node currently at that position (if any) and any subsequent nodes to the right. Your 
   method should take two `StringList.Node` parameters, one representing the starting node and another
   representing a node to insert. The method must begin with the starting node and traverse the `next` links to
   move toward the correct position. You should assume the node to insert is not already in the list.
  
1. In your notes, draw the expected linked list after calling your new insert method from `main` passing in 
   the `node` reference as the starting point along with a new node containing the string "Cupid". Your diagram 
   should illustrate any nodes that have been created along with their associated string values and next 
   references.

1. At the end of the `main` method of `Driver.java`, add the method call described in the previous step.
   
1. Write a method to verify that your insert method worked correctly. The output from this method should convince
   your instructor/TA that your method worked.

**CHECKPOINT**

<hr/>

[![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC%20BY--NC--ND%204.0-lightgrey.svg)](http://creativecommons.org/licenses/by-nc-nd/4.0/)

<small>
Copyright &copy; Michael E. Cotterell, Brad Barnes, and the University of Georgia.
This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/">Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License</a> to students and the public.
The content and opinions expressed on this Web page do not necessarily reflect the views of nor are they endorsed by the University of Georgia or the University System of Georgia.
</small>
