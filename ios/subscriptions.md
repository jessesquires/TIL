# iOS App Subscriptions

* [Linking to Subscription Management Settings](https://joecieplinski.com/blog/2018/11/26/linking-to-subscription-management-settings/)

* [The Ultimate Guide to iOS Subscription Testing](https://www.revenuecat.com/blog/the-ultimate-guide-to-subscription-testing-on-ios)

## Receipt Validation

For subscriptions and IAPs, often folks implement server-side receipt validation, but that is not _always_ necessary. It is possible to do receipt validation 100% clide-side, which might make sense in some cases. For example, simple client-side gating for client-side features. If subscriptions or IAPs access server content or services, _then_ you should definitely validate receipts on the server.

Be aware that client-side validation is susceptible to being undermined by hacks and jailbreaks. However, this may not be a concern for you.

- [Cocoanetics/Kvitto: App Store Receipt Validation](https://github.com/Cocoanetics/Kvitto)
- [Choosing a Receipt Validation Technique — Apple Developer](https://developer.apple.com/documentation/storekit/original_api_for_in-app_purchase/choosing_a_receipt_validation_technique#//apple_ref/doc/uid/TP40010573)
- Example: [ChatSecure-iOS](https://github.com/ChatSecure/ChatSecure-iOS/blob/38d6abba3e1c21156095ac3a1096d5e829df4b96/ChatSecureCore/Classes/View%20Controllers/PurchaseViewController.swift#L230)
- [New Receipt Validation Sample Code](https://mjtsai.com/blog/2022/05/20/new-receipt-validation-sample-code/) (2022)
- [verifyReceipt | Apple Developer Documentation](https://developer.apple.com/documentation/appstorereceipts/verifyreceipt)
- [Validating receipts on the device | Apple Developer Documentation](https://developer.apple.com/documentation/appstorereceipts/validating_receipts_on_the_device) (OLD)

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

- https://developer.apple.com/documentation/storekittest

## SDK

- [Upcoming changes to the App Store receipt signing intermediate certificate](https://developer.apple.com/news/?id=smofnyhj) (2023)
- [AppTransaction | Apple Developer Documentation](https://developer.apple.com/documentation/storekit/apptransaction)
- [Transaction | Apple Developer Documentation](https://developer.apple.com/documentation/storekit/transaction)
