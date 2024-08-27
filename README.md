# Performance Testing with JMeter and Fiddler

## Table of Contents

- [Overview](#overview)
- [User Scenario](#user-scenario)
- [Setup Instructions](#setup-instructions)
  - [Pre-Requisites](#pre-requisites)
  - [Traffic Capture with Fiddler](#traffic-capture-with-fiddler)
  - [Script Development with JMeter](#script-development-with-jmeter)
- [Best Practices](#best-practices)
- [Known Issues and Improvements](#known-issues-and-improvements)
- [Contributing](#contributing)
- [License](#license)

## Overview

This project focuses on performance testing a website using **Apache JMeter** and **Fiddler**. The objective is to simulate real user behavior, capture traffic, and refine the script according to performance testing best practices. The user scenario involves navigating through the main site, secondary pages, and dynamically selecting random articles.

## User Scenario

1. **Main Page Navigation**  
   The user opens the main page of the website.
2. **Secondary Page Navigation**  
   The user navigates to a specific static page (e.g., "Ecosystem").
3. **Random Article Navigation**  
   The user navigates to a random article on the secondary page. This step uses parameterization to extract random URLs.

## Setup Instructions

### Pre-Requisites

- [Install Apache JMeter](https://jmeter.apache.org/download_jmeter.cgi)
- [Install Fiddler](https://www.telerik.com/fiddler)

### Traffic Capture with Fiddler

1. Enable HTTPS decryption in Fiddler.
2. Set up Fiddler as a proxy to capture the browser traffic.
3. Filter out unnecessary requests (e.g., third-party resources) that should not be included in the JMeter script.

### Script Development with JMeter

1. **Configure Test Plan:** Set up thread groups, HTTP requests, and controllers.
2. **Parameterization:** Use regular expressions to dynamically select article URLs.
3. **Cache and Cookies:** Clear cache and cookies at the start of each user session.
4. **Error Handling:** Enable error handling in the thread group settings.
5. **Remove Proxy Settings:** Ensure proxy settings are disabled for script portability.

## Best Practices

- **Transaction Naming:** Use descriptive names like `S1_01_Open_Main_Page`.
- **Request Comparison:** Verify that JMeter captures all the necessary requests by comparing with Fiddler.
- **Headers and Referrers:** Add appropriate headers and referrers to requests, parameterizing when needed.
- **Random Pauses:** Include random pauses between transactions to simulate real user behavior.

## Known Issues and Improvements

- Ensure accurate traffic capture in JMeter by cross-referencing with Fiddler.
- Optimize the random article selection using proper regular expressions.
- Debug and remove unnecessary elements before the final script submission.

## Contributing

Please follow the best practices outlined above when contributing to the project. Ensure all debugging elements are removed and that your changes are properly tested.


