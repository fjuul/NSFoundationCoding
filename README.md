# Swift NSDict Encoder
A encoder for serializing Swift objects to NSDictionaries. Created from the Swift standard library `PropertyListEncoder` by removing the binary conversion components and adding support for converting dates to strings using a custom `DateFormatter`.

## Usage

```
import Foundation

struct UserDetails {
  var name: String
  var birthDate: Date
}

let profile = UserDetails(name: "Frank", birthDay: Date())

let dictEncoder = NSDictionaryEncoder.init()
let profileDict: NSDictionary = try dictEncoder.encode(profile)
```
