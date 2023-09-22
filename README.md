# homelab
Home lab servers BOM

I have been asked about my homelab a few times now so I thought I would document what I run.  I currently have 2 servers connected to my [Unifi network](https://ui.com/us).  The servers are as follows:

[ASrock 4x4 4800U](https://www.newegg.com/asrock-4x4-box-4800u/p/N82E16856158069?Item=N82E16856158069)
[64G DDR4 3200 RAM](https://www.newegg.com/g-skill-64gb-260-pin-ddr4-so-dimm/p/N82E16820374025?Item=N82E16820374025)
[1TB NVMe drive](https://www.newegg.com/samsung-970-evo-plus-1tb/p/N82E16820147743?Item=N82E16820147743)

Each of these servers has 8 cores / 16 threads, 64G RAM and a 1TB NVMe for fast disk performance. These servers also include 2 NICs; 1 1GBe and 1 2.5GBe. These are great servers for standing up an [Ovirt](https://ovirt.org/) or [Proxmox](https://www.proxmox.com/en/) cluster or for running containers with [Podman](https://podman.io/) or [Docker](https://www.docker.com/). You can also stand up a [minikube](https://minikube.sigs.k8s.io/docs/start/) stand alone server or even a small cluster. 

I ran an Ovirt cluster on 3 of these for years while I worked at Red Hat and never had a problem with them. Right now I am running podman containers on one server and Docker containers on the second as I have switched from running VMs to mostly running containers. I would run kubernetes but I find standing up the K8s cluster is more of a hassle than its worth for such a small cluster.  Its easier for me to just stand up Docker/podmamn containers manually.  

In addition to these servers and my Unifi network I also have a [Synology](https://www.synology.com/en-us) NAS.  I use NextDNS for my DNS where all devices in my house reference the NextDNS service and this service determines whether the DNS record is local or on the internet and routes the query appropriately. That allows me to block access to malicious websites and block ads and trackers at the DNS layer.

That's about it.  File and issue if you have any questions.

Cheers!
