# Troubleshooting Network Connectivity in a Peered VPC

[LINK](https://skillbuilder.aws/learn/2TBW2XHP7N/troubleshooting-network-connectivity-in-a-peered-vpc/NT28U6CDP9)

# **Description**

The lab covers the connectivity concepts of Amazon Virtual Private Cloud (Amazon VPC). It demonstrates configuring a VPC peering between two VPCs in the same account and allow client-server HTTP traffic between two hosts in the VPCs. AnyCompany needs to allow HTTP traffic between a client and a server. The HTTP client instance resides in one VPC while the HTTP server instance resides in a different VPC in the same AWS account. A junior member of your team already implemented the solution but it seems it was misconfigured. As a member of the cloud team at AnyCompany, you have been assigned to check connectivity between an HTTP client and server. Your task is to troubleshoot the issue and fix the configuration to allow the HTTP traffic between the client and server via the VPC peering. High-level guidance and references are provided to assist you in fixing the issue. The detailed solution instructions are provided in a collapsible section which you can expand.

# **Objectives**

- Test the HTTP connection between the client and server and verify the issue.
- Identify the issues in the existing configuration and remediate the configuration to allow HTTP traffic between the client and server via the VPC peering.
- Use the Reachability Analyzer to troubleshoot VPC connectivity issues.

# **AWS Services**

- Amazon VPC