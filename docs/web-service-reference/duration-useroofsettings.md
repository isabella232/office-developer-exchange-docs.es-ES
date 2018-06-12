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
description: El elemento de duración Especifica la duración de fuera de la oficina (OOF) está habilitado si se establece el elemento OofState en programado.
ms.openlocfilehash: 62a5492372fd80173d58e965376b7c8c466825a6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764293"
---
# <a name="duration-useroofsettings"></a>Duración (UserOofSettings)

El elemento de **duración** especifica la duración de la espera del estado de la oficina (OOF) está habilitada si se establece el elemento [OofState](oofstate.md) en **programado**.
  
```XML
<Duration>
   <StartTime/>
   <EndTime/> 
</Duration>
```

 **Duration**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[StartTime](starttime.md) <br/> |Representa el inicio de un período de tiempo establecido con un estado de fuera de la oficina. Se requiere este elemento.  <br/> |
|[Hora de finalización](endtime.md) <br/> |Representa el final de un período de tiempo establecido con un estado de fuera de la oficina. Se requiere este elemento.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[UserOofSettings](useroofsettings.md) <br/> |Especifica la configuración de fuera de la oficina.  <br/><br/>La siguiente es la expresión de XPath para este elemento:<br/><br/>`/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[OofSettings](oofsettings.md) <br/> |Contiene la configuración de fuera de la oficina.<br/><br/>La siguiente es la expresión de XPath para este elemento:<br/><br/>`/GetUserOofSettingsResponse/OofSettings` <br/> |
|[Fuera de la oficina](outofoffice.md) <br/> |Define el mensaje de respuesta de fuera de oficina (OOF) y un tiempo de duración para enviar el mensaje de respuesta para un buzón de correo.  <br/> |
   
## <a name="remarks"></a>Notas

El tipo de **duración** también es el tipo de los elementos [DetailedSuggestionsWindow](detailedsuggestionswindow.md), [ventana de tiempo](timewindow.md)y [fuera de la oficina](outofoffice.md) . 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="example"></a>Ejemplo

El siguiente ejemplo de una solicitud de [operación de SetUserOofSettings](setuseroofsettings-operation.md) la [OofState](oofstate.md) establece en **habilitado**, los mensajes de fuera de la oficina internos y externos y establece la duración de OOF durante 10 días.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetUserOofSettingsRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <Name>David Alexander</Name>
        <Address>someone@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
      <UserOofSettings xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación GetUserOofSettings](getuseroofsettings-operation.md)  
- [Operación SetUserOofSettings](setuseroofsettings-operation.md)

