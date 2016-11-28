My goal is to switch from leading with ScaleIO to leading with vSAN instead.  Randall Gressett (EMC Area Manager for the Southeast) agrees, and has the following strategy:
1.Lead with VxRAIL and vSAN for vSphere environments – simplest and most tightly integrated HCI solution.  Period.  EMC wins.
2.If Nutanix gains a foothold, relegate them to the non-VMware environment, but make sure it goes in on Dell gear. EMC wins.
3.The customer is truly looking for multihypervisor, scale-out HCI, then lead with ScaleIO.  EMC Wins.
  * Thus far very few customers actually see this as a need – competitors like Nutanix and Microsoft are playing their cards well… “Well, you won’t always be on VMware, will you?”
  * This is a false premise - The fact is vSphere is still 80% or more of their customers.  Don’t let them move the goalposts on you…
  * The implication here is clearly that ScaleIO, seen in this light, is clearly the niche player.
 
 
I try to point out the problem with their current positioning thusly:
·         I always go through the basics of vSAN:
o    Architecture
o    Features
o    Protection
o    Differences with Nutanix, etc.
o    Point out that ScaleIO – like Nutanix – requires a VSA, and therefore suffers from some of the same limitations (though truth be told the ScaleIO Client deploys as a Kernel module in the ESXi hypervisor, the SDS performs wide striping across all instances with automatic rebalancing, and I believe the client can read from multiple SDS simultaneously).
o    ScaleIO deployment is all CLI – tedious and particular.
·         Every VCE deck has the ‘family portrait’ – with poor little VxRAIL in the corner all by itself, and then a ton of massive converged or rack systems taking up the rest of the space.
·         Simply by having vSAN and ScaleIO represented on the same slide, they are compelled to differentiate…
o    “Well, vSAN is fine for vSphere, but you know it doesn’t scale, and it only supports vSphere.”
o    “ScaleIO, on the other hand, can scale as big as you want, and supports multiple hypervisors”
·         This is a false premise – vSAN scales to the size of the vSphere cluster. 
o    Just ask the VMware team in the room – what is your largest cluster?
o    Now ask the EMC team in the room – what is the use case for a workload to scale larger than that?
o    This only corroborates the fact that ScaleIO that is the corner case.
o    Exceptions will be things like:
§  Streaming media farms…  which likely will not be virtualized in the first place.
§  Hadoop farms…  which likely will not be virtualized in the first place.
§  Etc…
 
Properly positioned, ScaleIO:
·         makes a great replacement for an enterprise array:
·         offers all kinds of data services (file services, protection domains, storage pools, wide striping, etc) that vSAN simply doesn’t offer. 
As such, it just makes a lot more sense for ScaleIO to be deployed in a two-layer approach- a ScaleIO cluster providing storage, and the vSphere environment consuming it.

They clearly want to position ScaleIO as an x86, scale-out, commodity-based, SAN replacement.  That includes:
 
Distributed pool of storage capacity (GB) and performance (IOps, GBps) and consistent IOPS/latency – no hotspots, no matter the load
Dynamic storage pooling – share or move storage pool dynamically between hosts, cluster and even across different host/cluster type
Scale storage pool independently (GB, IOps, GBps) completely independently of compute
Scales bigger than traditional SAN – an order of magnitude bigger than the biggest external SANs in every dimension (GB, IOps, GBps)
Scales easily and non-disruptively compared to traditional SAN– small increments, pay as you grow and never do a data migration again
 
This is fundamentally different than the messaging platform for every other Hyperconverged solution:
Hyperconvergence Makes IT Easier by collapsing both the compute and storage
Hyperconvergence Makes IT Easier by greatly reducing the required administration of the storage layer.  This allows you to:  
Deploy infrastructure to support business initiatives more quickly.
Reduce ongoing costs associated with managing your virtual infrastructure
Eliminate daily tasks that burden your operational staff
Reduce capital needed for technology refreshes and new infrastructure projects.
 
That is to say, the messaging around Hyperconvergence is all about:
Tight integration between storage and compute layers
Greatly reduced administration of storage through the use of policy…
 
Spending 5 minutes with the ScaleIO Installation guide is enough to let you know that there is no way most vSphere teams are going to sign up for it… It is all Python scripting, requires a separate management domain, and is not tightly integrated with vSphere. 

·         Installation is cumbersome (all Python scripts)
·         Management is cumbersome (all Python scripts)
·         The positioning about scale and performance is a false premise, as vSphere only goes to 64 nodes to begin with
·         Thus far, less than 5% of their customers actually have a need for that kind of scale in a non-VMware environment.
