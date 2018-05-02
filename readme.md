# Cerebellum Gradient Mapping

## Generate `dockerfile`
```
docker run --rm kaczmarj/neurodocker:master generate "docker" \
  --base=neurodebian:stretch-non-free \
  --pkg-manager=apt \
  --install fsl freesurfer miniconda\
  --user=neuro \
  --workdir='/home/neuro' > dockerfile
```

## Build the dockefile
```
docker build .
```
