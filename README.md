# Hydrography Project

## How do I get set up?
### Base setup
Built on python 3.7 with a bunch of modules. Long live python!
~~~
sudo dnf install python37
git clone https://<username>@bitbucket.org/mmethot/ev-project.git
cd ev-project
virtualenv -p $(which python3.7) .venv
source .venv/bin/activate
pip install -r requirements.txt
~~~
