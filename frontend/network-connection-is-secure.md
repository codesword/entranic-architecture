### Network connection is secure
All connection to our app will be via https. HTTPS prevents bad-actors from tampering with communications between our app and the browser our users are using and you might have read that Google is pushing to shame sites that are unencrypted. Powerful new web platform APIs, like Service Worker, require secure origins via HTTPS. We will be leveraging [LetsEncrypt](https://letsencrypt.org/) to provide free [SSL certificates](https://www.globalsign.com/en/ssl-information-center/what-is-an-ssl-certificate/) for our frontend app.
The [Chrome DevTools Security panel](https://developers.google.com/web/updates/2015/12/security-panel?hl=en) allows us to validate issues with security certificates and mixed content errors. Some of the actions we will be taking while building out the frontend app includes:
- Upgrade unsecure requests (“HTTP” connections) to “HTTPS” redirecting users as needed.
- Ensure there are no references to `http` in our code. All third party resource we use must be accessed via `https`.
- Use [HTTP Strict Transport Security](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security) (HSTS) headers when serving pages. It’s a directive that forces browsers to only talk to our site in HTTPS.

**Recommended Resources**
- [Deploying HTTPS: The Green Lock and Beyond](https://developers.google.com/web/shows/cds/2015/deploying-https-the-green-lock-and-beyond-chrome-dev-summit-2015?hl=en)
- [Mythbusting HTTPS: Squashing security’s urban legends](https://developers.google.com/web/shows/google-io/2016/mythbusting-https-squashing-securitys-urban-legends-google-io-2016?hl=en)
