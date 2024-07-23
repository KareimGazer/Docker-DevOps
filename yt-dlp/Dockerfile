FROM ubuntu:22.04

WORKDIR /my-app

RUN apt-get update && apt-get install -y curl python3
RUN curl -L https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp -o /usr/local/bin/yt-dlp
RUN chmod a+rx /usr/local/bin/yt-dlp

ENTRYPOINT ["yt-dlp"]

# define a default argument
CMD ["https://www.youtube.com/watch?v=Aa55RKWZxxI"]