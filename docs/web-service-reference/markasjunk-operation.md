---
title: Operación MarkAsJunk
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 1f71f04d-56a9-4fee-a4e7-d1034438329e
description: Busque información sobre la operación ews MarkAsJunk.
ms.openlocfilehash: b165b415ce9380846b49d15dd321bfddba72b749
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524738"
---
# <a name="markasjunk-operation"></a>Operación MarkAsJunk

Busque información sobre la **operación ews MarkAsJunk.** 
  
La **operación MarkAsJunk** agrega y quita usuarios de la lista de correo electrónico bloqueado y mueve los mensajes de correo electrónico a la carpeta Correo no deseado. 
  
Esta operación se introdujo en Exchange Server 2013.
  
## <a name="using-the-markasjunk-operation"></a>Uso de la operación MarkAsJunk

La **operación MarkAsJunk** contiene dos opciones booleanas para indicar si un remitente de correo electrónico debe agregarse a la lista de remitentes bloqueados y si el mensaje de correo electrónico de destino debe moverse a la carpeta de correo electrónico no deseado predeterminada o a la carpeta Bandeja de entrada. Las acciones están determinadas por los valores de los **atributos IsJunk** y **MoveItem.** Las siguientes son las acciones posibles basadas en las combinaciones de valores para los **atributos IsJunk** y **MoveItem:** 
  
- Si el atributo **IsJunk** se establece en **true** y el atributo **MoveItem** se establece en **true**, el remitente del mensaje de correo electrónico de destino se agrega a la lista de remitentes bloqueados y el mensaje de correo electrónico se mueve a la carpeta correo no deseado.
    
- Si el atributo **IsJunk** se establece en **true** y el atributo **MoveItem** se establece en **false**, el remitente del mensaje de correo electrónico de destino se agrega a la lista de remitentes bloqueados y el mensaje de correo electrónico no se mueve de la carpeta.
    
- Si el atributo **IsJunk** se establece en **false** y el atributo **MoveItem** se establece en **true**, el remitente del mensaje de correo electrónico de destino se quita de la lista de remitentes bloqueados y el mensaje de correo electrónico se mueve a la carpeta Bandeja de entrada.
    
- Si el atributo **IsJunk** se establece en **false** y el atributo **MoveItem** se establece en **false**, el remitente del mensaje de correo electrónico de destino se quita de la lista de remitentes bloqueados y el mensaje de correo electrónico no se mueve de la carpeta.
    
> [!IMPORTANT]
> El contenido de la lista de remitentes bloqueados no se puede detectar desde EWS. Si se agrega un remitente a la lista de remitentes bloqueados, debe conservar una copia de un mensaje de correo electrónico enviado por el remitente bloqueado para desbloquear el remitente en el futuro. 
  
### <a name="markasjunk-operation-soap-headers"></a>Encabezados SOAP de la operación MarkAsJunk

La **operación MarkAsJunk** puede usar los encabezados SOAP que se enumeran en la tabla siguiente. 
  
|**Nombre de encabezado**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|**Suplantación** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica el usuario al que la aplicación cliente está suplantando. Este encabezado es aplicable a una solicitud.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural, tal como se define en RFC 3066, "Etiquetas para la identificación de idiomas", que se usará para tener acceso al buzón. Este encabezado es aplicable a una solicitud.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de operación. Este encabezado es aplicable a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que respondió a la solicitud. Este encabezado es aplicable a una respuesta.  <br/> |
   
## <a name="markasjunk-operation-request-example-add-a-sender-to-the-blocked-sender-list"></a>Ejemplo de solicitud de operación MarkAsJunk: Agregar un remitente a la lista de remitentes bloqueados

En el siguiente ejemplo de una solicitud de operación **MarkAsJunk** se muestra cómo agregar el remitente de un correo electrónico a la lista de remitentes bloqueados y mover el correo electrónico a la carpeta de correo no deseado. La **operación MarkAsJunk** acepta el identificador de mensaje de correo electrónico único para identificar el correo electrónico que se usa para hacer referencia al remitente que se agrega a la lista de remitentes bloqueados. 
  
