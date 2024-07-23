FROM ubuntu:22.04
RUN apt-get update && apt-get install -y curl
COPY script.sh .
RUN chmod +x script.sh
ENTRYPOINT [ "./script.sh" ]
CMD [ "helsinki.fi" ]