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
description: El elemento UserOofSettings especifica la configuración de fuera de la oficina (OOF).
ms.openlocfilehash: 417c3d5061a6229d41eb57f72e89f03213acf460
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461908"
---
# <a name="useroofsettings"></a>UserOofSettings

El elemento **UserOofSettings** especifica la configuración de fuera de la oficina (OOF). 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[OofState](oofstate.md) <br/> |Establece el estado de OOF del usuario.  <br/> |
|[ExternalAudience](externalaudience.md) <br/> |Establece o contiene un valor que determina a quién se envían los mensajes de OOF externos.  <br/> |
|[Duración (UserOofSettings)](duration-useroofsettings.md) <br/> |Especifica la duración para la que está habilitado el estado OOF si el elemento [OofState](oofstate.md) está establecido en **programado**. Si el elemento [OofState](oofstate.md) está establecido en **habilitado** o **deshabilitado**, se omite el valor de este elemento.  <br/> |
|[InternalReply](internalreply.md) <br/> |Contiene la respuesta OOF enviada a otros usuarios en el dominio del usuario o los dominios de confianza.  <br/> |
|[ExternalReply](externalreply.md) <br/> |Contiene la respuesta OOF enviada a direcciones fuera del dominio del destinatario o de dominios de confianza.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SetUserOofSettingsRequest](setuseroofsettingsrequest.md) <br/> |Contiene los argumentos usados para establecer los mensajes y la configuración de OOF de un usuario de buzón.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/SetUserOofSettingsRequest` <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="example"></a>Ejemplo

El siguiente ejemplo de una solicitud SetUserOofSettings establece la OoFState en **habilitada**, establece la duración de OOF durante 10 días y establece los mensajes OOF internos y externos.
  
```xml
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
      </UserOofSettings>
    </SetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación SetUserOofSettings](setuseroofsettings-operation.md)

