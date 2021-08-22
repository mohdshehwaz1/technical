
# Rendering Engine

The purpose of reading about rendering engine is that how html,css and java-script files converted into the working websites and users can interect with that.When a user wants to visit a website the rendering engine turns the website codes into the interactive pages and this generally refers to a html,css and javascript and this process is generally completed by a software which is used by a web browser called rendering engine.Sometimes we can call them as browser engines.

When the user wants a document then the rendering engine starts fetching the information of this document.Rendering engine receives this document from the network layer.Sometimes it is used with browser engines.Because of the rendering engine a user can see the layout of the website and user can see the layout in colorful mode . It is also used for the animation and fonts . It is used for brighten the pixels and create the visuals on the screen.



There are many rendering engines and each browser used a rendering engine.Some of the examples listed here.
1. **Blink**-Used by chrome
2. **WebKit**-Used in safari
3. **Gecko**-Used in mozilla
4. **Trident**-Used in internet explorer

# Rendering Process
Rendering process is done by the simple four basic steps-
* It parsed the HTML page in chunks and it include the external CSS. Now the DOM is created by the HTML pages and form a DOM tree.
* A render tree is created by the browser and this render tree define the order in which the elements will be displayed.

![rendering process](https://3fxtqy18kygf3on3bu39kh93-wpengine.netdna-ssl.com/wp-content/uploads/2019/11/Screenshot-2019-11-12-at-3.26.19-PM.png)

* Render tree does not assign the position or size values so for this a layout of the render tree created and it will evaluate the position .
* The last step is painting the screen and it paints each node on the screen.




# How does a browser render html to DOM

So for rendering the html pages we need to tell the browser what exactly we want or type the url in our browser and after that the browser generates the request page and after all this process we need to wait till the server response and then the browser creates the DOM tree.
## DOM Tree 

So first of all browser construct the DOM(Document object model) and CSSOM(CSS object model) tree. DOM is nothing bu the transformed HTML markup and CSSOM is nothing but CSS markup transformed. They both are the independent data structure .Html dom is the object model for html. And it is API for javascript.javascript can change,remove and add html element,css styles,html attributes and it can react to html events.

![name of the pic](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/images/render-tree-construction.png)

Now we start a plain html file for example-

now if we run a simple html file then how the browser process this page.
1. **Conversion**- The raw bytes of the html read by the browser and the browser translates them into the characters based on encoding file.
2. **Token** - Than the browser sees these characters as strings and then convert them into tokens.each and every token has its own rule.these token as a data structure
3. **Lexing** - Now this eject tokens are transformed into objects and these objects has their properties and rules.
4. **DOM construction** - Now the relationship between the different tags are defined by the HTML markup then these objects linked in a tree data structure and captures also the parent child relationship.

## CSSOM
When browser was creating DOM if it found the link tag which is referencing to the CSS and it assume that this links also need to be render and then it immediately dispatch the request for this file and which comes back with its content.now we keep our css file independent from the HTML so that some people can work separately with css file.
 
Now whatever CSS file we receive we need to convert it into something that the browser can understand.and now we apply all those rules whatever rules we apply for the css files.
# How does a browser render java-script file
After creating DOM and CSSOM using html file and css file what if html file contain java-script file in it .So if the browser found a script tag the DOM construction is stop until the script finishes its execution beacause browser does not the what this script file will do.That is the precautions which is taken by the browser.














# References-
1. https://www.seobility.net/en/wiki/Rendering

2. https://www.browserstack.com/guide/browser-rendering-engine

3. https://www.lambdatest.com/blog/browser-engines-the-crux-of-cross-browser-compatibility/

4. https://medium.com/@mustafa.abdelmogoud/how-the-browser-renders-html-css-27920d8ccaa6
5. https://www.w3schools.com/whatis/whatis_htmldom.asp

6. https://developers.google.com/web/fundamentals/performance/critical-rendering-path/constructing-the-object-model
7. https://blog.logrocket.com/how-browser-rendering-works-behind-scenes/

