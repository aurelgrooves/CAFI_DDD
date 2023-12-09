# CAFI/FAO Deforestation and Degradation Drivers Project CAFI DDD
deforestation and degradation monitoring in Central Africa

These scripts are used to support the assessment of direct drivers of deforestation and degradation in Central Africa. 
For more information on the CAFI Drivers data and project, visit [the website](https://www.fao.org/in-action/sepal/activities/drivers/en)

The SEPAL documentation on the worfklow is available [here](https://docs.sepal.io/en/latest/workflows/drivers.html)

This study is piloted in 6 countries in Central Africa: 
![CAFI study area](/images/study_area.png)

The GEE folder contains useful scripts to extract information from accessible datasets for the Central African region.

The eSBAE scripts perform the following:

esbae_05a_merge_esbae_ceo_str_random: This workflow combines the validated stratified random data from phase I with the eSBAE variables

esbae_05b_supervised_w_CAFI_data: performs a supervised classification of change types (deforestation, degradation, stable and non-forest) on the systematic eSBAE variables using the CEO validated data as training. 

esbae_05c_CAFI_sampling_for_CEO: using the supervised model in the previous step, the change probability model is stratified into 3 strata, and samples can be extracted proportionally for validation with CEO. 

esbae_05d_merge_sbae_ceo_systematic: the CEO validated data are merged with the eSBAE data for the country of interest

esbae_05e_supervised_CAFI_all_points: performs a supervised classification of change types on all points using the validated systematic data. The years of change are applied using CUSUM dates. 

esbae_06_calculate_areas: calculate areas based on all points, and estimates the margin of error using only validated points. 

