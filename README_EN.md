# The Ultime Jellyfin Media Stack
On this repository we will find how to deploy a whole Media Server stacks into Kubernetes.

## The main feature of this project are : 
- Automation of every tools with ArgoCD (using bitnami helm chart)
  -  Automation of ArgoCD Repository inside argocd/repository
  -  Automation of ArgoCD Applications inside argocd/applications
- Deploy cert-manager for certificate generation and rotation with let's encrypt
- Deploy a dyndns (I'm using scaleway but you cant use anyone)
- Deploy qBittorrent for torrent downloading.
  - Use gluetun IVPN as a sidecar of qBittorrent to secure torrent downloading
- Deploy indexers such as jackett and prowlarr (torrent) and nzbhydra2 
- Deploy **\*ARR** project (Sonarr, Radarr and you can add any one you wan't) (Will add Lidarr and Readarr in futures releases)
- Deploy bazarr to automatically download subtitle for all my movies/series
- Deploy Usenet downloaders sabnzbd
- **Not Available Yet** Deploy a requests implementation with Jellyseerr (and CSS integration in the Jellyfin UI)
- Deploy flaresolver to resolv captcha
- Deploy Jellyfin your free and Free Software Media System.
- Deploy Jellyseerr and add a custom CSS on Jellyfin to get a good integretion
- Deploy Homarr Customizable browser's home
- Deploy an nginx to secure your endpoints

All of those applications are deployed directly on Kubernetes, all the workflow can be automated and it's easy to maintain all your tools up-to-date. I made the choose to use Scaleway as a DNS but you can use any, if you do, you will need to reconfigure your cert-manager configuration and use another ddns tools (you can also create a custom one with à cronjob)

My homelab is running inside integrated Kubernetes inside Docker on a laptop running Windows 10 using WSL2. But you can also use any Kubernetes cluster since you adapt things.
I've allowed my Kubernetes Jellyfin pods to access to my Graphical Cards using Nvidia Container Runtime which permit to deliver more performance.

## Requirements : 
- You need to have a working Kubernetes clusters
- your own dns domain in any provider you wan't
- Understand Kubernetes basics
- Expose your Jellyfin and Jellyseerr on Internet if you wan't to.

## Future Improvements :
- Run containers securly with securityContext
- Use Recyclarr to automatically synchronize recommended settings from the TRaSH guides to your Sonarr/Radarr instances
- Use Vault to store credentials (a single one as my homelab is composed to only 1 server actually)
- Deploy a LunaSea (Don't know why exactly yet but seems usefull)

## Installation
I suggere you to fork my project that will made the installation process easier, as this stack is using some external tools such as DNS provider, lets encrypt, VPN etc... you will need to made some modification to it. The ArgoCD Synchonization is made over git, its why you will need to fork it or you will be based on my own project which will include my configuration !