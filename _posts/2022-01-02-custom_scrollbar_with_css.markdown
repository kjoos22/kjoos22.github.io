---
layout: post
title:      "Custom Scrollbar with CSS"
date:       2022-01-03 04:49:03 +0000
permalink:  custom_scrollbar_with_css
---


Have you ever been to a website where the scroll bar looked different from normal? Have you ever thought "I wish I could make something like that on my website/project!" Well, it turns out you can! With just 3 easy CSS classes, you can customize the scrollbar in so many different ways.

The 3 required classes are:

```
body::-webkit-scrollbar {

}
```

This one is the "base" of the bar, and is most useful for setting the width of the scroll bar.

```
body::-webkit-scrollbar-track {

}
```

This one is the track or groove of the scroll bar, the part that the button slides up and down in. This is where you would want to set background colors/effects.

```
body:-webkit-scrollbar-thumb {

}
```

This one is the button within the scrollbar, the draggable button that moves up and down relative to position on the page.

Once you have these classes, you can use any CSS tricks you have up your sleve that work on single divs. Go ahead and have some fun with this and see what the craziest scroll bar you could come up with is, and once you've had your fill of insanity, see if you can come up with a realistic, but still customize scrollbar that fits your project's theme.
