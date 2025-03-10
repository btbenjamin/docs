---
title: 'Crear respuestas automáticas en OWA'
excerpt: 'Cómo configurar respuestas automáticas en OWA'
updated: 2024-10-22
---

## Objetivo

Esta herramienta de Exchange le permite configurar respuestas automáticas, de manera de responder a los mensajes de correo electrónico enviados a su cuenta en función de diversos casos de uso, por ejemplo, un mensaje de fuera de la oficina <i>(out-of-office</i>).

**Descubra cómo activar las respuestas automáticas mediante Outlook en la web (OWA).**

## Requisitos

 - Haber instalado una solución de correo de OVHcloud [Exchange](/links/web/emails-hosted-exchange) o [Email Pro](/links/web/email-pro)
- Tener acceso a la cuenta de correo (dirección de correo electrónico y contraseña).

## Procedimiento

> [!warning]
>
> Si su dirección de correo electrónico está asociada a un producto **MX Plan** (incluida con los [alojamientos web](/links/web/hosting) y los [alojamientos gratuitos 100M](/links/web/domains-free-hosting), su área de cliente ofrece una sección titulada `Gestión de los contestadores`{.action}. En ese caso, deberá crear una respuesta automática desde el área de cliente de OVHcloud, utilizando la documentación "[MX Plan - Crear una respuesta automática en una dirección de correo electrónico](/pages/web_cloud/email_and_collaborative_solutions/mx_plan/feature_auto_responses)".

### Activar la herramienta

Inicie sesión en su cuenta de Exchange a través del [correo electrónico basado en la web de OVHcloud](/links/web/email). Haga clic en el símbolo del engranaje en la parte superior derecha para desplegar el menú "Opciones" y seleccione `Respuestas automáticas`{.action}.

![owaoptions](images/exchange-autorep-step1.png){.thumbnail}

En esta interfaz, simplemente active la herramienta seleccionando `Enviar respuestas automáticas`{.action}. Puede especificar un periodo de tiempo exacto en los campos siguientes o activarla de forma indefinida.

> [!primary]
>
> Si no especifica una hora de inicio y de finalización, la respuesta automática deberá desactivarse manualmente.

Escriba su mensaje en el cuadro de edición y confirme con el botón `Guardar`{.action} que se encuentra en la parte superior izquierda.

![owaautoreply](images/exchange-autorep-step2.png){.thumbnail}

### Tipos de respuestas

Las instrucciones anteriores se aplican a los mensajes de correo electrónico enviados por los usuarios de su servicio de Exchange. Puede crear un mensaje distinto para todos los demás usuarios si marca la casilla «Enviar mensajes de respuesta automática a remitentes fuera de mi empresa». Entonces tendrá dos opciones adicionales de respuesta automática:

- **«Enviar respuestas solo a los remitentes en mi lista de contactos»**: únicamente sus contactos recibirán un mensaje.

- **«Enviar respuestas automáticas a todos los remitentes externos»**: todas las personas que le envíen mensajes de correo electrónico durante su ausencia recibirán un mensaje.

Puede escribir un mensaje alternativo para los remitentes externos en el segundo cuadro de edición. Por ejemplo, un caso típico de uso sería responder con el primer mensaje a sus colegas y con el segundo, a amigos, clientes o cualquier otra persona que pueda contactarle.

![owaaddreply](images/exchange-autorep-step3.png){.thumbnail}

### Información adicional

- Aunque tenga activada la función de respuesta automática, seguirá recibiendo sus mensajes de correo electrónico en la bandeja de entrada como de costumbre.

- Cada remitente recibirá una sola respuesta automática para evitar bucles de correo electrónico y correos no deseados.

## Más información

[Usar Outlook en la web (OWA) con una cuenta de Exchange](/pages/web_cloud/email_and_collaborative_solutions/using_the_outlook_web_app_webmail/email_owa)

[Delegar permisos en una cuenta de Exchange](/pages/web_cloud/email_and_collaborative_solutions/microsoft_exchange/feature_delegation)

[Compartir calendarios en OWA](/pages/web_cloud/email_and_collaborative_solutions/using_the_outlook_web_app_webmail/owa_calendar_sharing)

Para servicios especializados (posicionamiento, desarrollo, etc.), contacte con [partners de OVHcloud](/links/partner).

Si quiere disfrutar de ayuda para utilizar y configurar sus soluciones de OVHcloud, puede consultar nuestras distintas soluciones [pestañas de soporte](/links/support).

Interactúe con nuestra [comunidad de usuarios](/links/community).