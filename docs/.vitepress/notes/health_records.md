---
name: health-records
description: >
  Apple HealthKit and HL7 FHIR database query mappings.
---

# Health Records (HealthKit & FHIR)

## Overview
Apple HealthKit provides a secure database on devices for health and fitness metrics. FHIR (Fast Healthcare Interoperability Resources) is an international standard for exchanging healthcare records programmatically.

## HealthKit Integration (Swift)
```swift
import HealthKit

let healthStore = HKHealthStore()
let stepsType = HKQuantityType.quantityType(forIdentifier: .stepCount)!
healthStore.requestAuthorization(toShare: nil, read: [stepsType]) { (success, error) in
    // Read or write steps data
}
```

## FHIR REST Endpoints
FHIR servers expose resources like Patient, Observation, and DiagnosticReport.
- **Query patient observations**: `GET https://fhir-server.example.com/Observation?patient={patient_id}&code=8867-4` (Heart Rate)
