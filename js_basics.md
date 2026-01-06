JavaScript Language Basics
1. Variables
2. Data Types
3. Operators
4. Statements
5. Functions
 Variables
- Variables are storage locations in memory, where you can store a value and use it as a
part of any expression.
- Variables have 3 phase of configuration
 a) Declaration
 b) Assignment
 c) Initialization
     var x; declaring
     x = 10; assignment
     var y=10; initialization
- JavaScript allows to use variables without declaring if it is not in strict mode
                     <script>
                      x = 10; // valid
                      document.write("x=" + x);
                     </script>
                                      <script>
                                       "use strict";
                                       x = 10; //invalid x is not defined
                                       document.write("x=" + x);
                                      </script>
- If Javascript is in strict mode, then you have to declare or initialize a variable.
- JavaScript variables can be initialized or declared by using 3 keywords
 a) var
 b) let
 c) const
Var
- It defines a function scope variable
- You can declare in any block of a function and access from any another block in the
same function.
- It allows declaring, initialization and assignment.
Ex:
                       <script>
                        "use strict";
                        function f1(){
                        var x; // declaring
                        x = 10; // assignment
                        if(x==10)
                        {
                        var y = 20; // initialization
                        }
                        document.write("x=" + x + "<br>" + "y=" + y);
                        }
                        f1();
                       </script>
- Var allows shadowing. It is the process of re-declaring or re-initializing same name
identifier within the function scope.
Syntax:
                     <script>
                     "use strict";
                     var x = 10;
                     var x = 20; // shadowing
                     document.write("x=" + x);
                     </script>
Ex:
                            <script>
                             "use strict";
                             function f1(){
                             var x; // declaring
                             x = 10; // assignment
                             if(x==10)
                             {
                             x = 30; // assigning
                             x = 40; // assigning
                             var x;
                             x = 15; // shadowing
                             var y = 20; // initialization
                             y = 50; // assigning
                             var y = 60; // shadowing
                             }
                             document.write("x=" + x + "<br>" + "y=" + y);
                             }
                             f1();
                            </script>
- Var allows hoisting. It is the process of declaring or initializing a variable after
using.
Ex:
                          <script>
                           "use strict";
                           function f1(){
                           x = 10;
                           document.write("x=" + x);
                           var x; // hoisting
                           }
                           f1();
                          </script>
- Interpeter uses Lexical approach [bottom to top]

Let
- It is used to define a block scope variable.
- It is accessible within the specified block and its inner blocks.
                      {
                      block outer - a
                      {
                      block inner - a is accessible to inner
                      b - is not accessible to outer
                      }
                      }
- It allows declaring, initialization and assignment.
- It will not allow shadowing and hoisting.
const
- It is also block scope variable.
- It allows only initialization.
- It will not allow declaring and assigning.
- It will not allow shadowing and hoisting.
Syntax:
 const x; // invalid
 x = 10; // invalid
 const x = 10; // valid
