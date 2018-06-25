---
title: ExternalAudience
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExternalAudience
api_type:
- schema
ms.assetid: 79dc2a4c-f7dd-46d1-8f31-149116e1f76e
description: El elemento ExternalAudience establece o contiene un valor que determina a quienes se envían los mensajes externos de fuera de oficina (OOF).
ms.openlocfilehash: 836b0f6a5140a37e1584f571cb8e26534fe7a25f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764542"
---
# <a name="externalaudience"></a>ExternalAudience

El elemento **ExternalAudience** establece o contiene un valor que determina a quienes se envían los mensajes externos de fuera de oficina (OOF). 
  
```xml
<ExternalAudience>None or Known or All</ExternalAudience>
```

 **ExternalAudience**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[UserOofSettings](useroofsettings.md) <br/> |Especifica la configuración de fuera de la oficina.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[OofSettings](oofsettings.md) <br/> |Contiene la configuración de fuera de la oficina.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/GetUserOofSettingsResponse/OofSettings` <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto es necesario para este elemento. En la siguiente tabla se enumera los valores posibles para este elemento.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|**None** <br/> |Los remitentes de correo electrónico fuera de la organización del usuario de buzón de correo que envían mensajes al usuario no recibirá una respuesta de mensaje de fuera de la oficina externa.  <br/> |
|**Conocidos** <br/> |Los remitentes de correo electrónico fuera de la organización del usuario de buzón de correo que envían mensajes al usuario sólo recibirá una respuesta de mensaje de fuera de la oficina externa si el remitente está en Exchange del usuario almacenan la lista de contactos.  <br/> |
|**All** <br/> |Los remitentes de correo electrónico fuera de la organización del usuario de buzón de correo que envían mensajes al usuario recibirá una respuesta de mensaje de fuera de la oficina externa.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento comparte el mismo tipo que el elemento [AllowExternalOof](allowexternaloof.md) . 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="example"></a>Ejemplo

El siguiente ejemplo de una solicitud de SetUserOofSettings la OoFState establece en **habilitado**, la audiencia externa establece en **todos los**, Establece la duración de OOF a 10 días y establece los mensajes de fuera de la oficina internos y externos.
  
```
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
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetUserOofSettings](getuseroofsettings-operation.md)
  
[Operación SetUserOofSettings](setuseroofsettings-operation.md)

