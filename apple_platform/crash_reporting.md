# Crash Reporting

On Apple platforms.

## [Implementing Your Own Crash Reporter](https://developer.apple.com/forums/thread/113742) (Hint: don't)

> **I strongly advise against implementing your own crash reporter.** It’s very easy to create a basic crash reporter that works well enough to debug simple problems. It’s impossible to implement a good crash reporter, one that’s reliable, binary compatible, and sufficient to debug complex problems. The bulk of this post is a low-level explanation of that impossibility.

## Legacy

#### [Reliable Crash Reporting](https://landonf.org/code/objc/Reliable_Crash_Reporting.20110912.html), Landon Fuller

> PLCrashReporter is a standalone open-source library for generating crash reports on iOS. When I first wrote the library in 2008, it was the only option for automatically generating and gathering crash reports from an iOS application. Apple's iOS crash reports were not available to developers, and existing crash reporters — such as Google's excellent Breakpad — were not supported on iOS (Breakpad still isn't).

#### [Own Your Crash Logs with PLCrashReporter: Part 1](https://www.bignerdranch.com/blog/own-your-crash-logs-with-plcrashreporter-part-1/)

> Welcome to the PLCrashReporter blog post series. For those unfamiliar with this crash reporting library, it is defined as follows...

#### [Own Your Crash Logs with PLCrashReporter: Part 2](https://www.bignerdranch.com/blog/own-your-crash-logs-with-plcrashreporter-part-2/)

> This is part two of our PLCrashReporter series. In this post, we will examine how crashes are created and learn more about specific crash types.

#### [Friday Q&A: Signal Handling](https://mikeash.com/pyblog/friday-qa-2011-04-01-signal-handling.html)

> In this edition, I will discuss various ways of handling signals in Mac programs, a topic suggested by friend of the blog Landon Fuller.
