Singularity recipe files for the Oxford Nanopore Guppy protocol 

Note: you must download the RPMs from the Nanopore Tech portal: https://community.nanoporetech.com/downloads (requires registration, but creating an account is free)

Note: RE previous note: This is suggested, but not technically true. Once you know the filename/link you can download the RPM from aywhere via HTTPS.

### generate symlinks
Once the container is built a safe-ish way to do generate the symlinks for the container executables is,
```
$ apptainer exec guppy-6.4.6.sif sh -c "find /usr/bin -executable -name 'guppy*' -printf '%f\n'" | xargs -L1 ln -sv guppy-6.4.6.sif
'guppy_aligner' -> 'guppy-6.4.6.sif'
'guppy_barcoder' -> 'guppy-6.4.6.sif'
'guppy_basecall_client' -> 'guppy-6.4.6.sif'
'guppy_basecall_server' -> 'guppy-6.4.6.sif'
'guppy_basecaller' -> 'guppy-6.4.6.sif'
'guppy_basecaller_duplex' -> 'guppy-6.4.6.sif'
'guppy_basecaller_supervisor' -> 'guppy-6.4.6.sif'
```



