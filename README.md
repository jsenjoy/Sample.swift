# Sample.swift

[![Build status][ci-image]][ci-url]
[![Coverage][codecov-image]][codecov-url]
[![Carthage compatible][carthage-image]][carthage-url]

[ci-image]: https://img.shields.io/travis/jsenjoy/Sample.swift/master.svg?style=flat-square
[ci-url]: https://travis-ci.org/jsenjoy/Sample.swift
[codecov-image]: https://img.shields.io/codecov/c/github/jsenjoy/Sample.swift/master.svg?style=flat-square
[codecov-url]: https://codecov.io/github/jsenjoy/Sample.swift
[carthage-image]: https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat-square
[carthage-url]: https://github.com/Carthage/Carthage

A simple node-like file operation library with swift.

## Requirements

- iOS 8.4
- Xcode 7.3 (Swift 2.2)

## Installation

### Using [Carthage](https://github.com/Carthage/Carthage)

Add `github "jsenjoy/Sample.swift"` to `Cartfile` in your project and run `carthage update --platform iOS`.

If unfamiliar with Carthage then checkout their [Getting Started section](https://github.com/Carthage/Carthage#getting-started) or this [sample app](https://github.com/ankurp/DollarCarthageApp)

Then add `import Sample` to the top of the files using Sample.swift.

### Manually

Download the file [`Sample.swift`](Sample/Sample.swift) and then add to your project.

## Usage

```swift
do {
  let content = try Sample.readFile(path)
  print(content)
} catch {}
```

## APIs

- `access(path: String, mode: Int)`
- `appendFile(filename: String, data: String)`
- `chmod(path: String, mode: Int)`
- `chmod(path: String, mode: String)`
- `chown(path: String, uid: Int, gid: Int)`
- `mkdir(path: String)`
- `stat(path: String) -> [String: AnyObject]`
- `exists(path: String) -> Bool`
- `readdir(path: String) -> [String]`
- `readFile(file: String) -> String`
- `writeFile(file: String, data: String)`
- `rename(path: String, another: String)`
- `rmdir(path: String)`
- `unlink(path: String)`

## License

Sample.swift is released under an MIT license. See the LICENSE file for more information.
