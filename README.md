# AdobeAnalytics-Core
The core components of a solid Adobe Analytics implementation.

## Contents

* [Background](#background)
* [Implementation](#implementation)
* [Report Suite Configuration](#report-suite-configuration)
* [Variable Design](#variable-solution-design)
  * [Value guidelines](#value-guidelines)
  * [Core Dimensions](#core-dimensions)


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
* Don't overload variables containing ID values

### Core Dimensions
* Dimensions are captured in Adobe Analytics through a variety of variables. Some default (pagename, channel, campaign) and other custom (eVars, props, listvars).


#### Page Identifiers

dimension | format
---: | :---
Page Name | lowercase, colon delimiter
Page Type | lowercase
Page URL  | lowercase, filter irrelevant query parameters
Previous Page | same as page name



#### Site Search

dimension | format
---: | :---
Search Keyword | lowercase
Search Result Size | integer



#### Technical Debugging

dimension | format
---: | :---
Code Deployment Date | YYYY-MM-DD
User Agent | More granular browser/OS debugging



#### Time-Based

dimension | format
---: | :---
User Date | YYYY-MM-DD
User Time | HH:MM (24H)
