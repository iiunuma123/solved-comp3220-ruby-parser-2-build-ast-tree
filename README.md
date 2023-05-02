Download Link: https://assignmentchef.com/product/solved-comp3220-ruby-parser-2-build-ast-tree
<br>
<strong>Homework Summary</strong>

For this part of the Ruby Interpreter Collection of Assignments we will be modifying our existing Parser so that instead of printing parser output, it will build an <strong>AST</strong> (abstract syntax tree) that our interpreter can use to “run” programs written in the Tiny Language.

<strong>Details</strong>

I have given you all of the files necessary to complete the assignment. You will need to modify <strong>Parser.rb</strong> so that it builds the AST while it is parsing a file. I have included an <strong>AST.rb</strong> file that defines an AST node object that can be used to build this tree. It also has a method that can print the tree in list format (convenient since our interpreter will be written in a list-based language!).

I have done some of the work for you in Parser, so that you can use that as an example of how you should proceed. At the end of this document are screenshots showing what correct output should look like given some input files that I will also provide to you for debugging.

<strong>Note</strong>: We are building an <strong>AST</strong> and <strong>NOT</strong> a parse tree. What is the difference anyway!? The difference is that a

<strong>Parse Tree </strong>

parse tree would look much like the examples we went through in class when we compared parse trees to derivations. They would INCLUDE every rule in our class as root nodes or sub nodes in the tree. However, an

<strong>AST (Abstract Syntax Tree)</strong>

AST <strong>ONLY</strong> includes the actual lexemes that are needed to be interpreted. If you take a look at the compiler series article that I mentioned in a Canvas announcement, they illustrate that in one of the series articles.

For our assignment, we will always start with a program node as the root of the whole tree. That is the only “not concrete” thing that should be part of our tree.

<strong>Rubric</strong>

<strong>(-20 pts)</strong> Program won’t run

<strong>(-5 pts)</strong> Each extraneous symbol that is added to the tree

<strong>(25 pts)</strong> AST is properly formed

<strong>Extra Credit (20 pts)</strong>

Because of the way our grammar is defined (and because we want to produce a tree in list format) our tree <strong>WILL</strong> be nested correctly <strong>BUT</strong> our operands will be in reverse order. Since it is something that is consistent, it is an easy problem to handle in our interpreter (we already know it will be have this way, so just read in the operands in reverse order).

However, it is possible to produce the tree in list form with the operands in correct order. In order to do this, you will need to modify the <strong>AST.rb</strong> class. You will need to:

<ul>

 <li>add a method in <strong>rb</strong> that allows you to swap the first child of a node</li>

 <li>instead of calling <strong>addChild</strong> everywhere in <strong>rb</strong>, there are at least 2 instances where you will need to call your new custom function instead (maybe called <strong>addAsFirstChild</strong>).</li>

</ul>

<strong>Deliverables (That means this is what you turn in)</strong>

<ul>

 <li>rb</li>

 <li>rb (ONLY if you attempted the extra credit)</li>

</ul>




<strong>Screenshots</strong>

Using input1.txt

Using input3.txt

Using input5.txt (not written according to grammar specifications)

Using input4.txt (not written according to grammar specifications)


