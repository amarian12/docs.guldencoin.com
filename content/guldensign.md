---
title: "guldensign"
date: "2014-07-06"
groups: ['other']
groups_weight: 10
---

The guldensign is a valuta sign like the dollar sign `$` and euro sign `€`. 
Because the Guldencoin valuta sign is not a UTF-8 character, a drop-in css 'workarround' has been created for websites. The character <span style='font-family:"proxima-nova", "HelveticaNeue-Light", "Helvetica Neue Light", "Helvetica Neue", Helvetica, Arial, "Lucida Grande", sans-serif !important;'>Ġ</span> is displayed as a Guldencoin valuta sign: Ġ

When using the Ġ sign, there's no need to add a space between the sign and the amount. Example: Ġ100.50


## Usage

To use the guldensign in websites, include the guldensign.css file into your html and use the <span style='font-family:"proxima-nova", "HelveticaNeue-Light", "Helvetica Neue Light", "Helvetica Neue", Helvetica, Arial, "Lucida Grande", sans-serif !important;'>Ġ</span> character. Alternatively, use the html character code `&Gdot;` or `&#288;`.

To include the guldensign.css file, either download the [latest files](https://github.com/nlgcoin/guldensign/archive/master.zip) from the [github repository](https://github.com/nlgcoin/guldensign) and include them in your source tree. Then include guldensign.css in your html.
Or simply use the [cdn](/services/cdn) to include guldensign.css:
{{% highlight html %}}
<link rel="stylesheet" type="text/css" href="//nlgcdn.com/guldensign/1/guldensign.css" />
{{% /highlight %}}

To display a <span style='font-family:"proxima-nova", "HelveticaNeue-Light", "Helvetica Neue Light", "Helvetica Neue", Helvetica, Arial, "Lucida Grande", sans-serif !important;'>Ġ</span> in your webpage as the guldensign, add `guldensign` as the first option in the font-family in your css. Example:
{{% highlight css %}}
body {
	font-family: guldensign, Arial, Helvetica, sans-serif;
}
{{% /highlight %}}

Or, to add a single guldensign as icon, use the class `guldensign`:
{{% highlight html %}}
<i class="guldensign" ></i>
{{% /highlight %}}

These documentation pages (docs.guldencoin.com) have guldensign.css included.

Overriding the effect (giving you back the original <span style='font-family:"proxima-nova", "HelveticaNeue-Light", "Helvetica Neue Light", "Helvetica Neue", Helvetica, Arial, "Lucida Grande", sans-serif !important;'>Ġ</span>) is possible by adding a style attribute directly on an element and setting the font-family.


## Credits
The guldensign font files are created with [fontforge](http://fontforge.org/) and [FontSquirrel's webfont tool](http://www.fontsquirrel.com/tools/webfont-generator).
