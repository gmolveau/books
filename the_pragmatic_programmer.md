# The Pragmatic Programmer

> The Pragmatic Programmer from journeyman to master - Andrew HUNT & David THOMAS - ISBN: 978-0-201-61622-4

## Notes

"Kaizen" is a Japanese term that captures the concept of continuously making many small improvements.

One of the cornerstones of the pragmatic philosophy is the idea of taking responsibility for yourself and your actions in terms of your career advancement, your project, and your day-to-day work.

- Your Knowledge Portfolio

Your knowledge and experience are your most important professional assets.

#### Building Your Portfolio

- **Invest regularly.** Just as in financial investing, you must invest in your knowledge portfolio regularly. Even if it's just a small amount, the habit itself is as important as the sums. A few sample goals are listed in the next section.

- **Diversify.** The more different things you know, the more valuable you are. As a baseline, you need to know the ins and outs of the particular technology you are working with currently. But don't stop there. The face of computing changes rapidly - hot technology today may well be close to useless (or at least not in demand) tomorrow. The more technologies you are comfortable with, the better you will be able to adjust to change.

- **Manage risk.** Technology exists along a spectrum from risky, potentially high-reward to low-risk, low-reward standards. It's not a good idea to invest all of your money in high-risk stocks that might collapse suddenly, nor should you invest all of it conservatively and miss out on possible opportunities. Don't pull all your technical eggs in one basket.

- **Buy low, sell high.** Learning an emerging technology before it becomes popular can be just as hard as finding an undervalued stock, but the payoff can be just as rewarding. Learning Java when it first came out may have been risky, but it paid off handsomely for the early adopters who are now at the top of that field.

- **Review and rebalance.** This is a very dynamic industry. That hot technology you started investigating last month might me stone cold by now. Maybe you need to brush up on that database technology that you haven't used in a while. Or perhaps you could be better positioned for that new job opening if you tried out that other language...

#### Goals

- **Learn at least one new language every year.** Different languages solve the same problems in different ways. By learning several different approaches, you can help broaden your thinking and avoid getting stuck in a rut. Additionally, learning many languages is far easier now, thanks to the wealth of freely available software on the Internet.

- **Read a technical book each quarter.** Bookstores are full of technical books on interesting topics related to your current project. Once you're in the habit, read a book a month. After you've mastered the technologies you're currently using, branch out and study some that don't relate to your project.

- **Read nontechnical books, too.** It is important to remember that computers are used by people - people whose needs you are trying to satisfy. Don't forget the human side of the equation.

- **Take classes.** Look for interesting courses at your local community college or university, or perhaps at the next trade show that comes to town.

- **Participate in local user groups.** Don't just go and listen, but actively participate. Isolation can be deadly to your career; find out what people are working on outside of your company.

- **Experiment with different environments.** If you've worked only in Windows, play with Unix at home. If you've used only makefiles and an editor, try an IDE, and vice-versa.

- **Stay current.** Subscribe to trade magazines and other journals. Choose some that cover technology different from that of your current project.

- **Get wired.** Want to know the ins and outs of a new language or other technology? News groups are a great way to find out what experiences other people are having with it, the particular jargon they use, and so on. Surf the web for papers, commercial sites, and any other sources of information you can find.

Think *critically* about what you read and hear. You need to ensure that the knowledge in your portfolio i accurate and unswayed by either vendor or media hype.

#### Evils of Duplication

Every piece of knowledge must have a single, unambiguous, authoritative representation within a system. <br>
DRY - Don't Repeat Yourself

With a bit of ingenuity you can normally remove the need for duplication. Often the answer is to write a simple filter or code generator.

The DRY principle tells us to keep the low-level knowledge in the code, where it belongs, and reserve the comments for other, high-level explanations.

Use the header files to document interface issues, and the implementation files to document the nitty-gritty details that users of your code don't need to know.

Impatient duplication is an easy form to detect and handle, but it takes discipline and a willingness to spend time up front to save pain later.

#### Orthogonality

When teams are organized with lots of overlap, members are confused about responsibilities. Every change needs a meeting of the entire team, because any one of them might be affected.

