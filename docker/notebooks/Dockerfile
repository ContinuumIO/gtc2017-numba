# Build with:
#     docker build -t numba_gtc2017:latest .
# Run with:
#     nvidia-docker run -p 8888:8888 -it numba_gtc2017:latest
FROM conda_cuda_base:latest

RUN conda install -y scipy matplotlib

RUN git clone https://github.com/ContinuumIO/gtc2017-numba

WORKDIR ./gtc2017-numba

ARG BRANCH="master"
RUN git fetch && git checkout $BRANCH

CMD jupyter notebook --ip=*
