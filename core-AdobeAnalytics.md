# AdobeAnalytics-Core

Recommended Adobe Analytics variables to leverage in most all solution designs.

## Contents

* [Report Suite Configuration](#report-suite-configuration)
* [Variable Design](#variable-solution-design)
  * [Value guidelines](#value-guidelines)
  * [Core Dimensions](#core-dimensions)


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
* In almost all cases, it makes sense to force these values to lowercase. This will help minimize duplication issues that might otherwise arise.


#### Page Identifiers

dimension | notes
---: | :---
Page Name | hierarchical; colon delimiter
Page Type |
Page URL  | exclude irrelevant query parameters
Previous Page | same format as page name


#### User Identifiers

dimension | notes
---: | :---
Adobe Visitor ID | make accessible to reporting
Browser User Agent | More granular debugging
User Date | YYYY-MM-DD
User Time | HH:MM (24H)


#### Site Search

dimension | notes
---: | :---
Search Keyword |
Search Result Size | integer


#### Technical Debugging

dimension | format
---: | :---
Code Deployment Date | YYYY-MM-DD
