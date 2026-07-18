# Architecture Overview

## System Design

FDR is built on a modular architecture that separates concerns into distinct layers, making the system maintainable, testable, and extensible.

## High-Level Architecture

```
┌─────────────────────────────────────────────┐
│              Presentation Layer             │
│         (API, Dashboard, CLI)               │
├─────────────────────────────────────────────┤
│              Application Layer              │
│    (Orchestration, Business Logic)          │
├─────────────────────────────────────────────┤
│              Processing Layer               │
│   (Harvesting, Transformation, AI)          │
├─────────────────────────────────────────────┤
│                Data Layer                   │
│      (Storage, Caching, Indexing)           │
└─────────────────────────────────────────────┘
```

## Core Components

| Component | Purpose |
|---|---|
| Harvesting Engine | Collects data from configured sources |
| Processing Pipeline | Transforms and validates incoming data |
| AI Module | Analyzes data and generates insights |
| API Gateway | Provides programmatic access to all features |
| Storage Service | Manages persistent data storage |

## Learn More

- [Overview](user-guide/overview.md) — Detailed component overview
- [Configuration](user-guide/configuration.md) — How to configure the system
