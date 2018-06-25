---
title: MarkAsJunk Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1f71f04d-56a9-4fee-a4e7-d1034438329e
description: Busque información sobre la EWS MarkAsJunk operación.
ms.openlocfilehash: b9d79e6fbec87ce41030b4981f3c16f2f9ce9507
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836353"
---
# <a name="markasjunk-operation"></a>MarkAsJunk Operation

Obtenga información acerca de la operación de EWS **MarkAsJunk** . 
  
La operación **MarkAsJunk** agrega y quita los usuarios de la lista de correo electrónico bloqueados y mueve mensajes de correo electrónico a la carpeta de correo electrónico no deseado. 
  
Esta operación se introdujo en Exchange Server 2013.
  
## <a name="using-the-markasjunk-operation"></a>Mediante la operación MarkAsJunk

La operación **MarkAsJunk** contiene dos opciones booleanas para indicar si se debe agregar un remitente de correo electrónico a la lista de remitentes bloqueados y si se va a mover el mensaje de correo electrónico de destino para la carpeta de correo electrónico no deseado predeterminada o en la carpeta Bandeja de entrada. Las acciones están determinadas por los valores de los atributos **IsJunk** y **MoveItem** . Los siguientes son las posibles acciones en función de las combinaciones de valores para los atributos **IsJunk** y **MoveItem** : 
  
- Si el atributo **IsJunk** se establece en **true**y el atributo **MoveItem** se establece en **true**, se agrega el remitente del mensaje de correo electrónico de destino a la lista de remitentes bloqueados y el mensaje de correo electrónico se mueve a la carpeta correo no deseado Dmail.
    
- Si el atributo **IsJunk** se establece en **true**y el atributo **MoveItem** se establece en **false**, se agrega el remitente del mensaje de correo electrónico de destino a la lista de remitentes bloqueados y no se mueve el mensaje de correo electrónico de la carpeta.
    
- Si el atributo **IsJunk** está establecido en **false**y el **MoveItem** atributo está establecido en **true**, el remitente de la messageis de correo electrónico de destino quitado de la lista de remitentes bloqueados y el mensaje de correo electrónico se mueve a la carpeta Bandeja de entrada.
    
- Si el atributo **IsJunk** está establecido en **false**y el atributo **MoveItem** se establece en **false**, el remitente del mensaje de correo electrónico de destino se quita de la lista de remitentes bloqueados y no se mueve el mensaje de correo electrónico de la carpeta.
    
> [!IMPORTANT]
> El contenido de la lista de remitentes bloqueados no es reconocible de EWS. Si un remitente se agrega a la lista de remitentes bloqueados, debe conservar una copia de un mensaje de correo electrónico enviado por el remitente bloqueado para desbloquear el remitente en el futuro. 
  
### <a name="markasjunk-operation-soap-headers"></a>Encabezados SOAP de operación de MarkAsJunk

La operación de **MarkAsJunk** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla. 
  
|**Nombre de encabezado**|**Element**|**Descripción**|
|:-----|:-----|:-----|
|**Suplantación** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica el usuario que está realizando la suplantación de la aplicación cliente. Este encabezado es aplicable a una solicitud.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural, como se define en RFC 3066, "Etiquetas para la identificación de idiomas," que se utilizará para acceder al buzón. Este encabezado es aplicable a una solicitud.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de la operación. Este encabezado es aplicable a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que ha respondido a la solicitud. Este encabezado es aplicable a una respuesta.  <br/> |
   
## <a name="markasjunk-operation-request-example-add-a-sender-to-the-blocked-sender-list"></a>Ejemplo de solicitud de operación de MarkAsJunk: agregar un remitente a la lista de remitentes bloqueados

El siguiente ejemplo de una solicitud de operación **MarkAsJunk** muestra cómo agregar el remitente de un correo electrónico a la lista de remitentes bloqueados y mover el correo electrónico a la carpeta correo electrónico no deseado. La operación **MarkAsJunk** acepta el identificador de mensaje de correo electrónico único para identificar el correo electrónico que se usa para hacer referencia al remitente que se agrega a la lista de remitentes bloqueados. 
  
> [!NOTE]
> Todos los identificadores de artículo y cambiar claves en este artículo se han abreviado para conservar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
    <soap:Header>
        <t:RequestServerVersion Version="Exchange2013" />
    </soap:Header>
    <soap:Body>
        <m:MarkAsJunk IsJunk="true" MoveItem="true">
            <m:ItemIds>
                <t:ItemId Id="AAMkAD=" ChangeKey="CQAAABYA" />
            </m:ItemIds>
        </m:MarkAsJunk>
    </soap:Body>
</soap:Envelope>

