# Whitepaper: **Data Interface Oriented Domain Specific Specification Language**
> By Marek Zelina
>
> *[bad draft 0.0]*

## Abstract
<!-- #LAST:  -->

---

## Table of contents
<!-- #LAST:  -->

---

## Ideology

Ideologies are everywhere. Whether we like it or not, even if we don't create one, when there will be enough people, an ideology will form naturally. We cannot control how an ideology will evolve, but we can at least define a starting point and create boundaries that must not be crossed.

Here we are outlining key directions and targets that the project should evolve towards. You can view them as the Original Vision. Those points are not set in stone, and can be changed. But Before changing a proper discussion concerning the full impact of the proposed changes.

### » Development process

This language is just a tool. And we use tools to achieve results. In case of a programming language, the main use case is in turning an idea into real working solution. The main difficulty is the difference in how wage our ideas are and how precise a program must be to work properly.

To maximize time spent on solving real problems and to minimize time spent on fighting with tools, we propose the following development structure:

- **Quick draft of an idea**:

  You can do this on paper. You can do this while talking to a client. It can have drawings or it can be written. It's anything You want to, just to get the idea out of Your head.

  It is good to start brainstorming and rethinking the idea.

- **Proof Of Concept [POC]**:

  Create a quick demo that actually works, or at least where the crucial components work. It can involve  copying and pasting, or doing hard and complex operations manually. The point is to show that it could actually be done. You don't need to implement everything, just the hard and crucial parts.

  Here a good tools and frameworks can really help You.

- **Minimal Viable Product [MVP]**:

  Now You want to take everything from POC and make it into a full package. It should have just the minimum amount of elements needed to fulfill the core idea. It is meant to be done quickly so You can show it off. If You can reuse elements of other projects, temporary assets, libraries. Don't focus on efficient or clean code (You will rewrite it anyway).

  Again good tools and frameworks will help You tremendously.

- **Version 1.0**:

  Now You are actually creating the full version 1.0. Now You should implement all the necessary functionality. You will probably maintain and develop this idea further, so write clean code. It also may be a good idea to think a little about code efficiency (within reason, since You are probably not starting with a 1 000 000 users). It may be worth considering how will You be able to add new features or expand the app in the future.

  Here a good guidelines and static analysis may be very helpful.

- **Maintain and optimize where necessary**:

  Now You have entered the long voyage. You will need to repair all the leaks and bugs. Sometimes it can happen that parts of Your code are no longer optimal enough, and You need to optimize them. You may want to benchmark many different solutions and implement the best one. At some point You may even need to redo the whole project structure.

  Here a good, modular project structure will help You.

This development structure, allows You to quickly test Your ideas and fail fast in case they are not good enough. This language should if possible work well for every level of a project.

### » Ease of use

Often a subpar tool is used, just because it is better known or simply easier. The harder it is to use a tool, the bigger the barrier of entry. The bigger the barrier of entry, the less likely it is that someone will use it. If not many people will use it, then it is also less likely that even professionals will use it if there are alternatives.

The most crucial part in making something popular is the first impression. In the case of tools the first impression is mostly about "What awesome can I do with it?" and "How hard is it to do this awesome thing that other guy did?".

- **Plug & Play**:

  If possible, the best option is to be able to just find something on the internet (or wherever) and just use it in Your project. No configuration files or education. This approach requires elements used in that way to be extremely intuitive with good examples and small scope.

- **Webapp**:

  The easiest way to get crossplatform support with no installation and easiest access is to create a webapp. Applications in browsers tend to be inefficient and somewhat limited (for example no file access by default and limited local storage). But if it doesn't even require logging in, a lot of people may start using it for small everyday things. Especially if there will be a simple single-click way to share.

- **Display only the necessary information**:

  Since we've opened our product to wide range of people, we can assume, that a lot of them will use it without clear goal or motivation in mind potentially other then curiosity or wanting to see what they friends has made.

  Such people will likely not want to spend hours learning how the interface work and what is important and what doesn't matter. Once they think it is too hard, they will just turn it off.

  The solution is, to present them with the minimal but readable and intuitive interface. Limit pointy corners and colors to important parts, since they grab attention. Make table borders less visible. Hide all non crucial information. Your users will appreciate it.

