FROM ubuntu

RUN apt-get update && apt-get install cowsay -y

ENV PATH="$PATH:/usr/games"

ENTRYPOINT ["cowsay"]

#docker run test <some text>
