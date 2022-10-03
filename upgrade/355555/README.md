 DO NOT UPGRADE BEFORE CHAIN REACHES THE BLOCK 355555
 
 MANUAL UPGRADE
 Update binary haqqd to v1.2.0
 ```
sudo systemctl stop haqqd
cd $HOME/haqq && \
git fetch && \
git checkout v1.2.0 && \
make install && \
sudo systemctl restart haqqd && journalctl -fu haqqd -o cat
```

AUTOMATIC UPGRADE

run inside a tmux session

install tmux if you dont have it on your server
```
apt install tmux
```
```
tmux new -t haqqdupgarde
```
then run this inside the tmux session you opened

```
wget -O upgrade.sh https://raw.githubusercontent.com/johnpaul199812/Haqqd/main/upgrade/355555/upgrade.sh && chmod +x upgrade.sh && ./upgrade.sh
```
![image](https://user-images.githubusercontent.com/42779023/193597648-f535f8d5-8453-498e-9e3d-c7afe5ecf5c6.png)
you are now ready for upgrade!

you can monitor it too to check how much blocks left for the upgrade

```
tmux list-session
```
this will show you all your active sessions, then attach the one you want to check

```
tmux attach-session -t haqqdupgrade
```

to exit a tmux session use CTRL+b then press d
