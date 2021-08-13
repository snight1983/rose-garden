It's still in the development stage, I hope it can crack the nft plot. 
---


```
git clone https://github.com/snight1983/chia-rosechain.git

git clone https://github.com/snight1983/rose-garden.git

cd rose-garden
python3 -m venv ./venv
source ./venv/bin/activate
pip install ../chia-rosechain/ 
sudo CHIA_ROOT="/your/home/dir/.chiarose/mainnet" ./venv/bin/python -m pool
```
# A simple way to close the console and keep the pool running 
---
```
screen -S rose
cd rose-garden
source ./venv/bin/activate
sudo CHIA_ROOT="/your/home/dir/.chiarose/mainnet" ./venv/bin/python -m pool
```
