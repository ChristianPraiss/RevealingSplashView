![Banner](/Web/banner.png)

[![Build Status](https://travis-ci.org/PiXeL16/RevealingSplashView.svg?branch=master)](https://travis-ci.org/PiXeL16/RevealingSplashView/) [![codecov.io](https://codecov.io/github/PiXeL16/RevealingSplashView/coverage.svg?branch=master)](https://codecov.io/github/PiXeL16/RevealingSplashView?branch=master) [![CocoaPods Compatible](https://img.shields.io/cocoapods/v/RevealingSplashView.svg)](https://img.shields.io/cocoapods/v/RevealingSplashView.svg) [![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/PiXeL16/RevealingSplashView/master/LICENSE)

# RevealingSplashView
A Splash view that animates and reveals its content, inspired by the `Twitter` splash.

![RevealingSplashView](/Web/revealingSplashView.gif)

:star: Features
---
* Customizable reveal icon image.
* Customizable icon image color.
* Customizable icon image size.
* Customizable background color.
* Customizable animation duration.
* Customizable animation delay.
* Several animation to choose from.
* Easy to use :wink:.

:octocat: Installation
---
Get `RevealingSplashView` on CocoaPods, just add `pod 'RevealingSplashView'` to your `Podfile` and then run `pod install`.

:metal: Usage
---
Usage is pretty easy, just initialize your `RevealingSplashView` and add it to your view. Then call `startAnimation()`:

```swift
import RevealingSplashView

override func viewDidLoad() {
        super.viewDidLoad()

        //Initialize a revealing Splash with with the iconImage, the initial size and the background color
        let revealingSplashView = RevealingSplashView(iconImage: UIImage(named: "twitterLogo")!,iconInitialSize: CGSizeMake(70, 70), backgroundColor: UIColor(rgba:"#1D8FF1"))

        //Adds the revealing splash view as a sub view
        self.view.addSubview(revealingSplashView)

        //Starts animation
        revealingSplashView.startAnimation(){
            print("Completed")
        }

    }
```

**Ideally** your `iconInitialSize` should match the size of the icon in your `LaunchScreen.storyboard`.

So it you set your constrains in your `LaunchScreen.storyboard` to be 80 `height` and 80 `width` you should set the same size as the initial size of the `RevealingSplashView`

:thumbsup: Animations Types
----
There are several animations to choose from just set the `animationType` property of the `RevealingSplashView`

### Twitter

Its the default animation that `Twitter` use for their app. ![RevealingSplashView](/Web/revealingSplashView.gif)

### Rotate Out

Similar to the `Twitter` one but rotating while zooming out.


TODO
-----
* Better code coverage
* More animations

:alien: Author
------
Chris Jimenez - http://chrisjimenez.net, [@chrisjimeneznat](http://twitter.com/chrisjimeneznat)

## License
`RevealingSplashView` is released under the MIT license. See [LICENSE](https://github.com/pixel16/RevealingSplashView/blob/master/LICENSE) for details.
