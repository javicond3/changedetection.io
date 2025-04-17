# Configurado en martell detrás de proxy martell
Crear red martell: docker network create --driver bridge martell

Reverse proxy: More here https://github.com/dgtlmoon/changedetection.io/wiki/Running-changedetection.io-behind-a-reverse-proxy-sub-directory (en la wiki)
Ojo en reverse proxy: proxy_set_header Host "localhost"; -> cambiar por proxy_set_header Host $host;
Y no hay que configurar BASE_URL=https://servicios-ging.dit.upm.es/wachete/
Simplemente docker compose up -d

Se puede configurar una contraseña para entrar en la app en settings (solo una) 


# Notificaciones
Notificaciones con slack (crear app y asociarla a workspace y canal, luego se configura dentro de la app de changedetection.io)
En el readme de changedetection.io viene como van las notificaciones
https://github.com/caronc/apprise#popular-notification-services: como se configura en changedetection.io slack
https://github.com/caronc/apprise/wiki/Notify_slack: crear app


Para gmail tienes que usar:
mailto://{usser}:{app password}@gmail.com
(Ahora ya no vale con la password de la cuenta tienes que crear app password) -> necesitas tener la doble autenticación en gmail

# Backups
Se pueden exportar los wachete para poder importarlos luego también
Volumen: persistencia, ahora mismo en ./datastore. Simplemente tienes que exportar el .zip del backup y al reiniciar automáticamente lo debe de coger


# Configurar RENFE

Poner 30 segundos en la carga al activar browser en cada wachete

document.getElementsByName('desOrigen')[0].value = "MADRID (TODAS)"
document.getElementsByName('cdgoOrigen')[0].value = "0071,MADRI,null"

document.getElementsByName('cdgoDestino')[0].value = "0071,22100,22100"
document.getElementsByName('desDestino')[0].value = "OURENSE"

document.getElementsByName('FechaIdaSel')[0].value = '11/06/2025'
document.getElementsByName('FechaVueltaSel')[0].value = '11/06/2025'


document.getElementsByName('FechaIdaSel')[0].parentElement.parentElement.submit()

Poner también 30 segundos de espera en la carga tras el submit (wait for seconds)


Una vez configurado y triggeado por primera vez puedes seleccionar que parte queires que visualice el wachete