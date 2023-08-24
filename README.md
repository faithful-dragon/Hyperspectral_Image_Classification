# Hyperspectral_Image_Classification

HybridSN: Exploring 3-D–2-D CNN Feature Hierarchy for Hyperspectral Image Classification 🌄🔍

Hyperspectral image (HSI) classification is widely used for the analysis of remotely sensed images. 🔬📸 Hyperspec- tral imagery includes varying bands of images. 🌈🖼️ Convolutional neural network (CNN) is one of the most frequently used deep learning-based methods for visual data processing. 🧠💻 The use of CNN for HSI classification is also visible in recent works. 📚🔍 These approaches are mostly based on 2-D CNN. On the other hand, the HSI classification performance is highly dependent on both spatial and spectral information. 🌐📊 Very few methods have used the 3-D-CNN because of increased computational complexity. This letter proposes a hybrid spectral CNN (HybridSN) for HSI classification 🚀📡. In general, the HybridSN is a spectral–spatial 3-D- CNN 🌀🌟 followed by spatial 2-D-CNN. The 3-D-CNN facilitates the joint spatial–spectral feature representation from a stack of spec- tral bands 🌌🎨. The 2-D-CNN on top of the 3-D-CNN further learns more abstract-level spatial representation. 🖼️✨ Moreover, the use of hybrid CNNs reduces the complexity of the model compared to the use of 3-D-CNN alone. 🔀📉 To test the performance of this hybrid approach, very rigorous HSI classification experiments 🧪🔬 are per- formed over Indian Pines, University of Pavia, and Salinas Scene remote sensing data sets. 🛰️🏞️ The results are compared with the state- of-the-art hand-crafted as well as end-to-end deep learning-based methods. 💡🤖 A very satisfactory performance is obtained using the proposed HybridSN for HSI classification. 🏆🌟

# HYBRIDSN model😁🔥 workflow for HSI classification 📊🔍"

 
 ![HSI-RN](https://github.com/faithful-dragon/Hyperspectral_Image_Classification/assets/141810876/3f43bb64-1e2c-4ac5-96f8-afad97a8d52c)

 <img width="520" alt="Screenshot 2023-08-24 at 5 54 26 PM" src="https://github.com/faithful-dragon/Hyperspectral_Image_Classification/assets/141810876/fa5f7c66-2530-44e6-bcca-bdd66bc9da1c">



 

 # Datasets :
 We have used three publicly available HSI data sets,1 namely, Indian Pines (IP), University of Pavia (UP) and Salinas Scene (SA). The IP data set has images with 145×145 spatial dimension and 224 spectral bands in the wavelength range of 400 to 2500 nm, out of which 24 spectral bands covering the region of water absorption have been discarded. The ground truth available is designated into 16 classes of vegetation. The UP data set consists of 610 × 340 spatial dimension pixels with 103 spectral bands in the wavelength range of 430–860 nm. The ground truth is divided into nine urban land-cover classes. The SA data set contains the images with 512 × 217 spatial dimension and 224 spectral bands in the wavelength range of 360–2500 nm. The 20 water absorbing spectral bands have been discarded. In total, 16 classes are present in this data set.



One dataset : IP


Input image : 

![IP-FC](https://github.com/faithful-dragon/Hyperspectral_Image_Classification/assets/141810876/2f029076-a0a4-4b55-9fe5-4c3fdf454050)




Ground truth image : 

![IP-GT](https://github.com/faithful-dragon/Hyperspectral_Image_Classification/assets/141810876/b15a3ec7-de67-4058-ac87-3128efd0b896)



Prediction using hybridSN model

![IP-Pr](https://github.com/faithful-dragon/Hyperspectral_Image_Classification/assets/141810876/ecc6eefc-028b-4d94-aae1-66b906680cee)


![IP_legend](https://github.com/faithful-dragon/Hyperspectral_Image_Classification/assets/141810876/09b7bcf4-d34b-4505-952a-95dfb22c8491)



# Classification Report:

739067167043686 Test loss (%)
98.85714054107666 Test accuracy (%)
98.69622007530346 Kappa accuracy (%)
98.85714285714286 Overall accuracy (%)
97.35303236467394 Average accuracy (%)


                              precision    recall  f1-score   support

                     Alfalfa       0.94      1.00      0.97        32
                 Corn-notill       0.97      0.97      0.97      1000
                Corn-mintill       1.00      0.99      0.99       581
                        Corn       1.00      0.96      0.98       166
               Grass-pasture       0.99      1.00      0.99       338
                 Grass-trees       0.99      1.00      1.00       511
         Grass-pasture-mowed       1.00      0.95      0.97        20
               Hay-windrowed       1.00      1.00      1.00       335
                        Oats       1.00      0.93      0.96        14
              Soybean-notill       0.99      1.00      1.00       680
             Soybean-mintill       0.99      1.00      0.99      1719
               Soybean-clean       0.97      0.97      0.97       415
                       Wheat       1.00      0.99      0.99       143
                       Woods       1.00      1.00      1.00       886
Buildings-Grass-Trees-Drives       1.00      1.00      1.00       270
          Stone-Steel-Towers       1.00      0.83      0.91        65

                    accuracy                           0.99      7175
                   macro avg       0.99      0.97      0.98      7175
                weighted avg       0.99      0.99      0.99      7175


 # confusion matrix

[[  32    0    0    0    0    0    0    0    0    0    0    0    0    0     0    0]

 [   2  966    0    0    0    0    0    0    0    5   24    0    0    3     0    0]
 
 [   0    3  576    0    1    0    0    0    0    0    1    0    0    0     0    0]
 
 [   0    6    0  160    0    0    0    0    0    0    0    0    0    0     0    0]
 
 [   0    0    0    0  338    0    0    0    0    0    0    0    0    0     0    0]
 
 [   0    0    0    0    0  510    0    0    0    0    1    0    0    0     0    0]
 
 [   0    0    0    0    1    0   19    0    0    0    0    0    0    0     0    0]
 
 [   0    0    0    0    0    0    0  335    0    0    0    0    0    0     0    0]
 
 [   0    0    1    0    0    0    0    0   13    0    0    0    0    0     0    0]
 
 [   0    0    0    0    0    0    0    0    0  679    0    0    0    1     0    0]
 
 [   0    4    0    0    0    3    0    0    0    0 1712    0    0    0     0    0]
 
 [   0   12    0    0    0    0    0    0    0    0    0  403    0    0     0    0]
 
 [   0    0    0    0    2    0    0    0    0    0    0    0  141    0     0    0]
 
 [   0    0    0    0    0    0    0    0    0    0    0    0    0  886     0    0]
 
 [   0    0    0    0    1    0    0    0    0    0    0    0    0    0   269    0]
 
 [   0    0    0    0    0    0    0    0    0    0    0   11    0    0     0   54]]


 Thank You😄.



 


 
