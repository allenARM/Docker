FROM gcc:4.9

COPY . /usr/src/myapp

WORKDIR /usr/src/myapp

RUN gcc -o myapp main.c

CMD ["./myapp"]

#docker build -t my-gcc-app .
#docker run -it --rm --name my-running-app my-gcc-app
