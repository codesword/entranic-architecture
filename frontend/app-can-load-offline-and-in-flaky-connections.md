### App can load on offline/flaky connections
The quality of network connections can be affected by a number of factor which include:
- Poor coverage of a provider.
- Extreme weather conditions.
- Power outages.
- Users travelling into “dead zones” such as buildings that block their network connections.
- Internet connection is managed by a third party and time boxed when it will be active or inactive like in an airport or hotel.
- Cultural practises that require limited or no internet access at specific times or days.

Due to the above conditions, our app should provide a good experience that lessens the impact of changes in connectivity.

We will be able to achieve this using a couple of technologies.

- [Cache API:](https://davidwalsh.name/cache) The cache API will be used to store URL addressable resources. This means all get requests will be cached using the cache API.
- [Service Workers:](https://developers.google.com/web/fundamentals/getting-started/primers/service-workers) a service worker is a background worker that acts as a programmable proxy, allowing us to control what happens on a request-by-request basis. We can use it to make (parts of, or even entire) apps work offline. It's the backbone of an offline app.
- [Push API: ](https://developers.google.com/web/fundamentals/engage-and-retain/push-notifications/) an API enabling push services to send push messages to a webapp. Servers can send messages at any time, even when the webapp or browser are not running.
- [Background Sync:](https://developers.google.com/web/updates/2015/12/background-sync?hl=en) or deferring actions until the user has stable connectivity. This is handy for making use whatever the user wants to send is actually sent. This enables pushing periodic updates when the app is next online.
- [IndexDB: ](https://developer.mozilla.org/en/docs/Web/API/IndexedDB_API) All data apart from URL addressable data are stored in IndexDB. This means, all post request to the server are cached using IndexDB when the app is offline. An [IndexedDB Promised](https://github.com/jakearchibald/idb) library will be used.

**Recommended Reading**
- [Offline Ux Considerations](https://developers.google.com/web/fundamentals/instant-and-offline/offline-ux)
- [Offline Web Applications course on Udacity](https://www.udacity.com/course/offline-web-applications--ud899)
- [Offline Storage for Progressive Web Apps](https://medium.com/dev-channel/offline-storage-for-progressive-web-apps-70d52695513c#.vrhptzlby)
- [Offline Support and Network Resilience](https://medium.com/@addyosmani/progressive-web-apps-with-react-js-part-3-offline-support-and-network-resilience-c84db889162c#.p7kchhlt2)
