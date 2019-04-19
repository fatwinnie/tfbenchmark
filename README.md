# tfbenchmark
Running tensorflow benchmark and nbody with docker

## nbody-docker

### Build a nbody image based on nvidia/cudagl:tag
```
wget https://raw.githubusercontent.com/hao3924/tfbenchmark/nbody-docker/Dockerfile
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
