# About

Linux Foundation Public Health hosts the GAEN Implementers Forum, a resource and community designed to help various teams working with Public Health Authorities (PHAs) implementing Google Apple Exposure Notification API (GAEN) apps in their communities.

This resource is designed to help you get access to the wisdom and experience of others working on this same challenge around the world.

[Learn more about the Implementer's Forum](https://www.lfph.io/community/implementers-forum/)

[LFPH GitHub](https://github.com/lfph)

## Countries and states with GAEN apps

See the [LFPH Landscape](https://landscape.lfph.io/category=gaen-bluetooth&format=card-mode&grouping=category)

## Key terminology

It is imperative that we are precise as we communicate about exposure notification technologies.
Even slight mischaracterizations can undermine efforts to build trust amongst the public.
Here, we aggregate some key terms, their meanings, and the context in which to use them.

| **Term** | **Definition** | **Context** |
|------|------------|---------|
| **Anonymous identifiers** | Unique values that do not carry personally identifying information nor can they be used to identify an individual | In exposure notification applications, anonymous identifiers are broadcast to devices whose proximity has led to a contact event. |
| **Contact event** | When two users have been within certain proximity for a specified amount to time | The proximity distance and specified amount of time are typically defined by the relevant public health agency. An example of a contact event could be when two people are within 6 feet of each other for 15 minutes. Within EN apps, events that do not meet the criteria are not recorded. |
| **Contact tracing** | A (typically manual) process for recording and notifying people who an infected person has come in to contact with | This term should be used to refer to the manual process, not to exposure notification applications as these applications do not track or trace users and their contacts |
| **GAEN** | Google/Apple Exposure Notification | You will often see this referring to the GAEN API (Application Programming Interface) or the GAEN Framework, technologies provided by Google and Apple to be used by development teams to build apps with the ability to perform private proximity detection and alerting. |
| **Implementer** | The team that is responsible for the technical execution of the exposure notification app | Usually, but not always, this is a technology firm hired by the PHA. |
| **PHA** | Public Health Authority | PHAs are typically associated with the government of a certain locality. |
| **Proximity** | A measure of distance between items, not associated with location | EN app measure the proximity between smartphones to understand whether a contact event has occurred. This allows notification of potential exposure without having to collect user locations. |
| **LFPH** | Linux Foundation Public Health | As an open source community, Linux Foundation's new Public Health initiative combines efforts of multiple groups working toward privacy-preserving technologies, initially geared toward technology to aid in the fight against COVID-19 |
| **Surveillance** | Monitoring or observing activity | Epidemiologists sometimes use this term to refer to their work to understand the spread and containment of a virus. Even though EN apps can aid in containment efforts, privacy-preserving apps do not perform surveillance from a technology perspective as they do not collect location, track, or record user activity. |
| **Tracing** | The process of understanding the prior contacts of a person who has tested positive; see also: contact tracing, tracking | Manual contact tracers typically work to collect information about an individuals activities in the relevant timeframe, i.e. tracing their potential contacts. EN apps collect relevant contact events locally on a user's device, but do not follow, trace, or share data about a user's activities. |
| **Tracking** | This generally refers to recording activity data about a user such as location; see also: contact tracing, tracing | EN apps do not track users. Contact events are recorded locally on the user's device and are not shared. Location data is not collected. |


## News

* LFPH GAEN Symposium, July 16, 2020
    * We hosted a symposium for the exposure notification community - view [notes](https://github.com/lfph/events/tree/master/2020-07-GAEN-Symposium) and [videos](https://www.youtube.com/playlist?list=PLLUsXRAaict7U00sMcwdLWwPPfRwpnMs5).

### Code of conduct

All contributors to the Implementer's Forum are expected to follow the LFPH [Code of Conduct](https://github.com/lfph/foundation/blob/master/code-of-conduct.md).

### Contact

For further questions and support please contact [jenny@lfph.io](mailto:jenny@lfph.io).
