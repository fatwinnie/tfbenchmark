# tfbenchmark
Running tensorflow benchmark and nbody with docker

## nbody-docker

### Build a nbody image based on nvidia/cudagl:tag
```
wget http://114.35.1.159/nbody/Dockerfile
docker build -t dqa4/nbody:[cuda_version] [PATH of Dockerfile]
```
### Run nbody benchmark
```
nvidia-docker run -it --rm dqa4/nbody:[cuda_version] ./nbody -benchmark
```
or
```
docker run --runtime=nvidia -it --rm dqa4/nbody:[cuda_version] ./nbody -benchmark
```
