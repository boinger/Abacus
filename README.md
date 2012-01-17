Abacus Alignment Plugin for Sublime Text 2
================

![This work?](http://dl.dropbox.com/u/5514249/Abacus.gif)

I'm pretty anal about aligning things in my code, but the alignment plugins I tried were more-or-less one-trick-ponies, and I didn't like any of their tricks, so I made my own.

My one anal pony trick involves allowing you to slide the midline separator token--the thing that defines where the left column ends and the right column begins--like an abacus bead, toward either the left or the right by giving each possible token a `gravity` property like so:

``` json
{
    "com.khiltd.abacus.separators": 
    [    
        { 
            "token":                ":",
            "gravity":              "left",
            "preserve_indentation": true
        },
        { 
            "token":                "=",
            "gravity":              "right",
            "preserve_indentation": true
        }
    ]
}
```

Abacus focuses on aligning assignments in as language-agnostic a manner as possible. It works best when there's one assignment per line; if you like shoving dozens of CSS or JSON declarations on a single line then you are an enemy of readability and this plugin will make every effort to hinder and harm your creature on Earth as far as it is able.

Usage
============

Make a selection, then `command + option + control + ]`.

There's no Linux or Windows keymappings because I don't use these operating systems (at least not their GUIs) and have no idea what's appropriate for them. If you have suggestions, I'm all ears. 

Caveats
============

I don't care if you like real tabs or Windows line endings and don't bother with handling them. Seriously, what year is this? 
