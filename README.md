# Entranic! V2
## Technology and Architecture


### Table of contents
- [Introduction](#introduction)
- [Frontend](/frontend/introduction.md)
    - [Network connection is secure](/frontend/network-connection-is-secure.md)
    - [User can be prompted to Add to Homescreen](/frontend/add-to-homescreen.md)
    - [Installed web app will launch with custom splash screen](/launch-with-custom-spash-screen.md)
    - [Design is mobile-friendly](/frontend/design-is-mobile-friendly.md)
    - [App can load on offline/flaky connections](/frontend/app-can-load-offline-and-in-flaky-connections.md)
    - [Page load performance is fast](page-load-performace-is-fast.md)
    - [Address bar matches brand colors](address-bar-matches-brand-colors.md)
    - [Site is progressively enhanced](site-is-progressively-enhanced.md)



## Introduction

This document provides a description of the the Entranic Version 2 systems and an architectural design created based on the requirements of the new version of the system and lessons learned during the development and long term support of the previous system. The is no legacy support for the system to be developed, but many of the design choices outlined in the document are based on experience gained from that system.

The underlying theme of this architecture is to allow flexibility and minimize complications typical in developing full stack solutions, by leveraging Functional and Reactive Programming paradigms. The majority of all logic will live on backend, with several dedicated micro services performing tasks based on User and Administrative Actions. Thin clients will connect, authenticate and reflect an immutable state object. The final solution should be elastic and highly scalable. It will achieve this by being cloud native, leveraging all the cloud has to offer to build such systems.

Due to the nature of our end users who will mostly be accessing the app via mobile phones and/or flaky network conditions, the application will be built with progressive enhancement and offline capabilities in mind.

## References

### Frontend
- [Udacity Course on Progressive Web apps](https://www.udacity.com/course/intro-to-progressive-web-apps--ud811)
- [Progressive Web Apps with ReactJS - Introduction](https://medium.com/@addyosmani/progressive-web-apps-with-react-js-part-i-introduction-50679aef2b12#.9o7u7a2t3)
- [Progressive Web Apps with ReactJS - page load performace](https://medium.com/@addyosmani/progressive-web-apps-with-react-js-part-2-page-load-performance-33b932d97cf2#.xaxvg47wi)
- [Progressive Web Apps with ReactJS - offline support and network resilience](https://medium.com/@addyosmani/progressive-web-apps-with-react-js-part-3-offline-support-and-network-resilience-c84db889162c#.p7kchhlt2)
- [Progressive Web Apps with ReactJS - progressive enhancement](https://medium.com/@addyosmani/progressive-web-apps-with-react-js-part-4-site-is-progressively-enhanced-b5ad7cf7a447#.hcmy1gtcc)
- [7 Principles of Rich Web Applications](https://rauchg.com/2014/7-principles-of-rich-web-applications)
- [Codelabs - Your first pw app](https://developers.google.com/web/fundamentals/getting-started/codelabs/your-first-pwapp/)
