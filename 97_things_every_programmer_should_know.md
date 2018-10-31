# 97 Things Every Programmer Should Know

> Kevlin HENNEY - O'REILLY - ISBN-10: 0596809484 - ISBN-13: 978-0596809485

## Super quick

### Act with Prudence

do things right first instead of "dirty-and-come-back-later". if you did dirty, track it right away in your bug-tracker. pay off technical debt as soon as possible.

### Beauty is in simplicity

read other's source code. wirte short methods (5-10 lines). achieve brevity.

### Before you refactor	

write tests against current code. avoid the tempation to rewrite everything. make many small changes instead of big ones. use TDD. let your ego aside. new frameworks does not mean refactor.

### Check your code first before looking to blame others

### Code in the language of the domain

> spot the difference

```java
if (portfolioIdsByTraderId.get(trader.GetId())
	.containsKey(portfolio.getId())) {
	[...]
}

---

if (trader.canView(portfolio)) {
	[...]
}
```	

Working for a bank ? use bank's language "account, credit, ...". create types for your needs.

### Coding with reason

* avoid using `goto`
* avoid modifiable global variables
* each variable should have the smallest possible scope
* make objects immutable whenever relevant
* make the code readable
* make the code self-documenting by using descriptive short names for objects, functions, types ...
* if you need a nested section, make it a function
* make your functions short and focused on a single task (24 lines max.)
* functions should have few parameters (four max), does not mean you should not pass a big object relative to your needs
* each unit of code should have a narrow interface

### Comment only what the code cannot say

* no commented-out code (leave that to Git)
* no version related comments
* comments must not be distracting

### Continuous learning

* read books, magazines, blogs, twitter, websites, mailing list, conferences, podcasts
* write code
* find a mentor
* use virtual mentors (authors, developers on the web)
* know under-the0hood of your frameworks/libraries
* when you have a bug, understand what happened deeply
* teach/speak about things (lunch'n'learn)
* join a study group (meet-up)
* know your IDE
* read `Pragmatic Programmers`
* learn other things that technology such as domain specific knowledge : productivity, management, business

### Convenience is not an -ility

avoid using the argument of _convenience_ i.e.

* why make another method if I can add a switch
* if the second parameter ends with ".txt" the method will know what to do so no need for 2 methods.

for example don't use `walk(true)` to express "running".

### Distinguish business exceptions from technical

* technical problem : trying to access the 83th element of a 17-size array / database no response -> server will handle
* business problem : try to withdraw more money than I have on my account -> client will handle

### Don't ingore that error

deal wit problems at the earliest opportunity

### Don't just elearn the language, understand its culture


### DRY Don't Repeat Yourself

Duplication is waste, repetition is bad

### Hard work does not pay off

be focus, work smart, be "lazy", keep yourself updated. prepare, effect, observer, reflect and change.

### Install me

* linux browser from a UK IP" &rarr; english linux version from a european mirror
* easily know the destination of installation
* easily removable
* wizards don't help
* read a file or write one, no create projects, import directories, write email adress
* quick start guide
* "hello world" example with 5 lines of code
* no big XML or templates to fill out
* tutorial easy to understand, in human language
* Q&A tutorial

### Keep the build clean

avoid warnings, errors in the console &rarr; zero-tolerance policy

### Know your next commit

dont be afraid to throw code away, define your next easy end-goal

### Large, interconnected data belongs to a database

easy to scale, writing database-centric app is quite easy. SQL is great.	

### Make interfaces easy to use correctly and hard to use incorrectly

* easy to use correctly : in an API, use almost always pass the correct parameters with the correct values, because that's what's most natural.
* hard to use incorrectly : good interfaces anticipate mistakes people might make. a GUI might disable or remove commands/buttons that make no sense in current context, for example API might eliminate argument-ordering problems.
* write calls to API before the functions have been declared
* study how interfaces are misused to fix them
* if users try to do an irrevocable operation, try to make this operation revocable.

### Make the invisible more visible

* if you're 90% done but you struggle to debug the remaining 10%, the you're not 90% done. make those things visible so you can see it for what it is.
* if your project is on track but one week later it's 6 months late, find what's the cause
* write unit tests
* track tasks (even with to do, doing, done)

### Testers are your friends

### Only the code tells the truth

If your code needs comments, refactor it so it does not need them anymore.

### The professional programmer

> __personal responsibility__

* a professional programmer is responsible for its own career, so keep learning
* a professional programmer takes responsibility for the code they write
* a professional programmer is a team player
* a professional programmer does not tolerate big bug lists (big issue lists)
* a professional programmer does not make a mess
* a professional programmer does not rush before deadline quick'n'dirty

### Read code

read other's code. read your own old code.

### Reinvent the wheel often

get intimate knowledge of the inner workings of various components that already exist (i.e. virtual paging, memory managers, GUI, web-browser widget)

> reinventing the wheel and getting it wrong is more valuable than nailing it first time

### Step back and automate, automate, automate

always typing the same things or clicking on the same buttons ? learn bash, powershell, python3, selenium.

### Test precisely and concretely

> test a sorting algorithm

* we may think that a good test is that the algorithm should return a list with the same number of elements.

	3 1 4 1 5 9 &rarr; 3 3 3 3 3 (does not work)

* a good test should be readable
	
	3 1 4 1 5 9 &rarr; 1 1 3 4 5 9 (should be your test)

* concrete examples are often better to illustrate a general behavior

### Two heads are often better than one

Do pair-programming, 

### The unix tools are your friends

learn basic `grep`, `bash`	, `sed`

### Use the right algorithm and data structure

> good example, find the 'bug'

```c
// s.size = 100 000
for (i=0; i<strlen(s); ++i) {
	if(... s[i] ...) ...
}
```
	
### Write code as if you had to support it for the rest of your life

imagine your old boss is legally able to call you at night to ask you design questions about the project you did 12 years ago.

---

## More books ?

### Clean Code: A Handbook of Agile Software Craftsmanship

>  Robert C. MARTIN - ISBN-10: 0132350882 - ISBN-13: 978-0132350884

### Clean Architecture: A Craftsman's Guide to Software Structure and Design

> Robert C. MARTIN - ISBN-10: 0134494164 - ISBN-13: 978-0134494166

### The Clean Coder: A Code of Conduct for Professional Programmers

> Robert C. MARTIN - ISBN-10: 0137081073 - ISBN-13: 978-0137081073


### The Pragmatic Programmer: From Journeyman to Master

> Andrew HUNT - ISBN-10: 020161622X - ISBN-13: 978-0201616224
