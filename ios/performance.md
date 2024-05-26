# iOS Performance

#### [Measuring iOS scroll performance](http://thisiskyle.me/posts/measuring-ios-scroll-performance-is-tough-use-this-to-make-it-simple-and-automated.html)

#### [iOS Performance tips you probably didn't know (from an ex-Apple engineer)](https://www.fadel.io/blog/posts/ios-performance-tips-you-probably-didnt-know/)

> 1. `UILabel` costs more than what you think
> 1. Always start with serial queues, and only use concurrent queues as a last resort
> 1. Avoid using `dispatch_semaphore_t` to wait for asynchronous work
> 1. Don’t use UIView tags
