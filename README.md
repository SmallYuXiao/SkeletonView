![](Assets/header2.jpg)

<p align="center">
    <a href="https://travis-ci.org/Juanpe/SkeletonView">
      <img src="https://img.shields.io/travis/Juanpe/SkeletonView.svg">
    </a>
    <a href="https://instagram.github.io/IGListKit/">
        <img src="https://img.shields.io/cocoapods/p/SkeletonView.svg" alt="Platforms">
    </a>
    <img src="https://img.shields.io/badge/Swift-4.2-orange.svg" />
    <a href="https://cocoapods.org/pods/SkeletonView">
        <img src="https://img.shields.io/cocoapods/v/SkeletonView.svg" alt="CocoaPods" />
    </a>
    <a href="https://github.com/Carthage/Carthage">
        <img src="https://img.shields.io/badge/carthage-compatible-4BC51D.svg?style=flat" alt="Carthage" />
    </a>
    <a href="https://cocoapods.org/pods/SkeletonView">
        <img src="https://img.shields.io/cocoapods/dt/SkeletonView.svg?style=flat" alt="CocoaPods downloads" />
    </a>
    <a href="https://twitter.com/JuanpeCatalan">
        <img src="https://img.shields.io/badge/contact-@JuanpeCatalan-blue.svg?style=flat" alt="Twitter: @JuanpeCatalan" />
    </a>
    <a href="https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=MJ4Y2D9DEX6FL&lc=ES&item_name=SkeletonView&currency_code=EUR&bn=PP%2dDonationsBF%3abtn_donate_SM%2egif%3aNonHosted">
        <img src="https://img.shields.io/badge/Donate-PayPal-green.svg" alt="Paypal" />
    </a>
    <a href="https://twitter.com/intent/tweet?text=Wow%20This%20library%20is%20awesome:&url=https%3A%2F%2Fgithub.com%2FJuanpe%2FSkeletonView">
      <img src="https://img.shields.io/twitter/url/https/github.com/Juanpe/SkeletonView.svg?style=social" alt="License" />
    </a>
    <a href="https://twitter.com/JuanpeCatalan">
      <img src="https://img.shields.io/twitter/follow/JuanpeCatalan.svg?style=social&label=Follow" alt="Twitter" />
    </a>
</p>

