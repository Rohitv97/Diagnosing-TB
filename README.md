# Diagnosing-TB
Using Neural Networks on Chest Xrays to find abnormal and normal xrays to diagnose for Pulmonary Tuberculosis


## Dataset
The [Dataset](https://www.kaggle.com/kmader/pulmonary-chest-xray-abnormalities) was taken from Kaggle.

In case you want to access the dataset through Kaggle API, use the following command to download the dataset:

```
kaggle datasets download -d kmader/pulmonary-chest-xray-abnormalities
```

The CNN was applied to a combination of 2 datasets.

###  China Set

The standard digital image database for Tuberculosis is created by the National Library of Medicine, Maryland, USA in collaboration with Shenzhen No.3 People’s Hospital, Guangdong Medical College, Shenzhen, China. The Chest X-rays are from out-patient clinics, and were captured as part of the daily routine using Philips DR Digital Diagnose systems. Number of X-rays:

* 336 cases with manifestation of tuberculosis, and
* 326 normal cases.

It is requested that publications resulting from the use of this data attribute the source (National Library of Medicine, National Institutes of Health, Bethesda, MD, USA and Shenzhen No.3 People’s Hospital, Guangdong Medical College, Shenzhen, China) and cite the following publications:

* Jaeger S, Karargyris A, Candemir S, Folio L, Siegelman J, Callaghan F, Xue Z, Palaniappan K, Singh RK, Antani S, Thoma G, Wang YX, Lu PX, McDonald CJ. Automatic tuberculosis screening using chest radiographs. IEEE Trans Med Imaging. 2014 Feb;33(2):233-45. doi: 10.1109/TMI.2013.2284099. PMID: 24108713
* Candemir S, Jaeger S, Palaniappan K, Musco JP, Singh RK, Xue Z, Karargyris A, Antani S, Thoma G, McDonald CJ. Lung segmentation in chest radiographs using anatomical atlases with nonrigid registration. IEEE Trans Med Imaging. 2014 Feb;33(2):577-90. doi: 10.1109/TMI.2013.2290491. PMID: 24239990

### Montogomery County Set

X-ray images in this data set have been acquired from the tuberculosis control program of the Department of Health and Human Services of Montgomery County, MD, USA. This set contains 138 posterior-anterior x-rays, of which 80 x-rays are normal and 58 x-rays are abnormal with manifestations of tuberculosis. All images are de-identified and available in DICOM format. The set covers a wide range of abnormalities, including effusions and miliary patterns. The data set includes radiology readings available as a text file.


## Running

* The IPython notebooks were trained on Google Colab with GPU(Tesla K80) enabled. The trained models have not been uploaded on to Github.
* 640 images were used to train, and 160 to validate the results

## Results

#### Resnet34
* The Resnet34 model trained over 20 epochs decreased the error rate from 0.518 to 0.081
* Learning Rate curve
![alt text](https://raw.githubusercontent.com/Rohitv97/Diagnosing-TB/master/resnet34-LR.PNG)
* Confusion Matrix
![alt text](https://raw.githubusercontent.com/Rohitv97/Diagnosing-TB/master/resnet34-confusion-matrix.PNG)
* Accuracy measured = 91.87%

#### Resnet50
* The Resnet50 model trained over 20 epochs decreased the error rate from 0.500 to 0.100
* Learning Rate curve
![picture alt](https://raw.githubusercontent.com/Rohitv97/Diagnosing-TB/master/resnet50-LR.PNG)
* Confusion Matrix
![alt text](https://raw.githubusercontent.com/Rohitv97/Diagnosing-TB/master/resnet50-confusion-matrix.PNG)
* Accuracy Measured = 90.0%

