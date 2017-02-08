# AdobeAnalytics-Core
The core components of a solid Adobe Analytics implementation.

## Contents

* [Background](#background)
* [Implementation](#implementation)
* [Report Suite Configuration](#report-suite-configuration)
* [Variable Design](#variable-solution-design)


## Background

Make no mistake about it, any great Adobe Analytics implementation will leverage a countless number
of customizations that best fit the individual needs of the organization. But at the same time, there are a set of core guidelines and best practices that can be followed for Adobe Analytics implementations that will help yield powerful analytical insights straight out of the box.

This project was created to help promote solid implementations as a foundational starting point. Because good, clean, and accessible data elements allow us all to become more insightful. Most of what is included can be taken generically across a variety of verticals, but keep in mind there are also an expanded set of best practices relevant to specific industries (for example: travel, media, and retail organizations will tend to focus on different performance metrics).

If you have any suggestions to improve what should be included in a solid basic (and general) implementation, I invite you to participate in this project.


## Implementation

It is highly recommended to implement a [W3C compliant data layer](https://www.w3.org/community/custexpdata/) and implement any Analytics tags through the use of a Tag Management System (TMS).


## Report Suite Configuration

**Best Practices**
* Report Suite Names should follow a similar pattern, and include "PROD" or "DEV" identifiers


## Variable Solution Design

### Value Guidelines
* Force lowercase to reduce any potential duplication issues
* Short values are better than long values, but don't sacrifice readability
* Notions of hierarchy and textual patterns are your friends (for simpler regex in the future)
* Use of the colon as a delimiter is preferable (the pipe can make regex slightly more complex)

### Core Dimensions
* Dimensions are captured in Adobe Analytics through a variety of variables. Some default (pagename, channel, campaign) and other custom (eVars, props, listvars).


**Page Identifiers**

dimension | Notes
--------- | -----
Page Name | Leverage hierarchy; lowercase  
Page URL  | More granular than pagename
Previous Page | Page name of previous page in session


**Site Search**

dimension | Notes
--------- | -----
Site Search Keyword | Force lowercase
Results Returned | Number of search results returned


**Technical Debugging**

dimension | Notes
--------- | -----
Browser User Agent | More granular browser/OS debugging
Code Deployment Date | Better debugging


**Time-Based Analysis**

dimension | Notes
--------- | -----
User Date | Time-based analysis. YYYY-MM-DD
User Time | Time-based analysis. HH:MM (24H clock)
