title: Firefox OS
author:
  name: "Les Orchard"
  twitter: "@lmorchard"
  url: "http://lmorchard.com/"
style: index.css
output: index.html
controls: true

--

# Firefox OS
## A look at Mozilla's OS for the Open Web
<img src="img/firefoxos.png" style="display: block; width: auto; height: 40%; margin: 0 auto 0 auto">

--

### Who am I?

<img src="img/me.jpg" style="float: right; width: 25%">

Hi there.

<pre>
les orchard
me@lmorchard.com

{web,mad,computer} scientist;
{tech,scifi} writer;
home{brew,roast}er;
mozillian
</pre>

--

### What is Firefox OS?

* Mozilla's open source OS for the Open Web

<img src="img/firefoxos.png" style="display: block; width: auto; height: 75%; margin: 0 auto 0 auto">

--

### First, there was Boot2Gecko

<img src="img/boot-to-gecko-logo.png" style="width: 18%; float: right; margin-top: -30px">

[Announced in July 2011.](https://groups.google.com/forum/#!topic/mozilla.dev.platform/dmip1GpD5II[1-25-false])

* Have you ever wanted to boot straight into Emacs?

* We built a Linux distro that boots into Gecko, the engine behind Firefox.

* And, from there, Gecko runs the Web.

--

### Gonk, Gecko, and Gaia

<img src="img/boot-to-gecko-logo.png" style="width: 18%; float: right; margin-top: -30px">

There's more to an OS than just a browser.

* **Gonk** - Linux kernel and hardware access

* **Gecko** - Web run-time engine from Firefox

* **Gaia** - User interface, written in HTML / CSS / JS

--

### Gonk, Gecko, and Gaia

[<img src="img/os-parts.png" style="display: block; margin: auto; width: auto; height: 85%">](https://developer.mozilla.org/en-US/docs/Mozilla/Firefox_OS/Platform/Architecture)

--

### Gonk<span class="dim">, Gecko, and Gaia</span>

* A very small Linux distro that borrows from the
  [Android Open Source Project](http://source.android.com/)

* Shares some drivers, hardware abstractions, and dev tools with
  Android

* Generally runs on the same hardware as Android (with some coaxing)

* Does *not* run Android apps

--

### Gonk<span class="dim">, Gecko, and Gaia</span>

<section style="overflow: hidden; display: block; height: 80%; background: url(img/os-parts.png) transparent no-repeat; background-position: center -500px">
</section>

--

### <span class="dim">Gonk,</span> Gecko<span class="dim">, and Gaia</span>

* The `b2g` executable into which Gonk boots.

* The guts of Firefox stripped down to a Web runtime.

* Renders HTML & CSS, executes JavaScript.

* Provides [WebAPIs](https://developer.mozilla.org/en-US/docs/WebAPI)
  through which JavaScript can access Gonk services.

--

### <span class="dim">Gonk,</span> Gecko<span class="dim">, and Gaia</span>

<section style="overflow: hidden; display: block; height: 80%; background: url(img/os-parts.png) transparent no-repeat; background-position: center -200px">
</section>

--

### <span class="dim">Gonk, Gecko, and</span> Gaia

<img src="img/gaia-home.png" style="display: block; float: right; width: 33%; height: auto">

<section style="margin-right: 33%">

* Written entirely in HTML, CSS, & JS using Web APIs

* Home screen & general app management

* Status bar & notifications

* Bundle of built-in apps - e.g. Browser, Calendar, Phone, etc

</section>

--

### <span class="dim">Gonk, Gecko, and</span> Gaia

<section style="overflow: hidden; display: block; height: 80%; background: url(img/os-parts.png) transparent no-repeat; background-position: center 0px">
</section>

--

### RED PANDA BREAK!

*Did you know?* Firefox was named for [the Red Panda](http://en.wikipedia.org/wiki/Red_panda).

[<img src="img/red-panda.png" style="display: block; width: auto; height: 60%; margin: 0 auto 0 auto">](https://blog.mozilla.org/blog/2010/12/03/meet-the-newest-and-cutest-mozillians/)

--

### Open Web Apps

* Basically, an Open Web App is a web page.

* But, web pages aren't <span class="dim">(just)</span> what they used to be.

[<img src="img/demo-studio.png" style="display: block; width: auto; height: 80%; margin: -20px auto 0 auto">](https://developer.mozilla.org/en-US/demos/)

--

### Open Web Apps

* HTML5 introduces new APIs for media, graphics, storage, geolocation, offline
  access, etc.

  * *Yes, apps can work without a net connection*

* New [WebAPIs](https://developer.mozilla.org/en-US/docs/WebAPI) proposed as public standards.

  * Provide access to Gonk hardware services like battery, vibration, bluetooth, SMS, etc.

--

### Web is the New Native

* Write once, run <strike class="dim">everywhere</strike> a whole bunch of places

* **Everything** is an Open Web App using the Gecko web runtime.

* Again, `b2g` is the one and only "native" executable run by Gonk, except for HAL
  processes.

* If you really, really need to compile C code - consider
  [asm.js](http://asmjs.org/) and
  [emscripten](https://github.com/kripken/emscripten/wiki)

--

### Web is the New Native

The Web is faster than you might think, these days.

[<img src="img/unreal.png" style="display: block; margin: auto; width: auto; height: 47%">](https://www.youtube.com/watch?v=XsyogXtyU9o)

[They ported Unreal Engine 3 to the Web in 4 days.](http://www.unrealengine.com/html5/)

--

### Developing for Firefox OS

* So, Firefox OS apps are "just" Open Web Apps.

* And Open Web Apps are "just" web pages.

* Use whatever JavaScript framework you'd like (e.g. jQuery, YUI, Dojo, Enyo,
  etc)

* Adapt your current web site to work better on a variety of small, medium, &
  large screens

--

### Developing for Firefox OS

* So, Firefox OS apps are "just" Open Web Apps.

* Still, [the Firefox OS Simulator add-on](https://addons.mozilla.org/en-US/firefox/addon/firefox-os-simulator/?src=search) is very handy.

<img src="img/dev-simulator.png" style="width: 49%; float: left; margin: -10px -1% -1% 0%">
<img src="img/dev-simulator-window.png" style="width: 49%; float: left; margin: -30px -1% -1% -1">

--

### Developing for Firefox OS

* So, Firefox OS apps are "just" Open Web Apps.

* Still, it's nice to have [an example to start from](https://hacks.mozilla.org/2013/01/introducing-the-firefox-os-boilerplate-app/).

<img src="img/boilerplate-github.png" style="width: 49%; float: left; margin: -10px -1% -1% 0%">
<img src="img/boilerplate.png" style="width: 49%; float: left; margin: -30px -1% -1% -1">

--

### Developing for Firefox OS

* So, Firefox OS apps are "just" Open Web Apps.

* Still, it's nice to have [some building blocks](http://buildingfirefoxos.com).

<img src="img/building-fxos.png" style="display: block; margin: auto; width: auto; height: 72%">

--

### Publishing Apps

What are apps without [a place to find them](https://marketplace.firefox.com)?

<img src="img/marketplace.png" style="display: block; margin: auto; width: auto; height: 72%">

--

### Publishing Apps

Firefox Marketplace implements the [Open Web Apps](https://developer.mozilla.org/en-US/docs/Web/Apps) publishing scheme:

* [A JSON manifest describing an App](https://developer.mozilla.org/en-US/docs/Web/Apps/Manifest)

* [JavaScript APIs for installing & managing Apps](https://developer.mozilla.org/en-US/docs/Web/Apps/JavaScript_API)

*TL;DR: You can run your own "marketplace", even if it's just a page with
install buttons for your own apps.*

--

### Publishing Apps

Sample `manifest.webapp`:

<pre style="font-size: 0.5em; line-height: 1.25em; margin-top: -2em">
{
    "version": "0.1",
    "name": "Area Tweet",
    "description": "Find tweets by for any location",
    "icons": {
        "48": "http://areatweet.com/images/icon-48.png",
        "128": "http://areatweet.com/images/icon-128.png"
    },
    "developer": {
        "name": "David Walsh",
        "url": "http://areatweet.com"
    },
    "installs_allowed_from": [
        "http://areatweet.com",
        "https://marketplace.firefox.com"
    ],
    "default_locale": "en" 
}
</pre>

--

### Publishing Apps

Sample App installation code:

<pre style="font-size: 0.6em; line-height: 1.25em; margin-top: -0.5em">
var MANIFEST_URL ='https://myapp.example.com/manifest.webapp';
var installApp = navigator.mozApps.install(MANIFEST_URL);
 
// Successful install
installApp.onsuccess = function(data) {
    console.log("Success, app installed!");
};
 
// Install failed
installApp.onerror = function() {
    console.log("Install failed\n\n:" + installApp.error.name);
};
</pre>

--

### Publishing Apps

* By the way, Open Web Apps can also be installed via Firefox for Android and
  Desktop <span class="dim">(Nightly)</span>

<img src="img/install-button.png" style="width: 48%; float: left; margin: 1%">
<img src="img/install-icon.png" style="width: 48%; float: left; margin: 1%">

--

### Publishing Apps

* By the way, Open Web Apps can also be installed via Firefox for Android and
  Desktop <span class="dim">(Nightly)</span>

<img src="img/clocks-fxos.png" style="width: 22%; float: left; margin: 0 1% 0 1%;">
<img src="img/clocks-android.png" style="width: 22%; float: left; margin: 0 1% 0 1%;">
<img src="img/clocks-ubuntu.png" style="width: 22%; float: left; margin: 0 1% 0 1%;">
<img src="img/clocks-osx.png" style="width: 26%; float: left; margin: -20px 1% 0 0;">

--

### The End (also: FENNEC BREAK!)

*Did you know?* Firefox for Mobile was codenamed "Fennec" for [the desert fox](http://en.wikipedia.org/wiki/Fennec_fox).

[<img src="img/fennec_logo.jpg" style="width: 48%; float: left">](https://wiki.mozilla.org/Mobile/Fennec)
[<img src="img/fennec.jpg" style="width: 48%; float: right">](http://www.flickr.com/photos/joachim_s_mueller/3775054635/)
