FROM continuumio/miniconda3
ADD tf.yml /tmp/tf.yml
RUN conda env create -f /tmp/tf.yml

# Pull the environment name out of the environment.yml
RUN echo "source activate $(head -1 /tmp/tf.yml | cut -d' ' -f2)" > ~/.bashrc
ENV PATH /opt/conda/envs/$(head -1 /tmp/tf.yml | cut -d' ' -f2)/bin:$PATH
