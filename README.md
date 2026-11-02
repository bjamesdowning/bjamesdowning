# Hi, I'm Billy Downing 👋

**Network engineer based in Dublin, Ireland.** I've designed and run production networks since 2011: USMC tactical/greenfield, Booz Allen, LCRA dual data centres, a Vectrus MPLS backbone, and Sterling DC fabrics and migrations. From 2022 I worked as a Customer Success Manager (GitLab, then Fin), helping teams build NetDevOps and GitOps pipelines. I'm now moving back into **hands-on DC and backbone network engineering**: BGP, IGP, EVPN/VXLAN, leaf-spine, and automation that takes repetitive work off the team.

> Below: what I've built, written, and talked about. Production work is labelled as production; demos and labs are labelled as demos and labs.

---

## Snapshot

| | |
|---|---|
| **2011–2022** | Hands-on network design and operations: DC, campus/core, MPLS backbone, Clos/VXLAN fabrics, NSX-V→T migrations |
| **2022–now** | Customer Success Manager (GitLab Senior CSM → Fin). NetDevOps/GitOps enablement, CI pipelines, digital-twin demos |
| **Now** | Rebuilding day-2 depth in labs: SR Linux/FRR BGP, telemetry-driven remediation (Axon), Arista EOS EVPN |
| **Studying** | Arista DC Engineering Specialist → NVIDIA NCP-AIN (AI networking) |

## Skills

- **Routing & switching:** BGP (eBGP/iBGP, route reflectors, communities, MP-BGP), OSPF, EIGRP, MPLS / MPLS-TE, BFD, QoS, multicast
- **DC fabrics:** leaf-spine/Clos, EVPN-VXLAN, Cumulus/NVIDIA, Arista EOS (cEOS labs), Cisco, Juniper SRX, VMware NSX-T
- **Automation:** Python (Netmiko, NAPALM, Nornir), Ansible/AWX, Go, Terraform, GitLab CI, Containerlab, Batfish
- **Observability:** gNMI/gnmic, Prometheus, Alertmanager, NetFlow/sFlow, SolarWinds, vRNI
- **Platform:** Kubernetes, VMware Tanzu (TKG/TMC), Flux/GitOps, AWS EKS

---

## Featured projects

### [Axon](https://gitlab.com/mayutic/axon) · lab · 2026
A self-healing network lab. Two Nokia SR Linux switches run BGP; gnmic → Prometheus → Alertmanager detects a broken session. A Python agent gathers context over MCP from NetBox (intent), Prometheus (live state), and SR Linux, asks a local LLM for a decision, and can only push a JSON-RPC fix once the evidence checks out. *Learning lab, not production.*

