FROM huggingface/transformers-pytorch-gpu:latest
LABEL authors="Chenhui Zhang"
LABEL description="Docker image for running DecodingTrust with the dt-run command"

RUN apt update && apt install curl -y
RUN git clone https://github.com/AI-secure/DecodingTrust.git
WORKDIR DecodingTrust
RUN git checkout docker && pip install -e ".[all]" && pip install -U datasets && mkdir ./.cache

ENTRYPOINT ["dt-run"]
