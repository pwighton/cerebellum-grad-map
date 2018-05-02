# Cerebellum Gradient Mapping

## Generate `dockerfile`
```
docker run --rm kaczmarj/neurodocker:0.4.0rc1 generate "docker" \
  --base=neurodebian:stretch-non-free \
  --pkg-manager=apt \
  --install fsl FreeSurfer Miniconda\
  --user=neuro \
  --workdir='/home/neuro' > dockerfile
```

## Build the dockefile
```
docker build .
```
