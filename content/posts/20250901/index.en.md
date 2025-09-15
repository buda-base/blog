+++
date = '2025-09-01T10:52:53+02:00'
draft = false
title = 'A little app for sorting Tibetan alphabetically'
tags = []
slug = 'tibetan-alphabetical-order'
categories = []
#ShowShareButtons = true
[params]
  author = ['Elie Roux']
  post_meta = ["author", "date", "categories", "translations"]
  showtoc = false
  tocopen = true

[cover]
    image = "Screenshot.png"
    caption = "The new minimalistic app"


+++

BDRC just released a minimalistic page to sort Tibetan in alphabetical order, in Unicode or Wylie:

https://buda-base.github.io/tibetan-sort-js/

The app has very limited functionality but the possibilities to sort Tibetan very simply and online are very sparse[^1] so we thought it would benefit our users to release it!

Any feedback can be given on [the issue tracker](https://github.com/buda-base/tibetan-sort-js/issues).

### An old problem

Sorting Tibetan automatically is something that was worked on as early as the 1980s, long before Tibetan Unicode was normalized. The earliest documented project was led by Yoshiro Imaeda (then working for the French CNRS) in Bhutan in the late 80s. Among other things, the project set up a [4th Dimension](https://en.wikipedia.org/wiki/4th_Dimension_(software)) database for the catalog of the National Library of Bhutan, which included alphabetical sorting as a feature.

{{< figure
    src="Kuensel_English.jpg"
    caption="Excerpt from the Bhutanese newspaper Kuensel, July 9 1988, picture kindly provided by Yoshiro Imaeda. The article mentions alphabetical order as a feature at the time."
>}}

### A solved problem?

Tibetan alphabetical order then remained a niche feature, with some specialized software (like the BDRC website!) being able to sort alphabetically, but most general software giving very poor results. 

Fast forward 33 years, the standard way for softwares to sort alphabetically is now to use the data from the [Common Locale Data Repository](https://cldr.unicode.org/). In 2021, BDRC contributed so-called collation rules for Tibetan[^2] and in theory solved the problem for everyone. The collation rules were shipped in all major software that can now sort in Tibetan!

Except... that's unfortunately not the case. A good example of why not is the case of Chrome, which chooses to exclude Tibetan support to reduce the download size[^3]. Fortunately the collation rules made it in recent LibreOffice and can now be used, see the [dedicated blog post](../sorting-tibetan-in-libreoffice/).

It thus seems to be the case that sorting Tibetan alphabetically will continue to require some specialized apps for some time, and we hope ours can fill the gap! We will continue to push for better Tibetan support in widely used software as much as we can.

[^1]: The [ICU collation demo](https://icu4c-demos.unicode.org/icu-bin/collation.html) is one of them if you select "bo" in the dropdown in the top left corner

[^2]: See related [blog entry on BDRC](https://www.bdrc.io/blog/2021/10/29/sorting-out-tibetan-alphabetical-order/)

[^3]: See [Chrome issue 40898842](https://issues.chromium.org/issues/40898842)

[^4]: See [LibreOffice issue 168225](https://bugs.documentfoundation.org/show_bug.cgi?id=168225)