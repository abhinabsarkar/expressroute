# ExpressRoute
ExpressRoute lets you extend your on-premises networks into the Microsoft cloud over a private connection with the help of a connectivity provider. 

Refer the below mentioned links for details on ExpressRoute
* [ExpressRoute connectivity models](ExpressRoute-connectivity-models.pdf)
* [Virtual Network Gateway & GatewaySubnet](virtual-network-gateway.md)
* [ExpressRoute circuit](expressroute.md)
* [ExpressRoute locations](expressroute-locations.md)
* [ExpressRoute peerings / routing domain](expressroute-peering.md)

### Items covered
1. ExpressRoute circuit
    * Redundancy i.e. primary & secondary link/subnet
    * ER circuit to Virtual Network Gateway connection
2. ER connectivity models & locations. What is a co-location?
3. MSEE
4. ER circuits across different environments non-prod & prod, how they are connected to each other.
5. Co-location
6. ExpressRoute sku - standard, premium, local
7. Ingress - free, Egress - metered. In ER local sku, ingress & egress both are free. 
8. Routing domain / Peering
9. Service Key 
10. ASN - Autonomous System Number, NAT public IPs [BGP & ASN](https://github.bns/abhinabsarkar/networking-basics/blob/main/concepts/bgp-how-it-works.md)
11. Route filter (Microsoft Peering)
12. Fastpath for Virtual Network Gateway
13. Virtual Network Gateway facilitates the communication between MSFT & Customer network. Inbound goes through the Virtual Network Gateway, outbound not. Also, it is used for BGP i.e. sharing of the routes.
14. ExpressRoute site is not a Azure DC. ER sites are named after cities like Washington, Toronto, etc. Azure DC are name after country like East US or geography regions like east Europe. Azure DCs contain the compute & storage services whereas ER sites are in a public co-location where the Microsoft & Service Providers like Equinix put their edge routers which are then cross-connected.

## References
* https://docs.microsoft.com/en-us/azure/expressroute/expressroute-connectivity-models
* https://docs.microsoft.com/en-us/azure/expressroute/expressroute-locations
* https://docs.microsoft.com/en-us/azure/expressroute/expressroute-erdirect-about
* Youtube
    * 1. ExpressRoute advanced - https://www.youtube.com/watch?v=0wsQrP6cAB8
    * 2. ExpressRoute deep dive - https://www.youtube.com/watch?v=oevwZZ1YFS0
* https://marckean.com/2018/09/03/azure-expressroute-demystified/
* https://kvaes.wordpress.com/2016/02/10/azure-expressroute-connection-methods/
