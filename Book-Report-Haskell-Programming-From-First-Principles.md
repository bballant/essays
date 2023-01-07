# Book Report: _Haskell Programming From First Principles_

[_Haskell Programming From First Principles_](https://haskellbook.com/) was written by Christopher Allen and
Julie Moronuki. 

I read/worked-through/abandoned/referenced/dreamt-about/lost-sleep-over/came-back-to/etc
this book starting roughly four years ago when I joined my current company. I was a clojure
refugee, a lower-case "fp" functional programmer playing fast and loose with the REPL.
Haskell felt next-level and this book really rises up to meet the challenge of
teaching such a complex and _different_ programming language.

The book is a monster at nearly 2000 pages and it is exercise-driven. Going through most of the
exercises is, in fact, imperative if you hope to get much from the book.

The authors do an excellent job of presenting and teaching Haskell. But this book
takes time--lots and lots of time. They start with the roots of FP, lamda calculus,
but soon introduce you to Haskell type declarations in an effort, I think, to get
you _Thinking With Types_ (The title of a popular advanced Haskell
[book](https://thinkingwithtypes.com/)) early on.

Haskell's type system is incredibly expressive. In many ways it is a second,
compile-time, language. Because Haskell is purely functional, the type signature
for a function tells you if there are side-effects. Haskell is also always lazily evaluated
unless you are explict about being "strict". This all means that the type signatures
tell you most of what you need to know about a function. There's even
a handy on-line tool, [Hoogle](http://hoogle.haskell.org), where you can plug
in the type signature you want, and get a list of functions across a myriad of
libraries that will do that thing. Usually the first result is exactly what you
were looking for.

Because I had never encountered anything as expressive at the type level as
Haskell, I found it difficult to map Haskell types to something
I knew. I think this is why the "first principles" approach taken by the authors
of this book is so... necessary. You need to build up the models in your
head from scratch to be able to understand them fully. This takes time. I made
the mistake of rushing through early parts of the book only having to double-back
and work though things again when I got inevitably lost later.

The authors say learning Haskell is easy. I disagree. But I also disagree with the
insinuation that hard is bad. For me it was difficult but fun and only frustrating
when I tried to move fast or pretend it was easy.

The authors also say that you can basically do anything you need in Haskell
without touching that mythical Monad. This may be technically correct, in the
sense that simple Haskell is likely Turing-complete, but practically this is
nonsense. In my PDF copy, which I bought soon after it came out (it may have even
been a pre-release version), the
chapter on Monads starts on page 1140 and ends on page 1211. So, if we're being
straight with each other, you really need to _go through_ (not just read) around
1200 pages of this Haskell book to be able to do anything acutally useful in the
language.

All that said, what can you do? The book is great and this is what it takes to learn the language. The
build up to Monads from Monoids through Applicative is the best part of the book.
For me it was when the dots finally started to connect. I finally knew, 100%, what
a Functor was! And I could see how Haskell allows a programmer to build commonality
around seemingly unrelated things, based on common behaviors or structures, in a
way that I had not seen before, after reading those chapters.

I did not engage with another Haskell book or learning resource in nearly as much depth
as I did with this one, but in my Haskell studies, no resource or tutorial came close to this
book. The authors do a wonderful job of building up understanding of complex concepts
from their foundations. It's up to the reader to take their time to get the most out of
and enjoy the challenging journey. Good luck!
