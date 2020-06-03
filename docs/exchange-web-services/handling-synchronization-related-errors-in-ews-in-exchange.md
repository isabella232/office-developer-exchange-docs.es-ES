---
title: Controlar errores relacionados con la sincronización en EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: a0807b90-645a-4ea6-aee1-96828df14be0
description: Descubra cómo controlar los errores relacionados con la sincronización en las aplicaciones que desarrolle mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: f62937ec444d64b0b358581371f1260f565215b3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455943"
---
# <a name="handling-synchronization-related-errors-in-ews-in-exchange"></a>Controlar errores relacionados con la sincronización en EWS en Exchange

Descubra cómo controlar los errores relacionados con la sincronización en las aplicaciones que desarrolle mediante la API administrada de EWS o EWS en Exchange.
  
Si la aplicación sincroniza elementos y carpetas, es posible que deba controlar los errores relacionados con la sincronización. Puede controlar estos errores en tiempo de ejecución, o mientras está desarrollando su aplicación de EWS. La mayoría de estos errores los define la enumeración [ResponseCodeType](https://msdn.microsoft.com/library/exchangewebservices.responsecodetype%28v=exchg.80%29.aspx) en la API administrada de EWS y el elemento [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) en servicios web Exchange (EWS). 
  
**Tabla 1. Errores relacionados con la sincronización y cómo controlarlos**

|**Error**|**Se produce cuando se intenta...**|**Controlarla por...**|
|:-----|:-----|:-----|
|ErrorInvalidSyncStateData  <br/> | Sincronizar elementos o carpetas con un valor de estado de sincronización no válido.  <br/>  Excluya una carpeta raíz en la solicitud de SyncFolderHierarchy inicial, cuando la solicitud posterior incluya una carpeta raíz.  <br/>  Usar carpetas raíz diferentes en las solicitudes siguientes.  <br/> | Asegurarse de que el valor de estado de sincronización que envía coincide con el valor de estado de sincronización devuelto durante una sincronización anterior.  <br/>  Asegurarse de que no se envía el estado de sincronización de la jerarquía de carpetas cuando se intenta sincronizar elementos, y viceversa.  <br/>  Asegurarse de que envía el estado de sincronización para la carpeta raíz correcta.  <br/>  Asegurarse de que se especifica la misma carpeta raíz en cada solicitud.  <br/>  Asegurarse de que la solicitud anterior no especificaba una carpeta raíz de NULL, mientras que la solicitud actual incluye una carpeta raíz de root. NULL y root no se tratan igual.  <br/> |
|ErrorSyncFolderNotFound  <br/> |Sincronice las subcarpetas o los elementos de una carpeta que no se encuentren en el servidor.  <br/> |Asegurarse de que el identificador de carpeta especificado en la solicitud coincide con un identificador de carpeta devuelto del servidor en una respuesta de sincronización anterior.  <br/> |
|ErrorTimeoutExpired  <br/> |Enviar demasiadas solicitudes.  <br/> |Limitar los lotes a 10 elementos por lote para evitar que se obtengan [límites](ews-throttling-in-exchange.md).  <br/> |
|[ServiceResponseException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx) <br/> |Conéctese a EWS cuando el servidor está sin conexión o hay un problema con la conectividad.  <br/> |Compruebe la conectividad con el servidor y vuelva a intentar la solicitud más adelante. Es probable que se deba a un error de servicio transitorio o a un error de red.  <br/> |
   
## <a name="see-also"></a>Vea también


- [Sincronización de buzones de correo y EWS en Exchange](mailbox-synchronization-and-ews-in-exchange.md)
    
- [Sincronización de carpetas mediante EWS en Exchange](how-to-synchronize-folders-by-using-ews-in-exchange.md)
    
- [Sincronizar elementos mediante EWS en Exchange](how-to-synchronize-items-by-using-ews-in-exchange.md)
    
- [ServiceResponseException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)
    

