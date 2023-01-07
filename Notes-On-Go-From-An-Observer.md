# Notes On Go From An Observer

A Go project of growing complexity, and thankfully the talented engineers working on the thing, became part of my team recently. I had noodled around with Go a bit previously, but this was my first engagement with the language and platform in any substantial way.

The Google hegemony is inescapable, especially when your business runs in the Google cloud, but I was weary of Go from the start because of Go's Google roots. I felt like there was a bit of an "Emperor's New Clothes" thing going on causing people to downplay the language's flaws.

Go's contemporaries, like Kotlin and Rust, are modern and evolved where Go seems primitive (Go's concurrency story notwithstanding). Functional programming paradigms, immutability by default, ADTs, and other programing language facilities that I would consider state-of-the-art are missing from Go.

This function from gobyexample.com really turned me off:

```
func addThree(arg int) (int, error) {
  if arg == 42 {
    return -1, errors.New("can't work with 42")
  }
  return arg + 3, nil
}
```

It is idiomatic to ignore the -1 return value on error. The -1 is a convention and it could be anything and there's nothing preventing a hapless programmer giving it meaning or assuming it has one. This seems like _bugs waiting to happen_.

One has to hope the caller knows this idiom (part of the training protocol, I'm sure) and doesn't use the -1. Every time someone uses this function, they have to do a bunch of extra work to make sure all is copacetic. For simple code bases, this is probably fine, but for a big project, the dependency on the programmer to get this right over and over again and, just, all the code required to manage this function call, makes Go seem not so simple after all.

It remains to be seen how Google holds up to our needs as the team takes on this new Go code base. I am mostly just reading Go for now through code reviews and patterns like the above don't seem too bad in practice. But I credit the engineers whose code I'm reading with this more than I do the language.

The biggest positive of Go, and the main reason this Go  project exists in the first place, is that it works nicely with the Google APIs. Compared with any other supported language like Java or Python, it seems simpler and more direct to interface with Google. That said, the throwback nature of the language is a concern. I'm sure Go will evolve but I hope our newish Go project doesn't scale beyond the language's current abilities.
