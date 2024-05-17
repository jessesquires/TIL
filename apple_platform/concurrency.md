# Concurrency

## WWDC 🎥

- [WWDC21: Explore structured concurrency in Swift](https://developer.apple.com/videos/play/wwdc2021/10134/)
    - `async let`, task tree, (cooperative) cancellation, group tasks (`withThrowTaskGroup()`), `for await`, unstructured tasks, detached tasks
- [WWDC21: Swift concurrency: Behind the scenes](https://developer.apple.com/wwdc21/10254)
    - advanced discussion on thread pool. comparisons to GCD, locks, etc.

## Swift Concurrency (`Task`, `async`, `await`, etc.)

#### [Concurrency Recipes](https://github.com/mattmassicotte/ConcurrencyRecipes), Matt Massicotte

> Practical solutions to problems with Swift Concurrency.

#### [What is structured concurrency?](https://oleb.net/2021/structured-concurrency/)

> Structured concurrency is a new term for most Swift developers. This is an attempt to decipher its meaning.

#### [The difference between `Thread.sleep()` and `Task.sleep()`](https://trycombine.com/posts/thread-task-sleep/)

> So here’s a quick and simple example that showcases some of the nice features of the new concurrency model without going into much detail.

#### [Swift Concurrency – Things They Don’t Tell You](https://wojciechkulik.pl/ios/swift-concurrency-things-they-dont-tell-you)

> However, with great power comes great responsibility. If you learn from tutorials or even from the documentation, it’s really hard to find some details on how it works under the hood.

#### [Modern Swift Concurrency Summary, Cheatsheet](https://www.andyibanez.com/posts/modern-swift-concurrency-summary-cheatsheet-thanks/)

> Since WWDC21, we have talked, extensively, about all the new concurrency features introduced in Swift 5.5. We covered a lot of topics, so I decided to finish off this series writing a summary article were we cover the most important topics of each article.

#### [Swift Concurrency Waits for No One](https://saagarjha.com/blog/2023/12/22/swift-concurrency-waits-for-no-one/)

> Swift Concurrency promises to make it possible to write correct, performant code designed for today’s world of asynchronous events and ubiquitous hardware parallelism. And indeed, when wielded appropriately it does exactly that. However–much like an iceberg–the simple APIs it exposes hide a staggering amount of complexity underneath. Unfortunately, concurrency is a challenging topic to reason about when compared to straight-line, synchronous code, and it is difficult for any programming model to paper over all of its subtleties.

## Swift Actors

#### [Actor reentrancy in Swift explained](https://www.donnywals.com/actor-reentrancy-in-swift-explained/)

> When you start learning about actors in Swift, you’ll find that explanations will always contain something along the lines of “Actors protect shared mutable state by making sure the actor only does one thing at a time”. As a single sentence summary of actors, this is great but it misses an important nuance. While it’s true that actors do only one thing at a time, they don’t always execute function calls atomically.

## GCD, libdispatch, threads, queues

#### [libdispatch efficiency tips](https://gist.github.com/tclementdev/6af616354912b0347cdf6db159c37057):

> The libdispatch is one of the most misused API due to the way it was presented to us when it was introduced and for many years after that, and due to the confusing documentation and API. This page is a compilation of important things to know if you're going to use this library. Many references are available at the end of this document pointing to comments from Apple's very own libdispatch maintainer (Pierre Habouzit).

#### [Underused and Overused GCD Patterns](https://mjtsai.com/blog/2021/03/16/underused-and-overused-gcd-patterns/)

> Underused GCD patterns:
>
>  - Making a serial queue that’s less aggressive about creating threads (“non-overcommit”) [...]
>  - Multiplexing work onto a single serial queue efficiently [...]
>
> Probably overused GCD patterns:
>
> - Global queues as anything but targets
> - Almost any use of concurrent queues
> - Queues as locks; os_unfair_lock is more efficient (sadly a little trickier to use in Swift; no ideal solution here yet)
> - Turning async into sync with semaphores

### Quality of Service

Queues with `.background` Quality of Service (QoS) may *never* be executed, e.g. low power mode, so plan accordingly.
- If using `.background`, you probably want `.utility` instead.
- [Tweet](https://twitter.com/gregheo/status/1001501337907970048)
- [Docs](https://developer.apple.com/library/content/documentation/Performance/Conceptual/EnergyGuide-iOS/PrioritizeWorkWithQoS.html)

### Threads != Queues

- [Main Queue vs Main Thread](http://blog.benjamin-encz.de/post/main-queue-vs-main-thread/)
- [Queues are not bound to any specific thread](https://blog.krzyzanowskim.com/2016/06/03/queues-are-not-bound-to-any-specific-thread/)

#### [What went wrong with the libdispatch. A tale of caution for the future of concurrency.](https://tclementdev.com/posts/what_went_wrong_with_the_libdispatch.html)

> Fast-forward to today's 2020 and most consumer machines have about 4 cores and pro machines have about 8 to 12 cores. Something must have gone wrong along the way. Spoiler: multithreading is hard.
>
> [...]
>
> How would serial queues help us with concurrency? Well various program components would have their own private queue which would be used to ensure thread-safety (locks would not even be needed anymore) and those components would be concurrent between themselves. They told us these were "islands of serialization in a sea of concurrency".

#### [Atomic property wrapper in Swift](https://www.onswiftwings.com/posts/atomic-property-wrapper/)

> Let’s take a closer look at this feature and check how can we use it to define atomic properties in Swift.

#### [Russ Bishop: The Law. Atomics Are Hard](http://www.russbishop.net/the-law)

> Swift 5 turns on exclusivity checking by default. This has some interesting interactions with atomics, especially when running under the Thread Sanitizer (TSAN). If you've ever seen a TSAN report on some simple Swift code that looks obviously correct then you're probably running into this issue:

#### [What does “atomic” mean in programming?](https://www.donnywals.com/what-does-atomic-mean-in-programming/)

> Generally, you can summarize atomic as "one at a time".
>
> For example, when accessing or mutating a property is atomic, it means that only one read or write operation can be performed at a time. If you have a program that reads a property atomically, this means that the property cannot change during this read operation.

#### [How NetNewsWire Handles Threading](https://inessential.com/2021/03/20/how_netnewswire_handles_threading)

> NetNewsWire is mostly *not* multi-threaded. Here’s what we do...

#### [Benefits of NetNewsWire’s Threading Model](https://inessential.com/2021/03/21/benefits_of_netnewswires_threading_model)

> In my previous post I describe how NetNewsWire handles threading, and I touch on some of the benefits — but I want to be more explicit about them.
