# Universal Links

[Preflight possible universal links before opening SFSafariController](https://recoursive.com/2019/02/22/preflight_universal_links/)

> Before you open a URL in SFSafariController or any other browser, you should check if it’s a universal link, 
> and if so, open it in the respective native app instead. 
> It’s a good way to improve the user experience since SFSafariController will not trigger universal links on open.

```swift
let url = URL(string: "https://youtu.be/k0kSc8hHzAM?t=1461")!
UIApplication.shared.open(url, options: [.universalLinksOnly: true]) { (success) in
    if !success {
        // not a universal link or app not installed
        let vc = SFSafariViewController(url: url)
        self.present(vc, animated: true)
    }
}
```
