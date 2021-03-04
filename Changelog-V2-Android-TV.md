# AppConsent TV

## 1.1.3 (04/03/2021)
- fix consent string encode with restrictions

## 1.1.2 (02/03/2021)
- add google atp id feature

## 1.1.1 (01/03/2021)
- fix ui constraints for consent descriptions item

## 1.1.0 (26/02/2021)
- migrate kotlin-android-extensions to view binding
- add cookie expiration in vendor detail view for TCF 2.1 
- delete description already displayed above from ConsentableDetail header
- add legal dialog in ConsentableDetail
- fix leg vendor radio display
- encode ConsentString with flexible purposes

## 1.1.0-beta03 (22/12/2020)
- fix bugs and improve SDK

## 1.1.0-beta01 (11/12/2020)
- add `saveExternalIds()`
- fix bugs and improve SDK

## 1.0.0-RC07 (25/11/2020)
- update modifier of classes to internal which are unused by user
- add setExtraConsentableConsents(), extraVendorAllowed() and extraConsentableAllowed()

## 1.0.0-RC06 (20/11/2020)
- add a new AppConsentLogListener to log details about client navigation
- do not display partner view if no internet

## 1.0.0-RC05 (19/11/2020)
- fix issue when downgrading GVL version to notice

## 1.0.0-RC04 (17/11/2020)
- IABTCF_gdprApplies depends on `forceApplyGDPR` and phone's locale

## 1.0.0-RC03 (13/11/2020)
- fix focus on mandatory fragment

## 1.0.0-RC02 (29/10/2020)
- catch crash and if app restart kill process

## 1.0.0-RC (02/10/2020)
- update libraries
- fix save consent with empty cache

## 1.0.0-beta05 (22/09/2020)
- add back buttons on many views
- add intermediate view on back pressed on notice EDIT mode
- hide second view on notice if empty
- fix focus issue on accept all and refuse all
- fix logo display on vendor list
- improve tab layout navigation

## 1.0.0-beta04 (07/09/2020)
- transform radio button Accept/Refuse All to button
- fix bug on object action
- improve remote theme customization

## 1.0.0-beta03 (08/2020)
- fix radio focus bug with first element
- add background while radio is focus
- add local translation for 8 languages

## 1.0.0-beta02 (07/2020)
- fix bug when implement SDK UI and TV in same project 

## 1.0.0-beta01 (07/2020)
- implementation Core `1.0.2`
