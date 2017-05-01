# Docker Instructions

To build the images:

```bash
docker build -t conda_cuda_base:latest ./base
docker build -t numba_gtc2017:latest ./notebooks
```

The notebook image takes an optional build argument `BRANCH` to
select the branch or commit to checkout

```
docker build -t numba_gtc2017:latest --build-arg BRANCH=master ./notebooks
```

Run the notebook with:

```bash
nvidia-docker run -p 8888:8888 -it numba_gtc2017:latest
```

It will start the jupyter notebook automatically.
