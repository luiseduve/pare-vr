# PARE-VR
## Physiologically Adaptable Relaxation Experience through Virtual Reality

Project for Master Thesis in Health Informatics

Karolinska Institutet & Stockholm University, Sweden

If this project was useful for you, please reference the following papers in your work:

> Luis Quintero, John Muñoz, Panagiotis Papapetrou. *Open-Source Physiological Computing Framework using Heart Rate Variability in Mobile Virtual Reality Applications*. 2nd International Conference on Artificial Intelligence and Virtual Reality (AIVR 2019), San Diego, CA, USA. <https://doi.org/10.1109/AIVR46125.2019.00027>

> Luis Quintero, Panagiotis Papapetrou, John Muñoz, Uno Fors. *Implementation of Mobile-based Real-time Heart Rate Variability Detection for Personalized Healthcare*. Workshop TMDM in IEEE International Conference on Data Mining (ICDM2019), Beijing, China. <https://doi.org/10.1109/ICDMW.2019.00123>

**By: Luis Quintero** | https://luiseduve.github.io

## Description
Project that provides VR applications developed in Unity with access to HR and PPG data to execute physiologically adaptable behaviors.

The architecture consists on three application as shown in following image.

![Technical Architecture](https://github.com/luiseduve/pare-vr/blob/master/docs/img/TechnicalArchitecture.png)

The first application is developed in C using Tizen Studio and can be found in [App 1](App1_Tizen_PPG-Recorder/). It collects HR and PPG data from Samsung Smartwatches and send it through SAP (Samsung Accessory Protocol) to the paired mobile phone.

The second application is developed in Java using Android Studio and can be found in [App 2](App2_PhysioSense_v2/). Based on the framework [PhysioVR](https://github.com/PhysioTools/PhysioVR). It receives data from smartwatches through SAP protocol and runs an algorithm to detect peaks and calculate HRV from the collected signal. Then, the results of the calculation are sent through UDP to a mobile VR application to perform adaptations based on physiological data.

The last application is a package developed in Unity contains the scripts to receive UDP data and design adaptation rules based. Copy and paste the folder in a new Unity Project, the provided files are not complete because the tested solution was a proprietary software [CalmPlace](https://mimerse.com/products/calm-place/). The files can be adapted for any Unity application and be deployed on Android.

For **developer's manual** to setup the environments: [Click Here](docs/Brief-DevGuide-PARE-VR.pdf)

To review the whole **thesis**: [Click Here](http://luiseduve.github.io/files/2019_MasterThesis_LuisQuintero.pdf)
