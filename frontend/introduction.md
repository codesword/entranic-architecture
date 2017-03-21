The frontend will be built as a progressive web app(PWA) and by leveraging new technologies, we bring the best of mobile and native apps to users. The frontend will be responsive, reliable, fast and engaging to our end users. The app will originate from a secure origin (https) and load regardless of network state(good, bad, offline). To ensure our app meets a respectable bar for web performance under emulated mobile conditions with progressively enhancement, we will a PWA checklist and a tool for auditing the app for PWA features. We will be using [LightHouse](https://github.com/GoogleChrome/lighthouse) as the auditing tool. Lighthouse is available as a [Chrome extension](https://chrome.google.com/webstore/detail/lighthouse/blipmdconlkpinefehnmjammfjpmpbjk)  and a [CLI](https://github.com/GoogleChrome/lighthouse#install-cli), both of which present a report that looks a little like this:

![lighthouse](images/light-house.jpeg)

The top-level audits Lighthouse runs effectively a collection of modern web best practices refined for a mobile world:
- Network connection is secure
- User can be prompted to Add to Homescreen
- Installed web app will launch with custom splash screen
- Design is mobile-friendly
- App can load on offline/flaky connections
- Page load performance is fast
- Site is progressively enhanced
- Address bar matches brand colors

Our app will be optimized for lighthouse. I will discuss what we need to do to check off the above list.
