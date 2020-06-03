---
title: Duración (UserOofSettings)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Duration
api_type:
- schema
ms.assetid: 01d67af3-658e-4acd-93e3-441ae827fdd3
description: El elemento Duration especifica la duración del estado de fuera de la oficina (OOF) si el elemento OofState está establecido en programado.
ms.openlocfilehash: 0ba0f1ea7498781c0cccb072c7ea0fa05414764c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457301"
---
# <a name="duration-useroofsettings"></a>Duración (UserOofSettings)

El elemento **Duration** especifica la duración del estado de fuera de la oficina (OOF) si el elemento [OofState](oofstate.md) está establecido en **programado**.
  
```XML
<Duration>
   <StartTime/>
   <EndTime/> 
</Duration>
```

 **Duración**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[StartTime](starttime.md) <br/> |Representa el inicio del intervalo de tiempo establecido con un estado de OOF. Se requiere este elemento.  <br/> |
|[EndTime](endtime.md) <br/> |Representa el final del intervalo de tiempo establecido con un estado de OOF. Se requiere este elemento.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[UserOofSettings](useroofsettings.md) <br/> |Especifica la configuración de OOF.  <br/><br/>La siguiente es la expresión XPath a este elemento:<br/><br/>`/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[OofSettings](oofsettings.md) <br/> |Contiene la configuración de OOF.<br/><br/>La siguiente es la expresión XPath a este elemento:<br/><br/>`/GetUserOofSettingsResponse/OofSettings` <br/> |
|[Oficina](outofoffice.md) <br/> |Define el mensaje de respuesta de fuera de la oficina (OOF) y un tiempo de duración para enviar el mensaje de respuesta para un buzón de correo.  <br/> |
   
## <a name="remarks"></a>Comentarios

El tipo **Duration** también es el tipo para los elementos [DetailedSuggestionsWindow](detailedsuggestionswindow.md), [TimeWindow](timewindow.md)y [Oficina](outofoffice.md) . 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="example"></a>Ejemplo

El siguiente ejemplo de una solicitud de [operación SetUserOofSettings](setuseroofsettings-operation.md) establece el [OofState](oofstate.md) en **habilitado**, los mensajes internos y externos OOF y establece la duración de OOF durante 10 días.
  
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
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación GetUserOofSettings](getuseroofsettings-operation.md)  
- [Operación SetUserOofSettings](setuseroofsettings-operation.md)