Ask yourself how decoupled your design is from changes in the real world. Don't rely on the properties of things you can't control.

#### Things to prototype

What sorts of things might you choose to investigate with a prototype ? Anything that carries risk. Anything that hasn't been tried before, or that is absolutely critical to the final system. Anything unproven, experimental, or doubtful. Anything you aren't comfortable with.

#### Estimating

If you say that something will take about 130 working days, then people will be expecting  it to come pretty close. However, if you say "Oh, about six months" then they know to look for it any time between five and seven months from now.

A basic estimating trick that always gives good answers : ask someone who's already done it.

#### The Power of Plain Text

Tip 20 - **Keep Knowledge in Plain Text** <br>
&middot; Plain text won't become obsolete. It helps leverage your work and simplifies debugging and testing.

The Unix Philosophy <br>
Unix is famous for being designed around the philosophy of small, sharp tools, each intended to do one thing well. This philosophy is enabled by using a common underlying format -- the line-oriented, plain text file.

#### Power editing

Tip 22 - **Use a Single Editor Well** <br>
&middot; The editor should be an extension of your hand; make sure your editor is configurable, extensible, and programmable.

Tip 23 - **Always Use Source Code Control**

#### Debugging

Tip 24 - **Fix the Problem, Not the Blame** <br>
&middot; It doesn't really matter whether the bug is your fault or someone else's -- it is still your problem, and it still needs to be fixed.

**Rubber Ducking** <br>
A very simple but particularly useful technique for finding the cause of a problem is simply to explain it to someone else.

Tip 29 - **Write Code That Writes Code** <br>
&middot; Code generators increase your productivity and help avoid duplication.

#### Pragmatic Paranoia

Tip 30 - **You Can't Write Perfect Software** <br>
&middot; Software can't be perfect. Protect your code and users from the inevitable errors.

#### Design By Contract

Liskov Substitution Principle: Subclasses must be usable through the base class interface without the need for the user to know the difference.

#### Dead Programs Tell No Lies

It's easy to fall into the "it can't happen" mentality.

Tip 33 - **Use Assertions to Prevent the Impossible** <br>
&middot; Whenever you find yourself thinking "but of course that could never happen," add code to check it. <br>
Assertions validate your assumptions. Use them to protect your code from an uncertain world.

Tip 34 - **Use Exceptions for Exceptional Problems** <br>
&middot; Exceptions can suffer from all the readability and maintainability problems of
classic spaghetti code. Reserve exceptions for exceptional things.

#### How To Balance Resources

1. Deallocate resources in the opposite order to that in which you allocate them. That way you won't orphan if one resource contains references to another.
2. When allocating the same set of resources in different places in your code, always allocate them in the same order. This will reduce the possibility of deadlock.

#### The Law of Demeter for Functions

The Law of Demeter for functions attempts to minimize coupling between modules in any giver program. It tries to prevent you from reaching into an object to gain access to a third object's methods.

#### Metaprogramming

Tip 37 - **Configure, Don't Integrate** <br>
&middot; Use metadata to describe configuration options for an application.

We recommend representing configuration metadata in plaintext. It makes life that much easier.

But when should a program read this configuration? many programs will scan such things only at startup, which is unfortunate. If you need to change the configuration, this forces you to restart the application. A more flexible approach is to write programs that can reload their configuration while they're running. This flexibility comes at a cost: it is more complex to implement.

So consider how your application will be used: if it is a long-running server process, you will want to provide some way to reread and apply metadata while the program is running. For a small client GUI application that restarts quickly, you may not need to.

#### Temporal Coupling

Tip 39 - **Analyze Workflow to Improve Concurrency** <br>
&middot; Exploit concurrency in your user's workflow.

To begin with, any global or static variables must be protected from concurrent access. Now may be a good time to ask yourself *why* you need a global variable in the first place. In addition, you need to make sure that you present consistent state information, regardless of the order of calls. For example, when is it valid to query the state of your object? If your object is in an invalid state between certain calls, you may be relying on a coincidence that no one can call your object at that point in time.

Tip 41 - **Always Design for Concurrency** <br>
&middot; Allow for concurrency, and you'll design cleaner interfaces with fewer assumptions.