### » All in one (for small projects)

  Today we need a lot of different tools for creating even a simple webpage. In most cases we use text, which needs spell and grammar checking, plus we deal with multiple languages. We use images and videos, which often need some adjusting. We even deal with procedurally generated graphics. We use animations. We use components. We unittest. We test integrations. We use many different and responsive layouts. We use many fonts. Different programming languages. And so on...

  The biggest and most amazing part of linux terminal is that we could do most of we needed without exiting it. It has a standard data exchange mechanism (stdin, stdout, stderr), and we can easily combine simple programs into big automated machines.

  Now, why not add this functionality to our IDEs. We don't need full Photoshop for simple resizing or adjusting colors in an image. If we would use a webapp, we could make some fields accessible by browser extensions like LanguageTool. We are already using multiple languages in ours IDEs. We don't need complex tools in most cases, and this already would help greatly (especially for new users, who can get overwhelmed by shear number of programs they need to learn).

### » Start from anywhere

  Every project is a bit different. Sometimes this means that it starts from a wireframe. Other times it may start from implementing a communication protocol. Yet other times it may begin from a simple button component or some utility functions. It may even start from creating a full memory layout and describing all the functions.

  Either way a programming language should allow for any way to start a project and then support combining everything into one seamlessly. We can do this by encouraging clear and modular project structure.

### » Safety first

  Safety in programming is a big topic. Since one piece of code, written by one programmer, can be used by millions of people millions of times, means that this programmer has a huge responsibility. It doesn't help, that most people just want to use the software without looking at the code, and understanding how it works (it would be unrealistic if they did). But all it takes, is just one vulnerability and one malicious person to find it.

- **Prove if possible**:

  So when we can, it would be great to prove that our code does what it should and nothing else. Most languages don't have any support for that (for example Idris does). Note that You don't need to create a full mathematical proof. It is often just enough to state and ensure that each step of the code is there for a reason and produces expected outcome.

- **Test otherwise**:

  If we cannot prove (or it just takes to much time), then we should test our code. If sensible, automatic testing is the best option, since we can run then every time we make a change or call with different parameters(like asserts, unittests, integration tests). It is also useful to ask other people to test the code, both programmers on different levels and non-programmers (if it makes sense)

- **Run static analysis**:

  It is also advised to run static analysis on Our code. It will not catch every problem, but it may greatly reduce the number of simple bugs in the code, or improve its readability. In cases where We need to manage memory ourselves it can find potential memory leeks. In other cases it may find optimizations or redundancies. It can also find a lot of missing cases or palaces where we didn't guard against exceptions. Those exceptions may not even come up in our testing and end up being a ticking bomb.

- **Do whatever when You're just testing**:

  But sometimes we are just exploring and testing stuff. In this case, we can do anything we want (if it is legal and morally acceptable). In those cases we don't need to bother with safety. We just need to take care to not take this mindset into our work.

### » No restrictions

  Product should not be restrictive. Making people rely solely on one technology or company stifles progress. It may work wonder for financial side of business is not really, but definitely will alienate a lot of people and discourage exploration.

- **Encourage exploration**: [minimize annoyances]

  In contrast if we encourage exploration, people will be more likely to find unexpected uses of our products and even help develop them. This is the case with many open source projects, where users with technical knowledge are finding bugs, fixing them, proposing and developing new features. And they do this even without getting payed.

  To encourage exploration we just need to give people simple tools to create something they want and to extend what they already have. The greatest games after many years are often those who have a big modding community. And the same goes for programs. Make it as simple as possible to create modifications to Your products.

  Next way of encouraging exploration is to add good instructions whenever somebody needs them and make it easy to test things. Granular version control (even simple `ctrl+z` or quick `make comment` with `ctrl+/`) is great for that. You can explore a couple of ways of doing things before committing.

- **Don't restrict 10x developers**:

  For some 10x developers are a myth, but certainly some developers are much more productive then others. It would be great to empower them even more. Everybody has certain tendencies and a unique way of thinking. Enforcing strict style rules may make the codebase more readable, but may also stifle the productivity of some. So why not take the best from both worlds?

  An actual structure of the code can be represented in many forms. We could create multiple ways of displaying the same structure and mechanisms for transforming the code from one to another. If on top of that we add an architecture focusing on interfaces and be free to replace instead of modifying code, we will create a project structure that maximizes productivity.

