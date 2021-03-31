# Core Data

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