#### Model-View-Controller

Tip 42 - **Separate Views from Models** <br>
&middot; Gain flexibility at low cost by designing your application in terms of models and views.

Tip 44 - **Don't Program by Coincidence** <br>
&middot; Beware of accidental complexity, and don't confuse a happy coincidence with a purposeful plan.

#### Refactoring

Tip 47 - **Refactor Early, Refactor Often** <br>
Just as you might weed and rearrange a garden, rewrite, rework, and re-architect code
when it needs it. Fix the root of the problem.
Keep track of the things that need to be refactored. If you can't refactor something immediately, make sure that it gets placed on the schedule.

Refactoring is an activity that needs to be undertaken slowly, deliberately, and carefully. Martin Fowler offers the following simple tips on how to refactor without doing more harm than good.

1. Don't try to refactor and add functionality at the same time.
2. Make sure you have good tests before you begin refactoring. Run the tests as often as possible. That way you will know quickly if your changes have broken anything.
3. Take short, deliberate steps: move a field from one class to another, fuse two similar methods into a superclass. Refactoring often involves making many localized changes that result in a larger-scale change. If you keep your steps small, and test after each step, you will avoid prolonged debugging.


#### Code That's Easy To Test

Why do we go to all this trouble? Above all, we want to avoid creating a "time bomb" -- something that sites around unnoticed and blows up at an awkward moment later in the project. By emphasizing testing against contract, we can try to avoid as many of those downstream disasters as possible.

Tip 48 - **Design to Test** <br>
&middot; Start thinking about testing before you write a line of code.

Regardless of the technology you decide to use, test harnesses should include the following capabilities:

- A standard way to specify setup and cleanup
- A method for selecting individual tests or all available tests
- A means of analyzing output for expected (or unexpected) results
- A standardized form of failure reporting.

Tip 49 - **Test Your Software, or Your Users Will** <br>
&middot; Test ruthlessly. Don't make your users find bugs for you.

Tip 50 - **Don't Use Wizard Code You Don't Understand** <br>
&middot; Wizards can generate reams of code. Make sure you understand all of it before you incorporate it into your project.


#### Project Requirements

> Perfection is achieved, not when there is nothing left to add, but when there is nothing left to take away. - Antoine de St. Exupery


Tip 51 - **Don't Gather Requirements–Dig for Them** <br>
&middot; Requirements rarely lie on the surface. They're buried deep beneath layers of assumptions, misconceptions, and politics.

How to recognize a true requirement ? A requirement is a statement of something that needs to be accomplished.

There's a simple technique for getting inside your users' requirements that isn't used often enough: become a user.

Tip 52 - **Work with a User to Think Like a User** <br>
&middot; It's the best way to gain insight into how the system will really be used.

