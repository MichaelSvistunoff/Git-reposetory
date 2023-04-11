Quick start 
Get started by including Bootstrap’s production-ready CSS and JavaScript via CDN without the need for any build steps. See it in practice with this Bootstrap CodePen demo.


Create a new index.html file in your project root. Include the <meta name="viewport"> tag as well for proper responsive behavior in mobile devices.


<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Bootstrap demo</title>
  </head>
  <body>
    <h1>Hello, world!</h1>
  </body>
</html>
Include Bootstrap’s CSS and JS. Place the <link> tag in the <head> for our CSS, and the <script> tag for our JavaScript bundle (including Popper for positioning dropdowns, poppers, and tooltips) before the closing </body>. Learn more about our CDN links.


<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Bootstrap demo</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-KK94CHFLLe+nY2dmCWGMq91rCGa5gtU4mk92HdvYe+M/SXH301p5ILy+dN9+nJOZ" crossorigin="anonymous">
  </head>
  <body>
    <h1>Hello, world!</h1>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ENjdO4Dr2bkBIFxQpeoTz1HIcje39Wm4jDKdf19U8gI4ddQ3GYNS7NTKfAdVQSZe" crossorigin="anonymous"></script>
  </body>
</html>
You can also include Popper and our JS separately. If you don’t plan to use dropdowns, popovers, or tooltips, save some kilobytes by not including Popper.


<script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.11.7/dist/umd/popper.min.js" integrity="sha384-zYPOMqeu1DAVkHiLqWBUTcbYfZ8osu1Nd6Z89ify25QV9guujx43ITvfi12/QExE" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/js/bootstrap.min.js" integrity="sha384-Y4oOpwW3duJdCWv5ly8SCFYWqFDsfob/3GkgExXKV4idmbt98QcxXYs9UoXAB7BZ" crossorigin="anonymous"></script>
Hello, world! Open the page in your browser of choice to see your Bootstrapped page. Now you can start building with Bootstrap by creating your own layout, adding dozens of components, and utilizing our official examples.

CDN links 
As reference, here are our primary CDN links.

Description	URL
CSS	https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/css/bootstrap.min.css
JS	https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/js/bootstrap.bundle.min.js
You can also use the CDN to fetch any of our additional builds listed in the Contents page.

Next steps 
Read a bit more about some important global environment settings that Bootstrap utilizes.

Read about what’s included in Bootstrap in our contents section and the list of components that require JavaScript below.

Need a little more power? Consider building with Bootstrap by including the source files via package manager.

Looking to use Bootstrap as a module with <script type="module">? Please refer to our using Bootstrap as a module section.

JS components 
Curious which components explicitly require our JavaScript and Popper? Click the show components link below. If you’re at all unsure about the general page structure, keep reading for an example page template.

Show components requiring JavaScript
Important globals 
Bootstrap employs a handful of important global styles and settings, all of which are almost exclusively geared towards the normalization of cross browser styles. Let’s dive in.

HTML5 doctype 
Bootstrap requires the use of the HTML5 doctype. Without it, you’ll see some funky and incomplete styling.


<!doctype html>
<html lang="en">
  ...
</html>
Viewport meta 
Bootstrap is developed mobile first, a strategy in which we optimize code for mobile devices first and then scale up components as necessary using CSS media queries. To ensure proper rendering and touch zooming for all devices, add the responsive viewport meta tag to your <head>.


<meta name="viewport" content="width=device-width, initial-scale=1">
You can see an example of this in action in the quick start.

Box-sizing 
For more straightforward sizing in CSS, we switch the global box-sizing value from content-box to border-box. This ensures padding does not affect the final computed width of an element, but it can cause problems with some third-party software like Google Maps and Google Custom Search Engine.

On the rare occasion you need to override it, use something like the following:


.selector-for-some-widget {
  box-sizing: content-box;
}
With the above snippet, nested elements—including generated content via ::before and ::after—will all inherit the specified box-sizing for that .selector-for-some-widget.

Learn more about box model and sizing at CSS Tricks.

Reboot 
For improved cross-browser rendering, we use Reboot to correct inconsistencies across browsers and devices while providing slightly more opinionated resets to common HTML elements.

Community 
Stay up-to-date on the development of Bootstrap and reach out to the community with these helpful resources.

Read and subscribe to The Official Bootstrap Blog.
Ask and explore our GitHub Discussions.
Chat with fellow Bootstrappers in IRC. On the irc.libera.chat server, in the #bootstrap channel.
Implementation help may be found at Stack Overflow (tagged bootstrap-5).
Developers should use the keyword bootstrap on packages that modify or add to the functionality of Bootstrap when distributing through npm or similar delivery mechanisms for maximum discoverability.
You can also follow @getbootstrap on Twitter for the latest gossip and awesome music videos.
