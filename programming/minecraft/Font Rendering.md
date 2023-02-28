Minecraft has a few different types of font. There are `Bitmap`, `Space`, `TTF`, and `Legacy Unicode`

## Classes

### TextRenderer

This is the class that handles the majority of text operations. The two main features is rendering text and maintaining the `TextHandler`

-----

### Drawer

Drawer accepts a single character at a time and draws it.

----

### TextHandler

`TextHandler` manages all things 

[[Native Images]]

-----


# Types

## Bitmap

Bitmap is the default type of font in Minecraft. It essentially has a grid of characters that is then loaded onto an image and then selects a certain cell whenever it needs to render a character. This is what all fonts before Minecraft 1.13 had to be. 

**Flaws**

- Everything is monospaced
- There is no support for ligatures

-----

## Space

This font type handles two things: spaces and new lines. It renders absolutely nothing but tells Minecraft how big a space should be. It's very simple.

----

## TTF

This is by far the best looking font option, but it isn't implemented fully. (Look at [[TTF Fonts]]).

**Flaws**

- Minecraft doesn't properly handle [[Font Rendering|Bearing X]], resulting in some characters like `j` to be completely messed up.
- Subpixel precision doesn't work. Fonts don't like snapping to pixels. There are a lot of times when a character is inbetween two pixels. Minecraft renders both of these the exact same, but a method called oversampling allows these to look crisper. Without oversampling Minecraft can have a very inconsistent look at smaller font sizes.

-----

# Configuration

```JSON
{
    "providers": [
        {
            "type": "space",
            "advances": {
                " ": 4,
                "\u200c": 0
            }
        },
        {
            "type": "bitmap",
            "file": "minecraft:font/nonlatin_european.png",
            "ascent": 7,
            "chars": [...]
	    },
	    {
            "type": "bitmap",
            "file": "minecraft:font/accented.png",
            "height": 12,
            "ascent": 10,
            "chars": [...]
	    },
	    {
            "type": "bitmap",
            "file": "minecraft:font/ascii.png",
            "ascent": 7,
            "chars": [...]
        },
        {
            "type": "legacy_unicode",
            "sizes": "minecraft:font/glyph_sizes.bin",
            "template": "minecraft:font/unicode_page_%s.png"
        }
    ]
	]
}
```

Minecraft handles it's configuration via [[JSON]] file. It has a list of providers that go in order from bottom to top. In `FontStorage` it uses this list of providers to find the proper renderer and glyph to draw.