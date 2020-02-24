# AppConsentKit SDK changelogs

## Version 2.3.8

### Changes
* SFBX name in copyrights

## Version 2.3.7

### New features
* XChange SDK

## Version 2.3.6

### Changes
* Copyright in *on user demand* screen.

## Version 2.3.5

### Fix
* iPad modale could have a broken size when app was built with Xcode 10.1 and app running on iOS 13.

## Version 2.3.4

### New features
* The CMP does not start if the device's region is not inside EU. Can be ignored.
* `shouldPresentGeolocationNotice()` method.
* Methods to get IAB vendors and purposes status

### Changes
* The `shouldPresentNotice` var is now a method

## Version 2.3.3

### New features
* Added languages: de, es, it, nl, pl, pt

### Fix
* Use `BUILD_LIBRARY_FOR_DISTRIBUTION` set to `YES` to make the Swift 5.1 library compatible with Swift 5.1.2

## Version 2.3.2

### New features
* Optional title in geoloc notice, can be set from the back-office.

### Changes
* Do not trigger an error when network store fails but only if local store fails.

### Fix
* On not consentables extra vendors, when re openning notice auth could be passed to `true`.

## Version 2.3.1

### New features
* Extra vendors can have purposes for which they are on legitmitate interest
* The notice can be displayed in *legitimate interest* mode

## Version 2.3.0

### New features
* Texts for headers in notice can be customized from back-office
* Clickable link to display vendors list in notice and geolocation notice

### Changes
* Geolocation notice presented in 'Form Sheet' on iPad

## Version 2.2.3

### Fix
* Swift 5.0 compatible build

## Version 2.2.2

### Changes
* iOS 13 support
* In geolocation notice, the optional 'View more' text is above the list of purposes

## Version 2.2.1

### New features
* When in single step, the CTAs in the notice onboarding can scroll
* The CTAs in the geolocation notice can scroll
* The icon in the geolocation notice has been moved into scroll and can be enlarged
* The title of the onboarding page can be changed by the client app

### Fix
* Fix a possible crash due to Appeareance selectors usage

## Version 2.2.0

### New features
* Allow single step
* Save a dictionary in `UserDefaults` so third parties SDKs can read
extra purposes states values

### Changes
* Extra vendors which does not have an authorization are pre set based
on the extra purpose state

## Version 2.1.4

### Changes
* Re build for swift 4.2

## Version 2.1.3

### Fix
* Swift 4.2 compilation was broken

## Version 2.1.2

### Fix
* In geolocation notice, get the consents by vendors when needed
* Getting consents by vendors also applies to extra purposes

## Version 2.1.1

### Fix
* If no AppIcon was set, the space was still reserved but empty 
on success screen and onboarding screen

## Version 2.1.0

### New features
* Methods to get IAB values from `AppConsent` class.
* A/B Testing

### Fix
* Double optional in `AppConsentDefaultCustomization` init when
accessing images from assetsProvider.

## Version 2.0

### New features
* Customization from back-office

### Changes
* Start SDK with a notice URL pointing to a json file on our CDN
* Purposes that does not come from GVL are not sorted anymore
* Do not use local pubvendors or extra vendors anymore
* Delegate returns a `AppConsentCMP` object to present notice on a view controller
* Protocols for custiomization removed, except for images with new protocol `AppConsentAssetsProvider`.

### Removes
* Web mode for notice removed

## Version 1.5.8

### Changes
* Geoloc icon removed in notice

## Version 1.5.7

### Changes
* The 'close' button in the notice header is hidden

## Version 1.5.6

### Fix:
* Compilation for simulator in objc projects was broken

## Version 1.5.5

### Changes
* **Accept all** buttons are highlighted
* In geoloc notice, text is above purposes

### Fix: 
* Banner theming could be broken

## Version 1.5.4

### Changes
* Swift 5 + iOS 12.2 build

## Version 1.5.3

### Changes
* Synchrnonize method doesn't have a `delegate` parameter anymore.

### New features
* Method to set multiple extra purposes consents (one with delegate, one with completion handler)
```
AppConsent.setGeolocPurposesAuthorization(["foo": true, "bar": false]) { err in
    print(err?.localizedDescription ?? "set geo purposes auth: no error")
}
```

## Version 1.5.2

### Changes
* In notice onboarding, buttons are now 'accept/deny' instead of 'accept all / deny all'

### Fixes
* In notice for geolocation purposes, theming could be applied wrong

## Version 1.5.1

### New features
* Handle extra vendors list from our own CDN
* Handle multiple geoloc purposes (GEOLOC_MARKET) added

### Changes
* `setGeoAdvertizing` method in `AppConsent` is now `setGeolocConsent` and set consent for all geoloc purposes

## Version 1.5.0

### New features
* Support of testing back platforms

### Changes
* Less delegate methods to implement for simpler integration

## Version 1.4.2

### New features
* Labels in onboarding screen and geo notice support `https` links detection and markdown type format
* Support banner buttons custo from backoffice


### Changes
* Offline mode also cache responses for `getNotice` and `gvl` so the last version is always used in case of bad network
 
## Version 1.4

### Fixes
* Geoloc consent could be invalid if user identifier changed
* The `syncrhonize` completion closure is always called on main thread
* Present and dismiss geo notice on main thread

### New features
* Offline support
* Uses IDFA as identifier if available, fallback on custom UUID otherwise

## Version 1.3

* Extra purposes and extra vendors support
* Banner and notice for geolocation for advertising purpose
* Theming and customizable texts
* Informational header with customizable text in notice
* Pubvendors support

## Version 1.2

### New features
* The *acceptAll* feature uses a specific protocol for delegation, `AppConsentAcceptAllDelegate`. 
* Can synchronize the IAB values stored in `UserDefaults` with the consents from the backend API.
* Can synchrnoize the notice GVL version. Updating the GVL version results in `shouldPresentNotice` to become true.

### Main features
* Present a native notice
* Present a web notice
* Can perform an *acceptAll* call
