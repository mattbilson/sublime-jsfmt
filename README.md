[jsfmt](https://github.com/rdio/jsfmt) for Sublime Text 2/3
=================


If you want your javascript automatically formatted to abide a particular style, 
then jsfmt is for you.  No need to read warnings and fix things yourself. 
Just keep it all auto. Boom boom [jsfmt](https://github.com/rdio/jsfmt) is pretty tight. 
And yeah, if you want it in Sublime Text this is your homeboy.

![](http://i.imgur.com/zkBvQ6X.gif)

Enable `autoformat` then save the file and it gets formatted.

### Installation

**Via package control**  
Open your command palette -> Package Control: Install Package -> jsfmt

**Manual**
```bash

## go to your ST packages folder. maybe something like …
cd ~/Library/"Application Support/Sublime Text 2"/Packages

# clone this repo
git clone https://github.com/ionutvmi/sublime-jsfmt jsfmt
```

On windows open cmd and:
```
cd %APPDATA%\"Sublime Text 3"\Packages
git clone https://github.com/ionutvmi/sublime-jsfmt jsfmt
```

### Plugins included
- [esformatter-braces](https://github.com/pgilad/esformatter-braces)
- [esformatter-semicolons](https://github.com/bulyshko/esformatter-semicolons)
- [esformatter-dot-notation](https://github.com/pgilad/esformatter-dot-notation)
- [esformatter-quotes](https://github.com/millermedeiros/esformatter-quotes)
- [esformatter-eol-last](https://github.com/briandipalma/esformatter-eol-last)
- [esformatter-literal-notation](https://github.com/kewah/esformatter-literal-notation)


### Settings
```javascript
{
    // autoformat on save
    "autoformat": false,

    // array of extensions for autoformat
    "extensions": ["js", "sublime-settings"],

    // options for jsfmt
    "options": {
        "preset": "jquery",
        "indent": {
            "value": "    "
        },
        // plugins included
        "plugins": [
            // "esformatter-quotes",
            // "esformatter-semicolons",
            // "esformatter-braces",
            // "esformatter-dot-notation"
            // "esformatter-literal-notation"
            // "esformatter-eol-last"
        ]
    },
    "options-JSON": {
        "plugins": [
            "esformatter-quotes"
        ],
        "quotes": {
            "type": "double"
        }
    },
    "alert-errors": true,
    // path to nodejs
    "node-path": "node"
}

```

### Commands
**Command palette:**  

- JSFMT: Format the current file
- JSFMT: Toggle autoformat
- JSFMT: Settings - Default
- JSFMT: Settings - User

**Menu:**  
Preferences -> Package Settings -> Sublime JSFMT


### Formatting rules

You can set global rules via a `.jsfmtrc`. Be crazy and establish one for all your 
projects in `~/.jsfmtrc`. (like in [dotfiles](https://github.com/paulirish/dotfiles/blob/master/.jsfmtrc))

Otherwise you're probably pretty levelheaded and will probably provide one in your 
project root. It'll be read and applied.

Rules you can intuit from these [esformatter preset files](https://github.com/millermedeiros/esformatter/tree/master/lib/preset).

There's a `.jsfmtrc-sample` in this repo. It's a good start. Rename it and toss it 
somewhere. Try it out. 

#### Compatibility 

Should work in both ST2 and ST3.


### Contributing

If you find any bugs feel free to report them [here](https://github.com/ionutvmi/sublime-jsfmt/issues)  
Pull requests are also encouraged.