### [corp-dc: GitOps for Network Engineers](https://gitlab.com/gl-demo-ultimate-bdowning/netdevops/corp-dc) · demo · 2024
NetDevOps reference pipeline I built for customer enablement at GitLab: two FRR routers with BGP in **Containerlab**. CI lints configs, **Batfish** validates BGP adjacency, STIG-style Python checks cover hostname/IPv6/routing, an ephemeral lab is built and torn down, and deploy is gated through MR review + CODEOWNERS. *Digital-twin/demo pipeline — not a customer production underlay.*  
More enablement demos: [gl-demo-ultimate-bdowning](https://gitlab.com/gl-demo-ultimate-bdowning)

### Network labs (GitHub)
- [MPLS-Traffic-Engineering](https://github.com/bjamesdowning/MPLS-Traffic-Engineering) — Cisco MPLS-TE lab configs
- [MP-BGP](https://github.com/bjamesdowning/MP-BGP) — multiprotocol BGP lab
- [IPsec-Modes](https://github.com/bjamesdowning/IPsec-Modes) — transport vs tunnel mode
- [netmiko_pull](https://github.com/bjamesdowning/netmiko_pull) — pull state from Cisco with Netmiko
- [gofigure](https://github.com/bjamesdowning/gofigure) · [TemplateGen](https://github.com/bjamesdowning/TemplateGen) · [orchlab](https://github.com/bjamesdowning/orchlab)

### Platform / GitOps
- [vmware-explore-gitops](https://gitlab.com/bjamesdowning/vmware-explore-gitops) — VMware Explore 2022 GitOps demo
- [tanzuworkshop](https://github.com/bjamesdowning/tanzuworkshop) — Tanzu workshops from Sterling
- [terraform-flux-eks](https://gitlab.com/bjamesdowning/terraform-flux-eks) — Terraform + Flux on EKS
- [explore-gitops-infra](https://gitlab.com/bjamesdowning/explore-gitops-infra) / [explore-gitops-app](https://gitlab.com/bjamesdowning/explore-gitops-app)

### Side builds
- [Ration](https://github.com/bjamesdowning/ration-mirror) — kitchen-management app with an MCP server so AI agents can use it

---

## Publications

**Sterling (VMware partner), 2020–2022**
- [Cloud Native Development On-Prem: Networking](https://sterling.com/cloud-native-development-on-prem-networking/) (Mar 2020)
- [Managing and Migrating Workloads Across Hybrid Cloud](https://sterling.com/managing-and-migrating-workloads-across-hybrid-cloud/) (Apr 2020)
- [Migrating to NSX-T from NSX-V](https://sterling.com/migrating-vmware-nsx-v-to-t/) (Jun 2020)
- [Automated Kubernetes Deployment using Tanzu Kubernetes Grid](https://sterling.com/deployment-using-tanzu-kubernetes-grid/) (Aug 2020)
- [Tanzu Mission Control Orchestrates Kubernetes Across Clouds](https://sterling.com/tanzu-mission-control-orchestrates-kubernetes/) (Nov 2020)
- [Trading Technical Debt for Managed Services in the Cloud](https://sterling.com/trading-technical-debt-for-managed-services-in-the-cloud/) (Jun 2021)
- [vSphere with Tanzu: The Fastest Route to a Modern Infrastructure](https://sterling.com/vsphere-with-tanzu-the-fastest-route-to-a-modern-infrastructure/) (Nov 2021)
- [Distributed Security with NSX-T, Part 1](https://sterling.com/distributed-security-with-nsx-t-part-1/) · [Part 2](https://sterling.com/distributed-security-with-nsx-t-part-2/) (Apr 2022)
- [GitOps with VMware Tanzu for Automated Application and Service Delivery](https://sterling.com/gitops-with-vmware-tanzu-for-automated-application-and-service-delivery/) (Aug 2022) — *confirm authorship if your byline isn't on the page*

**Press**
- GovLoop interview: [Trading Technical Debt for Managed Services in the Cloud](https://web.archive.org/web/20260307180206/https://www.govloop.com/trading-technical-debt-for-managed-services-in-the-cloud/)

**Personal blog — [billydowning.io](https://billydowning.io/)** (network engineering study notes, by topic):

*Datacenter fabrics / EVPN / VXLAN*
- [Cumulus Linux VXLAN](https://billydowning.io/home/cumulus-vxlan)
- [Ansible-provisioned EVPN-controlled VXLAN pods](https://billydowning.io/home/learning-ansible-provision-evpn-controlled-vxlan-pods)
- [Open networking tools & NOS](https://billydowning.io/home/learning-how-to-open-tools-nos)

*Routing, MPLS & protocols*
- [MP-BGP (part 1)](https://billydowning.io/home/mp-bgp-1)
- [MPLS Traffic Engineering](https://billydowning.io/home/mpls-te)
- [OSPF path selection](https://billydowning.io/home/learning-ospf-path-selection)
- [EIGRP named mode](https://billydowning.io/home/learning-about-eigrp-named-mode)
- [Bidirectional Forwarding Detection (BFD)](https://billydowning.io/home/learning-about-bidirectional-forwarding-detection-bfd)
- [Quality of Service (QoS)](https://billydowning.io/home/learning-about-quality-of-service-qos)
- [Multicast basics](https://billydowning.io/home/learning-the-basics-of-multicast)
- [Multicast with SSM / IGMPv3](https://billydowning.io/home/learning-about-multicast-with-ssm-igmpv3)
- [Multicast IGMP snooping](https://billydowning.io/home/learning-about-multicast-igmp-snooping)
- [IPsec transport vs tunnel mode](https://billydowning.io/home/learning-ipsec-transport-vs-tunnel-mode)

*Network automation / NetDevOps*
- [YANG, RESTCONF, Docker & Go for network engineers](https://billydowning.io/home/learning-how-yang-restconf-docker-and-golang-can-be-useful-for-a-network-engineer)
- [Learning Python](https://billydowning.io/home/learning-python)
- [Learning Git](https://billydowning.io/home/learning-git)

*Kubernetes / cloud-native*
- [Kubernetes: the one API](https://billydowning.io/home/kubernetes-the-one-api)
- [A Kubernetes analogy](https://billydowning.io/home/kubernetes-analogy)

*Career & learning*
- [How to become a network engineer](https://billydowning.io/home/learning-how-to-become-a-network-engineer)
- [Learning from exam blueprints](https://billydowning.io/home/learning-from-exam-blueprints)
- [Learning resources](https://billydowning.io/home/learning-resources)
- [Time management](https://billydowning.io/home/learning-about-time-management)
- [Ways to take notes](https://billydowning.io/home/learning-different-ways-to-take-notes)


---

## Talks & podcasts
- **K8sKoach streamcast** (Kubernetes / NetDevOps, LinkedIn Live): [watch](https://www.linkedin.com/events/k8skoach-astreamcastonkubernete7279512843157139456/theater/)
- **Packet Pushers, Priority Queue 146:** *Practical Python: Deploying BFD* *(episode URL currently broken — drop a working link when you have it)*
- **Upcoming:** personal podcast episode (audio TBD) — placeholder
- Speaking: VMware Explore 2022 (GitOps), Dell Technologies World, NATO *(from your resume — say if any title/year should change)*

---

## Contact
[LinkedIn](https://www.linkedin.com/in/billy-downing-38806084/) · [GitLab](https://gitlab.com/bjamesdowning) · [GitHub](https://github.com/bjamesdowning) · [Blog](https://billydowning.io/) · Dublin, Ireland (Stamp 4)
