<!--
 Copyright (c) 2022 Innodisk crop.
 
 This software is released under the MIT License.
 https://opensource.org/licenses/MIT
-->

- [How to update qspifw.](#how-to-update-qspifw)
# How to update qspifw.
- For partition A.
    ```
    sudo flashcp -v BOOT.BIN /dev/mtd5
    ```
- For partition B.
    ```
    sudo flashcp -v BOOT.BIN /dev/mtd7
    ```
- Example of successfuly update qspifw.
    ![](doc/update_qspifw.gif)