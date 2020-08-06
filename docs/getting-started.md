# Getting Started

The Implementer's Forum supports the Google Apple Exposure Notification API (GAEN). Both [Google](https://www.google.com/covid19/exposurenotifications/) and [Apple](https://developer.apple.com/documentation/exposurenotification) have extensive documentation on their particular version of the API.

## An introduction to GAEN and exposure notification

There have been a number of useful introductions to GAEN and exposure notification to help you learn more about the technology and its applications: 

* [**COVID-19 Case Investigation and Contact Tracing: Considerations for Using Digital Technologies**](https://www.astho.org/ASTHOReports/COVID-19-Case-Investigation-and-Contact-Tracing-Considerations-for-Using-Digital-Technologies/07-16-20/), ASTHO.
* [**How Covid-19 Contact Tracing Works on Your Phone**](https://www.wired.com/story/covid-19-contact-tracing-apple-google/), Wired Magazine

## Obtaining an entitlement

In order to begin development against the API, a team needs an **entitlement**. Developers are not allowed access to these APIs without an entitlement. Entitlements are only given to Public Health Authorities (PHAs) and the teams that are officially working with them to build exposure notification apps. The PHA has to be at the state or national level and the letter likely needs to come from the PHA's office or the executive office of the jurisdiction (i.e. the governor, president, or head minister).

To obtain an entitlement, the PHA needs to submit a letter to Apple and Google according to the following:

* On the official letterhead of the PHA or government executive's office.
* Specify the jurisdiction that the PHA is requesting the entitlement for
* State who within the PHA or government office is requesting the entitlement, and what their role is
* Share the organization of the implementer who needs an entitlement
* Include the date

To simplify this, we have a [template](https://github.com/lfph/exposure-notification-playbook/blob/master/entitlement.md) available which can be used on the PHA letterhead.

The letters for each company need to be submitted via a form on their websites:

* [Google](https://support.google.com/googleplay/android-developer/contact/expo_notif_api)
* [Apple](https://developer.apple.com/contact/request/exposure-notification-entitlement)

## Pick your codebase

One of the first decisions an implementation team needs to make in conjunction with its PHA is what codebase to use for the app. The factors to consider when choosing a codebase are:

* **Level of customization** Some PHAs want to have the app built from scratch for them and therefore completely customizable. Others want to build on the research and work done by others. Note that the greater level of customization, the more time it will take the implementer to build.
* **Support strategy** What level of support will the implementer be providing in the long term? Using an open-source codebase means that a team of maintainers will be updating the app as the API changes, allowing downstream apps to take advantage of this work. A fully custom app will require the implementation team to keep abreast of all API changes and update the app accordingly.
* **Additional Features Required** Some jurisdictions require the app to literally do nothing except exposure notification, while others want the app to be able to provide basic information on COVID-19 or disease progression in the community. Yet other PHAs would like to be able to add new modules in the future, such as services to assist those in self-isolation.

We strongly recommend using an open source codebase for your app to increase transparency and trust with your users. LFPH supports the following open source projects:

* [**COVID Shield**](https://github.com/CovidShield), used by Canada
* [**COVID Green**](https://github.com/covidgreen), used by Ireland, Northern Ireland, Gibraltar
