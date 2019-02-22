FROM pypy:3

WORKDIR /usr/src/app

#COPY requirements.txt ./
#RUN pip install --no-cache-dir -r requirements.txt

COPY . .

CMD [ "pypy3", "./hello.py" ]

#docker build -t my-python-app .
#docker run -it --rm --name my-running-app my-python-app
