# AppConsentKit SDK changelogs

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
* Use `getConsentsByVendors` when needed in geo notice too
* `getConsentsByVendors` also have a parameter for extra purposes

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
* Support of `feature` back platforms

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
* Uses IDFA as identifier is available, fallback on custom UUID otherwise

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


## Version 1.1

The changelog starts here. Previous versions won't be documented in this document.

### Main features
* Present a native notice
* Present a web notice
* Can perform an *acceptAll* call
