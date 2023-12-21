<!--
 Copyright (c) 2022 Innodisk Crop.
 
 This software is released under the MIT License.
 https://opensource.org/licenses/MIT
-->

# Changelogs

Type | desc. | version | Autor
--- | --- | --- | ---
Feat | Introduction of EXMU-X261 hardware<br/> Introduction of EXMU-X261 BSP v0.0.3 LTS<br/> Introduction of EXMU-X261 software application | 0.0.1 | Ju (hueiru_chen@innodisk.com)
doc | Add workflow of flashing qspi<br/> Update workflow of flashing emmc<br/> Update A2 carrier board info<br/> Update rpm discription<br/> Update "What is BSP"<br/> Modify FAQ and dependency versions<br/> Fix typos<br/> | 0.0.2 | Ju (hueiru_chen@innodisk.com)
doc | Update BSP v1.0.4 for A3 carrier board | 0.0.3 | Ju (hueiru_chen@innodisk.com)
doc | 1. Modify release note to changelog <br/> 2. add case study section <br/> 3. Modify wording <br/> 4. add ANPR.md <br/> 5. Rearrange defect detection| 0.0.4 | AH (allen_huang@innodisk.com)
doc | Add OTA.md <br/> Add utilities-intro.md <br/> Add some VVAS details <br/>  Hardware configuration reference diagram <br/>  Pre-build image intro and flashing details. <br/> | 0.0.5 | Billy (billy_chen@innodisk.com) <br/> Ju (hueiru_chen@innodisk.com) <br/> Jerry (jerry_hong@innodisk.com)
doc | Correct typos <br/> Correct path errors <br/> Add some new FAQs <br/> Add testing report <br/> | 0.0.6 | <br/> Ju (hueiru_chen@innodisk.com)


# Dependencies Version

BSP | Vitis-AI | VVAS|stesting|OTA|
|:---:|:---:|:---:|:---:|:---:|
|1.0.4|1.4|1.0|0.0.4||
|1.2.2|2.5|2.0|0.0.6||
|1.2.4|2.5|2.0|0.0.7||

- The dpu-sc would not be preload in BSP.
- The VVAS not be support before BSP version v0.0.3. Would be support start from v1.0.4 version.
- Hooray! OTA and Chboot is about to land with BSP 1.2.5. Stay tuned.
