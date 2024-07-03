# vent_variation_clif_2024

This project will assess variation in ventilation across multiple sites.

## Setup

------------------------------------------------------------------------

### Create a fork of this repository

Create a fork of this repository, the plan will be to fix things as they arise with peoples data and/or fix things at the level of this script If you need to change something, please email Nick Ingraham and he will change the main script and you can pull changes

For more information [GIT - CLIF Setup Instructions](https://kaveric.github.io/clif-consortium/posts/github-clif/)

------------------------------------------------------------------------

### Ensure you have set up your site specific txt file in CLIF-1.0

These should be defined in that file. use this format and save as `site_specific_information.txt`

|                  |                                           |           |                 |
|----------------|---------------------------------|----------|-------------|
| clif_institution | path_clif_files                           | file_type | i_ran_qc_script |
| umn              | Y:/DataStageData/CQODE DB Backbone/rclif/ | parquet   | yes             |


If needed, use this code one time. All future projects will work off this file which you can update as needed

```{r}
# Create the data frame
 

site_specific_info <- data.frame(

 ## Site
  # will help with saving tables
  clif_institution        = "umn"
  
 ## Clif Files Path
  # where are your clif files stored
  path_clif_files         = "Y:/DataStageData/CQODE DB Backbone/rclif/",

 ## File type
  # choose between csv, xls, xlsx, fst, parquet 
  # all will work (uses readr, fst, arrow packages to choose the command and put the .xyz after the file!)
  file_type               = "parquet",

 ## QC check
  # change this to yes when you have run the script
  i_ran_qc_script         = "no",

)

write_csv(site_specific_info, "site_specific_information.csv")

```

------------------------------------------------------------------------

### Create a folder with your fork

This must be in the SAME place as CLIF-1.0 OR within a subfolder that shares a location at somepoint in the path with CLIF-1.0

#### Good 😊

The project folder is in the same or a subfolder of the `CLIF-1.0` folder

```         
Y:
├── Nick
    ├── CLIF-1.0 📁
    ├── other folder
    └── vent_variation_clif_2024 📁


Y:
├── Nick
    ├── CLIF-1.0 📁
    ├── other folder
    ├── other folder
        ├── other folder
            └── vent_variation_clif_2024 📁
```

#### Bad 😟

The project folder is not within a parent folder that shares its path with `CLIF-1.0`

```         
├── Nick 
    ├── CLIF-1.0 📁
    ├── other folder
    ├── other folder
├── other folder
    └── vent_variation_clif_2024 📁
```
