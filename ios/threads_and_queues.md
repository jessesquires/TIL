# Threads and Queues

- [libdispatch efficiency tips](
https://gist.github.com/tclementdev/6af616354912b0347cdf6db159c37057)

- Queues with `.background` Quality of Service (QoS) may *never* be executed, e.g. low power mode, so plan accordingly.
    - If using `.background`, you probably want `.utility` instead.
    - [Tweet](https://twitter.com/gregheo/status/1001501337907970048)
    - [Docs](https://developer.apple.com/library/content/documentation/Performance/Conceptual/EnergyGuide-iOS/PrioritizeWorkWithQoS.html)

- Threads != Queues
    - [Main Queue vs Main Thread](http://blog.benjamin-encz.de/post/main-queue-vs-main-thread/)
    - [Queues are not bound to any specific thread](https://blog.krzyzanowskim.com/2016/06/03/queues-are-not-bound-to-any-specific-thread/)
