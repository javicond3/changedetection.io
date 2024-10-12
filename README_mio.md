Configurado en martell detrás de proxy martell
Crear red martell: docker network create --driver bridge martell
Notificaciones con slack (crear app y asociarla a workspace y canal, luego se configura dentro de la app de changedetection.io)
En el readme de changedetection.io viene como van las notificaciones
https://github.com/caronc/apprise#popular-notification-services: como se configura en changedetection.io slack
https://github.com/caronc/apprise/wiki/Notify_slack: crear app
Se puede configurar una contraseña para entrar en la app en settings (solo una) 
Se pueden exportar los wachete para poder importarlos luego también
Volumen: persistencia
Reverse proxy: More here https://github.com/dgtlmoon/changedetection.io/wiki/Running-changedetection.io-behind-a-reverse-proxy-sub-directory (en la wiki)
Ojo en reverse proxy: proxy_set_header Host "localhost"; -> cambiar por proxy_set_header Host $host;
Simplemente docker compose up -d