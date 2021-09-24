---
title: Actualizar la información de configuración mediante la detección automática
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: c2f3c6a5-e8ea-4375-b41a-686a6f238d33
description: Obtenga información sobre cómo y cuándo actualizar la información de configuración de su Exchange mediante detección automática.
ms.openlocfilehash: 0ec6910fcd8ab66085de2414f02a4f78419ec78b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513118"
---
# <a name="refresh-configuration-information-by-using-autodiscover"></a>Actualizar la información de configuración mediante la detección automática

Obtenga información sobre cómo y cuándo actualizar la información de configuración de su Exchange mediante detección automática.
  
Cuando la aplicación EWS se ejecuta por primera vez, la detección automática proporciona una excelente manera de recopilar la información que necesita para conectarse al buzón de correo Exchange usuario. Pero la detección automática no es solo la primera vez que se usa. El uso de detección automática de forma regular puede ayudar a mantener la aplicación conectada, ya que permite que responda a los cambios en la Exchange implementación.
  
## <a name="cache-autodiscover-endpoint-and-ews-settings"></a>Configuración de EWS y punto de conexión de detección automática de caché
<a name="bk_CacheSettings"> </a>

Aunque se recomienda usar Detección automática con regularidad, la regularidad con la que se usa requiere cierta consideración. Lo ideal es equilibrar la respuesta rápidamente a los cambios en el entorno frente a la generación de demasiado tráfico de red innecesario. Cuando la aplicación obtiene una respuesta de detección automática correcta por primera vez, debe guardar la siguiente información para que no tenga que repetir el proceso de detección automática cada vez que envíe una solicitud EWS.
  
**Tabla 1. Información para almacenar en caché para solicitudes de detección automática**

|**Configuración de la memoria caché**|**Válido para...**|**Detalles**|
|:-----|:-----|:-----|
|Extremo de detección automática  <br/> |Siempre que funcione  <br/> |Al guardar el extremo de detección automática que devolvió una [](how-to-generate-a-list-of-autodiscover-endpoints.md) respuesta correcta, no es necesario repetir el proceso de generación de una lista de extremos de detección automática y probarlos hasta que obtenga una respuesta correcta.<br/><br/> **NOTA:** La API administrada ews no admite el almacenamiento en caché del extremo de detección automática.           |
|Dirección URL de EWS y cualquier otra configuración recuperada de la respuesta de detección automática  <br/> |Una semana  <br/> |Al guardar la dirección URL de EWS y [](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) otras configuraciones relacionadas, no es necesario enviar una nueva solicitud de detección automática para cada solicitud EWS o si la aplicación se reinicia. Sin embargo, incluso si una dirección URL de EWS funciona para el usuario, es posible que un servidor esté disponible que sea más óptimo.<br/><br/> Por ejemplo, es posible que el buzón del usuario se haya movido a un nuevo servidor de buzones, lo que da como resultado un nuevo extremo de EWS preferido. Se recomienda actualizar la configuración del usuario enviando una nueva solicitud de detección automática después de que haya transcurrido una semana desde la última solicitud de detección automática. Esta vez se puede ajustar para cumplir los requisitos de la aplicación.  <br/> |
   
## <a name="refresh-cached-configuration-information"></a>Actualizar información de configuración almacenada en caché
<a name="bk_RefreshConfig"> </a>

Ahora que tiene la información almacenada en caché, vamos a examinar cómo puede mantener esa caché actualizada. Se recomienda actualizar la información almacenada en caché cuando:
  
- El período de validez de la información expira.
    
- Se [produce un error relacionado](#bk_ConnectionErrors) con la conexión y la información almacenada en caché se actualizó por última vez hace más de una hora.
    
Para actualizar la información almacenada en caché, envíe una solicitud de detección automática a un extremo de detección automática en caché y haga lo siguiente:
  
- Si la solicitud se realiza correctamente, compare el extremo EWS en la respuesta con el extremo ews almacenado en caché y haga lo siguiente:
    
  - Si son diferentes, use el nuevo extremo ews. Si va a actualizar para recuperarse de un error, vuelva a intentar la solicitud con error con el nuevo punto de conexión.
    
  - Si son iguales, siga usando el extremo ews original. Si está actualizando para recuperarse de un error, controle el error según corresponda.
    
- Si se produce un error en la solicitud, inicie el [proceso de detección automática](autodiscover-for-exchange.md) desde el principio. Después de obtener una respuesta correcta, reemplace el extremo de detección automática en caché por el extremo de detección automática que se ha realizado correctamente y siga usando el nuevo extremo EWS. Si no obtiene una respuesta correcta, siga usando el extremo de detección automática original y el extremo EWS. Si está actualizando para recuperarse de un error, controle el error según corresponda. 
    
La siguiente figura proporciona una representación visual de este proceso.
  
**Figura 1. Proceso para actualizar la información de configuración mediante detección automática**

![Diagrama esquemático que muestra cómo la detección automática actualiza la información de configuración.](media/Ex15_Autodiscover_Refresh_Flowchart.png)
  
### <a name="connection-related-errors"></a>Errores relacionados con la conexión
<a name="bk_ConnectionErrors"> </a>

Actualizar la información de configuración almacenada en caché puede ayudar con algunos errores, pero no todos. 
  
**Tabla 2. Errores resueltos al actualizar la memoria caché**

|**Error**|**Implementación de LA API administrada ews**|**Notas**|
|:-----|:-----|:-----|
|Errores de dns o de red<br/><br/> Ejemplo: no se pudo encontrar el nombre de host.  <br/> |[ServiceRemoteException](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.data.serviceremoteexception?view=exchange-ews-api) <br/> |Cualquier error que indique que no se pudo encontrar el servidor o que no se pudo alcanzar podría resolverse intentando detección automática. <br/><br/> Es posible que el extremo de EWS almacenado en caché ya no sea válido y la detección automática pueda apuntar al nuevo servidor.  <br/> |
|Errores de estado HTTP<br/><br/> Ejemplo: 503 Servicio no disponible  <br/> |[ServiceRemoteException](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.data.serviceremoteexception?view=exchange-ews-api) <br/> |Los errores de estado HTTP pueden producirse por muchas razones diferentes.<br/><br/> Sin embargo, es una buena idea probar detección automática para ver si hay un nuevo punto de conexión ews disponible para el usuario.  <br/> |
|Códigos de error ews <br/><br/> Ejemplo: ErrorConnectionFailed <br/> |[ResponseCodeType](../web-service-reference/responsecode.md) <br/> | La mayoría de los códigos de error de EWS no garantizan la actualización de la información de configuración.<br/><br/> Sin embargo, lo siguiente indica específicamente que la información de configuración debe actualizarse:<br/>- **ErrorConnectionFailed** <br/>- **ErrorMailboxMoveInProgress** <br/> |
   
## <a name="see-also"></a>Consulte también

- [Detección automática en Exchange](autodiscover-for-exchange.md)  
- [Generar una lista de extremos de detección automática](how-to-generate-a-list-of-autodiscover-endpoints.md)   
- [Obtener la configuración de usuario de Exchange mediante el uso de Detección automática](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    

