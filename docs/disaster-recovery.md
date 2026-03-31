# Disaster Recovery Strategy

## Overview
This document describes the Disaster Recovery (DR) strategy implemented for the Azure architecture.

The solution is designed to protect the application against a full regional outage by using a secondary Azure region.

## DR Model
- Active / Passive architecture
- Primary region handles production traffic
- Secondary region remains on standby

## Traffic Management
- Azure Traffic Manager is used to control traffic routing
- Health probes detect regional outages
- Traffic is redirected automatically to the DR region during failure

## Data Replication
- Azure SQL Database uses cross-region replication
- Data is continuously synchronized from primary to secondary region

## Failover
- In case of a primary region outage:
  - Database failover is triggered
  - Application in the DR region becomes active
  - Traffic Manager redirects users

## RTO and RPO
- Recovery Time Objective (RTO): ~1 hour
- Recovery Point Objective (RPO): ~15 minutes

## Scope and Limitations
- This DR design focuses on regional outages
- Application-level failures are handled by resiliency within a single region
