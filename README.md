joshchallenge1
==============


A Python Challenge For Josh
---------------------------


> "Oh, bird of my soul, fly away now, For I possess a hundred fortified towers."

--- **RUMI**


---

### Step 1

Your challenge requires a console zealot's dream of quickly locating CSS colors
with only the touch of a single key. To accomplish this, you must first greet
the user upon loading the program. The intro should be clearly visible, and I would
suggest trying to find and use the  `center()` feature built in to Python.

- For example try creating a line like this -------->  `'-'`
- ...you could instead do something like this:--> `line = '-' * 40`
- That way, you can then call `center()` function on a known length.

This is **important** & 1st appearances are everything, you know.
Also, everything, including this must have a function assigned to it. Meaning, no
long mess of a solution. Each item should be sectioned off into its own `def` statment.

---

### Step 2

After 'greeting' the player, ask them for a selection: this can be two things.

>0	_Exit the Program_   
1	_Enter a Letter_


After making their selection, the program should then execute correctly. Ensure
that all possible other combinations of entries either throw errors or exit the
program completely, I don't care which.

_Basically, the only selectable answer here that doesn't result in failure is **1**!_


### Step 3

Find a way to parse the dictionary of colors as given below into a usable output.

For example, if I enter 1 to the question posed in step 2, then this part should
ask, "_What letter do you wish to find colors for?_". Then, all color names with
the entered letter should be scanned through and returned with not just the color
itself, but its HEX value (*this is the second number in the dict called
__csscolors__*).

### Step 4

Finally, return the colors, **IN ALPHABETICAL ORDER** alongside the color
that represents that specific color . These should be printed to the console.

### Step 5

Ask the user if they'd like to try again, and if not, exit. If they do, run
the program again!

 ### Step 6


 Have fun!!!

---

### Let's A Go!
To start, here is the list of colors is a Python dictionary.

