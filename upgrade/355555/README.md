 DO NOT UPGRADE BEFORE CHAIN RECHES THE BLOCK 355555
 
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
