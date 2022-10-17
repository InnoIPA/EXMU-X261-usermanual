# FAQ

# How to use xmutil to check Accelerate Application is loaded?
You can use `xmutil` to check the `listapps`. The active shows `1` means accelerate application is loaded.

```
xmutil listapps
```

<!-- ![load_dpu](./fig/load_dpu.png) -->

If the accelerate application not loaded. you can use `xmutil` to load accelerate application. And check the accelerate application list again.

<!-- ![unload_dpu](./fig/unload_dpu.png) -->

```
xmutil loadapp <accelerate application name>
```
<!-- ![load_sucess](./fig/load_sucess.png) -->


# How to update the application on X261?
ALL application support using RPM to upgrade.
  
# How to check the verion on EXMU-X261?
 - For BSP verion, using the following command to check. The BSP verion is `Ver.x.x.x`.

    ```
    bash /etc/init.d/welcome_logo.sh
    ```
    ![bsp-verion](./fig/bsp-verion.png)

 - For vitis-AI verion, using the following command to check. The vitis-AI verion can be seen at `VAI Version`
    ```
    xdputil query
    ```
    ![xdputil_query](./fig/xdputil_query.png)

 - The dpu-sc not preload in our system. If you need to check dpu-sc verion, the verion shows when running dpu-sc. 
   ![dpu-sc](./fig/dpu-sc-verion.png)
 
 - For stesting verion, stesting can't check verion yet. Would be added in future verion.
   
# Aborted to run dpu-sc?
When running the dpu-sc and got the error as following shows. It is because system doeesn't load DPU accelerate application yet.

![dpu-sc-aborted](./fig/dpu-sc-aborted.png)

Please load DPU accelerate application. Double check accelerate application list. And run dpu-sc again.
```
xmutil loadapp <dpu accelerate application name>
```

