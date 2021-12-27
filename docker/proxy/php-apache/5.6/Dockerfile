FROM webdevops/php-apache:5.6
RUN a2enmod remoteip \
&& chmod +x /opt/docker/provision/service.d/postfix.sh \
&& bash /opt/docker/provision/service.d/postfix.sh \
&& mkfifo /var/spool/postfix/public/pickup

RUN sed -i 's/autostart = false/autostart = true/' /opt/docker/etc/supervisor.d/postfix.conf
