# Change Log

## [1.1.0](https://github.com/Flipkart/Swifty/releases/tag/1.1.0)
Released on 2017-12-14.

Swifty now supports the `Codable` Protocol, plus adds support response mocking.

#### Added
- Adds a new `.json(encodable: encoder:)` modifier to attach `Encodable` objects into request bodies.
- Adds a new method `.loadJSON<T: Decodable>(decodable: decoder:)` to support loading `Decodable` objects from network responses directly.
- Adds a new `.mock(withFile: OfType)` modifier to mock responses of requests using files in the main bundle.
- Tests for Codable Support & Response Mocking.

#### Fixed
- The `creationError` property in `NetworkResource` is now public, so that it can be utilized by a user's custom extensions.

## [1.0.2](https://github.com/Flipkart/Swifty/releases/tag/1.0.2)
Released on 2017-11-17.

#### Fixed
- Simpler logic for Query Preservation in `BaseResource` modifiers

## [1.0.1](https://github.com/Flipkart/Swifty/releases/tag/1.0.1)
Released on 2017-10-31.

#### Fixed
- Improved Query Preservation in `BaseResource` modifiers

## [1.0.0](https://github.com/Flipkart/Swifty/releases/tag/1.0.0)
Released on 2017-10-31.

#### Breaking
- Swifty 1.0.0 is now written in Swift 4

#### Added
- Support for macOS, watchOS & tvOS
- More Tests

#### Fixed
- `BaseResource` modifiers now preserve query params if present

## [0.9.3](https://github.com/Flipkart/Swifty/releases/tag/0.9.3)
Released on 2017-10-02.

#### Added
- JSON Parsing Interceptor now also parses the JSON returned in an error response, and puts the results into the NSError's `userInfo` property
- Added new Tests for JSON Parsing, Server Error Codes, Empty Response Codes
- Updated Example Project according to Xcode 9 Recommendations

#### Fixed
- Response Validation Error now carries over the HTTP Error Code (if available) as it's error code
- Fixed major issue in which the Response Validation logic might fallthrough incorrectly
- `.loadJSON()` now handles Empty Responses properly

## [0.9.2](https://github.com/Flipkart/Swifty/releases/tag/0.9.2)
Released on 2017-09-20.

#### Added
- New `.authorizationHeader()` modifier to add a Basic Hidden HTTP `Authorization` header to a resource
- Support for chaning multiple `.query()` methods on a resource
- Tests for `WebService` Modifiers

#### Fixed
- Bug due to which `NetworkResourceWithBody` methods could not be chained after using a `NetworkResource` modifier due to return type ambiguity

## [0.9.1](https://github.com/Flipkart/Swifty/releases/tag/0.9.1)
Released on 2017-09-13.

#### Fixed
- Swifty Inspector's table view reload being called on a background thread

## [0.9.0](https://github.com/Flipkart/Swifty/releases/tag/0.9.0)
Released on 2017-09-12.

#### Added
- Initial release of Swifty.