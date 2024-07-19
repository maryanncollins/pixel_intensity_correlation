# pixel_intensity_correlation
$ tree
├── LICENSE
├── README.md
└── R_code
    ├── pixel.intensity_norm.mean       <- Analysis using mean pixel intensity
    │   └── 2channels_delta.mean        <- for 2 channel images
    │       └── image_file_name         <- create a folder for each image with the following organization: 
    │           ├── images              <- folder with the images split by channel
    │           │   ├── Ch_1            <- channel_1
    │           │   └── Ch_2            <- channel_2
    │           └── output              <- output images from analysis saved here
    └── pixel.intensity_norm.SD         <- Analysis using StD pixel intensity
        ├── 1channel_zscore             <- for 1 channel images
        └── 2channel_delata.zscore      <- for 2 channel images
            ├── pixel.intensity.norm.sd_2channels.Rmd
            └── file_name               <- create a folder for each image with the following organization: 
                ├── images              <- folder with the images split by channel
                │   ├── Ch_1            <- channel_1
                │   └── Ch_2            <- channel_2
                └── output              <- output images from analysis saved here
