# AppConsent

## 1.0.12 (19/10/2020)
- fix bug NoticeListener call after completion, now it's called only after success of saveConsents()
- remove NoticeListener to `setConsentableConsents()`

## 1.0.11 (14/10/2020)
- first Xchange version

## 1.0.10
- update reducer for Android 4.4 compatibility
- fix bugs

## 1.0.9
- fix bug on notice view, bad number of consentable
- fix bug disable success screen
- improvements

## 1.0.8 (01/09/2020)
- refactor with new reducer
- translate progress loading
- geolocation view in fullscreen
- Kotlin `1.4`

## 1.0.7 (21/08/2020)
- fix bug switch status on scroll
- fix bug switch status in Stack detail view

## 1.0.6 (20/08/2020)
- fix bug on Theme
- fix switch alignment

## 1.0.5 (14/08/2020)
- fix bugs

## 1.0.4 (12/08/2020)
- fix bug with CTA

## 1.0.3 (10/08/2020)
- rename resource string folders
- map disable success screen to remote theme
- map CTA order to remote theme
- simplify `build.gradle` integration. Implementing `appconsent-core` is no more needed.

## 1.0.2 (31/07/2020)
- detail view of a Stack
- add legal description to consentable detail
- external links in banner view open in browser
- add a check for `cmp_hash` in `checkForUpdate` method and return `true` if no gvl version set
- fix bug on `consentableAllowed()`, `stackAllowed()` and `vendorAllowed()` 

## 1.0.1 (07/2020)
- load colors and images from remote config
- create custom Theme

## 1.0.0
- first release
