FROM alpine as build
RUN apk --no-cache add  curl && curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py && apk del curl

FROM gcr.io/distroless/python3
MAINTAINER Alexander Lindner <25225552+alexander-lindner@users.noreply.github.com>

COPY --from=build  get-pip.py /

RUN python /get-pip.py
RUN pip install magic-wormhole

ENTRYPOINT ["wormhole"]

ENV LC_ALL=C.UTF-8
ENV LANG=C.UTF-8

WORKDIR /data
