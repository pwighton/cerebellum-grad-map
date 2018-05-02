# Cerebellum Gradient Mapping

## Generate `dockerfile`
```
docker run --rm kaczmarj/neurodocker:master generate "docker" \
  --base=neurodebian:stretch-non-free \
  --pkg-manager=apt \
  --install fsl \
  --FreeSurfer version=6.0.0-min \
  --Miniconda env_name=conda \
  --user=neuro \
  --workdir='/home/neuro' > dockerfile
```

## Build the dockefile
```
docker build .
```

## Build neurodebian dockerfile
```
docker build -f ./dockerfile.fs6-neurodebian .
```
