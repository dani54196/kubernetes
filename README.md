# Kubernetes Multi-Environment Test Repository

## Overview
This is a public repository used for Kubernetes testing across multiple environments.

## Purpose
The main goal is to run and validate Kubernetes experiments in different deployment setups, with a focus on practical testing and environment comparison.

## Environments

### Pre-Production
- Infrastructure: 2 virtual machines
- Roles:
  - 1 Master node
  - 1 Worker node
- Kubernetes distribution: K3s

### Production
- Infrastructure: 1 virtual machine in OCI
- Kubernetes distribution: K3s

## Kubernetes Distribution
All environments in this repository use K3s.

## Notes
This repository is intended primarily for testing and experimentation purposes.