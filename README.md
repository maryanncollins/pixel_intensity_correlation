# pixel_intensity_correlation z-score
### This code will perform a normalization of the intensity between two channels, represented as a difference between two z-scores (`Δz-score`), as a way of visulizing where there is enrichment oen channel compared to the other.
A [z-score](https://www.codecademy.com/article/normalization) represents the number of standard deviations a value (x) is above or below the mean of a set of numbers when the data are normally distributed. This method of normalization centers the data around 0.

<img width="995" alt="Screenshot 2024-07-23 at 1 49 35 PM" src="https://github.com/user-attachments/assets/eeb1b442-dc61-4d1e-afa9-387cf12f304e">
<i>all images used in this demo are from ImageJ (https://imagej.net/ij/images/)</i>
<br>
<br>

> [!IMPORTANT]
> <b>DIRECTORY ORGANIZATION</b>: this is a guide for how folders/files should be organized
```
.
├── pixel_intensity_zscore.Rmd           <- code (saved here)
├── sample_images                        <- folder of fixed sample images with the following organization: 
│   ├── images                           <- folder called 'images' containing two sub-folders, split by channel (channel 1 and 2)
│   │   ├── ch_1                         <- sub-folder 1, contains all channel_1 slices, with the following name format
│   │   │   ├── C1_sample1_filename
│   │   │   ├── C1_sample2_filename
│   │   │   ├── ...
│   │   │   └── C1_sampleN_filename
│   │   ├── ch_2                         <- sub-folder 2, contains all channel_2 slices, with the same name format
│   │   │   ├── C2_sample1_filename
│   │   │   ├── C2_sample2_filename
│   │   │   ├── ...
│   │   │   └── C2_sampleN_filename
│   │   ├── sample1                      <- sample images (from: https://imagej.net/ij/images/)
│   │   ├── sample2                      
│   │   ├── ...                          
│   │   └── sampleN                      
│   └── output                           <- all output images saved here (will be generated automatically)
└── sample_movie                         <- create a folder for each movie file with the following organization: 
    ├── images                           <- folder called 'images' containing two sub-folders, split by channel (channel 1 and 2)
    │   ├── ch_1                         <- sub-folder 1, contains all channel_1 slices, with the following name format
    │   │   ├── C1_slice0001_filename
    │   │   ├── C1_slice0002_filename
    │   │   ├── ...
    │   │   └── C1_slice000N_filename
    │   ├── ch_2                         <- sub-folder 2, contains all channel_2 slices, with the same name format
    │   │   ├── C2_slice0001_filename
    │   │   ├── C2_slice0002_filename
    │   │   ├── ...
    │   │   └── C2_slice000N_filename
    │   └── sample_movie                 <- sample movie (from: https://imagej.net/ij/images/)
    └── output                           <- all output images saved here (will be generated automatically)
```

> [!TIP]
> - to split movies into splices, use ImageJ: Stack > Tools > Stack Splitter
> - input images can but either 8-bit or 16-bit .tif files
> - if `Error in apply(mtx.tmp, 2, rev) : dim(X) must have a positive length`
>   change LUT to grayscale for each channel
> - if green pixels appear, adjust the z-score range in line 172
>   `scale_fill_gradientn(labels = legend.labels, breaks = c(-6, 0, 6), limits = c(-6, 6)`
