# Road to Python
A collection of wild things I stumbled across that made me go 🤩 or 🤯

### [Why would you use `NotImplemented` instead of `NotImplementedError`?](https://stackoverflow.com/a/879005/1112611)
`NotImplemented` signals to the runtime that it should ask someone else to satisfy the operation. In the expression  `a == b`, if `a.__eq__(b)` returns  `NotImplemented`, then Python tries `b.__eq__(a)`. If `b` knows enough to return `True` or `False`, then the expression can succeed. If it doesn't, then the runtime will fall back to the built-in behavior (which is based on identity for `==` and `!=`)
