# vent_variation_clif_2024

This project will assess variation in ventilation across multiple sites.

## Setup

------------------------------------------------------------------------

### Create a fork of this repository

Create a fork of this repository, the plan will be to fix things as they arise with peoples data and/or fix things at the level of this script If you need to change something, please email Nick Ingraham and he will change the main script and you can pull changes

For more information [GIT - CLIF Setup Instructions](https://kaveric.github.io/clif-consortium/posts/github-clif/)



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

------------------------------------------------------------------------

### Ensure you have set up your site specific qmd file 

**MUST BE** in a folder shared with CLIF-1.0 or a subfolder with a shared parent (see above about folders)

These should be defined in that file. use this format and save as `site_specific_information.qmd`

#### finding `path_cliffed_files`
1) If you are the only user of these files and data structure.  You can hard code `path_cliffed_files`
    - this should point to all post-clif-files
    
2) If you share R projects on a server.  The base path may differ
    - Start by finding the first parent folder before your rclif files
    - use the find_up function to set that as the path
    - now use here to navigate DOWN that folder structure to find the rclif folder of interest!!
    

```{r}

## Clif Files Path

 # Option 1) 
 #  where are your clif files stored
 #  I need to find a parent folder first and then code in the rest of the path to my folder
 #  This will help with those that share using the same files
path_cliffed_files_start	<- find_up("CQODE DB Backbone")
path_cliffed_files_start
path_cliffed_files <- here(path_cliffed_files_start, "rclif")

 # OPTION 2) 
    # you can just hard code path_cliffed_files as well

```

#### Setting the other information
Change these as fits your needs for each project
```{r}
## Site
 # will help with saving tables
clif_institution <- "umn"


## QC check
 # change this to yes when you have run the script
i_ran_qc_script <- "yes"


## File type
 # choose between csv, xls, xlsx, fst, parquet 
 # all will work (uses readr, fst, arrow packages to choose the command and put the .xyz after the file!)
file_type	<- "parquet"

```




#### Full QMD file of `site_specific_information.qmd`
- Here is the full qmd file that should be used
- You can update however you need to 


```{r}
```{r}
# get path to clif 1.0
path_clif_1.0 <- find_up("CLIF-1.0")

## Clif Files Path

 # Option 1) 
 #  where are your clif files stored
 #  I need to find a parent folder first and then code in the rest of the path to my folder
 #  This will help with those that share using the same files
path_cliffed_files_start	<- find_up("CQODE DB Backbone")
path_cliffed_files_start
path_cliffed_files <- here(path_cliffed_files_start, "rclif")

 # OPTION 2) 
    # you can just hard code path_cliffed_files as well


## Site
 # will help with saving tables
clif_institution <- "umn"


## QC check
 # change this to yes when you have run the script
i_ran_qc_script <- "yes"


## File type
 # choose between csv, xls, xlsx, fst, parquet 
 # all will work (uses readr, fst, arrow packages to choose the command and put the .xyz after the file!)
file_type	<- "parquet"


# Get the current working directory
# might help with debugging 
path_current_project <- here::here()




print(clif_institution)
print(path_clif_1.0)
print(path_cliffed_files_start)
print(path_cliffed_files)
print(file_type) 
print(i_ran_qc_script) 
print(path_current_project) 

```
```
