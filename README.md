# 1. Environment ubuntu20 The pooled client has not been updated yet. Rose needs a hard fork, which is painful: { 

```
git clone https://github.com/snight1983/chia-rosechain.git

git clone https://github.com/snight1983/rose-garden.git

cd rose-garden
python3 -m venv ./venv
source ./venv/bin/activate
pip install ../chia-rosechain/ 
sudo CHIA_ROOT="/your/home/dir/.chiarose/mainnet" ./venv/bin/python -m pool
```
# 2. A simple way to close the console and keep the pool running 


```
screen -S rose
cd rose-garden
source ./venv/bin/activate
sudo CHIA_ROOT="/your/home/dir/.chiarose/mainnet" ./venv/bin/python -m pool
```
# 3. Open the Rose console and view the simple way to run the pool 
```
screen -r rose
```
# 4. Check if the pool is running 
```
ubuntu@VM-0-9-ubuntu:~$ ps -aux| grep pool
root      970672  0.0  0.1   9660  4560 pts/3    S+   18:17   0:00 sudo CHIA_ROOT=/root/.chiarose/mainnet ./venv/bin/python -m pool
root      970673  0.5  1.3 226028 55648 pts/3    Sl+  18:17   0:02 ./venv/bin/python -m pool
ubuntu    972010  0.0  0.0   6300   736 pts/1    S+   18:25   0:00 grep --color=auto pool
ubuntu@VM-0-9-ubuntu:~$ 



or Access via browser eg: http://11x.1xx.xx0.1x0:xx
```
# 5. Beta preview 

![image](https://github.com/snight1983/rose-garden/blob/master/images/pool1.png)
![image](https://github.com/snight1983/rose-garden/blob/master/images/pool2.png)


# 6. Support ability  

Chia's new plot can be added to the rose garden'pool' (using chia contract P chart)

Chia old plot can join the rose garden'pool' (using public key P)

Rose new plot can be added to the rose garden'pool' (using rose contract P chart ,Not recommended, this will result in only 1/8 of Chia’s income ) 
