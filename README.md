# Oracle Cloud Infrastructure (OCI) Sample Implementation

This repository contains a basic implementation sample for Oracle Cloud Infrastructure (OCI). The sample includes the creation of a Virtual Cloud Network (VCN), a compute instance, and an object storage bucket using OCI's Command Line Interface (CLI).

## Prerequisites

1. **OCI Account:** You need access to an Oracle Cloud Infrastructure account.
2. **OCI CLI:** Install and configure the OCI Command Line Interface. Instructions can be found [here](https://docs.oracle.com/en-us/iaas/Content/API/SDKDocs/cliinstall.htm).

## Steps to Run

### 1. Create a Virtual Cloud Network (VCN):

```bash
oci network vcn create --cidr-block "10.0.0.0/16" --display-name "MyVCN" --compartment-id <your-compartment-id>

### 1. Create a Virtual Cloud Network (VCN):

```bash
oci network vcn create --cidr-block "10.0.0.0/16" --display-name "MyVCN" --compartment-id <your-compartment-id>
