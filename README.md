# vent_variation_clif_2024

This project will assess variation in ventilation across multiple sites.

## Setup

------------------------------------------------------------------------

### Create a fork of this repository

Create a fork of this repository, the plan will be to fix things as they arise with peoples data and/or fix things at the level of this script If you need to change something, please email Nick Ingraham and he will change the main script and you can pull changes

For more information [GIT - CLIF Setup Instructions](https://kaveric.github.io/clif-consortium/posts/github-clif/)

------------------------------------------------------------------------

### Ensure you have set up your site specific txt file in CLIF-1.0

These should be defined in that file

site

cliffed_file_path

file_format

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
