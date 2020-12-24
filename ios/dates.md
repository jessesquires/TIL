# iOS Dates

[How expensive is `DateFormatter`?](https://sarunw.com/posts/how-expensive-is-dateformatter/)

> The key take away from all these stats are:
>
> 1. `DateFormatter` is expensive to create.
> 1. `DateFormatter` is expensive to change.
> 1. Subsequent use of `string(from: Date)` is cheap.
> 1. Subsequent use of `date(from: String)` **is not** cheap.
