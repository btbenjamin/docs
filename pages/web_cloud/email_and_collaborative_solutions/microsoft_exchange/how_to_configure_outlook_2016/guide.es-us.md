---
title: 'Exchange - Configure su cuenta de correo electrónico en Outlook para Windows'
excerpt: 'Cómo configurar una cuenta Exchange en Outlook para Windows'
updated: 2024-10-30
---

## Objetivo

Es posible configurar sus cuentas Exchange en el cliente de correo que usted utilice, siempre que sea compatible, para poder acceder a ellas desde cualquiera de sus dispositivos. Microsoft Outlook es el programa recomendado para utilizar una dirección de correo Exchange con sus funciones colaborativas.

**Esta guía explica cómo configurar una cuenta Exchange en Microsoft Outlook para Windows.**

> [!warning]
>
> La configuración, la gestión y la responsabilidad de los servicios que OVHcloud pone a su disposición recaen sobre usted. Por lo tanto, usted deberá asegurarse de que estos funcionen correctamente.
>
> Esta guía le ayudará a realizar las operaciones más habituales. No obstante, si tiene alguna duda le recomendamos que contacte con un proveedor de servicios especializado o con el editor del servicio. Nosotros no podremos asistirle. Para más información, consulte el apartado «Más información» de esta guía.

<iframe class="video" width="560" height="315" src="https://www.youtube-nocookie.com/embed/G4CVvTzFA58?si=Bd6SRW9258ptF-lt" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## Requisitos

- Tener un servicio [Exchange](/links/web/emails).
- Tener Microsoft Outlook o posterior instalado en su ordenador.
- Disponer del nombre de usuario y la contraseña de la cuenta de correo electrónico que quiera configurar.
- El registro SRV de OVHcloud debe estar correctamente configurado en la zona DNS del dominio. No dude en consultar nuestra guía [Añadir un dominio a un servicio Exchange](/pages/web_cloud/email_and_collaborative_solutions/microsoft_exchange/exchange_adding_domain).

> [!primary]
>
> Si utiliza Outlook y posterior para Mac, consulte nuestra guía [Configurar una cuenta Exchange en Outlook para Mac](/pages/web_cloud/email_and_collaborative_solutions/microsoft_exchange/how_to_configure_outlook_2016_mac)

## Procedimiento

### Añadir la cuenta

- **Si es la primera vez que usa la aplicación**, aparecerá un asistente de configuración solicitándole su dirección de correo electrónico.

- **Si ya tiene una cuenta configurada**, haga clic en `Archivo`{.action} en el menú superior y luego en `Agregar cuenta`{.action}.

- Introduzca su dirección de correo electrónico y haga clic en `Opciones avanzadas`{.action}. Marque la casilla `Permitirme configurar manualmente mi cuenta`{.action} y haga clic en `Conectar`{.action}. 

![exchange](images/config-outlook-exchange01.png){.thumbnail}

- A continuación, entre los distintos tipos de cuenta, seleccione **Exchange**.

- Introduzca la contraseña de su cuenta de correo electrónico en la siguiente ventana, marque la casilla para recordarla y haga clic en `Aceptar`{.action}.

![exchange](images/config-outlook-exchange02.png){.thumbnail}

> [!primary]
>
> Si aparece un mensaje indicándole que Outlook no ha podido configurar su cuenta, es posible que el registro SRV de OVHcloud no esté correctamente configurado en la zona DNS del dominio.
>
> ![exchange](images/config-outlook-exchange03.png){.thumbnail}
>
> Compruebe la configuración del dominio en su servicio Exchange en el [área de cliente de OVHcloud](/links/manager), en la pestaña `Dominios asociados`{.action}, en la columna `Diagnóstico`{.action}"de la tabla.

- Si la configuración del dominio es válida, puede aparecer un mensaje de autorización de conexión a los servidores de OVHcloud. Acepte la configuración automática de su cuenta Exchange.
- Determine la frecuencia de conservación de los elementos de su cuenta Exchange, **en local en su ordenador**. Haga clic en `Siguiente`{.action} y, a continuación, en `Finalizado`{.action}.

![exchange](images/config-outlook-exchange04.png){.thumbnail}

### Utilizar la dirección de correo

Una vez que haya configurado la dirección de correo electrónico, ya puede empezar a utilizarla enviando y recibiendo mensajes.

Su dirección de correo Exchange y todas sus funciones colaborativas también están disponibles en la interfaz [OWA](/links/web/email). Si tiene cualquier duda sobre su uso, no dude en consultar nuestra guía [Consultar su cuenta Exchange desde la interfaz OWA](/pages/web_cloud/email_and_collaborative_solutions/using_the_outlook_web_app_webmail/email_owa).

### Obtener una copia de seguridad de su dirección de correo

Si necesita realizar alguna operación que pueda provocar la pérdida de los datos de su cuenta de correo, le recomendamos que realice una copia de seguridad previa de la cuenta de correo. Para ello, consulte el apartado "**Exportar desde Windows**" en nuestra guía [Migrar manualmente su dirección de correo electrónico](/pages/web_cloud/email_and_collaborative_solutions/migrating/manual_email_migration#exportar-desde-windows).

## Más información

> [!primary]
>
> Para obtener más información sobre la configuración de una dirección de correo electrónico desde la aplicación Outlook en Windows, consulte [el Centro de ayuda de Microsoft](https://support.microsoft.com/es-es/office/agregar-cuenta-de-correo-en-outlook-6e27792a-9267-4aa4-8bb6-c84ef146101b).

[Configurar una cuenta de correo electrónico en Outlook para Windows](/pages/web_cloud/email_and_collaborative_solutions/mx_plan/how_to_configure_outlook_2016)

Interactúe con nuestra comunidad de usuarios en <https://community.ovh.com/en/>.
