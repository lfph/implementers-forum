# Test Cases

This section summarizes the critical paths that need to be covered in testing an exposure notification app. 

## Exposure Notification is On

* **Backgrounding an app so it stays active**
    * It is likely that many of your users will not be opening the app on a frequent basis. Therefore the app may become inactive if no actions are taken. The test case should cover that the app is still checking for keys even if it has been backgrounded or closed for a long period of time.
    