```python
csscolors = {
    'aliceblue': '#F0F8FFFF',
    'antiquewhite': '#FAEBD7FF',
    'aqua': '#00FFFFFF',
    'aquamarine': '#7FFFD4FF',
    'azure': '#F0FFFFFF',
    'beige': '#F5F5DCFF',
    'bisque': '#FFE4C4FF',
    'black': '#000000FF',
    'blanchedalmond': '#FFEBCDFF',
    'blue': '#0000FFFF',
    'blueviolet': '#8A2BE2FF',
    'brown': '#A52A2AFF',
    'burlywood': '#DEB887FF',
    'cadetblue': '#5F9EA0FF',
    'chartreuse': '#7FFF00FF',
    'chocolate': '#D2691EFF',
    'coral': '#FF7F50FF',
    'cornflowerblue': '#6495EDFF',
    'cornsilk': '#FFF8DCFF',
    'crimson': '#DC143CFF',
    'cyan': '#00FFFFFF',
    'darkblue': '#00008BFF',
    'darkcyan': '#008B8BFF',
    'darkgoldenrod': '#B8860BFF',
    'darkgray': '#A9A9A9FF',
    'darkgrey': '#A9A9A9FF',
    'darkgreen': '#006400FF',
    'darkkhaki': '#BDB76BFF',
    'darkmagenta': '#8B008BFF',
    'darkolivegreen': '#556B2FFF',
    'darkorange': '#FF8C00FF',
    'darkorchid': '#9932CCFF',
    'darkred': '#8B0000FF',
    'darksalmon': '#E9967AFF',
    'darkseagreen': '#8FBC8FFF',
    'darkslateblue': '#483D8BFF',
    'darkslategray': '#2F4F4FFF',
    'darkslategrey': '#2F4F4FFF',
    'darkturquoise': '#00CED1FF',
    'darkviolet': '#9400D3FF',
    'deeppink': '#FF1493FF',
    'deepskyblue': '#00BFFFFF',
    'dimgray': '#696969FF',
    'dimgrey': '#696969FF',
    'dodgerblue': '#1E90FFFF',
    'firebrick': '#B22222FF',
    'floralwhite': '#FFFAF0FF',
    'forestgreen': '#228B22FF',
    'fuchsia': '#FF00FFFF',
    'gainsboro': '#DCDCDCFF',
    'ghostwhite': '#F8F8FFFF',
    'gold': '#FFD700FF',
    'goldenrod': '#DAA520FF',
    'gray': '#808080FF',
    'grey': '#808080FF',
    'green': '#008000FF',
    'greenyellow': '#ADFF2FFF',
    'honeydew': '#F0FFF0FF',
    'hotpink': '#FF69B4FF',
    'indianred': '#CD5C5CFF',
    'indigo': '#4B0082FF',
    'ivory': '#FFFFF0FF',
    'khaki': '#F0E68CFF',
    'lavender': '#E6E6FAFF',
    'lavenderblush': '#FFF0F5FF',
    'lawngreen': '#7CFC00FF',
    'lemonchiffon': '#FFFACDFF',
    'lightblue': '#ADD8E6FF',
    'lightcoral': '#F08080FF',
    'lightcyan': '#E0FFFFFF',
    'lightgoldenrodyellow': '#FAFAD2FF',
    'lightgray': '#D3D3D3FF',
    'lightgrey': '#D3D3D3FF',
    'lightgreen': '#90EE90FF',
    'lightpink': '#FFB6C1FF',
    'lightsalmon': '#FFA07AFF',
    'lightseagreen': '#20B2AAFF',
    'lightskyblue': '#87CEFAFF',
    'lightslategray': '#778899FF',
    'lightslategrey': '#778899FF',
    'lightsteelblue': '#B0C4DEFF',
    'lightyellow': '#FFFFE0FF',
    'lime': '#00FF00FF',
    'limegreen': '#32CD32FF',
    'linen': '#FAF0E6FF',
    'magenta': '#FF00FFFF',
    'maroon': '#800000FF',
    'mediumaquamarine': '#66CDAAFF',
    'mediumblue': '#0000CDFF',
    'mediumorchid': '#BA55D3FF',
    'mediumpurple': '#9370D8FF',
    'mediumseagreen': '#3CB371FF',
    'mediumslateblue': '#7B68EEFF',
    'mediumspringgreen': '#00FA9AFF',
    'mediumturquoise': '#48D1CCFF',
    'mediumvioletred': '#C71585FF',
    'midnightblue': '#191970FF',
    'mintcream': '#F5FFFAFF',
    'mistyrose': '#FFE4E1FF',
    'moccasin': '#FFE4B5FF',
    'monnoroch': '#000000FF',
    'navajowhite': '#FFDEADFF',
    'navy': '#000080FF',
    'oldlace': '#FDF5E6FF',
    'olive': '#808000FF',
    'olivedrab': '#6B8E23FF',
    'orange': '#FFA500FF',
    'orangered': '#FF4500FF',
    'orchid': '#DA70D6FF',
    'palegoldenrod': '#EEE8AAFF',
    'palegreen': '#98FB98FF',
    'paleturquoise': '#AFEEEEFF',
    'palevioletred': '#D87093FF',
    'papayawhip': '#FFEFD5FF',
    'peachpuff': '#FFDAB9FF',
    'peru': '#CD853FFF',
    'pink': '#FFC0CBFF',
    'plum': '#DDA0DDFF',
    'powderblue': '#B0E0E6FF',
    'purple': '#800080FF',
    'red': '#FF0000FF',
    'rosybrown': '#BC8F8FFF',
    'royalblue': '#4169E1FF',
    'saddlebrown': '#8B4513FF',
    'salmon': '#FA8072FF',
    'sandybrown': '#F4A460FF',
    'seagreen': '#2E8B57FF',
    'seashell': '#FFF5EEFF',
    'sienna': '#A0522DFF',
    'silver': '#C0C0C0FF',
    'skyblue': '#87CEEBFF',
    'slateblue': '#6A5ACDFF',
    'slategray': '#708090FF',
    'slategrey': '#708090FF',
    'snow': '#FFFAFAFF',
    'springgreen': '#00FF7FFF',
    'steelblue': '#4682B4FF',
    'tan': '#D2B48CFF',
    'teal': '#008080FF',
    'thistle': '#D8BFD8FF',
    'tomato': '#FF6347FF',
    'turquoise': '#40E0D0FF',
    'violet': '#EE82EEFF',
    'wheat': '#F5DEB3FF',
    'white': '#FFFFFFFF',
    'whitesmoke': '#F5F5F5FF',
    'yellow': '#FFFF00FF',
    'yellowgreen': '#9ACD32FF',
}

```

If you need the solution, admit defeat!!! MWAHAHAH!
