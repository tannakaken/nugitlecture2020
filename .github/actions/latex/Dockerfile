FROM aruneko/texlive

RUN apt update \
  && apt install -y --no-install-recommends \
    curl \
    python3

RUN mktexlsr && mkdir -p /app
WORKDIR /app

ADD entrypoint.sh /entrypoint.sh
RUN ["chmod", "+x", "/entrypoint.sh"]
ENTRYPOINT ["/entrypoint.sh"]