[Alistair Cockburn's basic use case template](./alistair_cockburn_use_case_template.txt)

The Y2K problem came about two main causes: a failure to see beyond current business practice, and a violation of the DRY principle.

#### Maintain a glossary

Create and maintain a *project glossary* -- one place that defines all the specific terms and vocabulary used in a project. All participants in the project, from end users to support staff, should use the glossary to ensure consistency.

- Challenges
 - Can you use the software you are writing ? Is it possible to have a good feel for requirements *without* being able to use the software yourself ?
 - Pick a non-computer-related problem you currently need to solve. Generate requirements for a non-computer solution.

#### Solving Impossible Puzzles

When faced with an intractable problem, enumerate *all* the possible avenues you have before you. Don't dismiss anything, no matter how unusable or stupid it sounds. Now go through the list and explain why a certain path cannot be taken. Are you sure? Can you *prove* it?

Tip 59 - **Expensive Tools Do Not Produce Better Designs** <br>
&middot; Beware of vendor hype, industry dogma, and the aura of the price tag. Judge tools on their merits.

Formal methods certainly have their place in development. However, if you come across a project where the philosophy is "the class diagram *is* the application, the rest is mechanical coding," you know you're looking at a waterlogged project team and a long paddle home.


#### Pragmatic Teams

Teams as a whole should not tolerate broken windows -- those small imperfections that no one fixes. The team *must* take responsibility for the quality of the product.

Great project teams have a distinct personality. People look forward to meetings with them, because they know that they'll see a well-prepared performance that makes everyone feel good. The documentation they produce is crisp, accurate, and consistent. The team speaks with one voice. They may even have a sense of humor.

It is a mistake to think that the activities of a project -- analysis, design, coding, and testing -- can happen in isolation. They can't.

Tip 60 - **Organize Teams Around Functionality** <br>
&middot; Don't separate designers from coders, testers from data modelers. Build teams the way you build code.

The project needs at least two "heads" -- one technical, the other administrative. The technical head sets the development philosophy and style, assigns responsibilities to teams, and arbitrates the inevitable "discussions" between people. The technical head also looks constantly at the big picture, trying to find any unnecessary commonality between teams that could reduce the orthogonality of the overall effort. The administrative head, or project manager, schedules the resources that the teams need, monitors and reports on progress, and helps decide priorities in terms of business needs. The administrative head might also act as the team's ambassador when communicating with the outside world.

#### Ubiquitous Automation

> Civilization advances by extending the number of important operations we can perform without thinking. - Alfred North Whitehead

Tip 61 - **Don't Use Manual Procedures** <br>
&middot; A shell script or batch file will execute the same instructions, in the same order, time after time.

#### Ruthless Testing

Tip 62 - **Test Early. Test Often. Test Automatically** <br>
&middot; Tests that run with every build are much more effective than test plans that sit on a shelf.

What to Test ?

- Unit testing

A *unit test* is code that exercises a module.

If the modules don't work by themselves, they probably won't work well together. All of the modules you are using must pass their own unit tests before you can proceed.

- Integration testing

*Integration testing* shows that the major subsystems that make up the project work and play well with each other.

- Validation and verification

Does it meet the functional requirements of the system ? This, too, needs to be tested.

- Resource exhaustion, errors, and recovery

In the real world, your programs don't have limitless resources; they run out of things. A few limits your code may encounter include : memory - disk space - network speed - screen resolution

When the system does fail, will it fail gracefully? Will it try, as best it can, to save its state and prevent loss of work?

- Performance testing

Ask yourself if the software meets the performance requirements under real-world conditions -- with the expected number of users, or connections, or transactions per second. Is it scalable ?

- Usability testing

Usability testing is performed with real users, under real environmental conditions. Look at usability in terms of human factors. Were there any misunderstandings ?

- Regression testing

A regression test compares the output of the current test with previous (or known) values. We can ensure that bugs we fixed today didn't break things that were working yesterday.

After you have written a test to detect a particular bug, *cause* the bug deliberately and make sure the test complains.

Your design should be decoupled enough so that you can test the application logic *without* having a GUI present.

Tip 65 - **Test State Coverage, Not Code Coverage** <br>
&middot; Identify and test significant program states. Just testing lines of code isn't enough.
As soon as any production code exists, it needs to be tested.

If a bug slips through the net of existing tests, you need to add a new test to trap it next time. Once a human tester finds a bug, it should be the *last* time a human tester finds that bug. The automated tests should be modified to check for that particular bug from the on, every time, with no exceptions, no matter how trivial, and no matter how much the developer complains and says "Oh, that will never happen again".

#### It's All Writing

> The palest ink is better than the best memory. - Chinese Proverb

Tip 67 - **English is Just a Programming Language** <br>
&middot; Write documents as you would write code: honor the DRY principle, use metadata, MVC, automatic generation, and so on.

In general, comments should discuss *why* something is done, its purpose and its goal. The code already shows *how* it is done, so commenting on this is redundant -- and is a violation of the DRY principle.

Commenting source code gives you the perfect opportunity to document those elusive bits of a project that can't be documented anywhere else: engineering trade-offs, why decisions were made, what other alternatives were discarded, and so on.

One of the most important pieces of information that *should* appear in the source file is the author's name.

- example :

Suppose we have a specification that lists the columns in a database table. We'll then have a separate set of SQL commands to create the actual table in the database, and probably some kind of programming language record structure to hold the contents of a row in the table. The same information is repeated three times. Change any one of the three sources and the other two are immediately out of date. This is a clear violation of the DRY principle.

To correct this problem, we need to choose the authoritative source of information. This may be the specification, it may be a database schema tool, or it may be some third source altogether. Let's choose the specification document as the source. It's now out *model* for this process. We then need to find a way to export the information it contains as different *views* -- a database schema and a high-level language record, for example.

- challenges
    - Did you write an explanatory comment for the source code you just wrote ? Why not ? Pressed for time ? Not sure if the code will really work -- are you just trying out an idea as a prototype ? You'll throw the code away afterwards, right ? It won't make it into the project uncommented and experimental, will it ?

#### Great Expectations

Tip 69 - **Gently Exceed Your Users' Expectations** <br>
&middot; Come to understand your users' expectations, then deliver just that little bit more.

Some things you can add relatively easily that look good to the average user include :

- keyboard shortcuts
- log file analyzers
- a splash screen customized for their organization

As your understanding of their needs develops, you'll find area where their expectations cannot be met, or where their expectations are perhaps too conservative. Part of your role is to communicate this. WOrk with your users so that their understanding of what you'll be delivering is accurate.

## Quick Reference Guide

### Tips

1. **Care About Your Craft** <br>
&middot; Why spend your life developing software unless you care about doing it well?

2. **Think! About Your Work** <br>
&middot; Turn off the autopilot and take control. Constantly critique and appraise your work.

3. **Provide Options, Don't Make Lame Excuses** <br>
&middot; Instead of excuses, provide options. Don't say it can't be done; explain what can be done.

4. **Don't Live with Broken Windows** <br>
&middot; Fix bad designs, wrong decisions, and poor code when you see them.

5. **Be a Catalyst for Change** <br>
&middot; You can't force change on people. Instead, show them how the future might be and help them participate in creating it.

6. **Remember the Big Picture** <br>
&middot; Don't get so engrossed in the details that you forget to check what's happening around you.

7. **Make Quality a Requirements Issue** <br>
&middot; Involve your users in determining the project's real quality requirements.

8. **Invest Regularly in Your Knowledge Portfolio** <br>
&middot; Make learning a habit.

9. **Critically Analyze What You Read and Hear** <br>
&middot; Don't be swayed by vendors, media hype, or dogma. Analyze information in terms of you and your project.

10. **It's Both What You Say and the Way You Say It** <br>
&middot; There's no point in having great ideas if you don't communicate them effectively.

11. **DRY–Don't Repeat Yourself** <br>
&middot; Every piece of knowledge must have a single, unambiguous, authoritative representation within a system.

12. **Make It Easy to Reuse** <br>
&middot; If it's easy to reuse, people will. Create an environment that supports reuse.

13. **Eliminate Effects Between Unrelated Things** <br>
&middot; Design components that are self-contained. independent, and have a single, well-defined purpose.

14. **There Are No Final Decisions** <br>
&middot; No decision is cast in stone. Instead, consider each as being written in the sand at the beach, and plan for change.

15. **Use Tracer Bullets to Find the Target** <br>
&middot; Tracer bullets let you home in on your target by trying things and seeing how close they land.

16. **Prototype to Learn** <br>
&middot; Prototyping is a learning experience. Its value lies not in the code you produce, but in the lessons you learn.

17. **Program Close to the Problem Domain** <br>
&middot; Design and code in your user's language.

18. **Estimate to Avoid Surprises** <br>
&middot; Estimate before you start. You'll spot potential problems up front.

19. **Iterate the Schedule with the Code** <br>
&middot; Use experience you gain as you implement to refine the project time scales.

20. **Keep Knowledge in Plain Text** <br>
&middot; Plain text won't become obsolete. It helps leverage your work and simplifies debugging and testing.

21. **Use the Power of Command Shells** <br>
&middot; Use the shell when graphical user interfaces don't cut it.

22. **Use a Single Editor Well** <br>
&middot; The editor should be an extension of your hand; make sure your editor is configurable, extensible, and programmable.

23. **Always Use Source Code Control** <br>
&middot; Source code control is a time machine for your work—you can go back.

24. **Fix the Problem, Not the Blame** <br>
&middot; It doesn't really matter whether the bug is your fault or someone else's—it is still your problem, and it still needs to be fixed.

25. **Don't Panic When Debugging** <br>
&middot; Take a deep breath and THINK! about what could be causing the bug.

26. **"select" Isn't Broken.** <br>
&middot; It is rare to find a bug in the OS or the compiler, or even a third-party product or library. The bug is most likely in the application.

27. **Don't Assume It—Prove It** <br>
&middot; Prove your assumptions in the actual environment-- with real data and boundary conditions.

28. **Learn a Text Manipulation Language.** <br>
&middot; You spend a large part of each day working with text. Why not have the computer do some of it for you?

29. **Write Code That Writes Code** <br>
&middot; Code generators increase your productivity and help avoid duplication.

30. **You Can't Write Perfect Software** <br>
&middot; Software can't be perfect. Protect your code and users from the inevitable errors.

31. **Design with Contracts** <br>
&middot; Use contracts to document and verify that code does no more and no less than it claims to do.

32. **Crash Early** <br>
&middot; A dead program normally does a lot less damage than a crippled one.

33. **Use Assertions to Prevent the Impossible** <br>
&middot; Assertions validate your assumptions. Use them to protect your code from an uncertain world.

34. **Use Exceptions for Exceptional Problems** <br>
&middot; Exceptions can suffer from all the readability and maintainability problems of
classic spaghetti code. Reserve exceptions for exceptional things.

35. **Finish What You Start** <br>
&middot; Where possible, the routine or object that allocates a resource should be responsible for deallocating it.

36. **Minimize Coupling Between Modules** <br>
&middot; Avoid coupling by writing "shy" code and applying the Law of Demeter.

37. **Configure, Don't Integrate** <br>
&middot; Implement technology choices for an application as configuration options, not through integration or engineering.

38. **Put Abstractions in Code, Details in Metadata** <br>
&middot; Program for the general case, and put the specifics outside the compiled code base.

39. **Analyze Workflow to Improve Concurrency** <br>
&middot; Exploit concurrency in your user's workflow.

40. **Design Using Services** <br>
&middot; Design in terms of services—independent, concurrent objects behind well-defined, consistent interfaces.

41. **Always Design for Concurrency** <br>
&middot; Allow for concurrency, and you'll design cleaner interfaces with fewer assumptions.

42. **Separate Views from Models** <br>
&middot; Gain flexibility at low cost by designing your application in terms of models and views.

43. **Use Blackboards to Coordinate Workflow** <br>
&middot; Use blackboards to coordinate disparate facts and agents, while maintaining independence and isolation among participants.

44. **Don't Program by Coincidence** <br>
&middot; Rely only on reliable things. Beware of accidental complexity, and don't confuse a happy coincidence with a purposeful plan.

45. **Estimate the Order of Your Algorithms** <br>
&middot; Get a feel for how long things are likely to take before you write code.

46. **Test Your Estimates** <br>
&middot; Mathematical analysis of algorithms doesn't tell you everything. Try timing your code in its target environment.

47. **Refactor Early, Refactor Often** <br>
&middot; Just as you might weed and rearrange a garden, rewrite, rework, and re-architect code
when it needs it. Fix the root of the problem.

48. **Design to Test** <br>
&middot; Start thinking about testing before you write a line of code.

49. **Test Your Software, or Your Users Will** <br>
&middot; Test ruthlessly. Don't make your users find bugs for you.

50. **Don't Use Wizard Code You Don't Understand** <br>
&middot; Wizards can generate reams of code. Make sure you understand all of it before you incorporate it into your project.

51. **Don't Gather Requirements–Dig for Them** <br>
&middot; Requirements rarely lie on the surface. They're buried deep beneath layers of assumptions, misconceptions, and politics.

52. **Work with a User to Think Like a User** <br>
&middot; It's the best way to gain insight into how the system will really be used.

53. **Abstractions Live Longer than Details** <br>Invest in the
&middot; abstraction, not the implementation. Abstractions can survive the barrage of changes from different implementations and new technologies.

54. **Use a Project Glossary** <br>
&middot; Create and maintain a single source of all the specific terms and vocabulary for a project.

55. **Don't Think Outside the Box–Find the Box** <br>
&middot; When faced with an impossible problem, identify the real constraints. Ask yourself: "Does it have to
be done this way? Does it have to be done at all?"

56. **Start When You're Ready.** <br>
&middot; You've been building experience all your life. Don't ignore niggling doubts.

57. **Some Things Are Better Done than Described** <br>
&middot; Don't fall into the specification spiral—at some point you need to start coding.

58. **Don't Be a Slave to Formal Methods.** <br>
&middot; Don't blindly adopt any technique without putting it into the context of your development practices and capabilities.

59. **Expensive Tools Do Not Produce Better Designs** <br>
&middot; Beware of vendor hype, industry dogma, and the aura of the price tag. Judge tools on their merits.

60. **Organize Teams Around Functionality** <br>
&middot; Don't separate designers from coders, testers from data modelers. Build teams the way you build code.

61. **Don't Use Manual Procedures** <br>
&middot; A shell script or batch file will execute the same instructions, in the same order, time after time.

62. **Test Early. Test Often. Test Automatically** <br>
&middot; Tests that run with every build are much more effective than test plans that sit on a shelf.

63. **Coding Ain't Done Until All the Tests Run** <br>
&middot; 'Nuff said.

64. **Use Saboteurs to Test Your Testing** <br>
&middot; Introduce bugs on purpose in a separate copy of the source to verify that testing will catch them.

65. **Test State Coverage, Not Code Coverage** <br>
&middot; Identify and test significant program states. Just testing lines of code isn't enough.

66. **Find Bugs Once** <br>Once a human tester finds a bug, it
&middot; should be the last time a human tester finds that bug. Automatic tests
should check for it from then on.

67. **English is Just a Programming Language** <br>
&middot; Write documents as you would write code: honor the DRY principle, use metadata, MVC, automatic generation, and so on.

68. **Build Documentation In, Don't Bolt It On** <br>
&middot; Documentation created separately from code is less likely to be correct and up to date.

69. **Gently Exceed Your Users' Expectations** <br>
&middot; Come to understand your users' expectations, then deliver just that little bit more.

70. **Sign Your Work** <br>
&middot; Craftsmen of an earlier age were proud to sign their work. You should be, too.

## Checklists

**The WISDOM Acrostic - understanding an audience**

- **W**hat do you want them to learn?
- What is their **i**nterest in what you've got to say?
- How **s**ophisticated are they?
- How much **d**etail do they want?
- Whom do you want to **o**wn the information?
- How can you **m**otivate them to listen to you?

**Architectural Questions**

- Are responsibilities well defined?
- Are the collaborations well defined?
- Is coupling minimized?
- Can you identify potential duplication?
- Are interface definitions and constraints acceptable?
- Can modules access needed data—when needed?

**Debugging Checklist**

- Is the problem being reported a direct result of the underlying bug, or merely a symptom?
- Is the bug really in the compiler? Is it in the OS? Or is it in your code?
- If you explained this problem in detail to a coworker, what would you say?
- If the suspect code passes its unit tests, are the tests complete enough? What happens if you runthe unit test with this data?
- Do the conditions that caused this bug exist anywhere else in the system?

**Law of Demeter for Functions** <br>
An object's method should call only methods belonging to:

- Itself
- Any parameters passed in
- Objects it creates
- Component objects

**How to Program Deliberately**

- Stay aware of what you're doing.
- Don't code blindfolded.
- Proceed from a plan.
- Rely only on reliable things.
- Document your assumptions.
- Test assumptions as well as code.
- Prioritize your effort.
- Don't be a slave to history.

**When to Refactor**

- You discover a violation of the DRY principle.
- You find things that could be more orthogonal.
- Your knowledge improves.
- The requirements evolve.
- You need to improve performance.

**Cutting the Gordian Knot** <br>
When solving impossible problems, ask yourself:

- Is there an easier way?
- Am I solving the right problem?
- Why is this a problem?
- What makes it hard?
- Do I have to do it this way?
- Does it have to be done at all?

**Aspects of Testing**

- Unit testing
- Integration testing
- Validation and verification
- Resource exhaustion, errors, and recovery
- Performance testing
- Usability testing
- Testing the tests themselves
