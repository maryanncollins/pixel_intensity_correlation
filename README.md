# pixel_intensity_correlation

DIRECTORY ORGANIZATION: this is a guide for how folders/files should be organized
- to split movies into splices, use ImageJ: Stack > Tools > Stack Splitter

```
.
└── pixe_intensity_zscore.Rmd                 <- code (saved here)
     ├── sample_images                        <- folder of fixed sample images with the following organization: 
     │   ├── images                           <- folder called 'images' containing two sub-folders, split by channel (channel 1 and 2)
     │   │   ├── ch_1                         <- sub-folder 1, contains all channel_1 slices, with the following name format
     │   │   │   ├── C1_sample1_filename
     │   │   │   ├── C1_sample2_filename
     │   │   │   ├── ...
     │   │   │   └── C1_sampleN_filename
     │   │   └── ch_2                         <- sub-folder 2, contains all channel_2 slices, with the same name format
     │   │   │   ├── C2_sample1_filename
     │   │   │   ├── C2_sample2_filename
     │   │   │   ├── ...
     │   │   │   └── C2_sampleN_filename
     │   │   ├── sample1                      <- sample images (from: https://imagej.net/ij/images/)
     │   │   ├── sample2                      
     │   │   ├── ...                          
     │   │   └── sampleN                      
     │   └── output                           <- all output images saved here (will be generated automatically)
     ├── sample_movie                         <- create a folder for each movie file with the following organization: 
     │   ├── images                           <- folder called 'images' containing two sub-folders, split by channel (channel 1 and 2)
     │   │   ├── ch_1                         <- sub-folder 1, contains all channel_1 slices, with the following name format
     │   │   │   ├── C1_slice0001_filename
     │   │   │   ├── C1_slice0002_filename
     │   │   │   ├── ...
     │   │   │   └── C1_slice000N_filename
     │   │   └── ch_2                         <- sub-folder 2, contains all channel_2 slices, with the same name format
     │   │       ├── C2_slice0001_filename
     │   │       ├── C2_slice0002_filename
     │   │       ├── ...
     │   │       └── C2_slice000N_filename
     │   └── output                           <- all output images saved here (will be generated automatically)
     └── image_filenameN                      <- sample movie (from: https://imagej.net/ij/images/)
