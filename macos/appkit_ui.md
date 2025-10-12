# AppKit + macOS UI

#### [Resources for learning Objective-C and AppKit](https://lapcatsoftware.com/articles/learning.html), Jeff Johnson

#### [Fucking NSImage Syntax](https://hetima.github.io/fucking_nsimage_syntax/)

> A list of system image names that can be used for `+[NSImage imageNamed:]`

#### [Appreciating AppKit, Part 1](https://pilky.me/appreciating-appkit-part-1/)

> AppKit is Apple's UI framework for building apps for the Mac. It has existed in one form or another for around 30 years and is the basis for many of the concepts and features of UIKit on iOS. Understandably, given its age, it has quite a few quirks and dated features. Some can simply be ignored, such as drawers. Others are still core to how parts of AppKit function, such as NSCell. These features can make AppKit seem daunting and difficult to work with, especially for those who have only known UIKit.

#### [Appreciating AppKit, Part 2](https://pilky.me/appreciating-appkit-part-2/)

> Welcome to the second part of my Appreciating AppKit post. In the previous post I gave an overview of the many views and controls of AppKit that either don't exist or are not as powerful in UIKit. In this post I want to cover some of the more "behind the scenes" aspects of AppKit, things that help your productivity as a developer and can aid in the architecture of your apps.

#### [A guide to NSButton styles](https://mackuba.eu/2014/10/06/a-guide-to-nsbutton-styles/)

> The macOS SDK has quite a lot of different controls available, and while this gives you a lot of built-in functionality for free, using them in the right way might be a bit more tricky than on iOS. This is especially true in case of the base button class, `NSButton`, which lets you choose from as many as 15 different styles, not counting the subclasses.

#### [AppleProgramming](https://www.youtube.com/c/AppleProgramming/videos), YouTube

#### [Apple HIG](https://developer.apple.com/design/human-interface-guidelines/macos/overview/themes/), developer.apple.com

#### [View Clipping Changes in macOS 14 Sonoma - Indie Stack](https://indiestack.com/2023/06/view-clipping-sonoma/)

> One of the most impactful changes to AppKit in the forthcoming macOS 14 Sonoma update is a change to the default clipping behavior for views. Apple announced that a long-present internal property, “clipsToBounds”, is now public. In tandem with this change, they are changing the default value for this property to false for apps that link against the macOS 14 SDK.

#### [macOS Toolbar Guidelines](https://marioaguzman.github.io/design/toolbarguidelines/), Mario Guzman

> The following sections are general guidelines that describe fundamental Toolbar layout and design principles for Mac applications. Following these guidelines will help you create functional and aesthetically pleasing toolbars that are easy for Mac users to understand and use.

#### [Using `MDItemKeywords`](https://mastodon.social/@marioguzman/110578941262432702)

> If you ship an app for macOS, please do this! I hardly see this at all with Mac apps.
>
> In your `info.plist`, add `MDItemKeywords` and the value is a list of keywords for your app separated by commas. This will show up in your More Info window for your app under “Keywords”.
>
> Why is this useful? Let’s say you make a Mastodon client app called anything BUT Mastodon, if you throw “Mastodon” in this list in `MDItemKeywords`, searching “Mastodon” in Spotlight would surface it as a search result!

#### [NSWindowPlayground](https://github.com/martinhoeller/NSWindowPlayground)

> A small utility app to test out various NSWindow style settings.
