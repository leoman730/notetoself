---
layout: post
title: "Clean Code: A Handbook of Agile Software Craftsmanship"
description: ""
category: “Book”
tags: []
---
{% include JB/setup %}

The book [Clean Code: A Handbook of Agile Software Craftsmanship] by Robert C. Martin (Uncle Bob) is highly recommended and respected by many software developers. From reading the first chapter, I was hooked. This book is a must read by anyone who want to become a better coder and to write elegant code that is pleasae to read.


* TOC  
{:toc}

### Introduction
> Writing clean code is what you must do in order to call yourself a **professional**. 
> There is no reasonable excuse for doing anything less than your best.

 
> LeBlanc’s law: **Later equals never**.

![productivity vs. time]

> Every change they mak to the code breaks two or three other parts of the code.

Adding new staffs not necessary means it can solve problem.


> Spending time keeping your code clean is not just cost efective, it’s a matter of professional suvival. 

> it is unprofessional for programmers to bend to the will of managers who don’t understand the risks of making messes.

> I like my code to be **elegant** and **efficient**
> 
> <cite>- Bjarne Stroustrup</cite>

> Clean code:

> - pleasing to read
> - exhibits close attention to detail
> - does one thing well
> - is focused

> Clean code is **simple** and **direct**. Clean code read like **well-written prose**. Clean code **never obscures** the designer’s intent but rather is full of **crisp abstractions** and **strightforward** lines of controls.
> 
> <cite>- Grady Booch</cite>

> Think back on a really good book that you’ve read. Remember how the words disappeared to be replaced by images!

A really  good book I ever read - “Javascript the good part”

> Our code should be matter-of-fact as opposed to speculative. It shuld contain nly what is necessary. Our readers should perceive us to have been decisive.

I think writing good codes is like writting a good thesis. 

> Clean code can be read, and enhanced by a developer other than its original author. It **has unit and acceptance tests**. It has **meaningful names**. It provides one way rather than many ways for **doing one thing**. It has **minimal dependencies**, which are explicitly defined, and provides a **clear and minimal API**.
> 
> <cite>- Dave Thomas</cite>

But do remember code with tests doesn’t imply the code itself is clean.

> Clean code always looks like it was written by someone who **cares**... sitting in **appreciation** of the code someone left for you - code left by someone who **cares deeply** about the **craft**.
>
> <cite>- Michael Feathers</cite>

“Craft” is the megnetic word for clean code.

> Clean code = Reduced duplication, high expressiveness, and early buildings of simple abstractions.
> 
> <cite>- Ron Jeffries</cite>

> When each routine you read turns out to be pretty much what you **expected**... You will read it, and it will be pretty much what you expected. It will be **obvious, simple, and compelling**.
> 
> <cite>- Ward Cunningham</cite>

Clean code = expectation + no suprise

> **Next time when you write a line of code, remember you are an author, writing for readers who will judge your effort.**
 
 
> The ratio of time spent reading vs. writing is well over **10:1**. We are constantly reading old code as part of the effort to write new code.

The book mentioned to recording an editing session for every keystroke, and then play it back like in a high-speed movie, you will find how much time you will spend just navigate the code instead of writing new code. This is pretty true on myself.


*The Boy Scout Rule*
> If we all checked-in our code a little cleaner than when we checked it out, the code simply could not rot.


### Meaningful Names
> If a neme requires a comment, then the name does not reveal its intent.

> Programmer must **avoid leaving false clues** that obscure the meaning of the code.

> Beaware of using names which vary in small ways.  
> ex: ControllerForEfficientHandlingOfStrings vs. ControllerForEfficientStorageOfStrings

> The truly hideous practice of creating a variable named klass just because the name class was used for something else.

Whoever doing thing like this should truly be critized publically.

> 
> ```shell
> # How are the programmers in this project supposed to know which of these functions to call
> getActiveAccount();
> getActiveAccounts();
> getActiveAccountInfo();
> ```


> If a variable or constant used in multiple places in a body of code, it is imperative to give it a search-friendly name.


According to wikipedia, the [Hungarian notation (HN)] is an identifier naming convention in computer programming, in which the name of a variable or function indicates its type or intended use.

> One difference between a smart programmer and a professional programmer is that the professional **understands that clarity is king**. Professionals use their powers for good and write code that others can understand.

> When constructors are overloaded, use static factory methods with names that describe the arguments.
> 
> ```shell
> Complex fulcrumPoint = Complex.FromRealNumber(23.0); 
> # is better than
> Complex fulcrumPoint = new Complex(23.0);
> ```

> **Pick One Word per Concept**  
> It is confusing to have fetch, retrieve, and get as equivalent methods of different classes.
> 
> It is not wise to draw every name from the problem domain because we don’t want our coworkers to have to run back and forth to the customer asking what every name means when they already know the concept by a different name.

 As programmer, they already know the terms belongs to CS domain (algorithem, pattern, math etc.), so use those terms whenever is possible.

> The hardest thing about choosing good names is that it requires **good descriptive skills** and a **shared cultural background**.  

### Functions  
> Functions are the first line of organization in any program.

There’s a distinction between function, method, and procedures. According to [adamcod.es]:

> A function is essentially a **sub-routine** that **returns one or more values**. A function should **calculate its return value based on its input**; It should provide an answer about its arguments, or compute a new value based on its arguments. 
> 
> A procedure is a sub-routine that **doesn’t return a value**, but does have side-effects. This could be writing to a file, printing to the screen, or modifying the value of its input. 
> 
>  A method is really a function or procedure that is executed **in the context of an object**. 


> Lines should not be 150 characters long. Functions should not be 100 lines long, and hardly ever be 20 lines long.


> The indent level of a function should not be greater than one or two, this can makes the functions easier to read and understand.

**REMEMBER THE ABSTRACTION!!**

> **FUNCTIONS SHOULD DO ONE THING. THEY SHOULD DO IT WELL. THEY SHOULD DO IT ONLY.**

> The reason we write functions is to **decompose a larger concept into a set of steps** at the **next level of abstraction**. 


> In order to make sure fuctions are doing “one thing”, make sure that the statemetns within the function are **all at the same level of abstractions**... Mixing levels of abstraction within a function is always confusing.

> We want the code to read like a top-down narrative. We want every function to be followed by those at the next level of abstraction so that we can read the program, descending one level of abstraction at a time as we read down the list of functions.

> Making the code read like a top-down set of TO paragraphs is an effective technique for keeping the abstraction level consistent.



### References
[Clean Code: A Handbook of Agile Software Craftsmanship]


### Recommendation
Clean Coder: [cleancoders.com]



---

[productivity vs. time]: {{ BASE_PATH }}/assets/images/productivity_vs_time.jpg
[Clean Code: A Handbook of Agile Software Craftsmanship]:http://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882
[cleancoders.com]:https://cleancoders.com
[Hungarian notation (HN)]:https://en.wikipedia.org/wiki/Hungarian_notation
[adamcod.es]:https://adamcod.es/2013/09/27/function-method-procedure.html