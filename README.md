# SAR-AIS-Neighbourhood-Integration
The repository provides code level implementation of Synthetic Aprture Radar (SAR) - Automatic Identification System (AIS) data integration using neighbourhood technique. 

### Flowchart of SAR-AIS Neighbourhood model: 

![Alt text](Images/Figure_7.jpg?raw=true "Title")


### Input data: 

#### AIS data: 

AIS data is collected from vesselfinder.com. Following are some of specifications of AIS data:

Area coordinates -
Latitude bounds - 0.909 North to 2.898 North (degrees)
Longitude bounds - 104.132 East to 105.074 East (degrees)

Time range: 11:14:00 GMT to 11:20:00 GMT on 27 November 2019

#### SAR data:

SAR is collected from Sentinel -1 Copernicus Open Access Hub. Please visit - [link](https://scihub.copernicus.eu/)

SAR data specifications: 
Sentinel1 GRD product in IW mode taken during 11:17:22 to 11:17:47 27/11/2019.


#### Data Correction: 

AIS data is transmitted via Very High Frequency (VHF) signals between ships and corresponding AIS stations falling victim to signal attenuation. Signal attenuation makes data obtained at the receiving station unreliable. Therefore, it is important to screen inaccurate AIS data before its usage. Inspired from Zhang et al. (2017) [link](https://ieeexplore.ieee.org/document/8047888), two criteria are defined to screen AIS data:

1. Unreasonable stop in moving
2. Impossible high speed

#### Data Interpolation: 

Data interpolation is done using linear interpolation technique and piecewise hermite interpolation technique. For more details, refer - [link](https://doi.org/10.1016/j.asr.2021.08.042)

#### Azimuth Correction: 

When estimating target positions, SAR processing system usually assumes targets to be stationary. However, due to the relative motion between the target and SAR system, there is an azimuth shift in the return signals from the target (known as Doppler shift) and the return signal frequency increases when the SAR system approaches the target and decreases when the SAR system moves away from the target.

For more details on application of Azimuth shift, please refer Rees, W.G., 1990. Physical principles of remote sensing. 

#### SAR-AIS Neighbourhood Integration: 

A three-step approach is implemented for integration of SAR and AIS-based ships data: (i) time matching, (ii) position matching, and (iii) size matching. Please refer - [link](https://doi.org/10.1017/S0373463311000749). 


#### Disclaimer: 

The above work is done as part of research. Hence, while using the material, please cite below paper. 
Hrishikesh Relekar, Palanisamy Shanmugam, Transfer learning based ship classification in Sentinel-1 images incorporating scale variant features, Advances in Space Research, Volume 68, Issue 11, 2021, Pages 4594-4615, ISSN 0273-1177, https://doi.org/10.1016/j.asr.2021.08.042. 

I also encourage you to cite papers which are referred in various modules of proposed model. To contribute to project, please reach out on hrish.relekar@gmail.com

