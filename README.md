# pypywithnexus
## Access online PyPi repos for PIP installation in Local Network
### using Sonatype Nexus Repository Manager 

if you want to access and install PyPi packages with PIP on systems witout internet or airgapped
you could install Nexus and setup a PyPi Proxy so all of your machines could access and install packages woitout any internet connection 

i assume that you already have NEXUS repository manager installed and Accessibale by your machines over HTTP/HTTPS 



pip install  --trusted-host RepositoryIP -i http://Repository-IP/Repository/pypi-proxy-name/pypi-all/simple -v packagename

EX : in my SetUp Repo Address is  : 192.168.1.10 and serverd over HTTP Port 8080 and i want to install cx_Oracle Package
i hace PyPi repository named : pypi-proxy


pip3 install  --trusted-host 192.168.1.10 -i http://192.168.1.10:8080/Repository/pypi-proxy/pypi-all/simple -v cx_Oracle
