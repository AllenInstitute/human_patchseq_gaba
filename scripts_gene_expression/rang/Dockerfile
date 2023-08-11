FROM rocker/r-ver:4.1.1
RUN apt-get update -qq && apt-get install -y libpcre3-dev zlib1g-dev pkg-config libcurl4-openssl-dev && apt-get install -y libcurl4-openssl-dev libglpk-dev libgmp3-dev libicu-dev libpng-dev libssl-dev libxml2-dev make pandoc python3 zlib1g-dev
COPY rang.R ./rang.R
RUN Rscript rang.R
CMD ["R"]
