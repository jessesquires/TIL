# iOS In-App Purchases and Subscriptions

* [Linking to Subscription Management Settings](https://joecieplinski.com/blog/2018/11/26/linking-to-subscription-management-settings/)

* [The Ultimate Guide to iOS Subscription Testing](https://www.revenuecat.com/blog/the-ultimate-guide-to-subscription-testing-on-ios)

## Receipt Validation

For subscriptions and IAPs, often folks implement server-side receipt validation, but that is not _always_ necessary. It is possible to do receipt validation 100% clide-side, which might make sense in some cases. For example, simple client-side gating for client-side features. If subscriptions or IAPs access server content or services, _then_ you should definitely validate receipts on the server.

Be aware that client-side validation is susceptible to being undermined by hacks and jailbreaks. However, this may not be a concern for you.

- [Cocoanetics/Kvitto: App Store Receipt Validation](https://github.com/Cocoanetics/Kvitto)
- [Choosing a Receipt Validation Technique — Apple Developer](https://developer.apple.com/documentation/storekit/original_api_for_in-app_purchase/choosing_a_receipt_validation_technique#//apple_ref/doc/uid/TP40010573)
- Example: [ChatSecure-iOS](https://github.com/ChatSecure/ChatSecure-iOS/blob/38d6abba3e1c21156095ac3a1096d5e829df4b96/ChatSecureCore/Classes/View%20Controllers/PurchaseViewController.swift#L230)
- [New Receipt Validation Sample Code](https://mjtsai.com/blog/2022/05/20/new-receipt-validation-sample-code/) (2022)
- [Mac App Store receipt validation revisited](https://lapcatsoftware.com/articles/2023/11/4.html), Jeff Johnson 2023
- [verifyReceipt | Apple Developer Documentation](https://developer.apple.com/documentation/appstorereceipts/verifyreceipt)
- [Validating receipts on the device | Apple Developer Documentation](https://developer.apple.com/documentation/appstorereceipts/validating_receipts_on_the_device) (OLD)

#### [App Store Subscriptions and Family Sharing](https://furbo.org/2024/03/29/app-store-subscriptions-and-family-sharing/)

> That code will work fine until you encounter a customer that has Family Sharing enabled, as most do. The issue is that the Product.SubscriptionInfo can contain multiple items, and the code above only checks the first one.

## Tech Notes

- [TN3122: Receipt validation with the App Store fails with a non-zero error code](https://developer.apple.com/documentation/technotes/tn3122-receipt-validation-with-the-app-store-fails-with-a-non-zero-error-code)
- [TN3138: Handling App Store receipt signing certificate changes](https://developer.apple.com/documentation/technotes/tn3138-handling-app-store-receipt-signing-certificate-changes)

## Free Trials

- [Implementing Introductory Offers in Your App — Apple Developer](https://developer.apple.com/documentation/storekit/original_api_for_in-app_purchase/subscriptions_and_offers/implementing_introductory_offers_in_your_app)
- [Testing Introductory Offers — Apple Developer](https://developer.apple.com/documentation/storekit/original_api_for_in-app_purchase/subscriptions_and_offers/testing_introductory_offers)

## Subscription tutorial

- https://www.revenuecat.com/blog/engineering/ios-in-app-subscription-tutorial-with-storekit-2-and-swift/

## Paywall ideas

- https://blog.curtisherbert.com/slopes-diaries-42-building-ramps-not-walls/
- https://trycombine.com/posts/simple-view-modifier-to-handle-features-that-are-only-enabled-in-the-pro-version-of-the-app/

## Blogs

- https://sarunw.com/posts/manage-in-app-subscription-in-swiftui/

## Testing

- [StoreKit Test framework](https://developer.apple.com/documentation/storekittest)
- [How to test In-App purchases in Development](https://sarunw.com/posts/test-in-app-purchases-in-development/)

## SDK

- [Upcoming changes to the App Store receipt signing intermediate certificate](https://developer.apple.com/news/?id=smofnyhj) (2023)
- [AppTransaction | Apple Developer Documentation](https://developer.apple.com/documentation/storekit/apptransaction)
- [Transaction | Apple Developer Documentation](https://developer.apple.com/documentation/storekit/transaction)

## StoreKit

- [Mastering StoreKit 2](https://swiftwithmajid.com/2023/08/01/mastering-storekit2/)
- [Mastering StoreKit 2. ProductView and StoreView](https://swiftwithmajid.com/2023/08/08/mastering-storekit2-productview-in-swiftui/)
- [Mastering StoreKit 2. SubscriptionStoreView in SwiftUI](https://swiftwithmajid.com/2023/08/23/mastering-storekit2-subscriptionstoreview-in-swiftui/)
- [Mastering StoreKit 2. SwiftUI view modifiers](https://swiftwithmajid.com/2023/08/29/mastering-storekit2-swiftui-view-modifiers/)
- [StoreKit 2 Tutorial with Swift UI - How to add In-App Purchases to your app — Superwall](https://superwall.com/blog/make-a-swiftui-app-with-in-app-purchases-and-subscriptions-using-storekit-2)
- [StoreKit paywall views in SwiftUI: The Complete Fieldguide — Superwall](https://superwall.com/blog/storekit-paywall-views-in-swiftui-the-complete-fieldguide)
