### Installed web app will launch with custom splash screen
Tapping on a homescreen icon for an app would often take up to 200ms (or multiple seconds in slow sites) for the first frame of the document to be rendered to the screen.

During this time, the user would see a white screen, decreasing the perceived performance of your site. We can customise a splash screen (based on a background_color, name and icons from the Web App Manifest) used to color the screen until the browser is ready to paint something. This makes our webapp feel a lot closer to “native”.

**Recommended Resources**
- [Adding Splash Screen for Installed Web Apps](https://developers.google.com/web/updates/2015/10/splashscreen?hl=en)
