
# Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.microsoft.com.

When you submit a pull request, a CLA-bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

# Introduction

This repository contains terraform modules to deploy Azure-OCI Inter-connect as well as the infrastructure for Oracle applications. 

The repository contains modules for deploying the inter-connect between Microsoft Azure & OCI. The deployment is broken into two steps:

- [**InterConnect-1:**](azure-oci-cloud-interconnect/tree/master/InterConnect-1) This is the first step to establishing inter-connectivity.
- [**InterConnect-2:**](azure-oci-cloud-interconnect/tree/master/InterConnect-2) Once the connection between Oracle and Azure is setup, use this module to setup the connection to your Azure VNET and OCI VCN.

The repository conaints modules for deploying the infrastructure for the following Oracle applications:

- [**Oracle E-Business Suite**](azure-oci-cloud-interconnect/tree/master/EBusinessSuite)
- [**JD Edwards**](azure-oci-cloud-interconnect/tree/master/JDEdwards)
- [**Oracle Retail**](azure-oci-cloud-interconnect/tree/master/Retail)
- [**Peoplesoft**](azure-oci-cloud-interconnect/tree/master/Peoplesoft)

# Repository Structure

- InterConnect-1 => Contains the first set of terraform scripts to provision the Azure-OCI Cross-Cloud Interconnect
- InterConnect-2 => Contains modules for the second step to provisioning the inter-connect.
- JDEdwards => Contains scripts to provision the infrastructure for Oracle JDEdwards application
- EBusinessSuite => Contains scripts to provision the infrastructure for Oracle E-Business Suite
- Retail => Contains scripts to provision the infrastructure for Oracle Retail Suite
- Peoplesoft => Contains scripts to provision the infrastructure for Oracle Peoplesoft application

# Getting Started

To deploy Oracle Applications on the Cross-Cloud inter-connect, you will first need the inter-connect provisioned. Follow the steps listed in the README for [InterConnect-1](azure-oci-cloud-interconnect/tree/master/InterConnect-1) followed by [InterConnect-2](azure-oci-cloud-interconnect/tree/master/InterConnect-2) to deploy the inter-connect. Once the inter-connect has been deployed, you can deploy an application on that inter-connect using the application specific terraform modules here. Follow the instructions and guidance detailed in the README file for each application.
> **Note**: For Oracle applications, only infrastructure deployment can be automated using these terraform scripts. To install the specific application on the deployed infrastructure, please refer to the installation guide for that application.