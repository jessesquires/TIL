# Threads and Queues

- [libdispatch efficiency tips](
https://gist.github.com/tclementdev/6af616354912b0347cdf6db159c37057)

- Background QoS may *never* be executed, e.g. low power mode, so plan accordingly.<br>
If using `.background`, you probably want `.utility` instead.<br>
[Tweet](https://twitter.com/gregheo/status/1001501337907970048), [Docs](https://developer.apple.com/library/content/documentation/Performance/Conceptual/EnergyGuide-iOS/PrioritizeWorkWithQoS.html)
