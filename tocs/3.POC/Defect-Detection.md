# Table of contents
- [Table of contents](#table-of-contents)
- [Intorduction](#intorduction)
- [Defect Detection Solution](#defect-detection-solution)
    - [USB Defect Detection](#usb-defect-detection)
    - [Screw Defect Detection](#screw-defect-detection)
- [Demo](#demo)
   
# Intorduction
We create a defect detection solution on EXMU-X261. When camera catch the image, the image will input to EXMU-X261. The EXMU-X261 will preprocess the image. After all, the DPU will inference image and output result with bounding box. The result will shows on screen.
![DD-flow](./fig/DD-flow.png)


# Defect Detection Solution
### USB Defect Detection
This solution can be used in factory to detect the logo or the assembly of components error.

PASS
![DD-OK](./fig/DD_predict_result_true.png)

NG
![DD-False](./fig/DD_predict_result_false.png)

### Screw Defect Detection
This solution can be used in factory to detect the screw defect.
![screw_predict_result](./fig/screw_predict_result.png)

# Demo
|Solution| Model | Input Size | FPS on X261 |
|:------:| :-------------: |:----: |:---:|
| USB | YOLOv4-tiny | 320x320  | 35 FPS |

![DD-USB](./fig/DD-USB.gif)
