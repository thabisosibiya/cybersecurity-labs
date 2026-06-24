# Splunk Labs

## Overview

This section documents my hands-on learning with Splunk SIEM.

Splunk is a Security Information and Event Management (SIEM) platform used to collect, search, analyze, and visualize machine-generated data. It is commonly used by Security Operations Center (SOC) teams for monitoring, threat detection, and incident investigation.

## Topics Covered

### Introduction to Splunk
- Splunk architecture
- Data ingestion
- Indexes and sourcetypes
- Basic searching
- Search Processing Language (SPL)

## Skills Developed

- Log analysis
- Event investigation
- Basic SPL queries
- SIEM fundamentals
- Security monitoring concepts

## Example SPL Queries

```spl
index=*
```

```spl
index=* | stats count by host
```

```spl
index=* | top source
```

## Career Relevance

These skills support SOC analyst responsibilities including:
- Alert investigation
- Log review
- Threat hunting
- Security monitoring
