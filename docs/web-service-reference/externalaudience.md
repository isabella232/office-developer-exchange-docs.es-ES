---
title: ExternalAudience
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ExternalAudience
api_type:
- schema
ms.assetid: 79dc2a4c-f7dd-46d1-8f31-149116e1f76e
description: El elemento ExternalAudience establece o contiene un valor que determina a quién se envían los mensajes externos fuera de Office (OOF).
ms.openlocfilehash: da318bfcf4a43d880b86379364c6e40aa9861f83
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545142"
---
# <a name="externalaudience"></a>ExternalAudience

El **elemento ExternalAudience** establece o contiene un valor que determina a quién se envían los mensajes externos fuera de Office (OOF). 
  
```xml
<ExternalAudience>None or Known or All</ExternalAudience>
```

 **ExternalAudience**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[UserOofSettings](useroofsettings.md) <br/> |Especifica la configuración de OOF.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[OofSettings](oofsettings.md) <br/> |Contiene la configuración de OOF.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/GetUserOofSettingsResponse/OofSettings` <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto para este elemento. En la tabla siguiente se enumeran los valores posibles para este elemento.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|**Ninguno** <br/> |Los remitentes de correo electrónico fuera de la organización del usuario del buzón que envían mensajes al usuario no recibirán una respuesta de mensaje OOF externa.  <br/> |
|**Conocido** <br/> |Los remitentes de correo electrónico fuera de la organización del usuario del buzón que envían mensajes al usuario solo recibirán una respuesta de mensaje OOF externo si el remitente está en la lista de contactos del almacén Exchange del usuario.  <br/> |
|**Todo** <br/> |Los remitentes de correo electrónico fuera de la organización del usuario del buzón que envían mensajes al usuario recibirán una respuesta de mensaje OOF externa.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento comparte el mismo tipo que el [elemento AllowExternalOof.](allowexternaloof.md) 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="example"></a>Ejemplo

El siguiente ejemplo de una solicitud SetUserOofSettings establece OoFState en **Enabled**, establece la audiencia externa en **All**, establece la duración de OOF en 10 días y establece los mensajes OOF internos y externos.
  
```
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
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también



[Operación GetUserOofSettings](getuseroofsettings-operation.md)
  
[Operación SetUserOofSettings](setuseroofsettings-operation.md)

