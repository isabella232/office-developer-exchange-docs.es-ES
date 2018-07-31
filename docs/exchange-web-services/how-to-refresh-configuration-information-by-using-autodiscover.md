---
title: Actualizar la información de configuración mediante la detección automática
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: c2f3c6a5-e8ea-4375-b41a-686a6f238d33
description: Obtenga información sobre cómo y cuándo para actualizar la información de configuración de la conexión de Exchange mediante el uso de detección automática.
ms.openlocfilehash: 764909fbe5e4cd62ba6e05bfa4b2c417ef41a9ae
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353059"
---
# <a name="refresh-configuration-information-by-using-autodiscover"></a>Actualizar la información de configuración mediante la detección automática

Obtenga información sobre cómo y cuándo para actualizar la información de configuración de la conexión de Exchange mediante el uso de detección automática.
  
Cuando se ejecuta la aplicación de EWS por primera vez, detección automática proporciona un método excelente para recopilar la información que necesita para poder conectarse al buzón de Exchange del usuario. Pero detección automática no es sólo para el primer uso. Uso de detección automática de forma regular puede ayudar a mantener la aplicación conectada mediante la habilitación de él para responder a los cambios en la implementación de Exchange.
  
## <a name="cache-autodiscover-endpoint-and-ews-settings"></a>Extremo de detección automática y la configuración de EWS la memoria caché
<a name="bk_CacheSettings"> </a>

Mientras se recomendable que utilice detección automática con regularidad, cómo regularmente utiliza requiere atención especial. Lo ideal es que se puede equilibrar responder rápidamente a los cambios en el entorno frente a generar demasiado tráfico de red innecesarios. Cuando la aplicación obtiene una respuesta correcta de detección automática por primera vez, debe guardar la siguiente información para que no es necesario repetir el proceso de detección automática cada vez que envía una solicitud de EWS.
  
**La tabla 1. Información en memoria caché para las solicitudes de detección automática**

|**Si se establece en memoria caché**|**Válido para...**|**Detalles**|
|:-----|:-----|:-----|
|Extremo de detección automática  <br/> |Como funciona  <br/> |Cuando guarda el extremo de detección automática que devuelven una respuesta correcta, no es necesario repetir el proceso de [generación de una lista de extremos de detección automática](how-to-generate-a-list-of-autodiscover-endpoints.md) y tratando de hasta que obtenga una respuesta correcta.<br/><br/> **Nota**: la API administrada de EWS no admite el almacenamiento en memoria caché el extremo de detección automática.           |
|Dirección URL de EWS y cualquier otra configuración recuperados de la respuesta de detección automática  <br/> |24 horas  <br/> |Guardando la dirección URL de EWS y otras relacionadas con la configuración, no es necesario para [Enviar una nueva solicitud de detección automática](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) para cada solicitud EWS o si se reinicia la aplicación. Sin embargo, incluso si una dirección URL de EWS funciona para el usuario, un servidor podría estar disponible es decir más óptima.<br/><br/> Por ejemplo, es posible que movió el buzón del usuario a un nuevo servidor de buzón de correo, lo que resulta en un nuevo extremo EWS preferido. Se recomienda que actualice a su configuración de usuario mediante el envío de una nueva solicitud de detección automática después de 24 horas han pasado desde la última solicitud de detección automática. Este tiempo se puede ajustar para satisfacer los requisitos de la aplicación.  <br/> |
   
## <a name="refresh-cached-configuration-information"></a>Actualizar la información de configuración almacenada en caché
<a name="bk_RefreshConfig"> </a>

Ahora que tiene la información almacenada en caché, veamos cómo puede conservar esa memoria caché actualizados. Se recomienda que actualizar la información almacenada en caché cuando:
  
- Expira el período de validez de la información.
    
- Se produce un [errores relacionados con la conexión](#bk_ConnectionErrors) . 
    
Para actualizar la información almacenada en caché, enviar una solicitud de detección automática a un extremo de detección automática en caché y haga lo siguiente:
  
- Si la solicitud se realiza correctamente, compare el extremo EWS en la respuesta con el extremo EWS en caché y haga lo siguiente:
    
  - Si son diferentes, use el nuevo extremo EWS. Si está actualizando para recuperarse de un error, vuelva a intentar la solicitud con errores con el extremo de nuevo.
    
  - Si son las mismas, seguir usando el extremo EWS original. Si está actualizando para recuperarse de un error, controlar el error según corresponda.
    
- Si se produce un error en la solicitud, iniciar el [proceso de detección automática](autodiscover-for-exchange.md) desde el principio. Después de obtener una respuesta correcta, reemplace el extremo de detección automática en caché con el extremo de detección automática que se ha realizado correctamente y seguir usando el nuevo extremo EWS. Si no recibe una respuesta correcta, seguir usando el extremo de detección automática original y el extremo EWS. Si está actualizando para recuperarse de un error, controlar el error según corresponda. 
    
La ilustración siguiente proporciona una representación visual de este proceso.
  
**En la figura 1. Proceso para actualizar la información de configuración mediante el uso de detección automática**

![Diagrama esquemático que muestra cómo la detección automática actualiza la información de configuración.](media/Ex15_Autodiscover_Refresh_Flowchart.png)
  
### <a name="connection-related-errors"></a>Errores relacionados con la conexión
<a name="bk_ConnectionErrors"> </a>

Actualizar la información de configuración almacenada en caché puede ayudar con algunos errores, pero no todas. 
  
**Tabla 2. Errores dirigidos al actualizar la memoria caché**

|**Error**|**Implementación de la API administrada de EWS**|**Notas**|
|:-----|:-----|:-----|
|Errores de red o DNS<br/><br/> Ejemplo: No se pudo encontrar el nombre de Host.  <br/> |[ServiceRemoteException](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ServiceRemoteException.aspx) <br/> |Es posible que se puede resolver cualquier error que indica que el servidor no se pudo encontrar o no se pudo tener acceso al tratar de detección automática. <br/><br/> El extremo EWS en caché es posible que ya no sea válido y es posible que pueda detección automática para apunte al nuevo servidor.  <br/> |
|Errores de estado HTTP<br/><br/> Ejemplo: 503 Servicio no disponible  <br/> |[ServiceRemoteException](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ServiceRemoteException.aspx) <br/> |Errores de estado HTTP pueden ocurrir por muchas razones diferentes.<br/><br/> Sin embargo, es una buena idea para probar la detección automática para ver si un nuevo extremo EWS está disponible para el usuario.  <br/> |
|Códigos de error EWS <br/><br/> Ejemplo: ErrorConnectionFailed <br/> |[ResponseCodeType](../web-service-reference/responsecode.md) <br/> | La mayoría de los códigos de error EWS no requieran actualizar la información de configuración.<br/><br/> Sin embargo, el siguiente específicamente indica que debe actualizarse la información de configuración:<br/>- **ErrorConnectionFailed** <br/>- **ErrorMailboxMoveInProgress** <br/> |
   
## <a name="see-also"></a>Vea también

- [Detección automática de Exchange](autodiscover-for-exchange.md)  
- [Generar una lista de extremos de detección automática](how-to-generate-a-list-of-autodiscover-endpoints.md)   
- [Obtener la configuración de usuario de Exchange mediante el uso de detección automática](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    

