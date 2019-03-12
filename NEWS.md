promises 1.0.1.9001
===================

- `new_promise_domain` now takes a `wrapOnFinally` argument, which can be used
  to intercept registration of `finally()`. Previous versions treated `finally`
  as passing the same callback to `then(onFulfilled=..., onRejected=...)`, and
  ignoring the result; for backward compatibility, promise domains will still
  treat `finally` that way by default (i.e. if `wrapOnFinally` is `NULL`, then
  `finally` will result in `wrapOnFulfilled` and `wrapOnRejected` being called,
  but if `wrapOnFinally` is provided then only `wrapOnFinally` will be called).


promises 1.0.1
==============

- Initial CRAN release
