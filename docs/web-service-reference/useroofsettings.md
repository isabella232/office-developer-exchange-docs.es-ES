---
title: UserOofSettings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserOofSettings
api_type:
- schema
ms.assetid: 0a95ca63-660e-4cc0-82e4-3f74fb4ae21c
description: El elemento UserOofSettings especifica la configuración de fuera de oficina (OOF).
ms.openlocfilehash: a035fd89387ece632d83f5f72a564e4896bc6753
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840921"
---
# <a name="useroofsettings"></a>UserOofSettings

El elemento **UserOofSettings** especifica la configuración de fuera de oficina (OOF). 
  
[SetUserOofSettingsRequest](setuseroofsettingsrequest.md)
  
[UserOofSettings](useroofsettings.md)
  
```xml
<UserOofSettings>
   <OofState>...</OofState>
   <ExternalAudience>...</ExternalAudience>
   <Duration>...</Duration>
   <InternalReply>...</InternalReply>
   <ExternalReply>...</ExternalReply>
</UserOofSettings>
```

 **UserOofSettings**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[OofState](oofstate.md) <br/> |Establece el estado de fuera de la oficina del usuario.  <br/> |
|[ExternalAudience](externalaudience.md) <br/> |Establece o contiene un valor que determina a quienes se envían los mensajes externos de fuera de la oficina.  <br/> |
|[Duración (UserOofSettings)](duration-useroofsettings.md) <br/> |Especifica la duración para la que está habilitado el estado de fuera de la oficina si el elemento [OofState](oofstate.md) está establecido en **programado**. Si el elemento de [OofState](oofstate.md) se establece en **habilitada** o **deshabilitada**, se ignora el valor de este elemento.  <br/> |
|[InternalReply](internalreply.md) <br/> |Contiene la respuesta OOF enviada a otros usuarios de dominio o los dominios de confianza del usuario.  <br/> |
|[ExternalReply](externalreply.md) <br/> |Contiene la respuesta OOF enviada a direcciones fuera del destinatario dominio o dominios de confianza.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[SetUserOofSettingsRequest](setuseroofsettingsrequest.md) <br/> |Contiene los argumentos que se usa para establecer la configuración de fuera de la oficina y los mensajes de un usuario de buzón de correo.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/SetUserOofSettingsRequest` <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="example"></a>Ejemplo

El siguiente ejemplo de una solicitud de SetUserOofSettings la OoFState establece en **habilitado**, Establece la duración de OOF para 10 días y establece los mensajes de fuera de la oficina internos y externos.
  
```xml
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
      </UserOofSettings>
    </SetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación SetUserOofSettings](setuseroofsettings-operation.md)

