# Campaign Build Automation Framework

A sanitized portfolio example of a paid media campaign build and automation framework designed to support scalable setup across campaign, ad set, and ad levels.

## Overview

This workbook is built to make campaign execution more structured, repeatable, and scalable. It combines budget planning logic with automation-ready build support, helping teams translate campaign inputs into organized setup decisions across multiple delivery layers.

In addition to calculating daily pacing from lifetime budgets, the framework is designed to support campaign architecture and execution at the campaign, ad set, and ad level.

## What it does

- Converts lifetime budget into structured daily pacing guidance
- Supports campaign setup across campaign, ad set, and ad levels
- Helps standardize build logic across multiple campaign components cross-channel
- Applies pacing controls such as working-days-only logic
- Includes launch and close weighting multipliers
- Accounts for contingency reserve percentages
- Generates daily budget schedules and monthly rollups
- Supports more scalable and repeatable campaign execution workflows

## Workbook structure

### Guide
Reference guide and mappings for understanding the workbook structure and automation context.

### Daily Budget Calculator
Core calculator tab with campaign setup inputs and outputs, including:
- campaign name
- platform
- start date
- end date
- lifetime budget
- working-days-only toggle
- launch weighting
- close weighting
- contingency reserve percentage

### Automation / Build Logic
Framework logic that supports how campaign inputs can be translated into structured build decisions across:
- campaign level
- ad set level
- ad level

### Daily Schedule Output
Generated schedule showing:
- date
- day of week
- spend day status
- pacing sequence
- daily weight
- daily budget
- cumulative budget

### Monthly Rollup
Summary of total budget allocation by month across the campaign flight.

## Core logic

### Net deployable budget
The calculator first removes any contingency reserve from the lifetime budget.

Formula:
```text
Net Deployable Budget = Lifetime Budget × (1 - Contingency Reserve %)