> [!NOTE]
> Todos los identificadores de elementos y las claves de cambio de este artículo se han acortado para conservar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
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

El cuerpo SOAP de la solicitud contiene los siguientes elementos:
  
- [MarkAsJunk](markasjunk.md)
    
- [ItemIds](itemids.md)
    
- [ItemId](itemid.md)
    
## <a name="successful-markasjunk-operation-response"></a>Respuesta correcta de la operación MarkAsJunk

En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **MarkAsJunk** para agregar un remitente a la lista de remitentes bloqueados y mover el mensaje de correo electrónico a la carpeta Correo no deseado. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" 
                             MinorVersion="0" 
                             MajorBuildNumber="545" 
                             MinorBuildNumber="11" 
                             Version="Exchange2013" 
                             xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                             xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                             xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                             xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
            xmlns:xsd="http://www.w3.org/2001/XMLSchema">
        <m:MarkAsJunkResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

El cuerpo SOAP de la respuesta contiene los siguientes elementos:
  
- [MarkAsJunkResponse](markasjunkresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MarkAsJunkResponseMessage](markasjunkresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [MovedItemId](moveditemid.md)
    
## <a name="markasjunk-operation-request-example-remove-a-sender-from-the-blocked-sender-list"></a>Ejemplo de solicitud de operación MarkAsJunk: Quitar un remitente de la lista de remitentes bloqueados

En el siguiente ejemplo de una solicitud de operación **MarkAsJunk** se muestra cómo quitar el remitente de un mensaje de correo electrónico de la lista de remitentes bloqueados y mover el mensaje de correo electrónico a la carpeta Bandeja de entrada. Debe mantener un mensaje de correo electrónico enviado por el remitente bloqueado para quitar el remitente de la lista de remitentes bloqueados. La dirección de correo electrónico del remitente está asociada con los mensajes de correo electrónico enviados por el remitente. La eliminación de un remitente de la lista de remitentes bloqueados no se realizará correctamente si el mensaje de correo electrónico de referencia ya no existe en el buzón del usuario. El identificador de elemento usado para asociar un mensaje de correo electrónico con su remitente debe asociarse con un elemento que existe en el buzón Exchange correo. Se recomienda crear una carpeta oculta para almacenar los elementos enviados por remitentes bloqueados anteriormente para que los remitentes se puedan desbloquear desde la aplicación cliente. En caso de que se haya quitado un elemento del buzón de Exchange, un administrador debe usar el Consola de administración de Exchange para obtener acceso a la lista de remitentes bloqueados para quitar un remitente de la lista. Para obtener información sobre cómo desbloquear un usuario mediante el Consola de administración de Exchange, vea How [to configure the safe senders and blocked senders settings in Office 365](https://support.microsoft.com/kb/2545137).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
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

Una respuesta correcta para quitar un remitente de la lista de remitentes bloqueados es la misma que la respuesta para agregar un remitente a la lista de remitentes bloqueados.
  
El cuerpo SOAP de la solicitud contiene los siguientes elementos:
  
- [MarkAsJunk](markasjunk.md)
    
- [ItemIds](itemids.md)
    
- [ItemId](itemid.md)
    
## <a name="markasjunk-operation-error-response"></a>Respuesta de error de operación MarkAsJunk

En el ejemplo siguiente se muestra una respuesta de error a una **solicitud de operación MarkAsJunk.** Esta es una respuesta a una solicitud para agregar o quitar un remitente de la lista de remitentes bloqueados cuando el mensaje de correo electrónico especificado por el identificador de elemento ya no existe en el buzón. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="545" 
                         MinorBuildNumber="11" 
                         Version="Exchange2013" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:MarkAsJunkResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

El cuerpo SOAP de la respuesta de error contiene los siguientes elementos:
  
- [MarkAsJunkResponse](markasjunkresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MarkAsJunkResponseMessage](markasjunkresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Ver también

- [Operaciones ews en Exchange](ews-operations-in-exchange.md)
    
- [Operación GetItem](getitem-operation.md) Operación GetItem 
    
- [Operación FindItem](finditem-operation.md)
    

