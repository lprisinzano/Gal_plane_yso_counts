# Gal_plane_yso_counts
This repository includes the notebook to estimate the number of young stars with age t<10Myrs and mass M>0.3 Msun  (211116_yso_3D_90b.ipynb).
Four Opsim surveys are considered. The total counts are estimated assuming to observe only with gri filters. We strongly recommend to adopt the Opsim
/sims_maf/fbs_2.0/vary_gp/vary_gp_gpfrac1.00_v2.0_10yrs.db to homogeneously map the Galactic Plane. The number of stars detected is maximum even in regions
with E(B-V)>0.2.  This is an important metric and we want to use the results to change our view of survey strategy

## How to use

### 1. Getting the notebook

Open a terminal, navigate to a folder of choice (let's call it `root`) and type

```
git clone https://github.com/Thalos12/Gal_plane_yso_counts.git
```

This will put all the files in this repo in the folder `root/Gal_plane_yso_counts`.

### 2. Getting the extinction map and the code for querying it.

- Download the map file from [this link](http://www-personal.umd.umich.edu/~wiclarks/rubin/merged_ebv3d_nside64_defaults.fits.gz) 
 http://www-personal.umd.umich.edu/~wiclarks/rubin/merged_ebv3d_nside64_defaults.fits.gz provided by Will Clarkson (in datalab, you can use `wget` to get the file). Extract the map (you can use `gunzip`) and be sure to put it in the same folder as the notebook, that is in `root/Gal_plane_yso_counts`.

- Get the code to read the map with git: in the terminal, navigate to `root` and type


```
git clone https://github.com/willclarkson/rubinCadenceScratchWIC.git
```


** WARNING ** Until the relevant changes are implemented into Will Clarkson's repository, the version with the necessary code comes from Alessandro Mazzi's fork, so pleare run also

```
git clone https://github.com/Thalos12/rubinCadenceScratchWIC.git rubinCadenceScratchWIC_fork
```

then get into the newly created folder and type

```
git checkout distmag_pixels_subset_2
```

to get the branch that has the working code. The notebook will use the code from there. When the code is ready, I will update the README and the notebook, and the rubinCadenceScratchWIC_fork will have to be deleted.

### 3. Using the notebook.

Open the notebook and run every cell needed.

---

Many thanks to Will Clarkson (@willclarkson) for helping implementing the required functions.
Code written by Peter Yoachim, Loredana Prisinzano and Alessandro Mazzi
