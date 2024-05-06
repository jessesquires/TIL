# Debugging

*Debugging tips and tricks on Apple Platforms.*

## macOS Debugging

#### [Using `_eventFirstResponderChainDescription`](https://mjtsai.com/blog/2024/03/22/_eventfirstresponderchaindescription/)

> AppKit includes a private category on `NSApplication` that adds `_eventFirstResponderChainDescription` — a string describing the current responder chain. This can be a really useful debugging tool!
>
>  You can also set the `_NS_4445425547` user default to see a Cocoa debug menu.
>
> Today’s Darwin crazy hidden debugging tool of the day: iOS has a built in HUD for showing performance statistics like FPS, frame duration etc. [...] This HUD can be activated by calling the private `CARenderServerSetDebugOption` function

## iOS Debugging

#### [Hopper + lldb for iOS Developers: A Gentle Introduction](https://github.com/bartcone/reverse-engineering-blog)

> Lately I've seen a lot of people asking "How are you getting that pseudo-code," in regards to @steipete's radar he filed and I thought this would be a great first blog post of mine as I've been wanting to for awhile. I spend a lot of my time in a tool called Hopper (it's a must have in my toolbox) and while it's an amazing tool, it can seem overwhelming at first. The goal of this post is to bridge the gap for those that have shied away or aren't familiar with reverse engineering.

## Xcode / Instruments

#### [Instruments Tutorial with Swift: Getting Started](https://www.raywenderlich.com/16126261-instruments-tutorial-with-swift-getting-started)

> In this Xcode tutorial, you’ll learn how to use Instruments to profile and debug performance, memory and reference issues in your iOS apps.

#### [Profiling SwiftUI app using Instruments](https://swiftwithmajid.com/2021/01/20/profiling-swiftui-app-using-instruments/)

> Xcode comes with a bunch of tools you need to build, debug and release your apps. One of these tools is the Instruments app. The Instruments app is a great tool for profiling your iOS apps. It provides many profiling templates for debugging Core Data, catching memory leaks, disk read/writes, and much more. This week we will learn how to profile SwiftUI apps using the SwiftUI template.
