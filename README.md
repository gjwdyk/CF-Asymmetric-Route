# CloudFormation Asymmetric Route








The purpose of this repository is to build Test/Demo Environment with Asymmetric Route. Diagram below describe the targeted Logical Network Diagram which the CloudFormation designed to build.

![Logical Network Diagram](Figures/LogicalNetworkDiagram.png)

Below the same diagram depicting the traffic flows through the network elements in the network.

![Logical Network Diagram with Service Flows](Figures/LogicalNetworkDiagramWithServiceFlows.png)



***



VyOS Update :

VyOS is NOT capable to support Cloud-Init through User-Data form, as referred on the below respond to a

![VyOS Respond](Figures/VyOSCFCloudInitUserDataSupport20200702Marked.png)




To Do:

- [ ] Update existing AS3 with Pools from Windows Server ??? (should we do this or not?)
- [ ] Update Previous CF templates to use No OutBound versions of AS3 (and Update the corresponding Documentations)
- [ ] tmsh modify sys db ui.statistics.modulestatistics.localtraffic.persistencerecords value true
- [ ] Test Concept of Floating IP for High Availability. If 2 interfaces assigned same IP Address, will they be conflict? If not assigned, will they work?
- [ ] Default ASM Profiles
- [ ] APM (when applicable)



***