---

## Core concepts

Here is an overview of the most critical design decisions made for this language. They are arraigned into 4 categories and to then to build on each other. By themselves they aren't innovative, but they were chosen with deep care to work together really well and adhere to the vision form the Ideology.

### » Extendable IDE

The most important and somewhat controversial decision is to base this language on IDE instead of standard text.

- **Structural Editor**:

  Instead of the standard text based language, we propose a structural editor. This kind of editor doesn't require a parser to understand the code by the computer. Instead the programmer works more closely on the same AST that the compiler/interpreter uses. This can speed up the startup of the compiler/interpreter (or any other tool).

  Working closer to AST also doesn't require the programmer to hold the language model in the head, which can lead to smaller amount of bugs. Instead the programmer can inspect the AST as they construct the program.

  This approach allows to store much more information directly with the code, without overwhelming the programmer. Instead we could display this information in a much nicer form like for example display images as images or data tables. Then when the programmer needs to they can change how it is displayed for quicker editing. We could also display UI components alongside the code, so the programmer can modify them quicker and check the results.

  This type of programming was already explored with software like Jupyter Notebook with great success.

- **Co-programming**:

  Structural editing also allows for storing actual values alongside the code. If we then add some automated functionality, the IDE could help the programmer by dynamically annotating the code.

  For example when writing the code, the IDE could add type annotations if possible to deduce. Those would not only be a visual hint, but an actual type annotation like the ones written by hand. It could also write annotations if a function has side-effects, or throws an exception, or some cases are missing.

  Additionally, the IDE could differentiate between things generated and things written by the programmer. If the IDE would notice an change or an error it could instantaneously change it if it was generated by the IDE and ask to change if it was written by the programmer.

  In some cases, it could also auto fill a portion of the code or suggest optimizations. But always respecting the programmer.

- **Syntax as a library**:

  This way of structuring the code opens up a lot of new possibilities for syntax and semantics. It would take extreme effort to create all useful ways of using it. On the other hand, many people will think "If it would just have this one thing!".

  To solve both problems, we can just alow and even encourage, creating custom syntaxes and semantics. The core language will actually be just a way of specifying the syntax and semantics, and a common base computational model. This means that by creating one language, we are actually creating a huge family of languages, each made specifically to solve a particular problem, where all of them can communicate with each other (and thus also other languages like C or JavaScript).

- **Extendable IDE UI**:

  Another huge thing that is necessary and will work well with custom syntax, is extending the IDE itself. Like in Godot, here anybody will be able to add custom panels to the IDE UI that can display information or modify the code itself.

  By itself, this is nothing special, just a graphical way of creating macros and querying information. But now consider combining it with being able to display all kinds of data in there "natural" forms, and the ability to store information and values in the code itself, and interacting with other languages or programs. Now one can easily see that by adding a just a couple of buttons, a simple program for cropping a video can be made.

  Those element alone make this way of programming useful.

### » Life quality features

The IDE and structural editing make code more readable and can make programming more fun. Now lets look at decisions that actually make programming and maintaining the code a lot simpler.

- **Value semantics**:

  First is definitely value semantics by default. The moment when one does not need to think if the data will be mutated or not, relieves a lot of pressure. This is also used in Swift, Rust or C#.

  Now if a function mutates the data passed in, it must be explicitly specified. We want to allow mutating the data for optimality and instructions like `swap` or `sort`, to not generate copies unnecessarily.

  Another thing with value semantics is comparison. Even if a string is an array of characters  two strings containing `hello` but in different parts of memory should be considered equal. This can be quite expensive to check in cases of big nonlinear structures. But this will allow for intuitive checking if nested arrays are equal.

  If we want to check if they point to the same memory, we can just ask it explicitly (like `mem_ptr(A) === mem_ptr(B)`).

