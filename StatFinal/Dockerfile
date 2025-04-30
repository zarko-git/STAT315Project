FROM python:3.11.7-slim
LABEL maintainer="Scott A. Bruce <sabruce@tamu.edu>"
LABEL version="1.2"
LABEL description="Python Jupyter notebook development environment"

RUN apt-get update -y
RUN apt-get install -y gcc
RUN apt-get install -y build-essential libpq-dev
RUN apt-get install -y graphviz

RUN pip install --upgrade pip

RUN pip install numpy==1.26.3  
RUN pip install pandas==2.2.0 
RUN pip install seaborn==0.13.2 
RUN pip install jupyter==1.0.0 
RUN pip install scikit-learn==1.4.0 
RUN pip install SQLAlchemy==2.0.25 
RUN pip install psycopg2==2.9.9 
RUN pip install statsmodels==0.14.1 
RUN pip install dask[complete]==2024.1.1 
RUN pip install graphviz==0.20.1 
RUN pip install dask-ml==2023.3.24 
RUN pip install plotly==5.18.0

COPY FinalParts /home/notebooks/


WORKDIR /home/notebooks/

CMD jupyter notebook --no-browser --allow-root --ip 0.0.0.0
