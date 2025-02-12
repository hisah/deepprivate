===============================================================================

# Image Privacy Prediction Using Deep Neural Networks

This repository contains the code, features, and data for our following papers:

    Ashwini Tonge and Cornelia Caragea. 2018 “On the Use of Deep Features for Online Image Sharing.”
    In WWW’18 Companion: The 2018 Web Conference Companion, Lyon, France.
    
    Ashwini Tonge and Cornelia Caragea. 2016 “Image Privacy Prediction Using Deep Features.” In: Proceedings
    of the 30th American Association for Artificial Intelligence (AAAI 2016), Student Abstract and Poster
    Program, Phoenix, Arizona, USA, 2016.    

If you find the repository useful for your research, please cite our paper(s):

    @inproceedings{tongemsm18,
      author    = {Ashwini Tonge and
                   Cornelia Caragea},
      title     = {On the Use of ``Deep'' Features for Online Image Sharing},
      booktitle = {The Web Conference Companion},
      year      = {2018},

    }
    
    @inproceedings{DBLP:conf/aaai/TongeC16,
      author    = {Ashwini Tonge and
                   Cornelia Caragea},
      title     = {Image Privacy Prediction Using Deep Features},
      booktitle = {Proceedings of the Thirtieth {AAAI} Conference on Artificial Intelligence,
                   February 12-17, 2016, Phoenix, Arizona, {USA.}},
      pages     = {4266--4267},
      year      = {2016},
      timestamp = {Thu, 21 Apr 2016 19:28:00 +0200},
      biburl    = {http://dblp.uni-trier.de/rec/bib/conf/aaai/TongeC16},
      bibsource = {dblp computer science bibliography, http://dblp.org}
    }
    
    
# Features

You can find the features derived from the pre-trained networks at:

    AlexNet: deepprivate/Features/AlexNet/pre-trained-features/
    GoogLeNet: deepprivate/Features/GoogLeNet/pre-trained-features/
    VGG: deepprivate/Features/VGG/pre-trained-features/
    ResNet: deepprivate/Features/ResNet/pre-trained-features/
    
You can find the probabilities obtained for privacy classes (public and private) using the fine-tuned networks at:

    AlexNet: deepprivate/Features/AlexNet/fine-tune/prob/
    GoogLeNet: deepprivate/Features/GoogLeNet/fine-tune/prob/
    VGG: deepprivate/Features/VGG/fine-tune/prob/
    ResNet: deepprivate/Features/ResNet/fine-tune/prob/
    
# Data

You can find dataset and it's Train/Test splits at: deepprivate/dataset/dataset-splits-27k/

# Code

    1. Feature extraction from the pre-trained networks 
       Requirements: CAFFE, a deep learning framework.
       extract_to_txt <train|test> <path_to_weight_file> <path_to_model_prototxt> <path_to_csv> <blob_name> <total_no_images> 
       <output_format> [CPU/GPU] [DEVICE_ID=0]
       
    2. To Create CSV for the extracted features using Caffe
       Requirements: JAVA
       Java -jar CaffeFeatures.jar feature_file filenames_file privacy_settings_file 


