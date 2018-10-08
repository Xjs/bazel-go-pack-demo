# bazel go-pack demo

This repository doesn't build with rules_go-0.15.4 on Windows.
It does build with my [proposed fix](https://github.com/Xjs/rules_go/commit/2298baf5fbf0d75992a7c6c84bb1d4e328f1991e).
To reproduce, replace the `io_bazel_rules_go` import in `WORKSPACE` by

```
git_repository(
    name = "io_bazel_rules_go",
    remote = "https://github.com/Xjs/rules_go",
    commit = "2298baf5fbf0d75992a7c6c84bb1d4e328f1991e",
)
```
