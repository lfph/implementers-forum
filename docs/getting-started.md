# Getting Started

The Implementer's Forum supports the Google Apple Exposure Notification API (GAEN). Both [Google](https://www.google.com/covid19/exposurenotifications/) and [Apple](https://developer.apple.com/documentation/exposurenotification) have extensive documentation on their particular version of the API.

## An introduction to GAEN and exposure notification

There have been a number of useful introductions to GAEN and exposure notification to help you learn more about the technology and its applications: 

* [**COVID-19 Case Investigation and Contact Tracing: Considerations for Using Digital Technologies**](https://www.astho.org/ASTHOReports/COVID-19-Case-Investigation-and-Contact-Tracing-Considerations-for-Using-Digital-Technologies/07-16-20/), ASTHO.
* [**How Covid-19 Contact Tracing Works on Your Phone**](https://www.wired.com/story/covid-19-contact-tracing-apple-google/), Wired Magazine
* [**Demystifying the 60% in Exposure Notification**](https://www.lfph.io/2020/08/21/demystifying-the-60/), LFPH. There have been a number of questions around the necessary level of adoption needed in order to see an effect from exposure notification technologies. For a summary of the latest research, please see this blog post.

<div class="video-wrapper">
    <iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/1Cz2Xzm6knM" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

## Steps for public health authorities to launch

| Step     | Action          | Purpose  |
| ---------|:-------------| :------------------|
| 1 | Develop iOS & Android User-Facing Apps | Enable Bluetooth key exchange; Provide the user interface for exposure notification system |
| 2 | Identify & Connect to the Key Server      | Store the non-identifiable Bluetooth keys of users with verified positive diagnosis |
| 3 | Determine & Implement Positive Test Verification Methodology    | Enable verification of positive test on app |
| 4 | Define Meaningful Exposure | Determine which exposures warrant a notification |
| 5 | Define Next Steps for Contacts      |   Determine what next steps to provide to exposed users |
| 6 | Integrate with existing CRM solution      | Enable contact tracers to accelerate outreach |
| 7 | Launch a Public Awareness Campaign | Maximize public participation |

Source: [Google](https://youtu.be/H4YHvWvIwV4?t=1182)

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

It is best for the PHA to create their own developer account and give the technology team access to it so that the public sees the PHA as the company publishing the app rather than a tech company publishing the app. This will add another level of credibility to support the adoption of the app.

## Pick your codebase

One of the first decisions an implementation team needs to make in conjunction with its PHA is what codebase to use for the app. The factors to consider when choosing a codebase are:

* **Level of customization** Some PHAs want to have the app built from scratch for them and therefore completely customizable. Others want to build on the research and work done by others. Note that the greater level of customization, the more time it will take the implementer to build.
* **Support strategy** What level of support will the implementer be providing in the long term? Using an open-source codebase means that a team of maintainers will be updating the app as the API changes, allowing downstream apps to take advantage of this work. A fully custom app will require the implementation team to keep abreast of all API changes and update the app accordingly.
* **Additional Features Required** Some jurisdictions require the app to literally do nothing except exposure notification, while others want the app to be able to provide basic information on COVID-19 or disease progression in the community. Yet other PHAs would like to be able to add new modules in the future, such as services to assist those in self-isolation.

We strongly recommend using an open source codebase for your app to increase transparency and trust with your users. LFPH supports the following open source projects:

* [**COVID Shield**](https://github.com/CovidShield), used by Canada
* [**COVID Green**](https://github.com/covidgreen), used by Ireland, Northern Ireland, Gibraltar

## Key terminology

It is imperative that we are precise as we communicate about exposure notification technologies.
Even slight mischaracterizations can undermine efforts to build trust amongst the public.
Here, we aggregate some key terms, their meanings, and the context in which they are typically used.

| **Term** | **Definition** | **Context** |
|------|------------|---------|
| **Anonymous identifiers** | Unique values that do not carry personally identifying information nor can they be used to identify an individual | In exposure notification applications, anonymous identifiers are broadcast to devices whose proximity has led to a contact event. |
| **Contact event** | When two users have been within certain proximity for a specified amount to time | The proximity distance and specified amount of time are typically defined by the relevant public health agency. An example of a contact event could be when two people are within 6 feet of each other for 15 minutes. Within EN apps, events that do not meet the criteria are not recorded. |
| **Contact tracing** | A (typically manual) process for recording and notifying people who an infected person has come in to contact with | This term should be used to refer to the manual process, not to exposure notification applications as these applications do not track or trace users and their contacts |
| **Exposure notification (EN) apps** | Applications built for exposure notification | There are a variety of strategies which can be leveraged to aid in the containment of COVID-19 spread. Exposure notification in particular aims to notify users who may have had an exposure to someone who has tested positive. Typically, they do not provide contact tracing or other capabilities. |
| **GAEN** | Google/Apple Exposure Notification | You will often see this referring to the GAEN API (Application Programming Interface) or the GAEN Framework, technologies provided by Google and Apple to be used by development teams to build apps with the ability to perform private proximity detection and alerting. |
| **Implementer** | The team that is responsible for the technical execution of the exposure notification app | Usually, but not always, this is a technology firm hired by the PHA. |
| **PHA** | Public Health Authority | PHAs are typically associated with the government of a certain locality. |
| **Proximity** | A measure of distance between items, not associated with location | EN apps measure the proximity between smartphones to understand whether a contact event has occurred. This allows notification of potential exposure without having to collect user locations. |
| **LFPH** | Linux Foundation Public Health | As an open source community, Linux Foundation's new Public Health initiative combines efforts of multiple groups working toward privacy-preserving technologies, initially geared toward technology to aid in the fight against COVID-19. |
| **Surveillance** | Monitoring or observing activity | Epidemiologists sometimes use this term to refer to their work to understand the spread and containment of a virus. Even though EN apps can aid in containment efforts, privacy-preserving apps do not perform surveillance from a technology perspective as they do not collect, track, or record user location or activity. |
| **Tracing** | The process of understanding the prior contacts of a person who has tested positive; see also: contact tracing, tracking | Manual contact tracers typically work to collect information about an individuals activities in the relevant timeframe, i.e. tracing their potential contacts. EN apps collect relevant contact events locally on a user's device, but do not follow, trace, or share data about a user's activities. |
| **Tracking** | This generally refers to recording activity data about a user such as location; see also: contact tracing, tracing | EN apps do not track users. Contact events are recorded locally on the user's device and are not shared. Location data is not collected. |
