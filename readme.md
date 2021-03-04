# ExpressRoute Peering
New ExpressRoute circuits can include two independent peerings: 
* Private peering
* Microsoft peering 

Whereas existing ExpressRoute circuits may contain three peerings: Azure Public, Azure Private and Microsoft. Azure services are categorized as Azure public and Azure private to represent the IP addressing schemes.

> Azure public peering has been deprecated and is not available for new ExpressRoute circuits. New circuits support Microsoft peering and private peering.

![Alt text](/images/expressroute-peering.png)

### Azure Private Peering
The private peering domain is a trusted extension of your core network into Microsoft Azure. You can set up bi-directional connectivity between your core network and Azure virtual networks (VNets).

![Alt text](/images/private-peering.png)

[Private Peering Reference Architecture](https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/hybrid-networking/expressroute)

### Microsoft Peering
Connectivity to Microsoft online services (Microsoft 365 and Azure PaaS services) occurs through Microsoft peering. We enable bi-directional connectivity between your WAN and Microsoft cloud services through the Microsoft peering routing domain.

![Alt text](/images/microsoft-peering.png)

Traffic destined to Microsoft cloud services must be SNATed to valid public IPv4 addresses before they enter the Microsoft network. Traffic destined to your network from Microsoft cloud services must be SNATed at your Internet edge to prevent [asymmetric routing](https://docs.microsoft.com/en-us/azure/expressroute/expressroute-asymmetric-routing). The figure provides a high-level picture of how the NAT should be set up for Microsoft peering. Refer [NAT requirements for Microsoft Peering](https://docs.microsoft.com/en-us/azure/expressroute/expressroute-nat#nat-requirements-for-microsoft-peering)

## How ExpressRoute works?
[Azure ExpressRoute demystified - Video](https://www.youtube.com/watch?v=RkuZD8y2JnM)

## Connectivity Model

![Alt text](/images/expressroute-connectivity-model.png)

If you're co-located in a facility with a cloud exchange, you can order virtual cross-connections to the Microsoft cloud through the co-location provider’s Ethernet exchange. Co-location providers can offer either Layer 2 cross-connections, or managed Layer 3 cross-connections between your infrastructure in the co-location facility and the Microsoft cloud.

[Equinix](https://www.equinix.com/partners/microsoft-azure/) is one of the leading provider of Microsoft Azure ExpressRoute deployments. 

## References
* [ExpressRoute peering](https://docs.microsoft.com/en-us/azure/expressroute/expressroute-circuit-peerings#routingdomains)
* [ExpressRoute NAT peering](https://docs.microsoft.com/en-us/azure/expressroute/expressroute-nat)
* [ExpressRoute connectivity models](https://docs.microsoft.com/en-us/azure/expressroute/expressroute-connectivity-models)
* [Asymmetric routing with multiple network paths](https://docs.microsoft.com/en-us/azure/expressroute/expressroute-asymmetric-routing)
