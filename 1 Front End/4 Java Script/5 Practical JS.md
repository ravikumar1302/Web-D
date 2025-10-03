## Practical uses of JS

1. JS can change HTML Content

    - `getElementById()` : document.getElementById("demo").innerHTML = "Hello JavaScript";
    -

2. JS can change HTML Attribute Values

    ```
        <button onclick="document.getElementById('myImage').src='pic_bulbon.gif'">Turn on the light</button>
        <img id="myImage" src="pic_bulboff.gif" style="width:100px">
        <button onclick="document.getElementById('myImage').src='pic_bulboff.gif'">Turn off the light</button>
    ```

3. JS can change HTML Styles (CSS)

    - document.getElementById("demo").style.fontSize = "35px";

4. JS can hide/Show hiiden HTML elements

    - Hiding HTML elements can be done by changing the display style: document.getElementById("demo").style.display = "none";
    - Showing hidden HTML elements can also be done by changing the display style: document.getElementById("demo").style.display = "block";

5.
