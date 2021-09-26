---
title: EncryptionMethod (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: bc632c85-ec74-4a00-baec-df5973e032fa
description: El elemento EncryptionMethod representa el método criptográfico que se usa para los protocolos POP, IMAP y SMTP.
ms.openlocfilehash: 40b9f7736502f8def5389c1a70fddb61e38973aa
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546598"
---
# <a name="encryptionmethod-soap"></a>EncryptionMethod (SOAP)

El **elemento EncryptionMethod** representa el método criptográfico que se usa para los protocolos POP, IMAP y SMTP. 
  
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
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)

