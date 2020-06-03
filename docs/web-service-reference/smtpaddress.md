---
title: SmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SmtpAddress
api_type:
- schema
ms.assetid: 779305a6-ad1e-424e-8a69-4e3bef61d787
description: El elemento SmtpAddress representa la dirección del Protocolo simple de transferencia de correo (SMTP) de una cuenta que se va a usar para la suplantación o la dirección del destinatario del Protocolo simple de transferencia de correo (SMTP) de una solicitud de uso compartido de contactos o calendario.
ms.openlocfilehash: 915ff328cc384c1f2884e9fbea8c10c1ebc79288
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466692"
---
# <a name="smtpaddress"></a>SmtpAddress

El elemento **SmtpAddress** representa la dirección del Protocolo simple de transferencia de correo (SMTP) de una cuenta que se va a usar para la suplantación o la dirección del destinatario del Protocolo simple de transferencia de correo (SMTP) de una solicitud de uso compartido de contactos o calendario. 
  
```xml
<SmtpAddress/>
```

**SmtpAddressType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ConnectingSID](connectingsid.md) <br/> |Representa una cuenta que se va a suplantar cuando se usa el encabezado SOAP ExchangeImpersonation.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[InvalidRecipient](invalidrecipient.md) <br/> |Representa un destinatario no válido para un mensaje de uso compartido de calendarios o contactos.  <br/> |
|[Recipients (ArrayOfSmtpAddressType)](recipients-arrayofsmtpaddresstype.md) <br/> |Representa una colección de destinatarios a los que se concederá acceso a la carpeta compartida.  <br/> |
|[GetSharingFolder](getsharingfolder.md) <br/> |Define una solicitud para obtener el identificador de carpeta local de una carpeta compartida especificada.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se necesita un valor de texto que represente una dirección SMTP.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

