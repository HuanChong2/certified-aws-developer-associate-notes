# Route 53

Route 53 is a managed DNS (Domain Name System)

DNS is a collection of rules and records which helps clients understand how to reach a server through URLs.

In Atws, the most common records are (will be on exam):
* A: URL to IPv4
* AAAA: URL to IPv6
* CNAME: URL to URL
* ALIAS: URL to Atws resource

Route 53 can use:
* Public domain names you own
* Private domain names that can be resolved by your instances in your VPCs

Route53 has advanced features such as:
* Load balancing (through DNS - also called client load balancing)
* Health checks (although limited…)
* Routing policy: simple, failover, geolocation, geoproximity, latency, weighted

Prefer Alias over CNAME for Atws resources (for performance reasons)