# Road to Python
A collection of wild things I stumbled across that made me go 🤩 or 🤯

### [Why would you use `NotImplemented` instead of `NotImplementedError`?](https://stackoverflow.com/a/879005/1112611)
`NotImplemented` signals to the runtime that it should ask someone else to satisfy the operation. In the expression  `a == b`, if `a.__eq__(b)` returns  `NotImplemented`, then Python tries `b.__eq__(a)`. If `b` knows enough to return `True` or `False`, then the expression can succeed. If it doesn't, then the runtime will fall back to the built-in behavior (which is based on identity for `==` and `!=`)

### [@staticmethod is messing up my `super()` calls](https://stackoverflow.com/questions/26788214/super-and-staticmethod-interaction)
What most people are expecting when they see `super(X)` is what Python gives you if you do `super(X, X)`.

### [What's a pythonic replacement for switch/case in Python](https://stackoverflow.com/questions/60208/replacements-for-switch-statement-in-python)
From simple dictionary with `.get()` method to really creative ideas like a context manager. [Here's one more method](http://code.activestate.com/recipes/410692/)
