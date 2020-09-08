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
    "% Read Dataset Chanel R-G-Re-N-RGB"
    
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

Classify the samples using a clustering algorithm. **Kmeans** has been used 

<p align="center">
<img src="./imgREADME/img5.png" alt="drawing" width="1000"/>  
</p>
A greater number of groups have been defined. This characteristic presents better results and allows segmenting more complex images.

Complex images like these:

<p align="center">
<img src="./imgREADME/Complex images.PNG" alt="drawing" width="1000"/>  
</p>

**The masks found will be presented as follows:**
<p align="center">
<img src="./imgREADME/img6.png" alt="drawing" width="1000"/>   
</p>

#### **In the command window will appear:**
<p align="center">
<img src="./imgREADME/img7.PNG" alt="drawing" width="700"/>     
</p>

---
The aim is to indicate which are the masks. **Which are of vegetation and which are of the ground**

    Enter: VEGETETION MASK like this "mask1 + mask2 + .." here: mask1+mask3 
    Enter: GROUND MASK like this "mask1 + mask2 + .." here: mask2
---

<sub> This must be done due to the random nature of the cluster. The masks change position each time the code is executed</sub>
 
 **The result of grouping with four channels:**
 <p align="center">
<img src="./imgREADME/img11.png" alt="drawing" width="700"/>     
</p>

 <p align="center">
<img src="./imgREADME/img9.png" alt="drawing" width="700"/>     
</p>

 <p align="center">
<img src="./imgREADME/img10.png" alt="drawing" width="700"/>     
</p>

### **Strategy 3**

Now **grabCut** optimization is used on the whole image

 <p align="center">
<img src="./imgREADME/img13.png" alt="drawing" width="700"/>     
</p>


### **Strategy 4**

Finally a refinement stage through **Guided filter**

 <p align="center">
<img src="./imgREADME/img14.png" alt="drawing" width="700"/>     
</p>