🌎  Translations: </br>
[🇨🇳](https://github.com/Juanpe/SkeletonView/blob/master/README_zh.md) by [@WhatsXie](https://twitter.com/WhatsXie) </br>
[🇧🇷](https://github.com/Juanpe/SkeletonView/blob/master/README_pt-br.md) by [@brunomunizaf](https://twitter.com/brunomuniz_af)

今天，几乎所有的应用程序都有异步流程，例如Api请求，长时间运行的流程等。虽然流程正在运行，但通常开发人员会设置一个加载视图来向用户显示正在发生的事情

```SkeletonView``` 已经构想出来满足这种需求，这是一种优雅的方式，向用户展示正在发生的事情，并为他们准备等待的内容做好准备。

Enjoy it! 🙂

* [Features](#-features)
* [Requirements](#-supported-os--sdk-versions)
* [Guides](#-guides)
* [Example Project](#-example)
* [Installation](#-installation)
  * [Cocoapods](#using-cocoapods)
  * [Carthage](#using-carthage)
* [How to use](#-how-to-use)
  * [Collections](#-collections)
  * [Multiline text](#-multiline-text)
  * [Custom colors](#-custom-colors)
  * [Appearance](#-appearance)
  * [Custom animations](#-custom-animations)
  * [Hierarchy](#-hierarchy)
  * [Debug](#-debug)
* [Documentation](#-documentation)
* [Next steps](#-next-steps)
* [Contributing](#-contributing)
* [Mentions](#-mentions)
* [Author](#-author)
* [License](#-license)


## 🌟 Features

- [x] 使用方便
- [x] 所有UIView都是骷髅
- [x] 完全可定制
- [x] 通用（iPhone和iPad）
- [x] Interface Builder友好
- [x] 简单的Swift语法
- [x] 轻量级可读代码库

### 📋 支持的操作系统和SDK版本

* iOS 9.0+
* tvOS 9.0+
* Swift 4.2

### 🎬 Guides

 [<img src="Assets/thumb_getting_started.png">](https://youtu.be/75kgOhWsPNA)

### 🔮 Example

要运行示例项目，请克隆repo并运行SkeletonViewExample目标。

## 📲 Installation

#### Using [CocoaPods](https://cocoapods.org)

编辑Podfile并指定依赖项：

```ruby
pod "SkeletonView"
```

#### Using [Carthage](https://github.com/carthage)

Edit your `Cartfile` and specify the dependency:

```bash
github "Juanpe/SkeletonView"
```

## 🐒 How to use

使用SkeletonView只需要3个步骤：

**1.** 在适当的位置导入SkeletonView。
```swift
import SkeletonView
```

**2.** 现在，设置哪些视图将是可骨架的。您可以通过两种方式实现此目标

**使用代码：:**
```swift
avatarImageView.isSkeletonable = true
```
**使用IB / Storyboards:**

![](Assets/storyboard.png)

**3.** 设置视图后，您可以显示骨架。为此，您有4种选择：

```swift
(1) view.showSkeleton()                 // Solid
(2) view.showGradientSkeleton()         // Gradient
(3) view.showAnimatedSkeleton()         // Solid animated
(4) view.showAnimatedGradientSkeleton() // Gradient animated
```

**Preview**

<table>
<tr>
<td width="25%">
<center>Solid</center>
</td>
<td width="25%">
<center>Gradient</center>
</td>
<td width="25%">
<center>Solid Animated</center>
</td>
<td width="25%">
<center>Gradient Animated</center>
</td>
</tr>
<tr>
<td width="25%">
<img src="Assets/solid.png"></img>
</td>
<td width="25%">
<img src="Assets/gradient.png"></img>
</td>
<td width="25%">
<img src="Assets/solid_animated.gif"></img>
</td>
<td width="25%">
<img src="Assets/gradient_animated.gif"></img>
</td>
</tr>
</table>

> **重要！**
>>SkeletonView是递归的，因此如果要在所有可骨架视图中显示骨架，只需要在主容器视图中调用show方法。例如，使用UIViewControllers

### 🌿 Collections

 现在，SkeletonView与UITableView和UICollectionView兼容。

###### UITableView

如果要在UITableView中显示骨架，则需要符合SkeletonTableViewDataSource协议。

``` swift
public protocol SkeletonTableViewDataSource: UITableViewDataSource {
    func numSections(in collectionSkeletonView: UITableView) -> Int
    func collectionSkeletonView(_ skeletonView: UITableView, numberOfRowsInSection section: Int) -> Int
    func collectionSkeletonView(_ skeletonView: UITableView, cellIdentifierForRowAt indexPath: IndexPath) -> ReusableCellIdentifier
}
```
如您所见，此协议继承自UITableViewDataSource，因此您可以使用框架协议替换此协议。

该协议具有默认实现：

``` swift
func numSections(in collectionSkeletonView: UITableView) -> Int
// Default: 1
```

``` swift
func collectionSkeletonView(_ skeletonView: UITableView, numberOfRowsInSection section: Int) -> Int
// Default:
// It calculates how many cells need to populate whole tableview
```

为了让Skeleton知道单元标识符，您只需要实现一种方法。此方法没有默认实现：
 ``` swift
 func collectionSkeletonView(_ skeletonView: UITableView, cellIdentifierForRowAt indexPath: IndexPath) -> ReusableCellIdentifier
 ```

**例, 例子**
 ``` swift
 func collectionSkeletonView(_ skeletonView: UITableView, cellIdentifierForRowAt indexPath: IndexPath) -> ReusableCellIdentifier {
    return "CellIdentifier"
}
 ```

> **IMPORTANT!**
> 重要！如果您使用可调整大小的单元格（tableView.rowHeight = UITableViewAutomaticDimension），则必须定义estimatedRowHeight。

###### UICollectionView

For ```UICollectionView```, you need to conform to ```SkeletonCollectionViewDataSource``` protocol.

``` swift
public protocol SkeletonCollectionViewDataSource: UICollectionViewDataSource {
    func numSections(in collectionSkeletonView: UICollectionView) -> Int
    func collectionSkeletonView(_ skeletonView: UICollectionView, numberOfItemsInSection section: Int) -> Int
    func collectionSkeletonView(_ skeletonView: UICollectionView, cellIdentifierForItemAt indexPath: IndexPath) -> ReusableCellIdentifier
}
```

对于UICollectionView，您需要符合SkeletonCollectionViewDataSource协议。

### 📰 多行文字


![](Assets/multilines2.png)

使用带有文本的元素时，SkeletonView会绘制线条来模拟文本。此外，您可以决定您想要多少行。如果numberOfLines设置为零，它将计算填充整个骨架所需的行数，并将绘制它。相反，如果将其设置为一，二或任何大于零的数字，它将只绘制此行数。


##### 🎛 定制、自定义

您可以为多行元素设置一些属性。


| Property | Values | Default | Preview
| ------- | ------- |------- | -------
| 填写最后一行的百分比。 | `0...100` | `70%` | ![](Assets/multiline_lastline.png)
| 拐角半径。 （新） | `0...10` | `0` | ![](Assets/multiline_corner.png)



要使用代码修改百分比或半径，请设置属性：
```swift
descriptionTextView.lastLineFillPercent = 50
descriptionTextView.linesCornerRadius = 5
```

或者，如果您更喜欢使用IB / Storyboard：

![](Assets/multiline_customize.png)

### 🎨 自定义颜色

您可以决定骨架着色的颜色。您只需要将所需的颜色或渐变作为参数传递。

**使用纯色**
``` swift
view.showSkeleton(usingColor: UIColor.gray) // Solid
// or
view.showSkeleton(usingColor: UIColor(red: 25.0, green: 30.0, blue: 255.0, alpha: 1.0))
```
**使用渐变**
``` swift
let gradient = SkeletonGradient(baseColor: UIColor.midnightBlue)
view.showGradientSkeleton(usingGradient: gradient) // Gradient
```

此外，SkeletonView还有20种平面颜色🤙🏼

```UIColor.turquoise, UIColor.greenSea, UIColor.sunFlower, UIColor.flatOrange  ...```

![](Assets/flatcolors.png)
###### 从网站捕获的图像 [https://flatuicolors.com](https://flatuicolors.com)

### 🦋 Appearance

**NEW** 新骨架具有默认外观。因此，当您未指定颜色，渐变或多线属性时，SkeletonView将使用默认值。

Default values:
- **tintColor**: UIColor
    - *default: .clouds*
- **gradient**: SkeletonGradient
  - *default: SkeletonGradient(baseColor: .clouds)*
- **multilineHeight**: CGFloat
  - *default: 15*
- **multilineSpacing**: CGFloat
  - *default: 10*
- **multilineLastLineFillPercent**: Int
  - *default: 70*
- **multilineCornerRadius**: Int
  - *default: 0*

要获取这些默认值，您可以使用SkeletonAppearance.default。使用此属性您也可以设置值：
```Swift
SkeletonAppearance.default.multilineHeight = 20
SkeletonAppearance.default.tintColor = .green
```


### 🤓 自定义动画

```SkeletonView``` 有两个内置动画，固体骨架脉冲和渐变滑动
此外，如果你想做自己的骨架动画，那真的很容易。


Skeleton提供showAnimatedSkeleton函数，该函数具有SkeletonLayerAnimation闭包，您可以在其中定义自定义动画。

```swift
public typealias SkeletonLayerAnimation = (CALayer) -> CAAnimation
```

您可以像这样调用函数：:

```swift
view.showAnimatedSkeleton { (layer) -> CAAnimation in
  let animation = CAAnimation()
  // Customize here your animation

  return animation
}
```

它是可用的SkeletonAnimationBuilder。它是制作SkeletonLayerAnimation的构建器。

今天，您可以为渐变创建滑动动画，确定方向并设置动画的持续时间（默认值= 1.5秒）

```swift
// func makeSlidingAnimation(withDirection direction: GradientDirection, duration: CFTimeInterval = 1.5) -> SkeletonLayerAnimation

let animation = SkeletonAnimationBuilder().makeSlidingAnimation(withDirection: .leftToRight)
view.showAnimatedGradientSkeleton(usingGradient: gradient, animation: animation)

```

```GradientDirection``` is an enum, with this cases:

|  Direction | Preview
|------- | -------
| .leftRight | ![](Assets/sliding_left_to_right.gif)
| .rightLeft | ![](Assets/sliding_right_to_left.gif)
| .topBottom | ![](Assets/sliding_top_to_bottom.gif)
| .bottomTop | ![](Assets/sliding_bottom_to_top.gif)
| .topLeftBottomRight | ![](Assets/sliding_topLeft_to_bottomRight.gif)
| .bottomRightTopLeft | ![](Assets/sliding_bottomRight_to_topLeft.gif)

> **😉 TRICK!**
Exist another way to create sliding animations, just using this shortcut:
>>```let animation = GradientDirection.leftToRight.slidingAnimation()```

### 👨‍👧‍👦 Hierarchy

Since ```SkeletonView``` is recursive, and we want skeleton to be very efficient, we want to stop recursion as soon as possible. For this reason, you must set the container view as `Skeletonable`, because Skeleton will stop looking for `skeletonable` subviews as soon as a view is not Skeletonable, breaking then the recursion.

Because an image is worth a thousand words:

> ```ìsSkeletonable```= ☠️

| Configuration | Result
|------- | -------
|![](Assets/no_skeletonable.png) | ![](Assets/no_skeletonables_result.png)
|![](Assets/container_no_skeletonable.png) | ![](Assets/no_skeletonables_result.png)
|![](Assets/container_skeletonable.png) | ![](Assets/container_skeletonable_result.png)
|![](Assets/all_skeletonables.png) | ![](Assets/all_skeletonables_result.png)


### 🔬 Debug

**NEW** In order to facilitate the debug tasks when something is not working fine. `SkeletonView` has some new tools.

First, `UIView` has available a new property with his skeleton info:
```swift
var skeletonDescription: String

```
The skeleton representation looks like this:

![](Assets/debug_description.png)

Besides, you can activate the new **debug mode**. You just add the environment variable `SKELETON_DEBUG` and activate it.

![](Assets/debug_mode.png)

Then, when the skeleton appears, you can see the view hierarchy in the Xcode console.

<details>
<summary>Open to see an output example </summary>
<img src="Assets/hierarchy_output.png" />
</details>



### 📚 Documentation
Coming soon...😅

## 📬 Next steps

* [x] Set the filling percent of the last line in multiline elements
* [x] Add more gradient animations
* [x] Supported resizable cells
* [x] CollectionView compatible
* [x] tvOS compatible
* [x] Add recovery state
* [x] Custom default appearance
* [x] Debug mode
* [ ] Custom collections compatible
* [ ] Add animations when it shows/hides the skeletons
* [ ] MacOS and WatchOS compatible

## ❤️ Contributing
This is an open source project, so feel free to contribute. How?
- Open an [issue](https://github.com/Juanpe/SkeletonView/issues/new).
- Send feedback via [email](mailto://juanpecatalan.com).
- Propose your own fixes, suggestions and open a pull request with the changes.

See [all contributors](https://github.com/Juanpe/SkeletonView/graphs/contributors)

###### Project generated with [SwiftPlate](https://github.com/JohnSundell/SwiftPlate)

## 📢 Mentions

- [iOS Dev Weekly #327](https://iosdevweekly.com/issues/327#start)
- [Hacking with Swift Articles](https://www.hackingwithswift.com/articles/40/skeletonview-makes-loading-content-beautiful)
- [Top 10 Swift Articles November](https://medium.mybridge.co/swift-top-10-articles-for-the-past-month-v-nov-2017-dfed7861cd65)
- [30 Amazing iOS Swift Libraries (v2018)](https://medium.mybridge.co/30-amazing-ios-swift-libraries-for-the-past-year-v-2018-7cf15027eee9)
- [AppCoda Weekly #44](http://digest.appcoda.com/issues/appcoda-weekly-issue-44-81899)
- [iOS Cookies Newsletter #103](https://us11.campaign-archive.com/?u=cd1f3ed33c6527331d82107ba&id=48131a516d)
- [Swift Developments Newsletter #113](https://andybargh.com/swiftdevelopments-113/)
- [iOS Goodies #204](http://ios-goodies.com/post/167557280951/week-204)
- [Swift Weekly #96](http://digest.swiftweekly.com/issues/swift-weekly-issue-96-81759)
- [CocoaControls](https://www.cocoacontrols.com/controls/skeletonview)
- [Awesome iOS Newsletter #74](https://ios.libhunt.com/newsletter/74)



## 👨🏻‍💻 Author
[1.1]: http://i.imgur.com/tXSoThF.png
[1]: http://www.twitter.com/JuanpeCatalan

* Juanpe Catalán [![alt text][1.1]][1]

<a class="bmc-button" target="_blank" href="https://www.buymeacoffee.com/CDou4xtIK"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy me a coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;"><span style="margin-left:5px"></span></a>

## 👮🏻 License

```
MIT License

Copyright (c) 2017 Juanpe Catalán

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
