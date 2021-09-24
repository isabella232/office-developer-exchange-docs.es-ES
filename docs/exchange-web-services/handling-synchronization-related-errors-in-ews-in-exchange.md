---
title: Controlar errores relacionados con la sincronización en EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: a0807b90-645a-4ea6-aee1-96828df14be0
description: Descubra cómo controlar errores relacionados con la sincronización en aplicaciones que desarrolle mediante la API administrada ews o EWS en Exchange.
ms.openlocfilehash: fd52b54413c6fc791132fb01b47bc9077d0266b2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513251"
---
# <a name="handling-synchronization-related-errors-in-ews-in-exchange"></a>Controlar errores relacionados con la sincronización en EWS en Exchange

Descubra cómo controlar errores relacionados con la sincronización en aplicaciones que desarrolle mediante la API administrada ews o EWS en Exchange.
  
Si la aplicación sincroniza elementos y carpetas, es posible que tenga que controlar errores relacionados con la sincronización. Puede controlar estos errores en tiempo de ejecución, o mientras está desarrollando su aplicación de EWS. La mayoría de estos errores se definen mediante la enumeración [ResponseCodeType](https://msdn.microsoft.com/library/exchangewebservices.responsecodetype%28v=exchg.80%29.aspx) en la API administrada ews y el elemento [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) en Exchange Web Services (EWS). 
  
**Tabla 1. Errores relacionados con la sincronización y cómo controlarlos**

|**Error**|**Se produce cuando se intenta...**|**Controlarla por...**|
|:-----|:-----|:-----|
|ErrorInvalidSyncStateData  <br/> | Sincronizar elementos o carpetas mediante un valor de estado de sincronización no válido.  <br/>  Excluya una carpeta raíz en la solicitud SyncFolderHierarchy inicial, cuando la solicitud posterior incluya una carpeta raíz.  <br/>  Use diferentes carpetas raíz en solicitudes posteriores.  <br/> | Asegurarse de que el valor de estado de sincronización que está enviando coincide con el valor de estado de sincronización devuelto durante una sincronización anterior.  <br/>  Asegurarse de que no va a enviar el estado de sincronización de la jerarquía de carpetas al intentar sincronizar elementos y viceversa.  <br/>  Asegurarse de que va a enviar el estado de sincronización de la carpeta raíz correcta.  <br/>  Asegurarse de que se especifica la misma carpeta raíz en cada solicitud.  <br/>  Asegurarse de que la solicitud anterior no especificaba una carpeta raíz de null, mientras que la solicitud actual incluye una carpeta raíz de raíz. Null y root no se tratan igual.  <br/> |
|ErrorSyncFolderNotFound  <br/> |Sincronizar subcarpetas o elementos de una carpeta que no se encuentra en el servidor.  <br/> |Asegurarse de que el identificador de carpeta especificado en la solicitud coincide con un identificador de carpeta devuelto desde el servidor en una respuesta de sincronización anterior.  <br/> |
|ErrorTimeoutExpired  <br/> |Enviar demasiadas solicitudes.  <br/> |Limitar los lotes a 10 elementos por lote para evitar que se [limiten](ews-throttling-in-exchange.md).  <br/> |
|[ServiceResponseException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx) <br/> |Conectar ews cuando el servidor está sin conexión o hay un problema con la conectividad.  <br/> |Comprobar la conectividad con el servidor y volver a intentar la solicitud más adelante. Es probable que se trata de un error de servicio transitorio o de red.  <br/> |
   
## <a name="see-also"></a>Ver también


- [Sincronización del buzón y EWS en Exchange](mailbox-synchronization-and-ews-in-exchange.md)
    
- [Sincronizar carpetas mediante EWS en Exchange](how-to-synchronize-folders-by-using-ews-in-exchange.md)
    
- [Sincronizar elementos mediante EWS en Exchange](how-to-synchronize-items-by-using-ews-in-exchange.md)
    
- [ServiceResponseException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)
    