```

La solicitud SOAP body contiene los siguientes elementos:
  
- [MarkAsJunk](markasjunk.md)
    
- [ItemId](itemids.md)
    
- [ItemId](itemid.md)
    
## <a name="successful-markasjunk-operation-response"></a>Respuesta es correcta de operación MarkAsJunk

En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **MarkAsJunk** para agregar un remitente a la lista de remitentes bloqueados y mover el mensaje de correo electrónico a la carpeta correo electrónico no deseado. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" 
                             MinorVersion="0" 
                             MajorBuildNumber="545" 
                             MinorBuildNumber="11" 
                             Version="Exchange2013" 
                             xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                             xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                             xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                             xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
            xmlns:xsd="http://www.w3.org/2001/XMLSchema">
        <m:MarkAsJunkResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
           <m:ResponseMessages>
               <m:MarkAsJunkResponseMessage ResponseClass="Success">
                  <m:ResponseCode>NoError</m:ResponseCode>
                 <m:MovedItemId Id="AAMkAD=" ChangeKey="CQAAABYu" />
               </m:MarkAsJunkResponseMessage>
           </m:ResponseMessages>
        </m:MarkAsJunkResponse>
    </s:Body>
</s:Envelope>
```

La respuesta SOAP body contiene los siguientes elementos:
  
- [MarkAsJunkResponse](markasjunkresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MarkAsJunkResponseMessage](markasjunkresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [MovedItemId](moveditemid.md)
    
## <a name="markasjunk-operation-request-example-remove-a-sender-from-the-blocked-sender-list"></a>Ejemplo de solicitud de operación de MarkAsJunk: quitar un remitente de la lista de remitentes bloqueados

El siguiente ejemplo de una solicitud de operación **MarkAsJunk** muestra cómo quitar el remitente de un mensaje de correo electrónico de la lista de remitentes bloqueados y mover el mensaje de correo electrónico a la carpeta Bandeja de entrada. Debe tener un mensaje de correo electrónico enviado por el remitente bloqueado para quitar el remitente de la lista de remitentes bloqueados. Dirección de correo electrónico del remitente está asociada con los mensajes de correo electrónico que se han enviado por el remitente. Eliminación de un remitente de la lista de remitentes bloqueados no se realizará correctamente si el mensaje de correo electrónico de referencia ya no existe en el buzón del usuario. El identificador de elemento que se utiliza para asociar un mensaje de correo electrónico a su remitente debe asociarse con un elemento que existe en el buzón de Exchange. Recomendamos que cree una carpeta oculta para almacenar elementos enviados por remitentes bloqueados anteriormente para que los remitentes se puedan desbloqueados desde la aplicación cliente. En caso de que un elemento se ha quitado de los buzones de Exchange, un administrador tiene que usar la consola de administración de Exchange para tener acceso a la lista de remitentes bloqueados para quitar un remitente de la lista. Para obtener información acerca de cómo desbloquear un usuario mediante el uso de la consola de administración de Exchange, consulte [cómo configurar los remitentes seguros y remitentes bloqueados en Office 365](http://support.microsoft.com/kb/2545137).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
    <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
    </soap:Header>
    <soap:Body>
      <m:MarkAsJunk IsJunk="false" MoveItem="true">
        <m:ItemIds>
          <t:ItemId Id="AAMkAD=" ChangeKey="CQAAABYu" />
        </m:ItemIds>
      </m:MarkAsJunk>
    </soap:Body>
 </soap:Envelope>

```

Una respuesta correcta para quitar un remitente de la lista de remitentes bloqueados es el mismo que la respuesta para agregar un remitente a la lista de remitentes bloqueados.
  
La solicitud SOAP body contiene los siguientes elementos:
  
- [MarkAsJunk](markasjunk.md)
    
- [ItemId](itemids.md)
    
- [ItemId](itemid.md)
    
## <a name="markasjunk-operation-error-response"></a>Respuesta de error de la operación de MarkAsJunk

En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **MarkAsJunk** . Esta es una respuesta a una solicitud para agregar o quitar un remitente de la lista de remitentes bloqueados cuando el mensaje de correo electrónico especificado por el identificador del elemento ya no existe en el buzón de correo. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="545" 
                         MinorBuildNumber="11" 
                         Version="Exchange2013" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:MarkAsJunkResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:MarkAsJunkResponseMessage ResponseClass="Error">
          <m:MessageText>The specified object was not found in the store.</m:MessageText>
          <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:MarkAsJunkResponseMessage>
      </m:ResponseMessages>
    </m:MarkAsJunkResponse>
  </s:Body>
</s:Envelope>
```

La respuesta de error SOAP body contiene los siguientes elementos:
  
- [MarkAsJunkResponse](markasjunkresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MarkAsJunkResponseMessage](markasjunkresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Vea también

- [Operaciones de EWS en Exchange](ews-operations-in-exchange.md)
    
- [GetItem operation](getitem-operation.md) Operación GetItem 
    
- [Operación FindItem](finditem-operation.md)
    

