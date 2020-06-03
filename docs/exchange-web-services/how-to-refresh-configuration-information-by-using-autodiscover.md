---
title: Actualizar la información de configuración mediante la detección automática
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: c2f3c6a5-e8ea-4375-b41a-686a6f238d33
description: Obtenga información sobre cómo y cuándo actualizar la información de configuración de su conexión de Exchange mediante detección automática.
ms.openlocfilehash: b9a4264d150d09b0e143e0bf7365af351bb2ef44
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527757"
---
# <a name="refresh-configuration-information-by-using-autodiscover"></a>Actualizar la información de configuración mediante la detección automática

Obtenga información sobre cómo y cuándo actualizar la información de configuración de su conexión de Exchange mediante detección automática.
  
Cuando la aplicación de EWS se ejecuta por primera vez, detección automática proporciona una buena forma de recopilar la información necesaria para conectarse al buzón de correo de Exchange del usuario. Pero la detección automática no es solo para el primer uso. El uso de detección automática con regularidad puede ayudarle a mantener la conexión de la aplicación, ya que permite que responda a los cambios en la implementación de Exchange.
  
## <a name="cache-autodiscover-endpoint-and-ews-settings"></a>Configuración de EWS y extremos de detección automática de caché
<a name="bk_CacheSettings"> </a>

Aunque le recomendamos que use la detección automática con regularidad, la frecuencia con la que lo use requiere alguna consideración. Idealmente, puede equilibrar la respuesta rápidamente a los cambios en el entorno para generar demasiado tráfico de red innecesario. Cuando la aplicación obtenga una respuesta de detección automática correcta por primera vez, debe guardar la información siguiente para no tener que repetir el proceso de detección automática cada vez que envíe una solicitud de EWS.
  
**Tabla 1. Información para almacenar en caché las solicitudes de detección automática**

|**Establecer para la memoria caché**|**Válido para...**|**Detalles**|
|:-----|:-----|:-----|
|Punto de conexión de detección automática  <br/> |Siempre que funcione  <br/> |Al guardar el punto de conexión de detección automática que devolvió una respuesta correcta, no tiene que repetir el proceso de [generar una lista de extremos de detección automática](how-to-generate-a-list-of-autodiscover-endpoints.md) y probarlos hasta que obtenga una respuesta correcta.<br/><br/> **Nota**: la API administrada de EWS no admite el almacenamiento en caché del punto de conexión de detección automática.           |
|Dirección URL de EWS y cualquier otra configuración recuperada de la respuesta de detección automática  <br/> |Una semana  <br/> |Al guardar la dirección URL de EWS y otras configuraciones relacionadas, no es necesario [enviar una nueva solicitud de detección automática](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) para cada solicitud de EWS o si se reinicia la aplicación. Sin embargo, incluso si una dirección URL de EWS funciona para su usuario, puede que esté disponible un servidor que sea más óptimo.<br/><br/> Por ejemplo, es posible que el buzón del usuario se haya movido a un nuevo servidor de buzones de correo, lo que resulta en un nuevo punto de conexión de EWS preferido. Le recomendamos que actualice la configuración de usuario mediante el envío de una nueva solicitud de detección automática después de que haya transcurrido una semana desde la última solicitud de detección automática. Esta vez se puede ajustar para cumplir los requisitos de la aplicación.  <br/> |
   
## <a name="refresh-cached-configuration-information"></a>Actualizar la información de configuración almacenada en caché
<a name="bk_RefreshConfig"> </a>

Ahora que tiene la información almacenada en la caché, veamos cómo puede mantener esa memoria caché actualizada. Le recomendamos que actualice la información almacenada en caché cuando:
  
- El período de validez de la información expira.
    
- Se produce un [error relacionado con la conexión](#bk_ConnectionErrors) y la información almacenada en caché se actualiza por hora hace una hora.
    
Para actualizar la información almacenada en caché, envíe una solicitud de detección automática a un extremo de detección automática en caché y haga lo siguiente:
  
- Si la solicitud se realiza correctamente, compare el extremo de EWS en la respuesta con el extremo de EWS en caché y haga lo siguiente:
    
  - Si son diferentes, use el nuevo punto de conexión de EWS. Si está actualizando para recuperarse de un error, vuelva a intentar la solicitud con error con el nuevo punto de conexión.
    
  - Si son iguales, continúe usando el punto de conexión de EWS original. Si está actualizando para recuperarse de un error, controle el error según corresponda.
    
- Si se produce un error en la solicitud, inicie el [proceso de detección automática](autodiscover-for-exchange.md) desde el principio. Después de obtener una respuesta correcta, reemplace el punto de conexión de detección automática en caché con el extremo de detección automática que se realizó correctamente y continúe usando el nuevo punto de conexión de EWS. Si no obtiene una respuesta correcta, continúe usando el punto de conexión de detección automática original y el punto de conexión de EWS. Si está actualizando para recuperarse de un error, controle el error según corresponda. 
    
La siguiente figura proporciona una representación visual de este proceso.
  
**Figura 1. Proceso para actualizar la información de configuración mediante la detección automática**

![Diagrama esquemático que muestra cómo la detección automática actualiza la información de configuración.](media/Ex15_Autodiscover_Refresh_Flowchart.png)
  
### <a name="connection-related-errors"></a>Errores relacionados con la conexión
<a name="bk_ConnectionErrors"> </a>

La actualización de la información de configuración almacenada en caché puede ayudar con algunos errores, pero no todos. 
  
**Tabla 2. Errores corregidos al actualizar la caché**

|**Error**|**Implementación de la API administrada de EWS**|**Notas**|
|:-----|:-----|:-----|
|Errores de error de red o de DNS<br/><br/> Ejemplo: no se pudo encontrar el nombre de host.  <br/> |[ServiceRemoteException](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.data.serviceremoteexception?view=exchange-ews-api) <br/> |Cualquier error que indique que no se pudo encontrar o no se pudo tener acceso al servidor se puede resolver probando la detección automática. <br/><br/> Es posible que el punto de conexión de EWS en caché ya no sea válido, y que la detección automática pueda apuntarle al nuevo servidor.  <br/> |
|Errores de Estado HTTP<br/><br/> Ejemplo: servicio de 503 no disponible  <br/> |[ServiceRemoteException](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.data.serviceremoteexception?view=exchange-ews-api) <br/> |Los errores de Estado HTTP pueden ocurrir por muchos motivos diferentes.<br/><br/> Sin embargo, es una buena idea probar la detección automática para ver si hay un nuevo punto de conexión de EWS disponible para el usuario.  <br/> |
|Códigos de error de EWS <br/><br/> Ejemplo: ErrorConnectionFailed <br/> |[ResponseCodeType](../web-service-reference/responsecode.md) <br/> | La mayoría de los códigos de error de EWS no garantizan la actualización de la información de configuración.<br/><br/> Sin embargo, el siguiente indica específicamente que la información de configuración debe actualizarse:<br/>- **ErrorConnectionFailed** <br/>- **ErrorMailboxMoveInProgress** <br/> |
   
## <a name="see-also"></a>Vea también

- [Detección automática en Exchange](autodiscover-for-exchange.md)  
- [Generar una lista de extremos de detección automática](how-to-generate-a-list-of-autodiscover-endpoints.md)   
- [Obtener la configuración de usuario de Exchange mediante el uso de detección automática](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    

