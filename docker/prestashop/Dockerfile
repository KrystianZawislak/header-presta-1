FROM php:8.5.12-apache-bookworm@sha256:5e4418695f9b13b75edefaff547125bf6be267e865931731bdd5946461505736 AS patched-php

FROM prestashop/prestashop:9.1.5-8.5@sha256:9e006667c2cfe28daf27f3d49ac0b741d725a2fc0854ec39ebdbc8193e14ef92

ENV PHP_VERSION=8.5.12

COPY --from=patched-php /usr/local/bin/php /usr/local/bin/php
COPY --from=patched-php /usr/lib/apache2/modules/libphp.so /usr/lib/apache2/modules/libphp.so