- **Live coding**:

  The next big life quality change is Live coding. It turns out that one of the biggest problems for people to grasp when learning to program is the language execution model.

  The language execution model is about the structure of memory, scope of variables, how the values will mutate, and that after a variable changes in one place it will also have the new value in all other places plus the previous value is not accessible.

  Here we propose a different approach. Since we are working almost directly on the AST in an IDE with co-programming abilities, we can execute parts of the code immediately.This approach is one of the biggest points of success for SpreadSheets.

  Imagine that we are writing a function, but right after its declaration we also write an example call (like fib(5)) and turn on the live coding for it. The function is called, number 5 is written as a value for the argument, and is says that nothing is returned. Now we write `return fib(n-1) + fib(n-2)`. The IDE computes a couple of terms and displays information that the recursion doesn't terminate. So we add a base case `if(n < 2) return 1`. Now the function terminates, returns correct answer, but we also see all recursive calls to it, and we start wondering wy there are so many duplicates.

  This is a very simple example, but shows the idea. This is both a way to use parts of a program before it is written completely, as well as an extremely powerful debugger. With this people who are just starting programming, or people who are trying to understand how the code works will be able to test it live. This will encourage exploration and just having fun with programming.

- **Data oriented**:

  It is much harder to reason about complex things, than it is to reason about simpler things. Complexity can be crudely measured by the number of elements, but a much better measure is a number of combinations of interactions between elements. On top of that, smaller elements can be reused much more easily.

  This is a big drawback of objects combining data and functionality. Here we will take the best from both worlds.

  Fundamentally we will separate data from functionality. We will have a set of tools that will aid with this. It will be easy to combine data structures into a more complex ones and then extract the components similarly to inheritance and dynamic dispatch in OOP. Combinations of data structures and their functionality will be done by modules. The main difference from a class will be, that a module will not be inheriting from other modules, so no diamond patterns. Instead there will be a set of interfaces to handle all common cases and structure decomposition.

  Technically everything will be treated as data. All types, functions, the AST, all parts of the IDE, syntax rules and files. This style of programming will maximize code reuse, and extending functionality of already existing objects. It will also allow live manipulation if needed.

- **Algebraic data types**:

  A lot of functionality for defining and manipulating data structures will come in form of algebraic data types. With this we will be able to easily combine structures together, but also destructure them and rearrange to create new ones.

  Since basic rules for constructing complex data types will be know, it will be possible to create a comprehensive set of tools for data serialization, displaying, deserialization, and in the case of functions even automatic manipulation like symbolic differentiation (when possible).

- **Complex pattern matching**:

  The focus on data and its structures will make it possible to use one of the most intuitive programming technics pattern matching. Here however we will be able to match the data structure shape as well as its values.

  Pattern matching can greatly improve readability, but also safety since the IDE can check if all cases are covered.

  Here the pattern matching will also work with restructuring and destructuring from from the algebraic data types, to allow for polymorphism. We will be able to pattern match inside functions like a complex `switch case` expression, but also on the parameters allowing us to create partial definitions (like: `this function accepts only positive integers; for others report undefined error`)

- **Comprehensive naming**:

  Another big thing that help readability is naming of functions and data types. Not all functions are equal and made to do the same thing. Here we will want to explicitly call a function that deterministically returns a `true` or `false` a `predicate`, interface for getting or setting a value as a `getter` or a `setter`. Functions with side effects outside of manipulating memory as `procedures` and so on. Function that takes a structure and returns its equivalent in a different form a `mutator`. And so on.

  The IDE itself will suggest and enforce the naming.

- **Aliases**:

  On the side of smaller things is an ability to create aliases. This is a part of the IDE, and not the language itself. It will make it so if we forget if adding an element to a list was `add`, `push`, `append`, `Add`, `concat`, `unshift`, or any other, we can write any of them and the IDE will check all aliases for functions that would make sense in the context, and suggest the actual one.

- **Symbol context**:

  Since there will be a lot of manipulation of types, there needs to also be a set of tools to offset its complexity. For this we will allow a programmer to manipulate the context itself. It will be possible to create rules inside a semantic block that will specify how each symbols will be understood.

  Those rules can include statements like `let a ≡ array[i]` and then whenever `a` is mentioned `array[i]` will be used, even when the `i` changes, thus `a` is just a shorthand for `array[i]` in this semantic block. The rules can be much more complex. This can somewhat resemble macros from C, but is much more structured.

  Importantly, this type of context manipulation will be limited to semantic blocks (think of `{...}` in C as one semantic block).

