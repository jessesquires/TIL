# CoreData

- [Core Data Programming Guide: What Is Core Data?](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/CoreData/index.html#//apple_ref/doc/uid/TP40001075-CH2-SW1)
- [Requesting Lightweight Migration - CoreData](https://developer.apple.com/documentation/coredata/using_lightweight_migration)

#### [The Laws of Core Data](http://davedelong.com/blog/2018/05/09/the-laws-of-core-data/)

> In my conversations with developers, I’ve heard a pretty common theme from them that “Core Data is hard” or “Core Data is buggy” or “I could never get it to work right and gave up on it”.
>
> I’ve spent a lot of time using Core Data and thought I’d share my “Laws of Core Data”. These are a set of rules I’ve developed over time on how to use Core Data in such a way that it is almost entirely painless. When I follow these rules, I almost never have any problems using it.

#### [NSPredicate.xyz](https://nspredicate.xyz)

> Examples of NSPredicate usage.

#### [Replacing vs. Migrating Core Data Stores](https://mjtsai.com/blog/2021/03/31/replacing-vs-migrating-core-data-stores/)

> Additionally you should almost never use `NSPersistentStoreCoordinator`’s `migratePersistentStore` method but instead use the newer `replacePersistentStoreAtURL`. (you can replace emptiness to make a copy). The former loads the store into memory so you can do fairly radical things like write it out as a different store type. It pre-dates iOS. The latter will perform an APFS clone where possible.

#### [Making `NSFetchRequest.fetchBatchSize` Work With Swift](https://mjtsai.com/blog/2021/03/31/making-nsfetchrequest-fetchbatchsize-work-with-swift/)

> `Set` in Swift is an immutable value type. We do not recommend making Core Data relationships typed this way despite the obvious convenience. Core Data makes heavy use of Futures, especially for relationship values. These are reference types expressed as `NSSet`. The concrete instance is a future subclass however. This lets us optimize memory and performance across your object graph. Declaring an accessor as `Set` forces an immediate copy of the entire relationship so it can be an immutable Swift `Set`. This loads the entire relationship up front and fulfills the Future all the time, immediately. You probably do not want that.

#### [How to Set Up Core Data and CloudKit](https://beckyhansmeyer.com/2021/03/30/how-to-set-up-core-data-cloudkit-and-swiftui-when-you-havent-the-faintest-clue-what-youre-doing/)

> When Apple introduced changes to Core Data + CloudKit integration in 2019, they sold developers on a dead-simple API: add iCloud sync to your Core Data app with “as little as one line of code.” That one line, of course, is simply changing `NSPersistentContainer` to `NSPersistentCloudKitContainer` and enabling a few capabilities in the project settings. Boom, done! And in fact, Apple’s “Core Data –> Host in CloudKit” SwiftUI project template does those things for you, so you’re good to go, right?

#### [Changing The Core Data Test Store Location](https://useyourloaf.com/blog/changing-the-core-data-test-store-location/)

> When unit testing with Core Data I like using an in-memory store for speed and ease of clean up. But I also want, at least some of the time, to test with a disk-based store. Changing the location of the test database avoids overwriting or conflicting with any application database that I might already have installed on the simulator or device.

#### [Debugging Core Data](https://useyourloaf.com/blog/debugging-core-data/)

> Apple recommends adding some launch arguments and environment variables to your Xcode schemes to catch and debug Core Data problems. I’ve known about some of these for a long time others were new to me.

#### [Core Data In Memory Store](https://useyourloaf.com/blog/core-data-in-memory-store/)

> The old way of creating an in-memory store was to change the store type in the persistent store descriptor before loading the store. The default is `NSSQLiteStoreType` but we can switch to `NSInMemoryStoreType`:
>
> `storeDescription.type = NSInMemoryStoreType`
>
> There’s nothing I can find in the documentation but Apple showed a different way during WWDC 2018:
>
> `storeDescription.url = URL(fileURLWithPath: "/dev/null")`
>
> This still uses an SQLite store but we keep it in memory instead of writing it to disk. As well as being faster this also gives us a clean store each time.

#### [Async Core Data Testing](https://useyourloaf.com/blog/async-core-data-testing/)

> Testing Core Data has some challenges. Using an in-memory store helps but what if the operation you want to test happens asynchronously? One approach is to have the test listen for the notification Core Data sends when it saves changes.

#### [Core Data Reform: Achieving Elegant Concurrency Operations like SwiftData](https://fatbobman.com/en/posts/core-data-reform-achieving-elegant-concurrency-operations-like-swiftdata/)

> Can we integrate some of SwiftData’s excellent design philosophies and ingenious implementations into the practical use of Core Data? This article aims to explore how to introduce elegant and safe concurrency operations similar to those of SwiftData into Core Data, implementing a Core Data version of `@ModelActor`.

#### [Using `Codable` with Core Data and NSManagedObject](https://www.donnywals.com/using-codable-with-core-data-and-nsmanagedobject/)

> If you've ever wanted to decode a bunch of JSON data into NSManagedObject instances you've probably noticed that this isn't a straightforward exercise. With plain structs, you can conform your struct to Codable and you convert the struct from and to JSON data automatically.

#### [Effective Core Data With Swift - mjtsai](https://mjtsai.com/blog/2018/11/29/effective-core-data-with-swift/)

> Core Data brings a lot of power to an app and continues to evolve, but it can have rough spots when you’re working in Swift. What if you want to save an enum pr a struct? Does it help if your data is `Codable`? What’s the best way to create Swift-friendly model classes? This session will cover techniques and gotchas for integrating Core Data with your Swift code

#### [Changing The Core Data Test Store Location](https://useyourloaf.com/blog/changing-the-core-data-test-store-location/)

#### [Debugging Core Data](https://useyourloaf.com/blog/debugging-core-data/)

#### [Preventing unwanted fetches when using NSFetchedResultsController and fetchBatchSize](https://www.donnywals.com/preventing-unwanted-fetches-when-using-nsfetchedresultscontroller-and-fetchbatchsize/)

#### [How-to use Diffable Data Sources with Core Data](https://www.avanderlee.com/swift/diffable-data-sources-core-data/)

#### [How to create a Core Data fetch request using @FetchRequest](https://www.hackingwithswift.com/quick-start/swiftui/how-to-create-a-core-data-fetch-request-using-fetchrequest)

#### [The Curious Case of the Core Data Crash - The Breakroom](https://blog.iconfactory.com/2019/08/the-curious-case-of-the-core-data-crash/)

#### [Core Data Derived Attributes - mjtsai](https://mjtsai.com/blog/2019/10/17/core-data-derived-attributes/)

> [`NSDerivedAttributeDescription`](https://developer.apple.com/documentation/coredata/nsderivedattributedescription): A description of an attribute that derives its value by performing a calculation on a related attribute.

#### [Setting up a Core Data store for unit tests – Donny Wals](https://www.donnywals.com/setting-up-a-core-data-store-for-unit-tests/)

> When you want to test your Core Data code, it might not be immediately obvious how you can test your Core Data store in isolation.

#### [Persistent History Tracking in Core Data](https://www.avanderlee.com/swift/persistent-history-tracking-core-data/)

> WWDC 2017 introduced a new concept available from iOS 11 which is persistent history tracking. It’s Apple’s answer for merging changes that come from several targets like app extensions. Whenever you change something in your Core Data database from your Share Extension, a transaction is written which can be merged into any of your other targets.

#### [Core Data Saving Changes](https://useyourloaf.com/blog/core-data-saving-changes/)

#### [Michael Tsai - Blog - @Model for CoreData](https://mjtsai.com/blog/2023/10/02/model-for-coredata/)

#### [Michael Tsai - Blog - NSPredicate, Core Data, and NULL](https://mjtsai.com/blog/2023/05/12/nspredicate-core-data-and-null/)
