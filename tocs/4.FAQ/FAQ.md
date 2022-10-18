<!--
 Copyright (c) 2022 Innodisk crop.
 
 This software is released under the MIT License.
 https://opensource.org/licenses/MIT
-->

- [How to update qspi fw.](#how-to-update-qspi-fw)
# How to update qspi fw.
- For partition A.
    ```
    sudo flashcp -v BOOT.BIN /dev/mtd5
    ```
- For partition B.
    ```
    sudo flashcp -v BOOT.BIN /dev/mtd7
    ```
