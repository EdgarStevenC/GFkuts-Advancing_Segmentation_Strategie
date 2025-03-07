# **"GFKuts" Hyperspectral image segmentation**

DEMO --> https://drive.mathworks.com/sharing/b20314be-a491-461a-ade6-6ce0a0dc6738 
 Symposium in Plant Omics Sciences 2021 (OMICAS): https://www.omicas.co/sites/default/files/2022-07/P4_EVENTO%20CIENT_PARTICIPACION_%20Edgar%20Correa_Simposio%202020.pdf

Colorado JD, Calderon F, Mendez D, Petro E, Rojas JP, Correa ES, et al. (2020) A novel NIR-image segmentation method for the precise estimation of above-ground biomass in rice crops. PLoS ONE 15(10): e0239591. https://doi.org/10.1371/journal.pone.0239591

Jimenez-Sierra, D. A., Correa, E. S., Benítez-Restrepo, H. D., Calderon, F. C., Mondragon, I. F., & Colorado, J. D. (2021). Novel Feature-Extraction Methods for the Estimation of Above-Ground Biomass in Rice Crops. Sensors, 21(13), 4369. https://doi.org/10.3390/s21134369

E. S. Correa, F. Calderon and J. D. Colorado, "GFkuts: a novel multispectral image segmentation method applied to precision agriculture," 2020 Virtual Symposium in Plant Omics Sciences (OMICAS), Bogotá, Colombia, 2020, pp. 1-6, https://doi.org/10.1109/OMICAS52284.2020.9535659

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
<img src="./imgREADME/GFKuts.png" alt="drawing" width="700"/>     
</p>


GFKuts approach by https://doi.org/10.3390/s21134369
 <p align="center">
<img src="./imgREADME/sensors-21-04369-g002.webp" alt="drawing" width="700"/>     
</p>
Open to providing guidance, support, or answers: e_correa@javeriana.edu.co
