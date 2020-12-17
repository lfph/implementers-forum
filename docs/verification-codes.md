# Verification Codes and Notification Messages

Verification codes are the alphanumeric codes sent to people who have tested positive so that they can upload their keys and alert others who may have been exposed. It has become clear through the deployment of these systems that making it as seamless as possible to receive and upload a code after a positive test result is a critical piece of making any EN system work.

## Important consideration for health equity and inclusion

For many people, a positive test result is a very emotional and stressful moment. Many people receiving these notifications may know someone who passed away from COVID-19. Try as much as possible to accompany these messages with a human touch and quick follow-up from a case investigator. For more on this topic, visit [equity and inclusion](/equity-and-inclusion.md).

## The "Colorado method" 

This verification code process has come to be called the "Colorado method", though other states and countries have also separately implemented similar systems. The basic idea behind this is that the code issuance is integrated as closely as possible with a state's electronic laboratory reporting (ELR) system. Phone numbers are collected at the time of testing so that as soon as a positive test result is confirmed the text can go out without the need for any further action from a human being.

Colorado has open-sourced its integration between Twilio and the APHL server for other states in the US to use. [**You can view their code here**](https://github.com/coloradodigitalservice/aphl-send-verification-codes).

One state that has used this system have seen a 60% uptick in submitted codes as a result of making this process easier.

## Verification Messages

The message that gets sent out with the verification code varies from one jurisdiction to another. Anywhere you see a string of random letters on a URL note that that is to test message length. Where it says `PHA` is where a jurisdiction should sign with the name of the ministry or department of health name.

* APHL verification server default
     * `Your Exposure Notifications verification link: https://us-xx.en.express/v?c=asdfasdfasdfasdf. Expires in 24 hours (click for mobile device only)`
* Colorado
     * `Anonymously share your COVID test to CO Exposure Notifications & help your community. Your link https://us-xx.en.express/v?c=asdfasdfasdfasdf —PHA.`
* 

## TCPA Compliance

For US jurisdictions, *please consult with your legal team about TCPA compliance* in sending these messages. LFPH is unable to provide legal advice on this topic, but we have found resources online that indicate that these verification messages are compliant with TCPA because they are related to lab results, have a non-marketing purpose, and are concise. Beyond that, it is worth considering that there are HELP and STOP responses available for people to get assistance and opt out. (Sources: [Adventist Health Care](https://www.adventisthealthcare.com/terms-service/tcpa-policy-for-sms-communications/), [Holland and Hart](https://www.hollandhart.com/pdf/TCPA-Health-Law-Webinar-Slides.pdf), [WyrickRobbins](https://assets.hcca-info.org/Portals/0/PDFs/Resources/Conference_Handouts/Compliance_Institute/2016/404print2.pdf).)

## Exposure Notification Messages

Here are the messages different jurisdictions send out once someone receives a potential exposure notification. The critical piece here is to direct the person receiving the notification to further resources and information around testing and quarantine, including any support available to them for financial and logistical assistance (grocery delivery, etc.).

* Nevada
     * **Potential Exposures** on _date_: You were in close proximity to someone for X minutes who tested positive for COVID-19.
     * They then provide a phone number to the department of health, a symptom checker, and additional information. They request that anyone who receives an exposure notification reports it to the department of health.
* Arizona
     * Arizona reports multiple levels of exposure and different instructions accordingly.
     * **Some Exposure** in the past 14 days: The app detected someone who tested positive for COVID-19. Monitor for symptoms. (link to symptom checker) The exposure was not near enough for long enough to recommend quarantine. If you have COVID-19 symptoms, call ###-###-####. Learn how to protect yourself and others. (link)
     * **High Exposure** in the past 14 days: Stay at home and self-quarantine until _date_. (link to more information) Call ###-###-#### and schedule a COVID-19 Test for _date based on likelihood of testing positive based on date of exposure_. Monitor for COVID-19 symptoms and get tested ASAP if symptoms appear. (link to symptom checker) Register with _jurisdiction's_ contact tracing team. (link)
* Washington state
     * **You may have been exposed to COVID-19**: You have been near someone in the past 14 days who tested positive for COVID-19. Tap to learn more.
* Minnesota
     * **Someone you were nearby has since tested positive for COVID-19**.
     * This then leads directly into a screen with FAQ and guidance. 
* Scotland
     * **IMPORTANT: Close Contact Alert**: You have been in close contact with someone who has COVID-19. Tap here to open the app and find out what to do.