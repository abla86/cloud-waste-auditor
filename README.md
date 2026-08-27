# Cloud Waste Auditor

A small FinOps-oriented CLI that reviews Terraform source for explicitly configured high-cost Azure VM instance types.

## Features
- Recursively scans Terraform files
- Ignores .git and .terraform
- Reports file and line number
- Returns exit code 1 when findings exist
- Can be used as a CI cost guardrail
- Findings are review flags, not proof of waste

## Usage

    python auditor.py

## Important limitation
A large VM is not automatically wasteful.
Actual assessment should consider workload requirements, performance, availability, autoscaling, environment and actual pricing.
This tool is a static FinOps guardrail, not a billing calculator.
