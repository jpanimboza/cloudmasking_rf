# cloudmasking_rf
Script for cloud masking of Sentinel - 2 imagery using Random Forest and atmospheric correction using SIAC

This project uses a map function to perform cloud masking using Random Forest classification.
The script works as follows:
1. The user loads a cloudy multispectral image and the cloud probability image
2. Creates of a cloud/no cloud band based on a limit (for example: 50%)
3. Imports the Sentinel-2 L1C collection
4. Applies SIAC correction https://github.com/MarcYin/SIAC
5. Clips the image collection using the AOI
6. Sets stratified sample for cloud/no cloud for training the RF classifier
7. Apples RF classification for cloud masking
