# Threads and Queues

- [libdispatch efficiency tips](
https://gist.github.com/tclementdev/6af616354912b0347cdf6db159c37057):

> The libdispatch is one of the most misused API due to the way it was presented to us when it was introduced and for many years after that, and due to the confusing documentation and API. This page is a compilation of important things to know if you're going to use this library. Many references are available at the end of this document pointing to comments from Apple's very own libdispatch maintainer (Pierre Habouzit).

- Queues with `.background` Quality of Service (QoS) may *never* be executed, e.g. low power mode, so plan accordingly.
    - If using `.background`, you probably want `.utility` instead.
    - [Tweet](https://twitter.com/gregheo/status/1001501337907970048)
    - [Docs](https://developer.apple.com/library/content/documentation/Performance/Conceptual/EnergyGuide-iOS/PrioritizeWorkWithQoS.html)

- Threads != Queues
    - [Main Queue vs Main Thread](http://blog.benjamin-encz.de/post/main-queue-vs-main-thread/)
    - [Queues are not bound to any specific thread](https://blog.krzyzanowskim.com/2016/06/03/queues-are-not-bound-to-any-specific-thread/)
