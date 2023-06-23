FROM alpine
RUN apk --no-cache update 
RUN apk --no-cache upgrade
RUN apk add --no-cache bind
RUN mkdir -p /var/log/named
RUN chown named:named /var/log/named
RUN ln -sf /var/log/named/query.log /dev/stdout
EXPOSE 53/udp
CMD ["-4","-c","/etc/bind/named.conf","-g","-u","named"]
ENTRYPOINT ["/usr/sbin/named"]
