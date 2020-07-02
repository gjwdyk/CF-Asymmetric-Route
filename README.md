# CloudFormation Asymmetric Route








The purpose of this repository is to build Test/Demo Environment with Asymmetric Route.
Originally the Test/Demo Environment is planned to be implemented as below diagram, which describes the targeted Logical Network Diagram the CloudFormation designed to build.

![Logical Network Diagram](Figures/LogicalNetworkDiagramVyOS.png)

Below the same diagram depicting the traffic flows through the network elements in the network.

![Logical Network Diagram with Service Flows](Figures/LogicalNetworkDiagramVyOSwithServiceFlows.png)



Similar environment (but NOT exactly the same) has been successfully built on VMware Workstation with the help of VyOS to create the asymmetricity of the traffic.
However since VMware Workstation portability is not flexible enough (to transfer the image-files, one will need to upload/download tens of GigaBytes of image-files), and to run the VMware images one will require top of the class Laptop/Desktop with a lot CPU and Memory resources;
therefore building the environment on AWS where the resources are abundant and there is no need to transfer upload/download tens of GigaBytes of image-files, the AWS CloudFormation solution is viewed as a very good alternative.

However upon more research and quite some attempts to build a VyOS node with CloudFormation, it is revealed that VyOS is NOT capable to support Cloud-Init through User-Data form, as referred on the below highlighted respond to a customer feedback/review on VyOS product page on AWS.

![VyOS Respond](Figures/VyOSCFCloudInitUserDataSupport20200702Marked.png)

<a href="https://aws.amazon.com/marketplace/reviews/reviews-list/B07N3X1P1T/review/8e54e2e2-963c-4e6f-8fac-90a7adb8ec5b">![VyOS Respond](Figures/VyOSCFCloudInitUserDataSupport20200702Marked.png)</a>



Therefore the Test/Demo Environment plan is changed to use yet another two Big-IP instead of VyOS, as described on the below diagram:

![Logical Network Diagram](Figures/LogicalNetworkDiagramBigIP.png)

With the traffic flow similar as before, depicted in the below diagram:

![Logical Network Diagram with Service Flows](Figures/LogicalNetworkDiagramBigIPwithServiceFlows.png)



***



To Do:

- [ ] Post the current CF which Implements the Environment (only minus the 2 VyOS and Internal Node only)
- [ ] May Implement VyOS Part with yet another 2 Big-IPs



***


