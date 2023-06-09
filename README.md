### Hi there 👋

I currently work on the Developer Publications team at Apple and am currently focused on the developer user experience, such as learning and using Swift, and documentation systems.

As a former full-time Swift contributor, here are some things that I helped pioneer:

- [lib/Markup](https://github.com/apple/swift/tree/master/lib/Markup) and Markdown-style documentation comments.  
  I used the [cmark](https://github.com/apple/swift-cmark) library for parsing doc comments and an internal syntax tree to interface with the compiler.
- Reflection metadata for the [Xcode Memory Graph Debugger](https://developer.apple.com/documentation/xcode/improving_your_app_s_performance/reducing_your_app_s_memory_use/gathering_information_about_memory_use)
  - [lib/Reflection](https://github.com/apple/swift/tree/main/stdlib/public/RemoteInspection) (now RemoteInspection)
  - [SwiftRemoteMirror](https://github.com/apple/swift/blob/master/stdlib/public/SwiftRemoteMirror/SwiftRemoteMirror.cpp)
- [lib/Syntax](https://github.com/apple/swift/tree/master/lib/Syntax). 
  This was the original C++ implementation which is now removed in favor of the Swift-based [SwiftSyntax](https://github.com/apple/swift-syntax).  
  The model is an immutable tree that can share data between trees, using positional information to place the syntax in a concrete place such as a file.
- [lib/Migrator](https://github.com/apple/swift/tree/master/lib/Migrator). 
  This was a rewrite of the migrator engine which previously relied on integrating with a previous version of the Swift compiler to understand the old code.

Other things I helped create more recently:

- [Symbol Graph Documentation Format](https://github.com/apple/swift/tree/master/lib/SymbolGraphGen) and the library that implements it, [SymbolKit](https://github.com/apple/swift-docc-symbolkit).  
  This represents symbols as nodes and relationships such as "member of", "conforms to", and "subclass of". A symbol ontology, I guess.
- [Swift Markdown](https://github.com/apple/swift-markdown) and authoring experience for DocC.  
  I used a similar approach to lib/Syntax in Swift. This library also contains extensions for block directives, a block element container that allows for metadata such as key-value pairs or other information.
- [DocC](https://developer.apple.com/documentation/docc)

I post on <a rel="me" href="https://hachyderm.io/@bitjammer">Mastodon</a>.