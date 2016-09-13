# 2of5-font

the 2of5 font is a barcode font encoding the interleaved 2of5 barcode standard.


## available sizes

The font is available in 5 different height to width ratios.
(Usually i use code39_XL)

if you need other height to width ratios, you can generate your own font using the [barcode font generator](https://github.com/Holger-Will/barcode-font-generator)

| name | height to width ratio | font size to get 1px wide bars |
| --- | --- | --- |
| 2of5_S | 1:1 | 14px |
| 2of5 | 2:1 | 28px |
| 2of5_L | 3:1 | 42px |
| 2of5_XL | 4:1 | 56px |
| 2of5_XXL | 5:1 | 70px |

You can download the font in .ttf, .woff, and .svg format.

## install

You can install it as any other font.
To use it as a webfont, you can install with bower:

    bower install --save code-39-font

and the in your .html:

    <link rel="stylesheet" href="bower_components/code-39-font/code39_all.css"/>
    <div class="code_39_XL">*Test*</div>

## usage

an explicit encoding is not necessary. To create a barcode. Simply write your string to be encoded with this font.
**2of5 can only encode digits 0-9** and only an **even number of digits**. The standard does not specify a mapping of the start and stop symbols to a certain ascii code. So i made the mapping up myself. **The start code is `:` and the stop code is `;`**


so to encode the sequence `123456` just write `:123456;` and print it with the 2of5 font.
