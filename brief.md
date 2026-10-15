Version: NAFATH-V2
Track: Networking

## Overview

A reliable 5G service for emergency responders depends on several IT fields working together. Software must handle repeated requests safely when connections fail. AI can help predict network congestion, but models need proper evaluation before their predictions are trusted. Mobile applications should preserve essential information offline and synchronize updates when connectivity returns. Networking must manage resources and provide suitable service during high demand. Cybersecurity teams need to detect attacks, contain incidents, and restore operations. Data models should also support accurate daily reports by region, helping operators identify usage patterns and service problems. These areas are interdependent: reliable applications require resilient connectivity, secure systems, useful predictions, and trustworthy reporting. For the Networking track, the key question is how 5G network slicing can provide a dedicated service for emergency responders.

## Software

HTTP methods have different safety and idempotency properties. A safe method is intended to read information without changing the server's state. An idempotent method has the same intended effect when repeated. GET is both safe and idempotent, while PUT and DELETE are idempotent but not safe. This matters during retries: repeating a non-idempotent request may create duplicate actions unless the application includes safeguards.

Resource: RFC 9110: HTTP Semantics - https://www.rfc-editor.org/rfc/rfc9110.html

## AI

Overfitting occurs when a congestion prediction model learns patterns specific to its training data and performs poorly on unseen conditions. Cross-validation evaluates a model across multiple training and validation splits, helping reveal whether its performance is consistent. The operator should also reserve separate test data for final evaluation. Because network traffic changes across locations and times, evaluation should reflect realistic conditions rather than relying only on training accuracy.

Resource: 3.1. Cross-validation: evaluating estimator performance - https://scikit-learn.org/stable/modules/cross_validation.html

## Mobile

An emergency-response app should keep essential information available locally and clearly indicate when information may be outdated. Users should be able to perform suitable tasks offline, while changes are saved in persistent local storage. When connectivity returns, the app should synchronize queued changes, retry failed operations safely, and handle conflicting updates using explicit rules. This reduces data loss and helps responders continue working during temporary network outages.

Resource: Build an offline-first app - https://developer.android.com/topic/architecture/data-layer/offline-first

## Networking

5G network slicing allows an operator to create logical network slices with different service characteristics on shared infrastructure. A dedicated slice could be configured for emergency responders with appropriate capacity, priority, and security policies. However, a slice does not automatically guarantee uninterrupted connectivity during every outage or congestion event. Its effectiveness depends on resource availability, deployment, configuration, and end-to-end management. Operators should define measurable service targets and test performance under realistic failure conditions.

Resource: 5G Network Slicing - https://www.3gpp.org/technologies/network-slicing

## Cybersecurity

Incident response helps an organization manage cyber attacks systematically. Preparation establishes responsibilities and capabilities; detection and analysis identify suspicious activity and determine its impact. Containment limits further damage, while eradication removes the cause of the incident. Recovery restores affected systems and verifies that they operate correctly. Afterward, lessons learned should improve procedures and controls. For a 5G emergency service, these activities help reduce disruption and restore trusted communications as quickly as possible.

Resource: Incident Response - https://csrc.nist.gov/projects/incident-response

## Data

A star schema organizes analytical data around a central fact table connected to descriptive dimension tables, such as date and region. A snowflake schema further normalizes dimensions into related tables. This can reduce duplicated descriptive data but may require more joins. For daily service-usage reports by region, a star schema is often a practical choice because its simpler structure supports understandable reporting and queries. The final design should reflect reporting needs and data scale.

Resource: Understand star schema and the importance for Power BI - https://learn.microsoft.com/en-us/power-bi/guidance/star-schema

## Misconception in My Track

## Open Question
