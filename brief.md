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

## Cybersecurity

## Data

## Misconception in My Track

## Open Question
