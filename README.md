# gw-bartholomae.stb.de  
"upgrade" unsecure incoming http->https + relay outgoing smtp 25->external (office365)  
  
## traefik  
reverse proxy incl. ssl-offloading  
config\ .env : holds credentials - the HETZNER_API_KEY (Certresolver: Hetzner DNS)  
config\ traefik.yml : basic traefik setup  
config\dynamic\ dynamic.yml : Dynamic configuration file - provides a default certificate  
config\dynamic\ isp01.yml : https://isp01.domain.tld -> internal: http://isp01  
config\dynamic\ isp02.yml : https://isp01.domain.tld -> internal: http://isp01  
  
## postfix  
custom postfix smtp relay build  
config\ .env : holds credentials - the setup needed for the smtp relay to work  
  