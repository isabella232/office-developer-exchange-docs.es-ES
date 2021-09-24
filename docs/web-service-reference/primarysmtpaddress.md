---
title: PrimarySmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PrimarySmtpAddress
api_type:
- schema
ms.assetid: eee79904-9412-4e61-b9b8-aff0ce25fade
description: El elemento PrimarySmtpAddress representa la dirección principal del Protocolo simple de transferencia de correo (SMTP) de una cuenta que se usará para la autorización de servidor a servidor o el acceso delegado.
ms.openlocfilehash: 7963fbc92de88b38da93e577ebd2c39dbedac009
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523883"
---
# <a name="primarysmtpaddress"></a>PrimarySmtpAddress

El **elemento PrimarySmtpAddress** representa la dirección principal del Protocolo simple de transferencia de correo (SMTP) de una cuenta que se usará para la autorización de servidor a servidor o el acceso delegado. 
  
```xml
<PrimarySmtpAddress/>
```

 **PrimarySmtpAddressType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ConnectingSID](connectingsid.md) <br/> |Representa una cuenta que se va a suplantar cuando se usa el encabezado SOAP de ExchangeImpersonation.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[SerializedSecurityContext](serializedsecuritycontext.md) <br/> |Se usa en el encabezado SOAP para la serialización de tokens en la autenticación de servidor a servidor.  <br/> |
|[UserId](userid.md) <br/> |Identifica un usuario delegado o un usuario que tiene permisos de acceso a carpetas.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto que representa una dirección SMTP.
  
## <a name="remarks"></a>Comentarios

Exchange Servicios web requiere que los buzones se identifiquen mediante la dirección SMTP principal del buzón. No se aceptan direcciones alternativas o proxy.
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


[Autorización de servidor a servidor en EWS](https://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)
  
[Trabajar con acceso delegado](https://msdn.microsoft.com/library/dfd6b4a3-8fd3-47ba-83c0-52465cb5f3f3%28Office.15%29.aspx)

