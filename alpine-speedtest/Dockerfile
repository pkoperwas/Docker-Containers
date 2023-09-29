FROM alpine
CMD ["/bin/sh"]
ENV SPEEDTEST_VERSION=1.2.0
RUN /bin/sh -c set -eux; wget -O speedtest.tgz https://install.speedtest.net/app/cli/ookla-speedtest-1.2.0-linux-x86_64.tgz; tar -xvf speedtest.tgz -C /usr/local/bin speedtest; rm speedtest.tgz
COPY docker-entrypoint.sh /usr/local/bin/ 
CMD ["speedtest"]
