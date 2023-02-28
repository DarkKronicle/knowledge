TTF fonts are the life blood of every text you see (unless it is a bitmap). It stands for `True Type Font`. These aim to be high quality and provide lots of customization. There is OTF (Open Type Font) which supports everything `ttf` does as well as adds more features. 

## OTF and TTF Differences

**!! NOT COMPLETE**

- TTF uses quadratic Bezier curves, while OTF uses cubic. 
- OTF handles up to 65536 glyphs.
- Advanced layout

----

## Advances

Each character is not guaranteed to have the same spacing. `I` is a considerably narrower character than `m`. The amount a character shifts the current render x position is called the `advance`. Advances are typically a bit bigger than the actual width of the character. 

## Kerning

Advances work great and all, but sometimes characters need to overlap a small amount. Take a look at Ta and TM. See a difference? The `a` in `Ta` is shifted ever so slightly to the left to have less space in it. This is kerning. Kerning adds a value (can be negative) to the `advance` based on what character comes next. If fonts mess this up you can get really janky looking ones. Check out the subreddit [keming](https://reddit.com/r/keming) to see some examples.

## Bearing X

Some characters need to be shifted slightly the the *left* when rendering. Unlike kerning, Bearing x is global and effects centering. Take a look at the letter `j`. In a pair like 'nj' the bottom of the `j` is overlapping slightly under the `n`. This is the bearing X. In the case of `j` it is negative. Another common character for this is `g`.

## Rendering

A character is rendered using [[Bezier Curves]]. These are what allow vector graphics to have infinite quality. Essentially a glyph (character) is made up of a lot of these.