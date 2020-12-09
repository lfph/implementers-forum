# Risk Scoring

LFPH in conjunction with Apple, Google, and the CDC hosted a working group to come up with recommendations on how PHAs should set up their risk scoring settings.

[**You can view the full recommendations here.**](https://github.com/lfph/gaen-risk-scoring/blob/main/risk-scoring.md)

## Additional Resources

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

## Data Sets

These data sets contain bluetooth attenuation data for those who want to run their own calculations. 

* [**DP3T Bluetooth Measurements**](https://github.com/DP-3T/bt-measurements)
* [**NHSX GAEN Data**](https://github.com/nhsx/gaen_data-public)
