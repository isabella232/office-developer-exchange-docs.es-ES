---
title: PrimarySmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PrimarySmtpAddress
api_type:
- schema
ms.assetid: eee79904-9412-4e61-b9b8-aff0ce25fade
description: El elemento PrimarySmtpAddress representa la dirección de Protocolo Simple de transferencia de correo (SMTP) principal de una cuenta que se usará para la autorización de servidor a servidor o acceso delegado.
ms.openlocfilehash: d33bf22af4ddf6b2f6d8d8d434168264acfaea7c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836881"
---
# <a name="primarysmtpaddress"></a>PrimarySmtpAddress

El elemento **PrimarySmtpAddress** representa la dirección de Protocolo Simple de transferencia de correo (SMTP) principal de una cuenta que se usará para la autorización de servidor a servidor o acceso delegado. 
  
```xml
<PrimarySmtpAddress/>
```

 **PrimarySmtpAddressType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ConnectingSID](connectingsid.md) <br/> |Representa una cuenta para suplantar a cuando se usa el encabezado SOAP ExchangeImpersonation.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[SerializedSecurityContext](serializedsecuritycontext.md) <br/> |Se usa en el encabezado SOAP para la serialización de token de autenticación de servidor a servidor.  <br/> |
|[UserId](userid.md) <br/> |Identifica un usuario delegado o un usuario que tiene permisos de acceso de la carpeta.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto que representa una dirección SMTP.
  
## <a name="remarks"></a>Comentarios

Servicios Web de Exchange requiere que los buzones de correo se identificado por la dirección SMTP principal del buzón. No se aceptan direcciones alternativas o proxy.
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


[Autorización de servidor a servidor en EWS](http://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)
  
[Trabajar con el acceso delegado](http://msdn.microsoft.com/library/dfd6b4a3-8fd3-47ba-83c0-52465cb5f3f3%28Office.15%29.aspx)

