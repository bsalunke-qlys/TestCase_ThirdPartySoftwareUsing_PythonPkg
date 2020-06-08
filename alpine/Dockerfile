FROM bsalunke/alpine:pip_installed 
RUN apk update
RUN mkdir -p /usr/local/appusr/
ARG PATH=/usr/local/appusr/
RUN /usr/bin/pip install --install-option="--prefix=/usr/local/appusr/" numpy
ENV PYTHONPATH=/usr/local/appusr/lib/python2.7/site-packages/
COPY ./app.py /usr/local/appusr/bin/
ENTRYPOINT ["python", "/usr/local/appuser/bin/app.py"]   
