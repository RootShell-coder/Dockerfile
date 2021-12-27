FROM webdevops/php-apache:7.4
RUN a2enmod remoteip \
&& chmod +x /opt/docker/provision/service.d/postfix.sh \
&& bash /opt/docker/provision/service.d/postfix.sh \
&& mkfifo /var/spool/postfix/public/pickup

RUN sed -i 's/autostart = false/autostart = true/' /opt/docker/etc/supervisor.d/postfix.conf
