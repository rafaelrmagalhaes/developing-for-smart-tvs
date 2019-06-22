## Overview
Welcome and hope these information can be helpful to you. We placed some tips and tricks for our experience around three years developing for Smart TV applications.

Play with Smart TVs should be fun, if you like to be challenged. There are a lot of devices, with different operating systems, browsers engines and hardware level. Keep in mind that you will create applications running on these low end devices, with hardware limitations and obsolete operating systems.

Some devices have motion control support, such as webOS (LG operating system). This is a mandatory functionality so you need to support it to be approved in the app store. In the same way, Samsung has mandatory functionalities, like multitasking.

## Keep Track
[Get Started](GETTING_STARTED.md)

#### About TVs Manufacturers
[LG](LG.md)

## Ecosystem
| Manufacturer  | Operating System | Web Engine |
| ------------- | ---------------- | ------- |
| Samsung | Tizen¹ | - |
| Samsung | Orsay¹ | - |
| LG | webOS | Chromium / WebKit 538.2- |
| LG | NetCast | WebKit 537.1- |
| Sony | Linux | - |
| Sony | Android | - |
| Panasonic | Firefox OS | - |
| Philips | NetRange | - |
| TCL | NetRange | - |
| Philco | NetRange | - |

`¹ - Linux based OS`

## Be careful with
* `https`: You will play with low end and old devices. It means obsolate software with low resources, and these devices usually doesn't play well with encryptation.
* DOM level APIs: like `document.*`, `element.*`, `JSON.parse` and `XMLHttpRequest`, it costs for the TV to process.
* DOM update: avoid updates when there is an animation in progress, it causes the framerate dropping dramatically. Always do one thing at a time.
* `.focus()`: It affects performance. Use CSS classes to know which element is focused.

## Images
* Try to use images in place of CSS for the properties: `border`, `background`, `box-shadow` and `gradient`, because everything that is generated via CSS, needs to be calculated, rendered and then painted.
* `opacity` and `transform` are properties that can be animated (in moderation) because they perform well on TVs.
* Export your images with low quality, we can say to you that 40% is enough. Users will use your application a little bit far from the TV.

## CSS
* Avoid using properties `grid` and `flex` because some TVs do not fully support it.
