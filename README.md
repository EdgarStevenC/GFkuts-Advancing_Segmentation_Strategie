# **"GFKuts" Hyperspectral image segmentation**

<p align="center">
<img src="./imgREADME/baner.PNG" alt="drawing" width="1000"/>  
</p>

This guide has been developed with images captured with the remote sensing camera **parrot sequoia**. The **RGN image** represents the reconstruction of a multispectral image

<p align="center">
<img src="./imgREADME/img1.png" alt="drawing" width="1000"/>  
</p>

---
This project was written in MatLab softwar. To run it: **open PX.m**

    if you want to use another image change the reference in section:
    **"% Read Dataset Chanel R-G-Re-N-RGB"**
    
    Run "PX.m"
    
    
---

## **GFKuts works thereby**

### **Strategy 1**
Collect image samples with a random distribution. "between 40% and 60% of the total samples"
<p align="center">
<img src="./imgREADME/img4.png" alt="drawing" width="1000"/>  
</p>
<p align="center">
<img src="./imgREADME/img3.png" alt="drawing" width="1000"/>  
</p>

### **Strategy 2**

Classify the samples using a clustering algorithm. In this case, **Kmeans** has been used 

<p align="center">
<img src="./imgREADME/img3.png" alt="drawing" width="1000"/>  
</p>
