# gpui Tutorial

## Summary

[GPUI](https://www.gpui.rs) is a graphics processor accelerated user interface frameowork, created by the makers of [Zed](https://zed.dev) to make the fastest user interface possible, written in Rust. It's currently an [internal project](https://github.com/zed-industries/zed/tree/main/crates/gpui) in the zed project, but will soon be its own crate. It's licensed under the [Apache license](https://github.com/zed-industries/zed/blob/main/crates/gpui/LICENSE-APACHE), which makes it usable by commercial projects.

Currently there is not a lot of documentation, so this tutorial aims to take you through the basics of the framework to get started on your own project.

## Installation

To use gpui, add a reference to it in the `Cargo.toml` file:

```toml
gpui = { git = "https://github.com/zed-industries/zed" }
```

Since gpui is a part of Zed's codebase, we can borrow their setup instructions to get set up to do gpui development. Follow the instructions in the `Dependencies` section for [macOS](https://github.com/zed-industries/zed/blob/main/docs/src/development/macos.md#dependencies), [Linux](https://github.com/zed-industries/zed/blob/main/docs/src/development/linux.md#dependencies), or [Windows](https://github.com/zed-industries/zed/blob/main/docs/src/development/windows.md#dependencies). You'll ignore the other sections, but there might be troubleshooting at the bottom that will be helpful.

I used [these resources](resources.md) when learning gpui.

## Sections

* [01 Hello World](01-hello-world.md), where we learn the basics of creating a gpui app.
* [02 Likes Counter](02-likes-counter.md), where we update state when clicking a button.

To understand the basic terms, see [the dictionary](dictionary.md).

## Future Topics

* Elements
* Input Controls
* Menus
* App Icon
* CI

## Outstanding Questions

* If the `SharedString` is basically an `Arc<String>`, how does the framework avoid core contention when ensuring atomicity of the reference counter? [This article](https://blocklisted.github.io/blog/arc_str_vs_string_is_it_really_faster/) makes a good case that `Arc<string>` can be slower in some multithreaded scenarios.
