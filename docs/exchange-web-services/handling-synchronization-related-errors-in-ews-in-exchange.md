---
title: Tratamiento de errores relacionados con la sincronización en EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: a0807b90-645a-4ea6-aee1-96828df14be0
description: Encuentre información acerca de cómo controlar los errores relacionados con la sincronización de aplicaciones que desarrollar mediante el uso de la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 6de27d585e467d900941f34b2210877d17205502
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763010"
---
# <a name="handling-synchronization-related-errors-in-ews-in-exchange"></a>Tratamiento de errores relacionados con la sincronización en EWS en Exchange

Encuentre información acerca de cómo controlar los errores relacionados con la sincronización de aplicaciones que desarrollar mediante el uso de la API administrada de EWS o EWS en Exchange.
  
Si la aplicación sincroniza los elementos y carpetas, debe controlar los errores relacionados con la sincronización. Puede controlar estos errores en tiempo de ejecución, o mientras está desarrollando su aplicación de EWS. La mayoría de estos errores se define mediante la enumeración de [ResponseCodeType](http://msdn.microsoft.com/en-us/library/exchangewebservices.responsecodetype%28v=exchg.80%29.aspx) en la API administrada de EWS y el elemento [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) en Exchange Web Services (EWS). 
  
**La tabla 1. Los errores relacionados con la sincronización y cómo controlarlos**

|**Error**|**Se produce al intentar...**|**Controlarla por...**|
|:-----|:-----|:-----|
|ErrorInvalidSyncStateData  <br/> | Sincronizar elementos o carpetas mediante el uso de un valor de estado de sincronización no válido.  <br/>  Excluir una carpeta raíz en la solicitud de SyncFolderHierarchy inicial, cuando la solicitud subsiguiente incluye una carpeta raíz.  <br/>  Usar carpetas de raíz diferente en las solicitudes posteriores.  <br/> | Asegurarse de que el valor de estado de sincronización que va a enviar a las coincidencias de devolver el valor de estado de sincronización durante una sincronización anterior.  <br/>  Asegurarse de que no se envía el estado de sincronización para la jerarquía de carpetas al intentar sincronizar elementos y viceversa.  <br/>  Asegurarse de que va a enviar el estado de sincronización para la carpeta raíz correcta.  <br/>  Asegurarse de que se especifica la misma carpeta raíz en cada solicitud.  <br/>  Asegurarse de que la solicitud anterior no especificó una carpeta raíz de null, mientras que la solicitud actual incluye una carpeta raíz de la raíz. NULL y raíz no están tratan de la misma.  <br/> |
|ErrorSyncFolderNotFound  <br/> |Sincronizar las subcarpetas o los elementos en una carpeta que no se encuentra en el servidor.  <br/> |Asegurarse de la carpeta especificada en la solicitud de identificador coincide con un identificador de la carpeta devuelto desde el servidor en una respuesta de sincronización anterior.  <br/> |
|ErrorTimeoutExpired  <br/> |Enviar demasiadas solicitudes.  <br/> |Limitar los lotes de 10 elementos por lote para evitar que aparezcan [reducidas](ews-throttling-in-exchange.md).  <br/> |
|[ServiceResponseException](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx) <br/> |Conectar a EWS cuando el servidor está desconectado o no hay un problema de conectividad.  <br/> |Comprobar la conectividad con el servidor y volver a intentar la solicitud más adelante. Es probable que esto es un error de servicio transitorios o error de red.  <br/> |
   
## <a name="see-also"></a>Ver también


- [Sincronización de buzón de correo y EWS en Exchange](mailbox-synchronization-and-ews-in-exchange.md)
    
- [Sincronizar carpetas mediante el uso de EWS en Exchange](how-to-synchronize-folders-by-using-ews-in-exchange.md)
    
- [Sincronizar elementos mediante el uso de EWS en Exchange](how-to-synchronize-items-by-using-ews-in-exchange.md)
    
- [ServiceResponseException](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)
    

