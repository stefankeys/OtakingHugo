---
title: Kissmanga Autofit Userscript
sub_title: Death to Horizontal Scrolling
Date: 2020-02-22
LastMod: 2020-02-23
type: g
---

[Back to catalog](https://otaking.xyz/index.html)

## THIS SCRIPT NO LONGER WORKS BECAUSE KISSMANGA WAS TAKEN DOWN BY COPYRIGHT VULTURES

Kissmanga has a very simple website layout which I do quite like over other sites. The only I miss from Kissmanga is rss feeds or at least email notifications for new chapters. It is perfect for reading finished manga though. One issue I have had with their website is that by default you need to scroll horizontally for full double page spread. This was especially bad for when reading [Berserk](https://otaking.xyz/berserk.html) because Miura loves double-spreads and I hate scrolling horizontally. I was fortunately able to find some orphaned userscript on the userscript static mirror site which fixes this by setting the maximum width of the page to 100%.

_Disclaimer: Kissmanga admins are known to be pretty ban happy for suspected use of adblockers and they might ban for using this script by mistaking it for an adblocker._ Personally I use adblock origin with an anti-adblock list from r/kissanime and I have had no problems with kissmanga then again I don't use the kissmanga bookmark feature so even if I were banned I would only lose access to kissmanga. I use the easy mal sync userscript/extention to automatically update my myanimelist list while I am reading.

Without further ado here is the userscript:

```
// ==UserScript==
// @name       Kissmanga autofit
// @author     Bui Thanh Nhan
// @namespace  http://nerdyweekly.com/
// @version    0.1
// @description  Make wide pages on kissmanga.com fit into your browser width. No more horizontal scrolling!
// @match      http://kissmanga.com/Manga/*
// @include /https?:\/\/(www.)?kissmanga.com\/Manga\/.+\/.+?id=[0-9]+/
// @copyright  Public domain
// ==/UserScript==

var imgs = document.getElementById('divImage').getElementsBytypeName('p');
for (var i = 0; i < imgs.length; i++) {
    var img = imgs[i].getElementsBytypeName('img')[0];
    img.style['max-width'] = '100%';
}
```

Just copy and paste it into your userscript extension of your choice. I recommend violentmonkey on chrome/firefox and greasemonkey on the Pale Moon browser. Both extensions are open source.

I know it is ironic that this page has horizontal scrolling on smaller windows. It is not responsive.
