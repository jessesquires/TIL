# SwiftUI

You can find the [official documentation here](https://developer.apple.com/documentation/swiftui).

## Example Apps

Apps built fully (or mostly) with SwiftUI.

- [isowords](https://github.com/pointfreeco/isowords)
- [RedditOS](https://github.com/Dimillian/RedditOS)
- [MovieSwiftUI](https://github.com/Dimillian/MovieSwiftUI)
- [ACHNBrowserUI](https://github.com/Dimillian/ACHNBrowserUI)
- [MemeMaker](https://github.com/dempseyatgithub/MemeMaker)

## Guided Tutorials

- [Apple: iOS App Dev with SwiftUI Tutorials](https://developer.apple.com/tutorials/app-dev-training/#swiftui-essentials)

## Collections

- [Discover SwiftUI on Swift by Sundell](https://www.swiftbysundell.com/discover/swiftui/)
- [Swift with Majid](https://swiftwithmajid.com/archive/)
- [The SwiftUI Lab](https://swiftui-lab.com)
- [SwiftUI Weekly](http://weekly.swiftwithmajid.com)

## API Changes + Known Issues

- [SwiftUI betas - what changed before 1.0](https://mackuba.eu/2020/08/17/swiftui-beta/)
- [Apple Documentation and SwiftUI for Mac](https://mjtsai.com/blog/2021/02/26/apple-documentation-and-swiftui-for-mac/)
- [The State of SwiftUI](https://mjtsai.com/blog/2020/09/18/the-state-of-swiftui/)
- [What’s new in SwiftUI for iOS 14](https://www.hackingwithswift.com/articles/221/whats-new-in-swiftui-for-ios-14)
- [Poor performance for macOS apps](https://mobile.twitter.com/steipete/status/1376540592205860865)

## Debugging

#### [Building SwiftUI debugging utilities](https://www.swiftbysundell.com/articles/building-swiftui-debugging-utilities/)

> When working on any kind of app or system, it’s almost guaranteed that we’ll need to debug our code at one point or another. For example in order to reproduce a bug that’s been reported to us by either a tester or a user, to track down a race condition or some other source of ambiguity within our logic, or to fix a view that’s not being rendered correctly.

#### [Inspecting SwiftUI views](https://fivestars.blog/swiftui/inspecting-views.html)

> But what if we wanted to know more about that view? In this article, let’s explore how we can do so.

## Behind the scenes: How SwiftUI works

#### [How an Hstack Lays out Its Children](https://www.objc.io/blog/2020/11/09/hstacks-child-ordering/)

> For the most part SwiftUI’s layout system is intuitive to use, letting you achieve what you want with a little bit of experimentation. However, sometimes you encounter behaviors that are hard to reason about without a deeper understanding of the underlying implementation.

#### [SwiftUI’s Grid Views](https://www.objc.io/blog/2020/11/23/grid-layout/)

> A few days ago we tweeted a series of layout quizzes for SwiftUI’s LazyVGrid to highlight some of the less obvious behaviors. In this post we’ll take a look at all three quiz questions and explain why the grid lays out its contents in the way it does.
>
> Interestingly, we were not the only ones struggling to understand the behavior of grids: none of the most popular quiz answers were correct!

#### [SwiftUI View Lifecycle](https://www.vadimbulavin.com/swiftui-view-lifecycle/)

> Each view undergoes a series of events from its birth to its death, which is referred to as a lifecycle. Understanding it is essential when building apps in SwiftUI. In this article, we will explore the three phases of the SwiftUI view lifecycle.

#### [The Ultimate Guide to the SwiftUI 2 Application Life Cycle](https://peterfriese.dev/ultimate-guide-to-swiftui2-application-lifecycle/)

> For the longest time, iOS developers have used AppDelegates as the main entry point for their applications. With the launch of SwiftUI2 at WWDC 2020, Apple has introduced a new application life cycle that (almost) completely does away with AppDelegate, making way for a DSL-like approach.
>
> In this article, I will discuss why this change was introduced, and how you can make use of the new life cycle in new or existing apps.

## Working with Core Data

#### [Fetching objects from Core Data in a SwiftUI project](https://www.donnywals.com/fetching-objects-from-core-data-in-a-swiftui-project/)

> When you've added Core Data to your SwiftUI project and you have some data stored in your database, the next hurdle is to somehow fetch that data from your Core Data store and present it to the user.

#### [Quick guide to using Core Data with SwiftUI](https://tanaschita.com/20210320-using-core-data-with-swiftui)

> The easiest way to see how Core Data works with SwiftUI is by creating a new SwiftUI project and selecting the Use Core Data checkmark. Xcode will generate a working example that we can try out and review immediately.

## How To

#### [How SwiftUI can now be used to build entire iOS apps](https://wwdcbysundell.com/2020/building-entire-apps-with-swiftui/)

> This year, however, entire apps can now be defined directly using SwiftUI, thanks to a few new additions to its API.

#### [How to define SwiftUI properties](https://twitter.com/chriseidhof/status/1280433133813456896)

> Here's a first draft of a decision tree for how to define your SwiftUI properties...

#### [A guide to SwiftUI’s state management system](https://www.swiftbysundell.com/articles/swiftui-state-management-guide/)

> What separates SwiftUI from Apple’s previous UI frameworks isn’t just how views and other UI components are defined, but also how view-level state is managed throughout an app that uses it.
> 
>  [...]
> 
> This week, let’s take a closer look at each of those property wrappers, how they relate to each other, and how they make up different parts of SwiftUI’s overall state management system. 

#### [Mastering toolbars in SwiftUI](https://swiftwithmajid.com/2020/07/15/mastering-toolbars-in-swiftui/)

> This week we will learn all about the new Toolbar API.

#### [Setting up a multi-platform SwiftUI project](https://blog.scottlogic.com/2021/03/04/Multiplatform-SwiftUI.html)

> This blog will take a look at a basic setup for a multi-platform SwiftUI app.

#### [MatchedGeometryEffect | The SwiftUI Lab](https://swiftui-lab.com/matchedgeometryeffect-part1/)

> We are talking about a new extension to the View protocol, the .matchedGeometryEffect() modifier. On its own, it’s good enough, but in combination with other techniques we learned already (custom transitions and animatable modifiers), it becomes even better. It is an essential skill to put in your SwiftUI toolkit.

#### [Generating automatic placeholders for SwiftUI views](https://www.swiftbysundell.com/tips/swiftui-automatic-placeholders/)

> SwiftUI now ships with a new, built-in modifier that makes it really easy to automatically generate a placeholder for any view. 

#### [Creating custom `.redacted` effects](https://fivestars.blog/code/redacted-custom-effects.html)

> With the recent release of Xcode 12 we’ve gained a new `.redacted(reason:)` SwiftUI modifier.

#### [Impossible Grids with SwiftUI](https://swiftui-lab.com/impossible-grids/)

> Native support for grids in SwiftUI is finally here. This is made possible by two new views. These are LazyVGrid and LazyHGrid.

#### [Sharing layout information in SwiftUI](https://fivestars.blog/swiftui/swiftui-share-layout-information.html)

> SwiftUI views layout depends on each view state. This state is composed of a mix of internal properties, external values coming from the environment, etc.

#### [Label](https://fivestars.blog/swiftui/label.html)

> In this article, let’s explore this view beyond the basics.

#### [NSUserActivity with SwiftUI](https://swiftui-lab.com/nsuseractivity-with-swiftui/)

> And now that SwiftUI also supports user activities and the scene delegates are gone, there’s even more change. A good time then, for a new article.

#### [How to show and hide content with DisclosureGroup using SwiftUI](https://kristaps.me/blog/swiftui-disclosure-group/)

> Now with the new SwiftUI capabilities, we can collapse content with DisclosureGroup. Let's see how we could use it in various ways.

#### [Mastering transitions in SwiftUI](https://nerdyak.tech/development/2020/10/12/transitions-in-swiftui.html)

> In this article, we will go through all important parts related to the implementation of transitions in SwiftUI - from the very basics to more advanced techniques.
