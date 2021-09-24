---
title: SmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SmtpAddress
api_type:
- schema
ms.assetid: 779305a6-ad1e-424e-8a69-4e3bef61d787
description: El elemento SmtpAddress representa la dirección de protocolo simple de transferencia de correo (SMTP) de una cuenta que se usará para suplantación o una dirección de destinatario del Protocolo simple de transferencia de correo (SMTP) de un calendario o solicitud de uso compartido de contactos.
ms.openlocfilehash: c10e18ce77a1002a9c7a94718e8e9a2bd3877d8d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539090"
---
# <a name="smtpaddress"></a>SmtpAddress

El **elemento SmtpAddress** representa la dirección de protocolo simple de transferencia de correo (SMTP) de una cuenta que se usará para suplantación o una dirección de destinatario del Protocolo simple de transferencia de correo (SMTP) de un calendario o solicitud de uso compartido de contactos. 
  
```xml
<SmtpAddress/>
```

**SmtpAddressType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ConnectingSID](connectingsid.md) <br/> |Representa una cuenta que se va a suplantar cuando se usa el encabezado SOAP de ExchangeImpersonation.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[InvalidRecipient](invalidrecipient.md) <br/> |Representa un destinatario no válido para un mensaje de uso compartido de calendario o de uso compartido de contactos.  <br/> |
|[Recipients (ArrayOfSmtpAddressType)](recipients-arrayofsmtpaddresstype.md) <br/> |Representa una colección de destinatarios a los que se concederá acceso a la carpeta compartida.  <br/> |
|[GetSharingFolder](getsharingfolder.md) <br/> |Define una solicitud para obtener el identificador de carpeta local de una carpeta compartida especificada.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto que representa una dirección SMTP.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda Exchange Servicios web del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

