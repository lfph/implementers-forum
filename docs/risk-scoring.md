# Risk Scoring

```
Please note that this section was written with the v1 APIs in mind. 
Much has been updated since, so please do make sure to check the documentation 
before moving forward. 
That being said, we still expect the context here to be of use.
```

## Exposure risk value

Before diving into attenuation, a little bit of an explanation around risk needs to be introduced.

From [Apple](https://developer.apple.com/documentation/exposurenotification/enexposureconfiguration):

> The ExposureNotification framework defines an Exposure Risk Value (ERV) to allow Health Authorities to define when to alert a user that they may have been exposed to someone diagnosed with COVID-19. The app uses the ERV to calculate the user’s Meaningful Exposure Minutes (MEMs) value. Health Authorities have flexibility in calculating this value by setting weights and values related to Bluetooth attenuations, infectiousness of the affected individual, and diagnosis report type. They can also determine what threshold will result in a notification.

![Apple's risk scoring diagram](https://docs-assets.developer.apple.com/published/97a2dade3a/rendered2x-1596473348.png)

As you can see, the "minutes at attenuation weight" is an important piece of what actually generates the exposure risk value. Those attenuation levels can be set by the PHA and implementation team to define how sensitive the app is to potential exposures.

## What is attenuation? 

The attenuation is essentially the sensitivity of the app. There are several "thresholds" set by the PHA which in turn define the attenuation buckets:

* Immediate
* Near
* Medium
* Other

Two critical elements of attenuation need to be defined: first, what the levels are between each bucket, and second, what weight to assign each bucket.

## What is infectiousness weight? 

Another key part of the risk scoring is the infectiousness weight. This takes when a person's symptoms began to try and understand how likely it is that they were infectious when the exposure occurred.

The current belief is that is that a person's infectiousness changes over the duration of their infection: 

* Little chance of spreading during incubation period, from initial infection until 3 days before symptoms appear
* Greater chance of infection starting two days before symptoms appear
* Most infectious on the day symptoms appear
* Infectiousness decreases as symptoms decrease

The framework allows us to specify a separate transmission risk level for each day. 

The faster test results can be turned around and thereby reported into the app, the less critical this infectiousness level becomes. However, for any region where test turnaround might not be immediate, making sure that the infectiousness level settings are set carefully is an important piece of fine-tuning the app setup.

![Infectiousness goes up for a period of time, then comes back down](https://dailybrief.oxan.com/g/oxweb/GI252631/2020-05-14-INT-covid-transmissions_1000.png)

The PHA has the ability to define when infectiousness moves from none to standard to high and back down again. As our understanding of transmission evolves, so should how these thresholds get set. Similar to attenuation, both thresholds and weights need to be set. 

## Resources

* [**Updates to the algorithm underlying the NHS COVID-19 app**](https://www.turing.ac.uk/blog/updates-algorithm-underlying-nhs-covid-19-app)
    * The Alan Turing Institute shares their approach to risk scoring with the latests in GAEN APIs
* [**Quantifying SARS-CoV-2 infection risk within the Google/Apple exposure notification framework to inform quarantine recommendations**](https://www.medrxiv.org/content/10.1101/2020.07.17.20156539v2)
    * Detailed research specific to GAEN apps out of the University of Arizona, focused on how to make sure risk settings match epidemiological and public health goals. This model is utilized by Covid Watch.
* [**Infection Spread and High-Resolution Detection of Close Contact Behaviors**](https://www.mdpi.com/1660-4601/17/4/1445)
* [**A technical roadmap for the UK’s contact tracing app functionality**](https://www.turing.ac.uk/blog/technical-roadmap-uks-contract-tracing-app-functionality)
    * For details on the UK perspective on risk scoring, worth following through to their [paper](https://arxiv.org/pdf/2005.11057.pdf) on the topic.
* [**Coronavirus Contact Tracing: Evaluating The Potential Of Using Bluetooth Received Signal Strength For Proximity Detection**](https://www.scss.tcd.ie/Doug.Leith/pubs/bluetooth_rssi_study.pdf)
    * An early study around bluetooth proximity detection
* [**SwissCovid Exposure Score Calculation**](https://github.com/admin-ch/PT-System-Documents/blob/master/SwissCovid-ExposureScore.pdf)
    * A detailed account of Switzerland's approach to risk scoring using the v1 APIs
* [**Google Exposure Notification API Testing, Fraunhofer IIS**](https://github.com/corona-warn-app/cwa-documentation/blob/master/2020_06_24_Corona_API_measurements.pdf)
    * A presentation from Germany summarizing some lab testing around the GAEN APIs
