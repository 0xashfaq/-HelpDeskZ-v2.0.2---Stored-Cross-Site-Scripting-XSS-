### HelpDeskZ-v2.0.2 Stored Cross Site Scripting XSS

### Vulnerability Description:

Cross-site scripting (XSS) is a security vulnerability that allows an attacker to inject malicious scripts into web applications. These scripts can lead to severe consequences, such as session hijacking, defacement, or redirection to malicious sites.

In HelpDeskZ v2.0.2, an attacker can exploit an XSS vulnerability by injecting malicious code into the field name of a custom field. This code executes within the context of the administration panel, leading to potential security breaches.

### Payload:
"><img+src=x+onerror=alert(1)>

### Steps to Reproduce:

* Log in as a normal user.
* Navigate to Tools > Custom Fields > New custom field.
* Fill out the required fields and click on Submit.
* Capture the request using Burp Suite or a similar tool.
* Modify the title field with the following payload: "><img+src=x+onerror=alert(1)>
* Forward this modified request.
* Go to Tools > Custom Fields on the user panel to observe the XSS execution.

### POC URL
https://github.com/0xashfaq/-HelpDeskZ-v2.0.2---Stored-Cross-Site-Scripting-XSS-/blob/9c8618634f9b7b3601c5b7d8fc4ae21a076db215/2024-08-14%2021-09-00.mp4
