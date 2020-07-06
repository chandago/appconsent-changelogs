# AppConsent Android SDK

## v2.3.17 (07/2020)
- if an new version of GVL is detected in `checkForUpdate()`, you can now call `presentNoticeActivity(false)` to display notice and re-ask consents like the first time

## v2.3.16 (05/2020)
 - fix bug on xchange, to get device mac address

## v2.3.15 (04/2020)
 - fix crash on `shareUserLocation()`

## v2.3.14 (04/2020)
 - when call `startHuq()` locations permissions are not asked to user
 - add AppConsentError and return more specific errors in callbacks

## v2.3.13 (03/2020)
 - add Huq SDK to Xchange
 - fix bug request location permission

## v2.3.12 (03/2020)
 - add `android.permission.ACCESS_BACKGROUND_LOCATION` permission to allow Android 10 devices to get background geolocation
 - fix bug on single step
 - fix bug on some devices to get location

## v2.3.11 (01/2020)
 - check GDPR country list before displaying notices and send xchange datas
 - fix bug on injection
 
## v2.3.10 (01/2020)
 - reduce text size
 - add `isIABPurposeAllowed` and `isIABVendorAllowed` 
  
## v2.3.9 (12/2019)
 - update default languages management by adding tags on strings.xml files
 - make getPackagesInstalled configurable and set to false by default
 
## v2.3.8 (12/2019)
 - update SSL error management in WebView to avoid play store warning
 
## v2.3.7 (12/2019)
 - filter Location in db with a unique timestamp
 - update EN and FR strings.xml
 - try catch methods to generate xchange data
 - update deprecated code to generate xchange data
 
## v2.3.6 (12/2019)
 - store packages installed in preferences
 - send timestamps in milliseconds
 - avoid theme singleton to crash if instance is null
 - change partners link color
 - add copyright at the bottom of configuration activity
 
## v2.3.5 (11/2019)
 - fix notConsentableVendors visible in geo purposes but force to consentable
 - fix notConsentableVendors not count for purpose status
 
## v2.3.4 (11/2019)
 - change theme name to avoid conflicts with AppThemes
 - update xchange payload
 - fix bug on accelerometer an signalStrength listener

## v2.3.3 (11/2019)
 - update default local translation for DE ES IT NL PL PT
 - remove EN as default language from remote config
 - resize views as dialog for tablets
 
## v2.3.2 (11/2019)
 - fix bug on geolocation banner with cta scrolling
 - migrate prime code to xchange
 - add title on geolocation activity
 
## v2.3.1 (10/2019)
 - manage leg vendors for extra purposes
 - use EN as default language if default locale text is not found
 - update IntroductionActivity for understood feature
 - fix bug on vendor hashcode method
 
## v2.3.0 (10/2019)
 - migration to androidx
 
## v2.2.7 (09/2019)
 - filter extra purposes not geo before sending it to store
 - fix geolocation notice callback when more than 1 purpose
 - fix bugs
 - add translatable text
 - add link to display current vendors
 - remove geolocation permissions

## V2.2.6 (09/2019)
 - increase buttons height to avoid miss click
 - fix bug geolocation refresh data 

## v2.2.5 (09/2019)
 - fix bug with single step and extra purposes
 - fix ui geoloc see more text
 
## v2.2.4 (08/2019)
 - add feature single step inline (Meteoconsult)
 - can edit introduction title (cmp iab)
 - icon IAB and Geoloc are same size
 - can put geoloc banner to bottom of geoloc purpose list

## v2.2.3 (08/2019)
 - fix crash on API 19 devices and lower
 - fix policy url on click

## v2.2.2 (07/2019)
 - add log for sample app
 - fix vectaury's log on user demand
 - fix extra purposes and vendors storage for banner
 
## v2.2.1 (07/2019)
 - fix bug with single step callback
 - fix bug on status bar default color
 - fix copyright background color

## v2.2.0 (07/2019)
 - single step UI
 - fix bugs on extra vendors

## v2.1.3 (06/2019)
 - fix bug on text translation
 - update extra vendors management
 - fix bug on default remote theme value

## v2.1.2 (06/2019)
 - fix bug on `consentGiven()`
 - fix bug with translations

## v2.1.1 (06/2019)
 - remove functions from app consent theme
 - merge picture from local and remote config theme

## v2.1.0 (06/2019)
 - A/B test
 - fix bugs

## v2.0.1 (05/2019)
 - fix bug get text from customisation in finish activity
 - fix purpose view for customisation
 - fix refresh adapter in configuration activity on resume

## v2.0.0 (04/2019)
 - fix bugs
 - remote config

## v1.6.0 (04/2019)
 - switch to new architecture
 - update TU

## v1.5.12 (04/2019)
 - set call timeout to 2 sec
 
## v1.5.11 (04/2019)
 - fix timeout issues
 - fix geoloc purposes and vendors bug and add mixe state
 
## v1.5.10 (04/2019)
 - hide geolocation purpose icon on configuration activity

## v1.5.9 (04/2019)
 - allow clickable links on introduction and geolocation activities
 - add displayConfigCloseHeader on theme

## v1.5.8 (04/2019)
 - fix bug touch listener on switch
 - replace scrollview by nested scroll view in geolocation activity

## v1.5.7 (04/2019)
 - fix crash on `setGeolocPurposesAuthorization()`
 - highlight accept button
 - refresh switch in vendor list

## v1.5.6 (04/2019)
 - fix bug purpose Null ArrayList 

## v1.5.5 (03/2019)
 - improve switch button behavior

## v1.5.4 (03/2019)
 - fix `extraPurposeAllowed()`

## v1.5.3 (03/2019)
 - fix bug extras vendors list null
 - fix bug save consent, reset geolocation consent
 - rename `withDisplayVendorsByDefault()` to `showVendorsByDefault()`
 - create function `setGeolocPurposesAuthorization()` to init SDK with yours geolocation consents
 - update `presentNoticeActivity()` and `presentNoticeBanner()` to check expiration date
 - clear consent if Idfa change

## v1.5.2 (03/2019)
 - add vendorTitleListText to AppConsentTheme

## v1.5.1 (03/2019)
 - handle multiple geoloc purposes
 - `geolocationAllowed` deprecated

## v1.5.0 (01/2019)
 - update `build.gradle` to generate version code in function of version name
 - add `BASE_URL`, `VENDOR_LIST_URL`, `STATUS_PATH` to `build.gradle`
 - move consent keys in public constants
 - add `gitlab-ci.yml` : add `build` and `test` stages
 - shrink SDK
 - save last successful call to `getNotice` and `GVL` and use it in case of slow or unreachable network
 - show vendors by default in usage page + allow client app to set it has hidden
 - fix crash on devices < API 19, TLS exception
 - add `onBoardingIntroduction(@StringRes int resId)` in `AppConsentTheme`, to customize Notice with clickable links
 - add buttons `Refuse All` and `Accept All` in purpose list (from `getNotice()`)
 - Notice buttons and banner buttons are ordered from back office
 
