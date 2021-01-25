# Threads and Queues

#### [libdispatch efficiency tips](https://gist.github.com/tclementdev/6af616354912b0347cdf6db159c37057):

> The libdispatch is one of the most misused API due to the way it was presented to us when it was introduced and for many years after that, and due to the confusing documentation and API. This page is a compilation of important things to know if you're going to use this library. Many references are available at the end of this document pointing to comments from Apple's very own libdispatch maintainer (Pierre Habouzit).

#### Quality of Service
Queues with `.background` Quality of Service (QoS) may *never* be executed, e.g. low power mode, so plan accordingly.
- If using `.background`, you probably want `.utility` instead.
- [Tweet](https://twitter.com/gregheo/status/1001501337907970048)
- [Docs](https://developer.apple.com/library/content/documentation/Performance/Conceptual/EnergyGuide-iOS/PrioritizeWorkWithQoS.html)

#### Threads != Queues
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
