# Development Tips for Smart TVs

[Português](README_pt.md)

## Manufacturers and Operating System
* Samsung
    - Tizen
    - Orsay
* LG
    - webOS
    - Netcast
* Sony
    - Linux
    - Android
* Panasonic
    - Firefox OS
* Philips
* TCL
* Philco

## Overview
* Because there are multiple operating systems and different browsers, running on one TV model does not guarantee that in another model your application will work.
* Some TVs have a motion control, such as webOS. So this functionality should be implemented if you want your app to be approved in the app store.

## DOM
* Avoid using `https`.
* The use of `document.*`, `element.*`, `JSON.parse` and `XMLHttpRequest` is costly for the TV to process.
* Updating the DOM while there is an animation in progress, causes the framerate to drop dramatically. Always do one thing at a time.
* Using `.focus()` affects performance. Use CSS classes to know which element is focused.

## Images
* Try to use images in place of CSS for the properties: `border`, `background`, `box-shadow` and `gradient`, because everything that is generated via CSS, needs to be calculated, rendered and then painted.
* `opacity` and `transform` are properties that can be animated (in moderation) because they perform well on TVs.

## CSS
* Avoid using properties `grid` and `flex` because some TVs do not fully support it.