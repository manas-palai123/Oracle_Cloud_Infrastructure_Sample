# Oracle Cloud Infrastructure (OCI) Sample Implementation

This repository contains a basic implementation sample for Oracle Cloud Infrastructure (OCI). The sample includes the creation of a Virtual Cloud Network (VCN), a compute instance, and an object storage bucket using OCI's Command Line Interface (CLI).

## Prerequisites

1. **OCI Account:** You need access to an Oracle Cloud Infrastructure account.
2. **OCI CLI:** Install and configure the OCI Command Line Interface. Instructions can be found [here](https://docs.oracle.com/en-us/iaas/Content/API/SDKDocs/cliinstall.htm).

## Steps to Run

### 1. Create a Virtual Cloud Network (VCN):

```bash
oci network vcn create --cidr-block "10.0.0.0/16" --display-name "MyVCN" --compartment-id <your-compartment-id>
```
### 2. Create a subnet within the VCN:

```bash
oci network subnet create --vcn-id <your-vcn-id> --cidr-block "10.0.0.0/24" --display-name "MySubnet" --compartment-id <your-compartment-id>
```
### 3. Create a compute instance:

```bash
oci compute instance launch --availability-domain "<your-availability-domain>" --compartment-id <your-compartment-id> --display-name "MyInstance" --shape "VM.Standard2.1" --subnet-id <your-subnet-id> --image-id <your-image-id> --ssh-authorized-keys-file <path-to-ssh-public-key>
```
### 4. Create an Object Storage Bucket:

```bash
oci os bucket create --compartment-id <your-compartment-id> --name <your-bucket-name>
```
### 5. Upload your file in Object Storage Bucket:

```bash
oci os object put --bucket-name <your-bucket-name> --file <path-to-local-file> --name <object-name-in-bucket>
```
## Additional Information

1. Always refer to the official Oracle Cloud documentation for detailed and up-to-date information.
2. Feel free to customize and extend the implementation based on your specific use case.
```vbnet
This README file provides a brief overview of the project, lists prerequisites, and provides step-by-step instructions for users to run the sample implementation. It also includes additional information and references to the official documentation for further details. Feel free to customize it further based on your specific needs.
```
