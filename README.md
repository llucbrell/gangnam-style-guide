# gangnam-style-guide

Starting to building my own JavaScript style guide starting with npm's as sketch.

This JavaScript coding style is a bit unconventional. It is not different for difference's sake, but rather a carefully crafted style that is designed to reduce visual clutter and make bugs more apparent.


<h2>Line Length</h2>

Keep lines shorter than 80 characters. It's better for lines to be too short than to be too long. Break up long lists, objects, and other statements onto multiple lines.

12345678901234567890123456789012345678901234567890123456789012345678901234567890

1________10_______20_________30_______40________50________60________70________80  

gangnam-style!

<h2>Indentation</h2>

Two-spaces. Tabs are better, but they look like hell in web browsers (and on GitHub), and node uses 2 spaces, so that's that.

Configure your editor appropriately.

gangnam-style!

<h2>Curly braces</h2>

Curly braces belong on the same line as the thing that necessitates them.

<b>Bad:</b>

      function ()
      
      {

<b>Good:</b>

      function () {

If a block needs to wrap to the next line, use a curly brace. Don't use it if it doesn't.

<b>Bad:</b>

    if (foo) { bar() }
    while (foo)
    bar()

<b>Good:</b>

    if (foo) bar()
    while (foo) {
    bar()
    }

gangnam-style!

<h2>Comas</h2>

If there is a list of things separated by commas, and it wraps across multiple lines, put the comma at the start of the next line, directly below the token that starts the list. Put the final token in the list on a line by itself. For example:


      var magicWords = [ "abracadabra"
   
                  , "gesundheit"
                  
                  , "ventrilo"
                  
                  ]
      , spells = { "fireball" : function () { setOnFire() }
   
              , "water" : function () { putOut() }
              
              }
              
      , a = 1
   
      , b = "abc"
   
      , etc
   
      , somethingElse
   


gangnam-style!

<h2>Whitespace</h2>

Put a single space in front of ( for anything other than a function call. Also use a single space wherever it makes things more readable.

Don't leave trailing whitespace at the end of lines. Don't indent empty lines. Don't use more spaces than are helpful.
Functions

gangnam-style!

<h2>Errors</h2>

Always create a new Error object with your message. Don't just return a string message to the callback. Stack traces are handy.

gangnam-style!

<h2>Writting practices</h2>

Use <b>lowerCamelCase</b> for multiword identifiers when they <i>refer to objects, functions, methods, properties, or anything not specified in this section.</i>

Use <b>UpperCamelCase</b> for <i>class names</i> (things that you'd pass to "new").

Use <b>all-lower-hyphen-css-case</b> for multiword <i>filenames and config keys</i>.

Use named functions. They make stack traces easier to follow.

Use <b>CAPS_SNAKE_CASE</b> for <i>constants</i>, things that should never change and are rarely used.

Use a <b>single uppercase letter</b> for function <i>names where the function would normally be anonymous, but needs to call itself recursively</i>. It makes it clear that it's a "throwaway" function.
null, undefined, false, 0


<h2>More</h2>

*Boolean variables and functions should always be either true or false. Don't set it to 0 unless it's supposed to be a number.

*When something is intentionally missing or removed, set it to null.

*Allways use delete for removing objects.

*Don't set things to undefined. Reserve that value to mean "not yet set to anything."

*Use named functions. They make stack traces a lot easier to read.
Callbacks, Sync/async Style

*Use the asynchronous/non-blocking versions of things as much as possible. 

*The callback should always be the last argument in the list. Its first argument is the Error or null.

*Be very careful never to ever ever throw anything. It's worse than useless. Use the console to handle them.

*Boolean objects are verboten.


gangnam-style!
