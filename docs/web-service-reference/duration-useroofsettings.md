---
title: Duration (UserOofSettings)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Duration
api_type:
- schema
ms.assetid: 01d67af3-658e-4acd-93e3-441ae827fdd3
description: El elemento Duration especifica la duración que el estado de fuera de la oficina (OOF) está habilitado si el elemento OofState está establecido en Programado.
ms.openlocfilehash: cb6529bfe3799ff41550d7fe3ce2c79b8a4197e2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544160"
---
# <a name="duration-useroofsettings"></a>Duration (UserOofSettings)

El **elemento Duration** especifica la duración que el estado de fuera de la oficina (OOF) está habilitado si el elemento [OofState](oofstate.md) está establecido en **Scheduled**.
  
```XML
<Duration>
   <StartTime/>
   <EndTime/> 
</Duration>
```

 **Duration**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[StartTime](starttime.md) <br/> |Representa el inicio del intervalo de tiempo establecido con un estado OOF. Se requiere este elemento.  <br/> |
|[EndTime](endtime.md) <br/> |Representa el final del intervalo de tiempo establecido con un estado OOF. Se requiere este elemento.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[UserOofSettings](useroofsettings.md) <br/> |Especifica la configuración de OOF.  <br/><br/>A continuación se muestra la expresión XPath de este elemento:<br/><br/>`/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[OofSettings](oofsettings.md) <br/> |Contiene la configuración de OOF.<br/><br/>A continuación se muestra la expresión XPath de este elemento:<br/><br/>`/GetUserOofSettingsResponse/OofSettings` <br/> |
|[OutOfOffice](outofoffice.md) <br/> |Define el mensaje de respuesta Office (OOF) y un tiempo de duración para enviar el mensaje de respuesta para un buzón.  <br/> |
   
## <a name="remarks"></a>Comentarios

El **tipo** Duration también es el tipo de los elementos [DetailedSuggestionsWindow](detailedsuggestionswindow.md), [TimeWindow](timewindow.md)y [OutOfOffice.](outofoffice.md) 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="example"></a>Ejemplo

En el siguiente ejemplo de una solicitud de operación [SetUserOofSettings](setuseroofsettings-operation.md) se establece [OofState](oofstate.md) en **Enabled**, los mensajes OOF internos y externos y se establece la duración de OOF durante 10 días.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetUserOofSettingsRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <Name>David Alexander</Name>
        <Address>someone@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
      <UserOofSettings xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <OofState>Enabled</OofState>
        <ExternalAudience>All</ExternalAudience>
        <Duration>
          <StartTime>2005-10-05T00:00:00</StartTime>
          <EndTime>2005-10-25T00:00:00</EndTime>
        </Duration>
        <InternalReply>
          <Message>I am out of office.  This is my internal reply.</Message>
        </InternalReply>
        <ExternalReply>
          <Message>I am out of office. This is my external reply.</Message>
        </ExternalReply>
        <SetByLegacyClient>false</SetByLegacyClient>
      </UserOofSettings>
    </SetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Operación GetUserOofSettings](getuseroofsettings-operation.md)  
- [Operación SetUserOofSettings](setuseroofsettings-operation.md)

