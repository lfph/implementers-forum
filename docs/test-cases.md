# Test Cases

This section shares some of the learnings that other teams have had from testing an exposure notification app. 

## Exposure Notification is On

* **Backgrounding an app so it stays active**
    * It is likely that many of your users will not be opening the app on a frequent basis. Therefore the app may become inactive if no actions are taken. The test case should cover that the app is still checking for keys even if it has been backgrounded or closed for a long period of time.
    
## TEKs and RPIs

* [**Sample File**](https://github.com/minvws/nl-contact-tracing-odds-and-ends/tree/master/test-vectors/tek-rpi)
    * The Netherlands contributed a test file that generated both temporary exposure keys (TEKs) and associated rotating proximity indicators (RPIs) which can be used for various test scenarios.

## App Validation

Most jurisdictions launching an app have had a security and compliance review completed by a neutral 3rd party. This is strongly recommended - please contact a staff member at LFPH if you would like a referral to a group that can do this.

## Test in the Mornings

It takes a few hours for the alerts to come through, so as you're testing your system make sure to upload codes in the morning so that you can have the notifications appear during the workday. 
