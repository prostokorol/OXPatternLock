# OXPatternLock
An iOS pattern lock like Android authentication written in Swift.

<img src="https://github.com/oxozle/OXPatternLock/raw/master/assets/ox-pattern-lock.gif">

## Installation
OXPatternLock requires Swift 3.0 and Xcode 8

### Manually
Add [OXPatternLock.swift](https://github.com/oxozle/OXPatternLock/blob/master/Source/OXPatternLock.swift) to your project in Xcode  

### CocoaPods

[CocoaPods](http://cocoapods.org) is a dependency manager for Cocoa projects. You can install it with the following command:

```bash
$ gem install cocoapods
```

To integrate OXPatternLock into your Xcode project using CocoaPods, specify it in your `Podfile`:

```ruby
source 'https://github.com/CocoaPods/Specs.git'
platform :ios, '9.0'
use_frameworks!

target '<Your Target Name>' do
	# for stable release
    pod 'OXPatternLock'

    # for latest release
    pod 'OXPatternLock', :git => 'https://github.com/oxozle/OXPatternLock.git', :branch => 'master'
end
```

Then, run the following command:

```bash
$ pod install
```

## Usage

1. Create an implementation of the `OXPatternLockDelegate` protocol.

2. Add `OXPatternLock` to your Storyboard/xib file or create it manually.

```swift
func didPatternInput(patterLock: OXPatternLock, track: [Int]) {
  //store, check and update patter with track array
}
```

### Interface Builder support

There is support for Interface Builder. All properties configurable from Interface Builder.

<img src="https://github.com/oxozle/OXPatternLock/raw/master/assets/interface-builder.jpg"> <img src="https://github.com/oxozle/OXPatternLock/raw/master/assets/properties.png">

## Customisation

The locker can be customized by setting any of the following public properties before displaying the OXPatternLock. The defaults are shown below.

| Property | Description |
--- | ---
**dot**: UIImage | Default dot image in grid
**dotSelected**: UIImage | Selected icon
**lockSize**: Int | Width and Height of grid. Default value is 3 (grid 3x3 size).
**trackLineColor**: UIColor | Track line highlight color. Default value is White.
**trackLineThickness**: CGFloat | Thickness of track line. Default value is 5.


## Known Issues

If you find any bugs please create an issue on Github.

## <a name="license">License</a>

OXPatternLock is available under [the MIT license][license].

[license]:      https://github.com/oxozle/OXPatternLock/blob/master/LICENSE
