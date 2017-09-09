**Doing serious business and got no time to contribute? Please [support us on Patreon](https://www.patreon.com/codenamemetasys), every bit helps.**

# Intro

Ever got impressed by the most mind-blowing ideas of theoretical physics?

The time of lab experiments in physics is rather gone, because nowadays our fantasy about how the universe works in micro and macro scales goes beyond our practical ability to test and verify stuff. How do researchers know they are right about their ideas? It's all about logic.

What we are doing in science is trying to *reconstruct* the laws of the universe (the system) in our heads using Boolean algebra. We are trying to put rules on top of each other and try to verify whether they are `true` or `false`. What an analogy to software development?

With growing set of rules our *reconstruction* of the universe (the system) gets bigger and our heads are not big enough to compare all established `true` rules with new ideas. And so happens that we have 2 different theories largely backed by many `true` rules, but they don't make sense with each other together in certain parts, like the quantum physics and the theory of relativity.

Fortunately, we have these wonderful things called computers that can do stuff for us. We can build a massive database of rules and have a machine comparing all established `true` rules with rules coming from new ideas and verify them this way. I am confident about building an experiment system for verifying massively complex theoretical sciences like physics. Imagine it like **unit testing of science**.

Once such a system is built, which can store *rules of theories* in both human and machine readable way, it can not only serve the mankind in verifying new and existing theories, it may also... try to generate new theories automatically.

I know I can't do this on my own. I would like to invite you to think with me about such an experiment practically and attempt to create a real project.

Let's start by thinking [what could the data structure look like](https://github.com/Codename-METASYS/theory/issues/1).

We can also chat on [Gitter](https://gitter.im/Codename-METASYS/Lobby)!

![Preview](subjectpage.png)

# Q/A

### What features should the platform include?

- Structured information about *subjects* and *rules* between them.
- The ability to change the existing of information by the community/users (proposals).
- Automatic verification of proposals with established rules.
- The ability to add, delete or change information sources for each subject.
- The ability to check whether the user acknowledged selected subject (learned it).
- The ability to discuss new ideas or topics and ask questions (maybe integration with StackExchange?).
- Notification of changes about a given subject if the user opts in.
- Goals of science (maybe?).

### What will this project help with?

- Organisation of knowledge.
- Verification of existing theories.
- Learning, with related subjects you won't miss anything as well as with many community-verified information sources you won't have to search the internet by trial and error.
- Staying up to date with theories you are interested about.
- Having a place where to seriously discuss scientific questions and ideas with the widest community.
- Access to the latest scientific information and research results for everyone with internet connection (not just for university students).
- Automatic generating of new theories (?).

### How will this be different from Wikipedia or similar websites?

Wikipedia and other encyclopedias are meant to store information. This project is supposed to organize and verify information and identify valid information sources.

Besides that, Wikipedia does not:
- programatically verify theories,
- allow you to mark learned subjects,
- offer discussions / forums dedicated to subjects.

This platform is not supposed to be a source of information, instead it will be a *sign post* to existing information sources. No articles here.

### What fields of knowledge should the platform cover?

Perhaps natural sciences. Should we start with just theoretical physics and see?

### How will this project be secured to work for years to come?

Although alternative (commercial) plans for funding exist as an emergency solution, this project would the best go off donations.

### Will *Codename METASYS* be the actual name of the platform?

This name is just a working name. There has been several suggestions for the actual name of the platform, yet none has been chosen yet.

### Why is there *ScienceLog* on the preview image?

Original idea for a name of the platform from when the preview UI was built back in 2014.

# The Theory

What is a system (in general)?

The boring definitions:

- **Wikipedia (from Merriam-Webster dictionary):** *A system is a regularly interacting or interdependent group of items forming a unified whole.* [1](https://en.wikipedia.org/wiki/System), [2](https://www.merriam-webster.com/dictionary/system)
- **businessdictionary.com:** *An organized, purposeful structure that consists of interrelated and interdependent elements (components, entities, factors, members, parts etc.). These elements continually influence one another (directly or indirectly) to maintain their activity and the existence of the system, in order to achieve the goal of the system.* [3](http://www.businessdictionary.com/definition/system.html)
- **Oxford Dictionaries:** *A set of things working together as parts of a mechanism or an interconnecting network; a complex whole.* [4](https://en.oxforddictionaries.com/definition/system)
- **Dictionary.com:** *An assemblage or combination of things or parts forming a complex or unitary whole.* [5](http://www.dictionary.com/browse/system)
- ...

The nice and actually useful definition:

> **System is a set of (logical) rules.**

*Tadaa!* A bit different point view - of a computer engineer. The difference between this and the other definitions of system is the fact that we can use it with the tools that are probably the most common to us in this age: digital devices. What's digital works with logical rules and we can use such devices to help us with discovering the rules of a system.

### *A system* or *The system*?

Computer engineers often create rules their applications work under. An application (computer program) is a system - a set of rules saying what should happen under certain conditions. Development of an application is a fair example of system evolution - from a few primitive rules (a few of `if`s) an application usually grows to hundreds of thousands of rules. Obviously, rules can be extended. Let's have a look at an example.

A very basic rule in an application may be:
```
if (userRole == 'registered') // basic rule
{
    // allow viewing
}
```

This rule may be extended with another one:
```
if (userRole == 'registered') // basic rule
{
    // allow viewing

    if (userRole == 'admin') // extending rule
    {
        // allow editing
    }
}
```

Having these two rules in an application, we could say that we have created *a system*. If we think about it further, we realize that behind the scenes, our example *basic rule* is actually already an extending rule, which extends rules that are given by the interpreter of our script. The interpreter of our script further extends the rules of the operating system we run the application under, which further extends the rules given by the physical machine.

It's basically just the rules of `1`s and `0`s we are extending in computers, every operating system or application running on a computer seem to be just "extensions" of these very basic two rules of *existing electric current* (`1`) or *non-existen electric current* (`0`). All these systems like applications, plugins, script interpreters, drivers, operating systems or even hardware like graphics cards, memory modules and so on, would it be better to rather call them **subsystems**?

Of course those `1`s and `0`s are just an extension too, computer systems are just a subsystem of a system we call *the laws of physics*.

![We need to go deeper](http://i0.kym-cdn.com/entries/icons/original/000/012/886/wntgd.jpg)

This being said, it appears that the Universe is *the ultimate system* and everything we call *a system* is in fact *a subsystem*. For convetional use, let's keep calling these *subsystems* (specific sets of rules) simply *systems*. By saying *a system*, let's understand *a subsystem* of the Universe, yet for our definition of *system*, should we not use either *the* or *a*?

### The Holy Grail of science

If everything is a subsystem, does the Universe extend only a few fundamental rules just like our computer programs only extend `1`s and `0`s? How many are they?

Knowing what are the very basic rules / laws of the Universe would probably help us with accurately verifying the rules that we already think we know. The trouble is that we don't know where is this *root of extensions*. At this point the mankind is able to observe only a certain portion of the whole rule set of *the system*, and we are trying to figure out what rule / law is based on another one.

We are trying to reconstruct (or reverse-engineer in other words) the rules of the Universe, and we've been already coming up with as many ideas for rules that could apply as we are not able to verify them against already *established rules*. That's why the mankind needs a project like this one.

An *established rule* is a rule that *makes sense* with other rules (is logically verified). The more established rules make sense with a new rule, the more likely is the new rule to be true. On the other hand, the history has proven that even well established rules may turn out to be not true with alternative theories (alternative rule set ideas) coming up. A good example would be [aether](https://en.wikipedia.org/wiki/Aether_(classical_element)) versus [gravity](https://en.wikipedia.org/wiki/Gravity).

It is common for one theory (understand rule set) to take over another. The fun comes when two large rule sets develop and get relatively established, but don't make sense with each other in certain parts, like the [theory of relativity](https://en.wikipedia.org/wiki/Theory_of_relativity) and [quantum physics](https://en.wikipedia.org/wiki/Quantum_mechanics). How can it happen? Pure logic tells us that something is either *true* or *false*, there's nothing like partially true or something between. The cause to such an existing issue is the fact that humans are not accurate enough. No single scientist has got all the rules of the Universe we think we know packed in their head to be able to verify them with each other. A machine may do it. Even if a machine may not be able to hold all rules of the Universe (because it may be and incredible amount of data), it will most certainly be able to hold and verify more rules than all scientists together.

Do we already know one of more of the Universe's fundamental rules? What do you think? [Fork this repository](https://github.com/Codename-METASYS/theory/edit/master/README.md) and create a pull request to add your thoughts. Let's shape this theory together.

### Hacking beyond the box

Numerous writers and philosopers have came up with the idea that we may live in a (computer-like) simulation or that the Universe we know is just one of many dimensions. Although none of these theories (rule sets) were explicitly proven (established) yet, it may be possible that the Universe is not *the system*, but just a *subsystem* of something much bigger.

Imagine you lived in a computer game. Would you be able to recognize if the fact that your world is a computer simulation is true? If you saw an object going through a wall (which still often happens in games), you would probably think that "this is not real". You would think that because you know how the "real world" works (the system/subsystem you actually live in) and that it is not possible for an object to just go through wall easily. But imagine you never saw the thing we call the "real world" and you always only lived inside the game, where objects often go through walls and nothing happens - you would think that it is pretty normal.

What seems to be normal for us in this world may be abnormal in another, if another world exists. Is it possible to logically recognize whether we are living in a subsystem of multiverse or something else in general? What do you think?
