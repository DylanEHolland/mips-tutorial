#INTRODUCTION

MIPS is a CPU architecture that has been used in various embedded systems
including a few things like the Game Boy Advance. It is a simple enough 
architecture learn and is a good stepping stone if one wants to learn assembly
for other CPU architectures, such as those found in personal computers.

This is a tutorial that aims to give a thorough walkthrough of usage.

##Why learn assembly?

Learning assembly is a must if one hopes to get a solid understanding of how
higher-level programming languages like C, or even Java or Python eventually
translate (*compile*) to actual instructions. In many ways however, knowing
this will help you better implement algorithms as you get used to thinking at
a more basic level.

Also, if you ever intend to use debugging software like gdb, or want to
reverse-engineer software, with things like Cheat Engine to hack videogames
(Just do it in single-player please ;) ) assembly is a must-know. Of course,
don't take me too literally here, as with things like Cheat Engine or gdb,
you'll be using a different architecture that will be a bit more complicated
than MIPS, but not too much. This is a good starting ground.

If you also wanna write a compiler, or otherwise wanna work
low-level for other reasons, MIPS is a good place to get your feet wet. But,
if this applies to you, I doubt you needed an explanation.

##Is it difficult?

In a fundamental sense, one can learn *"theoretically"* learn assembly easier
than other programming languages, such as Python or C++. This is because it
is the most basic level of direction. But, here in the real world, assembly is
actually much more difficult to write software in, even trivial applications
can easily become a headache in assembly to the inexperienced and experienced
alike.

There's no OOP to learn, inheritance, lambdas, or anything like that. There is
a simplicity you may learn to appreciate. Of course, you'll also gain an
appreciation of many higher-level language features ;) I promise it's fun,
though.

##Why MIPS Assembly and not another architecture?

* MIPS is a *RISC* architecture (Reduced Instruction Set), so learning the
basics is much simpler, and can focus on the actual programming. It is simpler
to learn than the arch used in standard personal computers: x86-64.

* Implementations of MIPS simulators (In particular, MARS) I've found to be
much simpler and easier to use than those for LLVM or LC3 or ARM. (Don't read
this as negativity about LLVM and LC3, those are very good projects with a lot
of smart people.)

* Actually runs on native hardware. Unlike things like LC3.

##What do I need to already know?

If you know any basic programming, you should be fine, if you know C or C++
you're golden. 

##A few notes before you start 

You will hear both *registers* and *memory* talked about. A register is a
memory unit that is directly "on" the CPU as opposed to RAM that we can perform
actions directly with. For your memory that isn't in one of your few registers,
you must load it from memory before you can do things like math, I/O, etc. If
this doesn't quite make sense, it should make sense as you go through this
tutorial and have a bit more context.

##Set-up and usage

I highly recommend the MARS simulator 
([available here](http://courses.missouristate.edu/KenVollmar/mars/download.htm))
for running these MIPS code samples. It runs on Windows, Mac, Linux, and since
it's a Java .jar, likely also will run on *BSD too, but I can't attest to that.
Running a program involves a two step process:

* Assemble (F3)

This will translate what you wrote to the actual machine language, and prepare
for actually running your code.

* Run (F5)

This will run your assembled code, note you *must* assemble it first.

##Resources

This tutorial is not meant to supersede/replace some of the already great
resources out there, but to instead complement what already exists. For this
reason, I opted to not include copies of the instruction sets or the definitive
``syscall`` list, look to some of these resources for information.

* [The instruction set (James F. Frenzel @ University of Idaho)](http://www.mrc.uidaho.edu/mrc/people/jff/digital/MIPSir.html)

This is a very good general reference. MIPS is a simple enough architecture
to read all of. Useful to lookup the different branching
instructions available, math, etc.

* [syscall list (Ken Vollmar @ Missouri State)](http://courses.missouristate.edu/KenVollmar/mars/Help/SyscallHelp.html)

There are many different system services, MARS supports most, if not all of
these. 

* [MARS Download (Ken Vollmar @ Missouri State)](http://courses.missouristate.edu/KenVollmar/mars/download.htm)

This is the same link in the previous section, but placed here also for
consistency.
