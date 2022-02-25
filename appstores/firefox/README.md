## Firefox Add-ons Store Submission Notes

- Please Update [Changelog](../changelog.md) (v3.0+) and [Description](../description.md).
- [Old Changelog](changelog-firefox.md).


### Notes

The main difficulty is signing in, as it requires using an authenticating app to scan a bar code for 2FA.

This process may seem complicated but not anymore - just follow the directions for packaging the extension below.

There isn't really any review done, and the submission will be approved immediately after ZIP is submitted. There's no method to set a release datetime like there is for Safari. Changing the metadata and screenshots is a separate step that may be done before or after submitting code, may be updated anytime and doesn't require updating the version or code.


### Get Extension Signed

#### More Info

- [Get your extension signed](https://extensionworkshop.com/documentation/publish/#get-your-extension-signed)

- [Signing and distributing your add-on](https://extensionworkshop.com/documentation/publish/signing-and-distribution-overview/)

- [Submitting an add-on](https://extensionworkshop.com/documentation/publish/submitting-an-add-on/)

- [Getting started with web-ext](https://extensionworkshop.com/documentation/develop/getting-started-with-web-ext/)


#### Package Extension

- [Package your extension](https://extensionworkshop.com/documentation/publish/package-your-extension/)


- Create a .ZIP file of the `webextension` directory. It must not include the directory name, and should not contain any `.DS_Store` or other hidden files, nor any hidden `__MACOSX/` directories which the Finder compress tool usually includes.

- If on a mac, run the following using Terminal, from within the `webextension` directory:

```
zip -r webext.zip . -x ".*" -x "*/.*"
```
- Then move ZIP file to another location on your computer outside of this repo.

- Verify that ZIP file is formatted correctly by testing in Firefox. See [Temporary installation in Firefox](https://extensionworkshop.com/documentation/develop/temporary-installation-in-firefox/).


#### Source Code Submission

- [Source code submission](https://extensionworkshop.com/documentation/publish/source-code-submission/)

- Make sure that all libraries included are non-minimized. Since we removed the webpack build step and no longer generate `build.js`, we no longer need to provide any build steps to the reviewer. The ZIP'd `webextension` should be good enough and not require a separate Source Code submission.


#### Submit Extension

- https://addons.mozilla.org/developers/addon/submit/

- To submit a new version, select the existing approved extension rather than adding a new one.

- Upload ZIP file.

- The validation proccess will find the following issue: "Unsafe assignment to innerHTML". **This is OK**.


#### Answer Questions

- Which application is this version compatible with? [x] Firefox, [ ] Firefox for Android.

- Do You Need to Submit Source Code? [x] NO

- Release Notes: See [changelog.md](../changelog.md)

- Notes to Reviewer:
  - You can provide a test username and password for reviewer to use, however since it appears that no one actually reviews these before being approved, you might not have to.


### Store Metadata

Name: Wayback Machine

Add-on URL:
- https://addons.mozilla.org/en-US/firefox/addon/wayback-machine_new/ (current URL)
- https://addons.mozilla.org/en-US/firefox/addon/wayback-machine (non-active URL)

- Note that the *current URL* is also listed in `about.html` and `scripts/utils.js`.

Summary:
- see [description.md](../description.md)

Leave blank:
- [ ] This add-on is experiemental
- [ ] This add-on requires payment...

Firefox categories:
- [x] Search Tools
- [x] Feeds, News & Blogging

Firefox for Android catagories:
- [x] My add-on doesn't fit into any of the categories

Support email: info@archive.org

Support website: https://archive.org/about/contact.php

Homepage: https://archive.org

License:
- GNU Affero GPL Version 3 (which is not offered in the list)
- see [LICENSE](../../LICENSE)

Privacy Policy:
- [x] This add-on has a Privacy Policy
- see [privacy-policy.md](../privacy-policy.md)


### Images

- See [image assets](image-assets.md) for screenshot info.
- Upload `add-on-icon128.png` (will resize to 32x32, 64x64, 128x128)
- Upload screenshots under version's directory.


#### Screenshot Captions

1. See how websites have changed through the history of the Web.
2. View archived copies of missing websites.
3. Instantly save the page you are currently viewing in the Wayback Machine.
4. View archived research papers and books referenced in Wikipedia.
5. See annotations for the current web page and domain provided by Hypothes.is.