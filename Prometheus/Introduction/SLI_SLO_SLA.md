# SLI, SLO, & SLA:

When designing a system or applications, its important for teams to set specific measurable targets/goals to help organizations strike the right balance between product development and operation work.

These targets help customers & end users quantify the level of reliability they should come to expect from a service "Application should have 97% uptime in a rolling 30 day window".

****SLI:****

Service Level Indicator(SLI)– quantitative measure of some aspect of the level  of service that is provided
Common SLIs:
• Request Latency
• Error Rate
• Saturation
• Throughput
• Availability

Not all metrics make for good SLIs. You want to find metrics that accurately measure a user’s experience.
Things like high-cpu/high-memory make for a poor SLI as a user might not see any impact on their end during these events.

****SLO:****

Service Level Object(SLO)– target value or range for an SLI

SLI- Latency
SLO– Latency < 100ms

SLI– availability
SLO– 99.9% uptime

SLOs should be directly related to the customer experience. The main purpose of the SLO is to quantify reliability of a product to a customer.

The goal is not to achieve perfection but instead to make customers happy with the right level of reliability

****SLA:****

Service Level Agreement(SLA)– contract between a vendor and a user that guarantees a certain SLO.

The consequences for not meeting any SLO can be financial-based, but can also be a variety of other things as well.

****Usecase#1****

Several outages have occurred due to high memory on the server hosting a MySql database.

The operations team would like to be notified through email when the memory gets to 80% max capacity so that proactive measure can be taken.


****Usecase#2****

A new video upload feature has been added to the website, however there is some concerns about users uploading too large of videos.

The team would like to find out at which video length the applications starts to degrade and to do this, they need a chart plotting the avg file size of upload and the average latency per request.
