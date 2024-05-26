# SwiftUI

You can find the [official documentation here](https://developer.apple.com/documentation/swiftui).

Also see [Fucking SwiftUI](https://fuckingswiftui.com) (or [Gosh Darn SwiftUI](https://goshdarnswiftui.com)) for a nice "cheat sheet" and a [breakdown of UIKit equivalent APIs](https://fuckingswiftui.com/#uikit-equivalent-in-swiftui).

## Changelogs

- [SwiftUI updates - Apple Developer](https://developer.apple.com/documentation/updates/swiftui)
- [SwiftUI Index – mackuba.eu](https://mackuba.eu/swiftui/changelog)

## WWDC Lounges

- [2021 SwiftUI Lounge Q&As](https://roblack.github.io/WWDC21Lounges/)

## Example Apps

Apps built fully (or mostly) with SwiftUI.

- [isowords](https://github.com/pointfreeco/isowords)
- [RedditOS](https://github.com/Dimillian/RedditOS)
- [MovieSwiftUI](https://github.com/Dimillian/MovieSwiftUI)
- [ACHNBrowserUI](https://github.com/Dimillian/ACHNBrowserUI)
- [MemeMaker](https://github.com/dempseyatgithub/MemeMaker)
- [Pulse](https://github.com/kean/Pulse)

## Tutorials

- [Apple: iOS App Dev with SwiftUI Tutorials](https://developer.apple.com/tutorials/app-dev-training/#swiftui-essentials)
- [SwiftUI Examples for macOS](https://gavinw.me/swift-macos/), Gavin Wiggins
- [Accessibility in SwiftUI - Swift with Majid](http://swiftwithmajid.com/2019/09/10/accessibility-in-swiftui/)
- [ImageRenderer in SwiftUI - Swift with Majid](https://swiftwithmajid.com/2023/04/18/imagerenderer-in-swiftui/)

## Tools + Tips

#### [A Companion for SwiftUI](https://swiftui-lab.com/companion/)

> An app that documents all the SwiftUI views, shapes, protocols, scenes, property wrappers, styles and environment values found in all platforms (iOS, macOS, tvOS, watchOS).

#### [DetailsPro](https://detailspro.app/)

> A GUI for SwiftUI Design.

#### [How to Find Why a SwiftUI View Is Updating](https://mjtsai.com/blog/2021/12/21/how-to-find-why-a-swiftui-view-is-updating/)

> SwiftUI has a new, pretty cool, debugging utility to help you understand what is causing a view to be reevaluated.
>
> Call `Self._printChanges()` inside the body of a view to print out the changes that have triggered the view update.

#### [SwiftUI performance tips](https://martinmitrevski.com/2022/04/14/swiftui-performance-tips/)

> SwiftUI has been around for almost 3 years now, and during this period working with it, I’ve noticed few groups of developer mistakes (both mine and from others) that can impact its performance. In this post, we will look at these pitfalls, and their potential solutions.

#### [Working With UIViewRepresentable](https://chris.eidhof.nl/post/view-representable/)

> When we work with SwiftUI, we can always drop down to UIKit level by using UIViewRepresentable, NSViewRepresentable or UIViewControllerRepresentable. The documentation around these protocols is still pretty sparse, and it can be hard to get them to work exactly the way we want. I tried to come up with some rules and patterns for using them.

#### [SwiftUI Prefers Semantics](https://danielsaidi.com/blog/2023/06/15/swiftui-prefers-semantics)

> SwiftUI get amazing updates every year. If you however have to support old OS versions, you may be unable to use the new tools, or jump through hoops to make it work.
>
> In this post, let’s look at a semantic approach to use new, non-critical features in apps that target old OS versions.

## Collections

- [Discover SwiftUI on Swift by Sundell](https://www.swiftbysundell.com/discover/swiftui/)
- [The SwiftUI Lab](https://swiftui-lab.com)
- [SwiftUI Weekly](http://weekly.swiftwithmajid.com), [Swift with Majid](https://swiftwithmajid.com/archive/)

## API Changes

- [SwiftUI betas - what changed before 1.0](https://mackuba.eu/2020/08/17/swiftui-beta/)
- [What’s new in SwiftUI for iOS 14](https://www.hackingwithswift.com/articles/221/whats-new-in-swiftui-for-ios-14)

## Known Issues + Workarounds

- [Apple Documentation and SwiftUI for Mac](https://mjtsai.com/blog/2021/02/26/apple-documentation-and-swiftui-for-mac/)
- [The State of SwiftUI](https://mjtsai.com/blog/2020/09/18/the-state-of-swiftui/)
- [Self-Sizing UITableView Cells with SwiftUI](https://noahgilmore.com/blog/swiftui-self-sizing-cells/)
- [Fixing keyboardShortcut in SwiftUI](https://steipete.me/posts/fixing-keyboardshortcut-in-swiftui/)
- [Supporting Both Tap and Long Press on a Button in SwiftUI](https://steipete.me/posts/supporting-both-tap-and-longpress-on-button-in-swiftui/)
- [Disabling Keyboard Avoidance in SwiftUI's UIHostingController](https://steipete.me/posts/disabling-keyboard-avoidance-in-swiftui-uihostingcontroller/)
- [Poor performance for macOS apps](https://mobile.twitter.com/steipete/status/1376540592205860865)
- [Keyboard Navigation in SwiftUI](https://pspdfkit.com/blog/2021/keyboard-navigation-in-swiftui/)
- [iOS 14 `.onAppear()` is called on **DISappear** instead of appear](https://developer.apple.com/forums/thread/655338)

#### Dismissing the keyboard

Unfortunately, [`.keyboardDismissMode`](https://developer.apple.com/documentation/uikit/uiscrollview/1619437-keyboarddismissmode) is not available in SwiftUI, so hacks are required:

- [How to dismiss the keyboard for a TextField](https://www.hackingwithswift.com/quick-start/swiftui/how-to-dismiss-the-keyboard-for-a-textfield)
- [Dismissing The Keyboard In SwiftUI 2.0](https://www.dabblingbadger.com/blog/2020/11/5/dismissing-the-keyboard-in-swiftui)

#### [Why Conditional View Modifiers are a Bad Idea](https://www.objc.io/blog/2021/08/24/conditional-view-modifiers/)

> There are many blog posts out there with similar modifiers. I think all these blog posts should come with a huge warning sign. Why is the above code problematic? Let's look at a sample.

#### SwiftUI seems to be breaking across OS releases on all platforms

See Michael Tsai's post on [iOS 15 Shortcuts and SwiftUI](https://mjtsai.com/blog/2021/10/01/ios-15-shortcuts-and-swiftui/).

> SwiftUI metrics & padding changes in macOS 12 are… ‘a problem’. I’m seeing all kinds of wrong behavior across my apps, compared to macOS 11. Fixing for one will break the other, which would mean a lot of nasty if statements. I hear iOS 15 has similar issues.
>
> &mdash; [@stroughtonsmith](https://twitter.com/stroughtonsmith/status/1430746752039231496)

> Growing increasingly concerned about this critical SwiftUI Button bug that breaks trackpad/click focus on iPadOS 15 + macOS Monterey.
> [...]
> Oh wow, this bug is actually present in the Shortcuts app too (created in SwiftUI w/ iOS 15?)
>
> &mdash; [@michael_tigas](https://mobile.twitter.com/michael_tigas/status/1435549427691769867)

> We’re in ‘year 3’ of SwiftUI, and my base advice remains unchanged — it is great for auxiliary non-critical UI layouts (inspector sidebars, settings windows, and panels), watchOS apps, and rapid prototyping. Beyond that, it just does not meet the bar for complex, reliable apps
>
> &mdash; [@stroughtonsmith](https://twitter.com/stroughtonsmith/status/1443692971187130373)

## Retrospectives + Lessons Learned

- [SwiftUI In Production](https://pspdfkit.com/blog/2021/swiftui-in-production/)
- [The SwiftUI Experiment - Retrospective](https://kean.blog/post/swiftui-experiment#retrospective)
- [SwiftUI Animation Lessons From Building “Time’s Up! Timer”](https://blog.overdesigned.net/posts/2021-09-29-swiftui-animation-tricks/)

## Debugging

#### [SwiftUI-Introspect](https://github.com/siteline/SwiftUI-Introspect) library

> Introspect underlying UIKit components from SwiftUI

#### [Building SwiftUI debugging utilities](https://www.swiftbysundell.com/articles/building-swiftui-debugging-utilities/)

> When working on any kind of app or system, it’s almost guaranteed that we’ll need to debug our code at one point or another. For example in order to reproduce a bug that’s been reported to us by either a tester or a user, to track down a race condition or some other source of ambiguity within our logic, or to fix a view that’s not being rendered correctly.

#### [Inspecting SwiftUI views](https://fivestars.blog/swiftui/inspecting-views.html)

> But what if we wanted to know more about that view? In this article, let’s explore how we can do so.

#### [Random Color for SwiftUI](https://gist.github.com/steipete/579edd8bd8b25dc8a89b546b54d9222f)

> Setting a random background color is a great way to detect an accidental SwiftUI loop. The tricky part is understanding what triggers the loop tho.
>
> — [@steipete, Peter Steinberger](https://mobile.twitter.com/steipete/status/1379483193708052480)

See also, [David Smiths's "Random Border Trick"](https://www.david-smith.org/blog/2021/04/08/watchsmith-2-dev-notes/):

> A little trick I found super useful was to set the border of each of the various views involved to a random color and then it see what borders change whenever the view rebuilds. This helped me countless times to determine where in the view tree the problem was.

## Behind the scenes: How SwiftUI works

#### [clipped() doesn’t affect hit testing](https://oleb.net/2022/clipped-hit-testing/)

> The clipped() modifier in SwiftUI clips a view to its bounds, hiding any out-of-bounds content. But note that clipping doesn’t affect hit testing; the clipped view can still receive taps/clicks outside the visible area.

#### [How an Hstack Lays out Its Children](https://www.objc.io/blog/2020/11/10/hstacks-child-ordering/)

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

#### [SwiftUI List Bindings: Behind the Scenes](https://peterfriese.dev/swiftui-list-item-bindings-behind-the-scenes/)

> As of WWDC 2021, SwiftUI supports bindings for list elements.
>
> [...]
>
> But how does it work?

#### [SwiftUI: Understanding identity via transitions](https://sakunlabs.com/blog/swiftui-identity-transitions/)

> In SwiftUI, identity holds the key to understanding how the rendering system works. A View's identity tells SwiftUI which of that View's values correspond to the same rendered view over time. This identity has strong implications for correctness, performance, and as we will see, transitions.

#### [How the SwiftUI View Lifecycle and Identity Work](https://doordash.engineering/2022/05/31/how-the-swiftui-view-lifecycle-and-identity-work/)

> A beginner friendly article on view identity with an intro about Swift UI in general.

## Working with Core Data

#### [Core Data and SwiftUI](https://davedelong.com/blog/2021/04/03/core-data-and-swiftui/)

> This is a large part of why I suggest creating an abstraction layer for Core Data. An abstraction layer allows me to hide the nitty gritty details of data mutation and persistence from the parts of the app that deal with displaying that data in the UI.
>
> An initial approach might suggest that creating a Core Data abstraction layer requires foregoing all the nice affordances we have for quickly and expressively extracting information from the persistent store. Not so! The setup we’ll be going over allows me to have the abstraction layer while still using cool things (like property wrappers) for retrieving data.

#### [Fetching objects from Core Data in a SwiftUI project](https://www.donnywals.com/fetching-objects-from-core-data-in-a-swiftui-project/)

> When you've added Core Data to your SwiftUI project and you have some data stored in your database, the next hurdle is to somehow fetch that data from your Core Data store and present it to the user.

#### [Quick guide to using Core Data with SwiftUI](https://tanaschita.com/20210320-using-core-data-with-swiftui)

> The easiest way to see how Core Data works with SwiftUI is by creating a new SwiftUI project and selecting the Use Core Data checkmark. Xcode will generate a working example that we can try out and review immediately.

#### [Configuring SwiftUI Fetch Requests](https://useyourloaf.com/blog/configuring-swiftui-fetch-requests/)

> In iOS 15, it’s easier to dynamically configure a Core Data fetch request for use with SwiftUI.

## Project Setup

#### [Setting up a multi-platform SwiftUI project](https://blog.scottlogic.com/2021/03/04/Multiplatform-SwiftUI.html)

> This blog will take a look at a basic setup for a multi-platform SwiftUI app.

#### [How SwiftUI can now be used to build entire iOS apps](https://wwdcbysundell.com/2020/building-entire-apps-with-swiftui/)

> This year, however, entire apps can now be defined directly using SwiftUI, thanks to a few new additions to its API.

## Layout

#### [Impossible Grids with SwiftUI](https://swiftui-lab.com/impossible-grids/)

> Native support for grids in SwiftUI is finally here. This is made possible by two new views. These are LazyVGrid and LazyHGrid.

#### [Sharing layout information in SwiftUI](https://fivestars.blog/swiftui/swiftui-share-layout-information.html)

> SwiftUI views layout depends on each view state. This state is composed of a mix of internal properties, external values coming from the environment, etc.

#### [Adaptive SwiftUI views](https://fivestars.blog/swiftui/adaptive-swiftui-views.html)

> While this is great and can save us hundreds of hours, sometimes we want to make our UI declarations even more adaptive: in this article, let’s see how we can do so.

#### [SwiftUI View That Fits](https://useyourloaf.com/blog/swiftui-view-that-fits/)

> The SwiftUI ViewThatFits view, introduced in iOS 16, makes it a lot simpler to build layouts that adapt to make best use of the available space.

## General "How To"

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

#### [MatchedGeometryEffect - The SwiftUI Lab](https://swiftui-lab.com/matchedgeometryeffect-part1/)

> We are talking about a new extension to the View protocol, the .matchedGeometryEffect() modifier. On its own, it’s good enough, but in combination with other techniques we learned already (custom transitions and animatable modifiers), it becomes even better. It is an essential skill to put in your SwiftUI toolkit.

#### [Generating automatic placeholders for SwiftUI views](https://www.swiftbysundell.com/tips/swiftui-automatic-placeholders/)

> SwiftUI now ships with a new, built-in modifier that makes it really easy to automatically generate a placeholder for any view.

#### [Creating custom `.redacted` effects](https://fivestars.blog/code/redacted-custom-effects.html)

> With the recent release of Xcode 12 we’ve gained a new `.redacted(reason:)` SwiftUI modifier.

#### [Label](https://fivestars.blog/swiftui/label.html)

> In this article, let’s explore this view beyond the basics.

#### [NSUserActivity with SwiftUI](https://swiftui-lab.com/nsuseractivity-with-swiftui/)

> And now that SwiftUI also supports user activities and the scene delegates are gone, there’s even more change. A good time then, for a new article.

#### [How to show and hide content with DisclosureGroup using SwiftUI](https://kristaps.me/blog/swiftui-disclosure-group/)

> Now with the new SwiftUI capabilities, we can collapse content with DisclosureGroup. Let's see how we could use it in various ways.

#### [Mastering transitions in SwiftUI](https://nerdyak.tech/development/2020/10/12/transitions-in-swiftui.html)

> In this article, we will go through all important parts related to the implementation of transitions in SwiftUI - from the very basics to more advanced techniques.

#### [Encapsulating SwiftUI view styles](https://www.swiftbysundell.com/articles/encapsulating-swiftui-view-styles/)

> However, if we start exploring SwiftUI’s various APIs and conventions a bit further, it turns out that there are a number of tools and techniques that we can use to create a clean separation between our view hierarchy, its styles, and the components that we’re looking to reuse across a given project.

#### [Handling loading states within SwiftUI views](https://www.swiftbysundell.com/articles/handling-loading-states-in-swiftui/)

> One of the most important aspects of that kind of asynchronous work, at least when it comes to building UI-based apps, is figuring out how to reliably update our various views according to the current state of the background operations that we’ll perform. So this week, let’s take a look at a few different options on how to do just that when building views using SwiftUI.

#### [Attributed Strings with SwiftUI](https://swiftui-lab.com/attributed-strings-with-swiftui/)

> Before we begin, let’s put it right there: SwiftUI is not prepared to handle attributed strings easily. With that out of the way, let’s see the best approaches to fill that void and the limitations or problems we will find along the way.

#### [Keyboard shortcuts in SwiftUI](https://swiftwithmajid.com/2020/11/17/keyboard-shortcuts-in-swiftui/)

> This week, we will discuss the new keyboardShortcut modifier, which allows us to assign a shortcut to any interacting view.

#### [Focus management in SwiftUI](https://swiftwithmajid.com/2020/12/02/focus-management-in-swiftui/)

> One of these new APIs was the focus management API that we can use on iOS, macOS, tvOS, and watchOS. This week we will talk about SwiftUI functionality that allows us to manage the focus in our apps.

#### [Avoiding SwiftUI’s AnyView](https://www.swiftbysundell.com/articles/avoiding-anyview-in-swiftui/)

> So, in this article, let’s take a look at two core techniques that can help us avoid AnyView while still enabling us to work with multiple view types in very dynamic ways.

#### [Which SwiftUI property wrapper to choose in any situation](https://www.hackingwithswift.com/articles/227/which-swiftui-property-wrapper)

> SwiftUI uses property wrappers to understand how we create and store data in our views, but if you need helping choosing which property wrapper is right for you I've made a tool to help. To find the right property wrapper for you, answer the questions below.

#### [Nested Observable Objects in SwiftUI](https://rhonabwy.com/2021/02/13/nested-observable-objects-in-swiftui/)

> At first blush, this looks fine – the view displays, and property within the nested view is shown as you’d expect; so what’s the problem? The issue is when you update that nested element’s property, even though it’s listed as @Published, the change doesn’t propagate to the view.

#### [SwiftUI Custom Environment Values](https://useyourloaf.com/blog/swiftui-custom-environment-values/)

> Here’s my quick guide to creating your own custom SwiftUI environment values for things like global app settings.

#### [Mastering SwiftUI previews](https://swiftwithmajid.com/2021/03/10/mastering-swiftui-previews/)

> SwiftUI previews allow you to look at your SwiftUI views inside Xcode without running the app in the simulator. You can also preview UIKit views and controllers by wrapping them in SwiftUI. Today we will learn about all the powerful features of previews in Xcode.

#### [The @ScaledMetric Property Wrapper](https://useyourloaf.com/blog/the-scaledmetric-property-wrapper/)

> How can you scale other metrics, like spacing, as the dynamic type content size changes? In iOS 14, SwiftUI gained the @ScaledMetric property wrapper that can scale any numeric value.

#### [Implementing Three Column Navigation in SwiftUI](https://serialcoder.dev/text-tutorials/swiftui/implementing-three-column-navigation-in-swiftui/)

> In UIKit and AppKit, a UISplitViewController and a NSSplitViewController would be the necessary classes for building that functionality. In SwiftUI things are different though; a NavigationView with a couple of List views do the job in a much simpler fashion. The only requirement is to follow certain steps in the proper order.

#### [Every SwiftUI Environment Value explained](https://www.fivestars.blog/articles/swiftui-environment-values/)

> ...in this article, let's review all environment values that SwiftUI offers.

#### [How to add a clear button to a TextField](https://sanzaru84.medium.com/swiftui-how-to-add-a-clear-button-to-a-textfield-9323c48ba61c)

> The TextField element of the SwiftUI framework does not have such a feature built-in, so you’d have to build your own solution for that. In this article I want to show how to accomplish a simple clear button inside a SwiftUI TextField element.

#### [How to render text with a color gradient in SwiftUI](https://sarunw.com/posts/how-to-render-text-with-color-gradient-in-swiftui/)

> This article will explore how to render text with color gradients.

#### [Running Code Only Once in SwiftUI](https://www.swiftjectivec.com/swiftui-run-code-only-once-versus-onappear-or-task/)

> I’ve had a few situations in SwiftUI where I only want things to fire once and initially. At face value, this seems like a job for either `.onAppear` or the more nascent `.task`.

#### [Michael Tsai - Blog - SwiftUI Data Flow 2023](https://mjtsai.com/blog/2023/07/06/swiftui-data-flow-2023/)

> Michael Tsai roundup.