- **References**:

  The final life quality feature are references and a reference graph. Here we are allowing programmers to specify relationships between elements that are more complex then just context manipulation.

  Here we could for example declare that a value in one part of a program (for example health bar percentage) is to be linked by reference to a different value in a separate part of a program (an actual heath value of a player). By doing so we instruct the IDE to update the value whenever the reference changes (to update the health bar when the actual player's heath changes).

  This could be easily done by creating a function `update` and calling it whenever the value changes, but it is the same case as with memory management in C, it makes everything more complex and people tend to forget.

  The reference could also be linked to function call executing a function whenever some value is updated. The timing of the update will be settable by the programmer if it should be resolved immediately or after everything is finished.

  With this creating event driven applications, or interactive UIs should become much simpler, and in some cases the optimizer may find a better way of handling it then a programmer would without spending hours on it.

### » Program structure

All the different syntaxes, notations, symbols, and ways to write our programs, will lead to a lot of confusion if not handled carefully. And since we are the most creative when working in constrain environments, the language will be geared towards a uniform file and code structure.

The IDE will enforce this structure unless one specifically declares not to use it.

- **Alternative paths**:

  First major decision is to separate the main execution path from the alternatives. Usually we write our main code and do a lot of error handling right in the code itself. This makes it less readable at first reading. Here however we will keep the main execution path clean and lean. But we will also create alternative code paths whenever needed.

  These paths will be marked by a special set of symbols and an indication when they take over. Some of those paths may simply fix something and go back to the main path, or they may exit from the function early, or even crash the whole program. They may even have side effects. All of it will be marked in the symbol.

- **Data Interfaces**:

  Another big thing are data interfaces. Since there will be so many different types there will be a set of common interfaces that will be used to implement basic functionality like `sort`, `swap`, `add`, `subtract`, and so on.

  When we create a new type, instead of implementing those functions ourselves, we simply will create an interface that tells the IDE how to interpret our type in this context.

  The interfaces will also work in the other direction. When we will want to implement something, we will often use structures provided by the interfaces instead of a the actual structures. This way our implementations will work on a wide range of types without any additional work.

  In simple cases, we will not even need to specify the interfaces ourselves, since the IDE will be able to figure them for us.


  Additionally, when working with libraries, whenever we use a function, the IDE will automatically generate a shallow minimal interface of the functions we use (we can do it ourselves). This way, we will be able to see the minimum requirements for the library, the optimizer will be able to minimize the library. In case the library changes, we will be able to easily test if it still fits our needs. If it doesn't, we can simply write our own.

  In some cases, we may even want to combine multiple libraries to account for one interface. In such a case, the IDE will generate interfaces for each of them and link them. Later, the optimizer will be able to generate a single simplified library.

  And finally, this approach will also be used when writing code without using a specific library. In such a case, whenever we use anything that is not defined, it will be added to the interface. Thus the interface will also be a collection of all things we need to implement or find a solution for.

  This type of programming will also allow us to create a clear specification of the whole program and each of its parts separately, that the type checker will be able to check prior to development. This should really help in developing large projects with any size of a team, both by big teams and solo programmers.

- **Graph model**:

  Since everything will be done using interfaces, we can use the most versatile structure for actual code without worrying that the underling data structures would be suboptimal.

  So the structure we will use is a directed graph. This way values will be treated as graph nodes. The graph will have named nodes and edges and it is possible to have multiple connections between two nodes. Nodes can also be virtual and not store any data, but just be interfaces or contain information that will be removed in optimized release build.

  For example given an array `A`, we can always ask for the `next` and `prev` element. And this also will work in case of strings or even multi arrays. In multi arrays, the `next` element will work in a manner of going through deepest array, and then the `next` of the final element is the first element of the next array.

  By using `next` we will always be guaranteed to receive the deepest value in the structure and all values will be accessible by repeatedly calling `next` or `prev` (i.e. it will loop over the values). This will be ensured by `value` edge. A `value` of a simple value is just it itself, but a `value` of a container is the `value` of its first children. Importantly value from `value` also will contain information about its position in the structure, from which `next` is calculated.

  Another useful set of edges will be `up`, `down`, `left`, and `right` (potentially more). This will allow us to intuitively move around grids (for example UI).

  A comprehensive list of the implemented edges and algorithms will be created later in a separate document.

- **Semantic code segregation**:

  Potentially the most controversial decision comes in the form of semantic code segregation. Here the idea is to somewhat force the code structure.

  Each program will be composed of files, and each file will define a single thing. This thing could be a simple module, data structure, syntax rule, settings, a function or an interface.

  As the most important thing, each file will first specify what it will define, and what it will requires from other files.

  Most of the basic elements will have a forced structure and file type. For example we may specify a utility file, where we put common utility functions and data types. Or we could specify a format file, where we put common formatting rules. Or we could specify a startup file.

  In case of functions, we first declare a function, its requirements (parameters, types, and constraints), and its return type with assertions. Then we can proceed to its basic implementation. And then we may specify additional optimized implementations.

  The IDE will enforce a correct use of this format (if possible it will also suggest how to use it), unless clearly specified not to. The format itself will be specified in the language, so it will be possible to specify a new format.

  The hope is, that even thou the language itself will allow for bizarre and weird code, the enforced structure will help to keep it clean, modular and readable.

- **Attributes**:

  To aid the communication between programers and with the IDE, the code will make heavy use of attributes. The attributes will clearly stand out as not being code, but just an information on how it should be run. This stems from the idea, that nothing should be hidden from the programmer.

  Attributes will for example specify, which overload should be used, or how `right` or `next` should behave in ambiguous cases. They will also add additional information for the optimizer in case the programmer suspects that a certain option will came up much more then others, to prioritize optimizing it.

  Attributes will both be written by the programmer as well as the IDE. Attributes written by the IDE will be visually different.

- **Requirements & Assertions**:

  To ensure that the program does what we want to, and also to communicate what we expect of it, we will use requirements and assertions.

  Requirements will be set as specification that this code cannot pass typechecking if the conditions are not meet. They will make heavy use of pattern matching and be able to check, types, values, and introspect the code checking if the type has a certain implementation, attributes, fields, or if it doesn't contain something.

  Requirements can be used anywhere we declare something. Examples are functions, types, interfaces, modules, rules.

  At run time requirements will crash the program if they are not satisfied.

  When we will want to check if the code actually does what we want it to, we will use assertions. Assertions will also be able to check the same things as requirements.

  They however will not crash the program if they are not satisfied. Instead will run an alternative execution path (that may crash the program).

  Requirements and assertions can also be used for automatic unit test generation.

### » Optimization

Many of the already describe concepts, may have raised a lot of red flags for those of us who want to write optimal code. Here we want to address this issue, because one of the targets of this language is to achieve code runtime comparable to C and not worse then Rust. Importantly, the language will help to write efficient code, but not enforce it.

- **Strong typing**:

  The most important element is strong typing. The language will allow for dynamic like types using boxes similarly to Rust. But this will not be advised and the IDE will suggest alternatives whenever possible.

  In all other cases the IDE and the optimizer will work hard to optimize any dynamic dispatch and simplify control flow. With the use of attributes, the compiler will ask questions and try to determine the actual best options at the stage of writing the code.

- **No native types**:

  The language will not provide a set of standard types like `int` native to the hardware. Instead it will use abstract types for the IDE and the programmer will specify the necessary hardware types in a compilation specification. 

  The types will be specified by in the libraries or by the programmers themselves. With this using custom implementations and specifications will be possible and natural.

  This means that all algorithms will can be written without using specific types, and then the types can be inserted during compilation and optimized for each platform specifically.

  This may potentially lead to situations where a native type is not compatible with the implementation. In such a case the type checker will most likely notice it and check if it could automatically rewrite the implementation and then the IDE will ask if it should actually commit the change. In case it is impossible to do it automatically the IDE will just leave it to the programmer to resolve the problem.

  This also means that transpiring code to other languages is possible. It could even enable writing code that would feel native to the targeted language.

- **Zero cost abstraction**:

  Implementing everything from specification could lead to extremely inefficient code. For this we will use technics similar to the C++ idea of Zero cost abstraction. Its a promise that any generic code that adheres to basic rules will later be optimized to being indistinguishable from a hand written code in terms of performance.

  This especially will be important in case of the large use of interfaces and custom types.

- **Zero cost redundancy**:

  Additionally, the programmer is free to define as much code as they want to with a promise that all unneeded code will be striped away. Some languages include deleting dead code. Here the optimizer will be allowed to generate new data structures optimized for certain operations. It will be able to even remove parts of functions if they compute values for removed fields.

  All optimizations generated with this method will be shown to the programmer alongside the code, when they are used.

- **Binary over text**:

  Since we are working with IDE and will be displaying everything in a processed form, we can use binary data directly. Since data written by hand will be stored as binary data, then it makes it easier to also store all other types of data as binary. This also means that most of communication between parts of the program and libraries will be done in binary. Since so much will be done in binary, there will be a set of tools for working with it.

  In case where binary is not available (such as HTTP or HTML) text will be used. To make it possible a set of tools will also be available here.

- **Hardware ambivalence**:

  All compilation steps and definitions including native and internal functions and types, as well as calling conventions will be specified as a library. This means that any program may be compiled without changes (if compatible) to any hardware, OS, and or target language.

- **"Zero" startup cost interpretation**:

  Since the code will be in edited and saved in a form of the actual AST, and most of expressions will be stored in optimized versions already alongside the AST, the interpretation startup cost will be minimal. In some cases it may even be ready to be executed without parsing.

- **Reflection & Meta-programming = static analysis**:

  Since most of the program will be abstracted as a graph, we will be working almost directly on the AST, and we will be co-programming with the IDE, we will also have the ability to introspect the program itself from the code.

  This means that we can run automatic analysis and change the code for example adding and removing debug info. This makes it so we can write tools for static analysis or testing as a library instead of external tools.

## Examples [after POC]

## Program provability

Important part of specification is to ensure that the final product will do what it is suppose to. In cases of programming this also involves security and user privacy. In some cases like scientific, military, medical or financial software the correctness it is even more important to ensure that the program correctly accomplishes all tasks and can handle all errors.

### » Requirements & Asserts

  The basic way of ensuring correctness is making use of requirements and assertions. This way we can ensure that, the type checker will ensure that the code satisfies what programmer expect it to do.

### » Code segmentation with Requirements & Asserts

  In case of bigger functions and procedures, even more granular requirements may be given. This can be done by segmenting the code into logical parts (like steps of an algorithm) and placing requirements and assertions at both ends of it. Thanks to structural editing, this can be done even for each inline expression.

### » Code segmentation with local proofs

  Unfortunately just having the assertions can sometimes not be sufficient. In such cases, the programmer can prove that the each segment will achieve the result and that they each segment will create required state for the next one. For now this must be done by hand and also will need to be confirmed by hand.

### » Meta programming for automatic testing and proof checking

  And finally, using reflection and meta programming a libraries implementing automatic test generation and even proof checking can be created inside the lanugage.

## For non programmers

One of the goals for the project is to also serve as a tool for non programmers. Both as an introduction to programming, but also as a interactive sandbox for simple but useful tools. 

### » IDE as an interface

  First use comes from the fact that the IDE itself is extendable and can host tools similarly to game engines like Godot or Unity, where for the purposes of developing games a lot of tools are created to make it easier for less technical people on the team (but also for the programers themselves).

  Here however, we are not focusing on developing games, but any program. So it is possible to even create fully fledged programs.

### » DSL

  Very often, non programmers are experts in other fields. Each field has its own notation and structure understood only by the people versed in the filed. Giving them a tool that would allow for making their representation be understood by the computers could greatly help them work.

## Roadmap

Here we present the roadmap of the project and how it will develop. Instead of time this roadmap will be measured by milestones. Anything in the roadmap is subject to change since everything in the language is to final. Firstly we lay down targets that will be instrumental in making future decisions on the direction. Then we will provide a rough sketch of the future plans.

### » POC

  There were already versions of the POC made on paper. They however were not enough to convey the idea and uniqueness of the project. Because of this, the first order of business will be to create a set of interactive examples of UI and the IDE. The examples will showcase the idea of the structural editor in practice. However they will have no execution model behind them and be limited to only examples prepared.

  Examples include

  - Client-Server communication protocol;
  - State machine;
  - Text;
  - Alternative paths;
  - Attributes;
  - Graphical syntax declarations;

### » MVP

  For the MVP, the examples form POC will be possible to create without handcrafting and a simple runtime interpretation model will be created. The execution model will be made to run using Javascript, so the behavior and basic functions will be directly taken from it.

### » v1.0

  For version 1.0 a basic but fully flushed out syntax editor will be created. We will also implement a simple VM with binding to Javascript but allowing more specific runtime.

### » full roadmap

While working solo:

- Writing first draft of this **whitepaper**;
- Publishing the first draft;
- Correcting and rewriting the first draft;
- Creating the **POC**;
- Testing the POC with a small group;
- Updating the whitepaper to version 1.0;
- Creating the **MVP**;
- Testing the **MVP**;
- Updating the whitepaper to version 1.1;
- Developing the **v1.0**;
- Testing and improving the UI;
- Specifying the first draft of basic STD;
- Adding basic support for missing core concepts;

## Shortcomings

As with any bigger decision there are drawbacks. Some of them may be deal breakers for some, but unimportant to others. Non the less we should always at the very least be aware of them.

### » Disk space of projects will be bigger

  Since a project will be a syntax specification, compilation/interpretation specification, multiple versions of optimized code, and more complex structures together with data itself (including images and videos), projects may tend to require more memory. For now it is hard to estimate how much exactly and first estimations will be given in version 1.0.

### » No uniform notation = each project is a unique ecosystem

  C is a simple language, to the point that if preprocessor macros are not abused, most programmers knowing C should be able to understand arbitrary C code. This is not the case with this language. Since a even syntax, not to mention semantics will be changeable, aside from libraries and conventions it will not be possible to understand the code without experimenting or learning the specific project rules.

  Because of this it will be advised to use STD as much as possible.

### » It is potentially impossible to prove everything

  The language will give tools for testing the code and ensuring its correctness. However it will most likely not be possible to prove every program due to the nature of the provability itself.

## Open problems

Not every part of the language is designed. There is still a lot of work left to be done.

### » Enabling team development

  Even if the language is designed to enable solo programers to do more amazing things easier, most productions will still be done as a team effort. The language still needs support for version control systems, that will allow multiple parties working on the same project without interfering. Even more challenging may be to solve cases where people work on custom syntax or semantics, or cases where people work on elements close together.

  The first way we will implement is dividing the project into smaller independent parts with interfaces.

### » Enable library API & optimization without code sharing

  We could argue if forcing open source code and sharing the knowledge and ideas, makes progress quicker or if it makes it more likely that people will hide what they do. Non the less as of in some cases, an ability to make code unreadable is desired by some.

  There may be no official way for achieving this result, but compilation itself or transpaling with minimization may be enough. It is still needed to find a solution.

### » Interact with other languages

  A lot of code is already developed and requiring everybody to suddenly switch to just one new language that almost nobody has even heard about is quite impossible to say the least. To solve this problem we need to develop easy ways of interacting both ways with other languages like JavaScript or C++ aside from protocols like HTTP. Preferably a way of calling functions from other languages like native functions would be welcomed.

  This is not a hard problem, but important.

### » Support for git

  Probably the most wellknown version control system is Git. Git deals well with text and files. We will need to figure out a way of storing a 1TB project as a git with optimized file differences.

### » Develop Standard Library

  There is no STD even in the making right now. The STD as a standard set of functions, interfaces, types, compilation steps, syntax, and semantics is needed.

### » Develop package manager

  The needs to be a simple and secure way of shearing projects or simple examples. Since the project structure is different from most system, we need to find or develop a suitable replacement.

### » Define standard for companies

  Bigger projects cannot be made on shaky, ever changing, and unstable ground. The companies will not trust the project unless proper standard enforced from outside is defined.

### » Define politics

  This is a solo project right now, but it will evolve into a huge open source project with many contributors. In such cases even companies may get involved and someone may want to grab influence on the project development. This by itself may not be critically bad, but it poses a risk. To cover it at least a little, the project should have clearly defined how important decisions will be made, how the code can be contributed, and how the responsibilities will be divided.