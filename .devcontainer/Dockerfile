FROM python:3.10.14
USER root

RUN apt-get update && \
    apt-get -y install --reinstall ca-certificates && \
    apt-get -y install software-properties-common && \
    pip install --upgrade pip && \
    apt-get install -y sudo wget vim curl gawk make gcc

# Install Basic Packages
RUN pip install ipykernel jupyter && \
    pip install scikit-learn && \
    pip install matplotlib && \
    pip install feature-engine && \
    pip install pandas && \
    pip install streamsync[ds] && \
    pip install tqdm && \
    pip install tensorflow && \
    pip install xgboost && \
    pip install lightgbm && \
    pip install fastapi && \
    pip install uvicorn && \
    pip install pillow && \
    pip install python-multipart && \
    pip install shap && \
    pip3 install torch && \ 
    pip install torchvision && \
    pip install torchaudio

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
