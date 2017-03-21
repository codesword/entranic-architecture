### User can be prompted to Add to Homescreen
Nobody likes to have to type in long URLs on a mobile keyboard if they don't need to. With the [add to homescreen](https://developer.chrome.com/multidevice/android/installtohomescreen) feature, our users can choose to add a shortcut link to their device just as they would install a native app from a store, but with a lot less friction.. We can achieve this by adding a [web application manifest](https://developer.mozilla.org/en-US/docs/Web/Manifest). The web app manifest is a simple JSON file that gives you, the developer, the ability to control how your app appears to the user in the areas that they would expect to see apps (for example the mobile home screen), direct what the user can launch and more importantly how they can launch it.

Using the web app manifest, your web app can:

- Have a rich presence on the user's Android home screen
- Be launched in full-screen mode on Android with no URL bar
- Control the screen orientation for optimal viewing
- Define a "splash screen" launch experience and theme color for the site
- Track whether you're launched from the home screen or URL bar

An example manifest.json file looks like this.
```json
{
  "name": "Entranic",
  "short_name": "Entranic",
  "icons": [{
    "src": "images/icons/icon-128x128.png",
      "sizes": "128x128",
      "type": "image/png"
    }, {
      "src": "images/icons/icon-144x144.png",
      "sizes": "144x144",
      "type": "image/png"
    }, {
      "src": "images/icons/icon-152x152.png",
      "sizes": "152x152",
      "type": "image/png"
    }, {
      "src": "images/icons/icon-192x192.png",
      "sizes": "192x192",
      "type": "image/png"
    }, {
      "src": "images/icons/icon-256x256.png",
      "sizes": "256x256",
      "type": "image/png"
    }],
  "start_url": "/index.html",
  "display": "standalone",
  "background_color": "#3E4EB8",
  "theme_color": "#2F3BA2"
}
```
[realfavicongenerator](realfavicongenerator.net) will be used to generate cross browser and OS favicon.

With a manifest.json file located in the root, we can tell the browser to use it via:
```
<link rel="manifest" href="/manifest.json">
```
However, since we a building a multitenant app, we will like to customize the manifest file per tenant. So, we will have a manifest file per tenant which will be loaded dynamically via:

```
<link rel="manifest" href="/manifest/tenant-id.json">
```

**Recommended Resources**
- [Web app manifest](https://developers.google.com/web/fundamentals/engage-and-retain/web-app-manifest/)
- [App install banners](https://developers.google.com/web/fundamentals/engage-and-retain/app-install-banners)
- [Web app install banners and add to homescreen](https://developers.google.com/web/fundamentals/getting-started/codelabs/your-first-pwapp/#web_app_install_banners_and_add_to_homescreen_for_chrome_on_android)
