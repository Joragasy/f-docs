# AI Assistant Overview

## Introduction

The AI Assistant is a core component of FDR that provides intelligent analysis, pattern detection, and natural language interaction with your data.

## Capabilities

### Data Analysis

- **Pattern Detection** — Automatically identify trends and patterns in collected data
- **Anomaly Detection** — Flag unusual data points or behavior for further investigation
- **Statistical Summaries** — Generate comprehensive statistical overviews of datasets

### Natural Language Interface

- Query your data using natural language questions
- Receive contextual explanations of data findings
- Get recommendations based on historical patterns

### Automation

- Schedule recurring analysis tasks
- Set up alerting rules based on AI-detected conditions
- Generate automated reports on configurable intervals

## Configuration

The AI Assistant can be configured through the main configuration file:

```yaml
ai:
  enabled: true
  model: default
  analysis_interval: 3600
  alert_threshold: 0.8
```

## Usage Examples

### Query Data

```
> What are the top 5 data sources by volume this week?
```

### Detect Anomalies

```
> Are there any anomalies in the harvesting pipeline for the last 24 hours?
```

### Generate Reports

```
> Generate a summary report for all data collected in July 2026.
```

## Learn More

- [Architecture Overview](../user-guide/overview.md) — System design and AI module placement
- [Configuration](../user-guide/configuration.md) — Full configuration reference
