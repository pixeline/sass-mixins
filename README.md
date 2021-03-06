# Evan's SASS Mixins

A collection of my favorite custom [SASS](http://sass-lang.com/) mixins.

## Requirements
These scripts were designed to fit into my design workflow, which makes use of :

- [SASS](http://sass-lang.com/)
- [Compass](http://compass-style.org/)
- [Foundation 5](http://foundation.zurb.com/), or at least it's [_functions.scss file](https://github.com/zurb/foundation/blob/master/scss/foundation/_functions.scss)

## Medium.com Style Underlines
This mixin is intended to replicate Medium.com's super sexy underlines style, [elaborated in fantastic detail by Marcin Wichary here.](https://medium.com/designing-medium/7c03a9274f9). This mixin is a bit of a remix based on several [other's](https://github.com/Team-Sass/toolkit#underline) [attempts](http://codepen.io/ghepting/pen/tLnHK/), with my own added contributions. It supports clearing descenders and graceful multiline spanning.

![Underline Example](https://raw.githubusercontent.com/evansims/sass-mixins/screenshots/screenshots/underlines.png "Underline Example")

![Multiline underlines are supported.](https://raw.githubusercontent.com/evansims/sass-mixins/screenshots/screenshots/underlines_multiline.png "Multiline underlines are supported.")

Usage example:
```scss
a.author {
    color: #5f5164;
    @include underline(#fff, #D6DDDE)

    &:hover {
        @include underline(#fff, #5f5164)
    }
}
```

Parameters (in order):
- Background color; defaults to #fff.
- Underline color; defaults to #ccc.
- Distance of underline from text base; defaults to 2.
- Width of underline; defaults to 1.
- Clear descenders true/false; defaults to yes.
