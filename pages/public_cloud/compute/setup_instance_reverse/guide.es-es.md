---
title: "Configurar el registro DNS inverso de una instancia de Public Cloud"
excerpt: Cómo activar la resolución inversa DNS
updated: 2024-06-10
---

> [!primary]
> Esta traducción ha sido generada de forma automática por nuestro partner SYSTRAN. En algunos casos puede contener términos imprecisos, como en las etiquetas de los botones o los detalles técnicos. En caso de duda, le recomendamos que consulte la versión inglesa o francesa de la guía. Si quiere ayudarnos a mejorar esta traducción, por favor, utilice el botón «Contribuir» de esta página.
> 

## Objetivo

El registro **inverso** (*rDNS*) es el complemento de la resolución "clásica" de los DNS que permite convertir un dominio en una dirección IP (registro de tipo **A**). Una solicitud de este tipo permite resolver una dirección IP en el dominio (registro de tipo **PTR**). Esto significa que las peticiones DNS a la dirección IP correspondiente devolverán un dominio.

La configuración de la resolución **inversa DNS** de una instancia resulta especialmente útil para el envío de mensajes de correo. Si la dirección IP de su servidor de envío se resuelve correctamente en su nombre de dominio, se reducirá el riesgo de que sus mensajes sean rechazados por un sistema de protección contra el spam.

**Esta guía explica cómo configurar el registro DNS inverso para la dirección o direcciones IP de una instancia de Public Cloud.**

## Requisitos

- Tener una [instancia de Public Cloud](https://www.ovhcloud.com/es-es/public-cloud/) en su cuenta de OVHcloud.
- Un dominio con un registro `A` que apunta a la instancia.
- Tienes acceso a tu [Panel de configuración de OVHcloud](/links/manager).

## Procedimiento

Conéctese al [Panel de configuración de OVHcloud](/links/manager), acceda a la sección `Bare Metal Cloud`{.action} y haga clic en `IP`{.action} en el menú de la izquierda.

El menú desplegable **Mis direcciones IP públicas y servicios asociados** le permite filtrar sus servicios por categoría.

![Reverse IP](images/filterippci.png){.thumbnail}

Haga clic en `...`{.action} en la línea de la dirección IP correspondiente y seleccione `Cambiar el registro inverso`{.action}.

![Registro inverso](images/modifyreversepc.png){.thumbnail}

En la nueva ventana, introduzca el registro inverso y haga clic en `Confirmar`{.action}.

![Registro inverso](images/enterreverse.png){.thumbnail}

También puede editar el registro inverso directamente a través del icono de la columna **inversa** de la tabla.

> [!primary]
>
Si la modificación no funciona como se esperaba, compruebe que el registro `A` esté bien configurado en la zona DNS del dominio. Atención: La modificación de la [zona DNS](/pages/web_cloud/domains/dns_zone_edit) puede tardar hasta 24 horas si solo ha cambiado recientemente el registro `A`.
>

## Más información <a name="gofurther"></a>

[Crear una primera instancia de Public Cloud y conectarse a ella](/pages/public_cloud/compute/public-cloud-first-steps)

Interactúe con nuestra [comunidad de usuarios](/links/community).