---
title: EncryptionMethod (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: bc632c85-ec74-4a00-baec-df5973e032fa
description: El elemento EncryptionMethod representa el método criptográfico que se usa para los protocolos POP, IMAP y SMTP.
ms.openlocfilehash: 26236d9b08eae1bcabfd9aac59f5b01714ba9841
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530659"
---
# <a name="encryptionmethod-soap"></a>EncryptionMethod (SOAP)

El elemento **EncryptionMethod** representa el método criptográfico que se usa para los protocolos pop, IMAP y SMTP. 
  
```XML
<EncryptionMethod/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ProtocolConnection (SOAP)](protocolconnection-soap.md) <br/> |Representa la conexión de protocolo del cliente web del servidor.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto de este elemento es el método criptográfico que se usa para los protocolos POP, IMAP y SMTP.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)

