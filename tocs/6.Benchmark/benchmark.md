<!--
 Copyright (c) 2023 Innodisk crop.
 
 This software is released under the MIT License.
 https://opensource.org/licenses/MIT
-->

# Benchmark

Model | Test Size | Parms(M) | FLOPs(B) | BSP Version | TOPS | PL | Inferencing Flow | FPS(E2E)
--- | --- | --- | --- | --- | --- | --- | --- | ---
YOLOv4-Tiny | 416 | 6.0535 | 6.9289 | v1.2.4 | 0.94 | h264 encoder | seq. | *29.8*
YOLOv4 | 416 | 64.33 | 129.5567 | v1.2.4 | 0.94 | h264 encoder | seq. | *8.7*

- E2E: end to end, 1080p 
- seq.: sequential ```read frame -> pre-process -> inference -> post-process -> output ```

# Benchmark: multiple-channel using VVAS

Channel | Res. | Model | Test Size | FPS(E2E)/Per-channel | SW Framework
--- | --- | --- | --- | --- | ---
4 | 1080p | YOLOv4-Tiny | 416 | *17* | VVAS 2.0
4 | 720p | YOLOv4-Tiny | 416 | *21* | VVAS 2.0
4 | 540p | YOLOv4-Tiny | 416 | *23.5* | VVAS 2.0

- Res.: Resolution from IP camera setting
- E2E: end to end 
- VVAS: Refer to [here](../3.POC/VVAS-Demo.md) 