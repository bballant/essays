# Book Report: _Effective C_

I recently read [_Effective C_](https://nostarch.com/Effective_C) by Robert C.
Seacord. This is a relatively short tour of the C language with a strong lean
toward practical software development and secure programming in C. It is subtitled,
"An Introduction to Professional C Programming" which, of course, is exactly what it is!

Many programing books are very hands-on in the sense they take you through
building something, or through a complex, multi-chapter example, or require
the reader to spend time at the computer typing out examples. But, happily,
_Effective C_ is not that type of book. Instead, it's something you can just
read! It's not necessarily _readable_ because of the subject matter, but I was very
interested in re-learning some C quickly while I was going through other excercise-
oriented books on microcontroller development ([Begining STM32](https://www.apress.com/9781484236239)).

_Effective C_'s straighforward approach 
made the book easy to pick up. It is organized as you might expect, taking
you through some practicals on editors and compilers, then through types,
expressions, control flow, memory, strings, I/O, preprocessor/macros, program
structure, and debugging.

The book provides information and examples for gcc, clang, and Visual C++. I am
not really interested in Windows programming, but I still enjoyed reading about
the different approaches. For times when I did try out the example code, I used gcc.
In some places, like in the discussion of debugging, one or another of the
platforms was used to illustrate the point. Therefore, to my surprise, GDB wasn't
 even mentioned in the debug section.

The fast pace threw me off a couple of times. For example, `errno` is mentioned
in chapter 8 in a way that had me flipping back to find where the author had
explained it earlier--he hadn't.

My experience with C is spotty. It was the main language I used in college, but
professionally I can't remember using it. I've used some notable C successors,
like C++ and C# professionally, but not the OG. I am,
however, a Linux freak so I've downloaded, compiled, and used many many C applications
without touching the code. Recently I've been messing around with microcontrollers,
and C is the main language in the embedded world.

When I first started playing with microcontrollers, it was clear early on that
they are just big, complex, state machines. Most microcontroller code (at least
at the hobbiest/beginner level) is just managing that state. Push some bits into
a register and let the clock tick.

As I started digging into C for itself, on my laptop, I started to feel like
my computer is just one big state machine. For a kool-aide's-been-drunk functional
programmer like myself, this was a little hard to take at first. My computer
was starting to feel like a house of cards.

It's clear parts of C are a mess. The chapter on strings is almost explicit about
this fact. Here's a dumb thing that probably smells like air to the daily C
programmer: The C standard function `getchar()` returns an `int` because one value,
`EOF`, is an int. Most of the time, you can safely cast this into a char, but not
if the value is `EOF`. Many functions are unsafe in the C standard library and
overflow errors seem easy to make happen. It's no wonder that there are so many
zero-day exploits of C programs and that someone invented Rust.

Seacord's book made me feel a little better about all that. He showed POSIX or
Windows alternatives to unsafe standard functions and showed how to prevent overflow
in your own code. After reading _Effective C_ I feel like I could build something
complex, safe, and "professional" in the C programming language. C now feels to
me like a simple (and fun but I usually find programming fun), albeit dangerous,
tool for manipulating that big state machine in my laptop.

