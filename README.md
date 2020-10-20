# TouchVisualizer - SPM Fork

TouchVisualizer is a lightweight pure Swift implementation for visualising touches on the screen. This is a fork built for implementation with SPM.  Everything not relevant to the package install has been removed.

## Features
- Works with just **a single line of code**!
- Supports multiple fingers.
- Supports multiple `UIWindow`'s.
- Displays touch radius (finger size).
- Displays touch duration.
- Customise the finger-points image and colour.
- Supports iPhone and iPad in both portrait and landscape mode.


## Installation and Setup



## Usage

To start using TouchVisualizer, write the following line wherever you want to start visualising:

```swift
import TouchVisualizer
```

Then invoke visualisation, by calling:

```swift
Visualizer.start()
```

and stop the presentation like this:

```swift
Visualizer.stop()
```
Get touch locations by this:

```swift
Visualizer.getTouches()
```

It is really simple, isn't it?

## Customisation

TouchVisualizer also has the ability to customize your touch events. Here is an example of what can be customized:

```swift
var config = Configuration()
config.color = UIColor.redColor()
config.image = UIImage(named: "YOUR-IMAGE")
config.showsTimer = true
config.showsTouchRadius = true
config.showsLog = true
Visualizer.start(config)
```

### Configuration properties

|name|type|description|default|
|:----|:----|:----|:----|
| color | `UIColor` | Color of touch point and text. | default color |
| image | `UIImage` | Touch point image. If rendering mode is set to  `UIImageRenderingModeAlwaysTemplate`, the image is filled with color above. | circle image |
| defaultSize| `CGSize` | Default size of touch point.| 60 x 60px |
| showsTimer| `Bool` | Shows touch duration. | false |
| showsTouchRadius | `Bool` | Shows touch radius by scaling touch point. It doesn't work on simulator. | false |
| showsLog | `Bool` | Shows log. | false |

## Documentation
### Peripheral

- [How to take an iOS screen movie](misc/take_a_movie.md)

### Presentation

- [TouchVisualizer Demo movie #potatotips // Speaker Deck](https://speakerdeck.com/morizotter/touchvisualizer-demo-movie-number-potatotips) @potatotips May 13 2015

## Contributing

Please file issues or submit pull requests for anything you’d like to see! We're waiting! :)

## Licensing
TouchVisualizer is released under the MIT license. Go read the LICENSE file for more information.
#### Miscellaneous
There is a similar *touch visualization* library called [COSTouchVisualizer](https://github.com/conopsys/COSTouchVisualizer), which is written in Objective-C. [COSTouchVisualizer](https://github.com/conopsys/COSTouchVisualizer) supports earlier versions of iOS and is more mature. If TouchVisualizer isn't enough for you, try that!
