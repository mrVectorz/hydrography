# Hydrography Project

## How do I get set up?
### Base setup
Built on python 3.7 with a few of modules.
~~~
sudo dnf install python37
git clone https://<username>@bitbucket.org/mmethot/ev-project.git
cd ev-project
virtualenv -p $(which python3.7) .venv
source .venv/bin/activate
pip install -r requirements.txt
~~~

Sending data to graphite.
~~~
docker pull graphiteapp/graphite-statsd
docker run -d\
 --name graphite\
 --restart=always\
 -v ./conf/storage-schemas.conf:/opt/graphite/conf/storage-schemas.conf\
 -p 80:80\
 -p 2003-2004:2003-2004\
 -p 2023-2024:2023-2024\
 -p 8125:8125/udp\
 -p 8126:8126\
 graphiteapp/graphite-statsd
~~~

The mounted volume is the storage configuration for the graphite testing.
