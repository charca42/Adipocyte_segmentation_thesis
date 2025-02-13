# Adipocyte_segmentation_thesis
Additional information about the custom model used for adipocyte segmentation, and files to use and improve the model.

This folder holds the protocol, custom model, and helpful QuPath scripts to automate the segmentation and assessment of adipocytes.

You will need to install Cellpose and QuPath. QuPath is simple to install, but Cellpose is a bit trickier, there are some tutorials online that can help. See https://cellpose.readthedocs.io/en/latest/installation.html 

If you want to improve on the model, you will need the training images. I didn't include them in this because of file size restrictions, but you can message me about those. You don't need the training images to run the custom model, but you do need the training images if you wish to train the model further. 

The model works decently well but it still struggles with smaller cells and cells with not strictly defined boundaries. You can add more training images to improve the model's performance. Training images have to be fully segmented, so you can run a general model on the image, manually fix the segmentation, and add it to the training image directory. Adding training images won't change the current model, but you can train a new and improved model with the updated training images.

Cellpose comes with a GUI but you can give it more precise instructions using command line interface. I have more about this in the protocol (and there is a guide at https://cellpose.readthedocs.io/en/latest/cli.html#cellpose-cli) but a usage example is:

cellpose --dir [PATH TO SAMPLE IMAGES] --pretrained_model [MODEL NAME] --diameter 50.0 --min_size 20 --chan 0 --exclude_on_edges 

Feel free to contact me (https://github.com/charca42) if you have other questions.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Citations:

Bankhead, P. et al. QuPath: Open source software for digital pathology image analysis. Scientific Reports (2017).
https://doi.org/10.1038/s41598-017-17204-5

Pachitariu, M. & Stringer, C. (2022). Cellpose 2.0: how to train your own model. Nature methods, 1-8.
