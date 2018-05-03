# Cerebellum Gradient Mapping

## Generate the dockerfile
```
docker run --rm kaczmarj/neurodocker:master generate "docker" \
 --base=neurodebian:stretch-non-free \
 --pkg-manager=apt \
 --install fsl connectome-workbench \
 --freesurfer version=6.0.0-min \
 --miniconda env_name=conda \
   conda_install="python=3.6 nibabel numpy seaborn" \
 --user=neuro \
 --workdir='/home/neuro' > dockerfile
```

## Build the dockerfile
```
docker build -t cereb-grad-map .
```
