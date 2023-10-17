# Keychain

#### [SecItem: Fundamentals](https://developer.apple.com/forums/thread/724023), Quinn “The Eskimo!”

> I regularly help developers with keychain problems, both here on DevForums and for my Day Job™ in DTS. Many of these problems are caused by a fundamental misunderstanding of how the keychain works. This post is my attempt to explain that. I wrote it primarily so that Future Quinn™ can direct folks here rather than explain everything from scratch (-:

#### [SecItem: Pitfalls and Best Practices](https://developer.apple.com/forums/thread/724013), Quinn “The Eskimo!”

> f you’re on macOS and targeting the file-based keychain, kSecMatchLimitAll always defaults to kSecMatchLimitOne
>
> I regularly help developers with keychain problems, both here on DevForums and for my Day Job™ in DTS. Over the years I’ve learnt a lot about the API, including many pitfalls and best practices. This post is my attempt to collect that experience in one place.

#### [TN3137: On Mac keychain APIs and implementations](https://developer.apple.com/documentation/technotes/tn3137-on-mac-keychains)

> All Apple platforms support the keychain. On iOS, tvOS, and watchOS the keychain story is very simple: There’s a single SecItem API with consistent behavior. This is not the case on macOS. The keychain on macOS has a long history, dating back to the previous millenium. This history, combined with a requirement to maintain compatibility with existing code, complicates the keychain’s design. If you don’t understand that design, you may find some of its behavior surprising.
