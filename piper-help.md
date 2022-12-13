## Piper docking software commands 

To see piper commands and options, open your terminal and go to where the binary codes of piper are. Then, run the below command:

```
$ ./piper --help

```

Now, you will see the following options:

```
usage: ./piper [options] RECEPTOR LIGAND
perform fft docking of RECEPTOR and LIGAND

```




## Parameter files:

````
   -f <coeffs>          Use <coeffs> as the coefficient parameter file
                        (default: coef.prm)
   -p <atom>            Use <atom> as atom parameter file
                        (default: atom.prm)
   -r <rots>            Use <rots> as the rotations parameter file
                        (default: rot.prm)
   --ff-psf-rec=FILE    Use FILE as the receptor force field psf file
                        (default: rec.psf)
   --ff-psf-lig=FILE    Use FILE as the ligand force field psf file
                        (default: lig.psf)
                        
````                        
                        

## Output:

````
   -v                   Increase verbosity. Multiple -v options increase
                        the verbosity. The maximum is 2.
   --print-grids        Print the grid files
   
````

## Other options:

```
   -c <cellsize>        Use <cellsize> as grid cell size (default: 1.0)
   --grid-pad=<pad>     Use <pad> as fft grid padding (default: 2)
   --lig-all-sa         Rather than calculating solvent accessibility, mark all atoms as solvent accessible
   -k <k>               Use first <k> eigenvalues from prm file (default: all)
   -R <nrots>           Use first <nrots> rotation matrices from rotation file
                        (default: all)
   --surface-potential  Place pairwise potential only on surface atoms.
   -T <plan type>       Use <plan type> as planning type rigor for fftw.
                        (default: FFTW_ESTIMATE)
                        
```


## Multiple results per rotation:


````
   -d <radius>          Use <radius> as the angstrom radius of the top hit per
                        rotation to be marked. (default: 5.0)
   -t <N>               Save the top <N> results from each rotation.
                        (default: 1)
                        
````



## Functions:


```
   --pb=FILE            Read poisson boltzmann grid from FILE
   --pbt=<t>            Use <t> for poisson boltzmann extrema threshold (default: 40.0)
   --pb-scale=<k>       Use <k> for poisson boltzmann grid scaling (default: 1.0)
   --water_sigma=<sigma> Use <sigma> for gaussian water sphere (default: 10.0)
   --enative            Print energies for given input structures
   --maskrec=FILE       Mask receptor with FILE
   --masklig=FILE       Mask ligand with FILE
   --maskr=<k>          Mask all atoms within <k> angstroms of mask atoms
   --axis=FILE          Enforce symmetric docking. Use axis file

```


## VdW: 

```
   --scale_radii=<k>    Use <k> for prm radii scaling (default: 1.0)
   --msur_k=<k>         Use <k> for msur solvent and prm radii scaling (default: 1.0)
   --rvdw_sa_scale=<k>  Repulsive vdw sa scale (default: 0.9)
   --rvdw_nsa_scale=<k> Repulsive vdw not sa scale (default: 1.2)
   --avdw_sa_scale=<k>  Attractive vdw sa scale (default: 0.0)
   --avdw_sa_inc=<k>    Attractive vdw sa increment (default: 6.5)
   --avdw_nsa_scale=<k> Attractive vdw not sa scale (default: 0.0)
   --avdw_nsa_inc=<k>   Attractive vdw not sa increment (default: 6.5)
   
```
   
   
## Box mode:
   
``` 
   --box=FILE           Select FTRESULTS with box from FILE
   --box-pad=<float>    Padding around box (default=0.0)
   
```

   
## Restraints:

```
   --restraints=FILE    Use restraints from FILE
   
```

   
## Miscellaneous:
   
```
   -h, --help           Display this help and exit
   -V, --version        Display the version information and exit

```
