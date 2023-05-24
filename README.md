# nvidia-cuda-master
Master Nvidia and Cuda configs


# restart cuda that has been interrupted previously
```
sudo rmmod nvidia_uvm 
sudo modprobe nvidia_uvm
```

# Update Nvidia driver
- Go to site: https://www.nvidia.com/download/index.aspx?lang=en-us
- Choose the your Nvidia Driver info:
![nvidia](/figs/Nvidia%20Driver%20info.png)
- Download run file '.run'
- Hit Ctrl+Alt+F1 and login using your credentials.
- Kill your current X server session by typing 
```
sudo service lightdm stop 
# or 
sudo lightdm stop
```
- Enter runlevel 3 by typing 
`sudo init 3`
- Install your *.run file.
    - cd path_to_downloaded_run_file
    ```
    chmod +x ./your-nvidia-file.run
    sudo ./your-nvidia-file.run
    ```
- You might be required to reboot when the installation finishes. If not, run 
```
# reboot ubuntu
shutdown -r

# if not, restart x server
sudo service lightdm start

# or 
sudo start lightdm 
```

kudos :tada: 