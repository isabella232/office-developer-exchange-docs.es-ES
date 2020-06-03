---
title: ProtocolConnection (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 6eef2188-6194-48f1-ad7e-46104aecdf56
description: El elemento ProtocolConnection representa la conexión de protocolo del cliente web del servidor.
ms.openlocfilehash: b9df3febe36db53d7c5bf0610ba857f13aa96abc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528863"
---
# <a name="protocolconnection-soap"></a>ProtocolConnection (SOAP)

El elemento **ProtocolConnection** representa la conexión de protocolo del cliente web del servidor. 
  
```XML
<ProtocolConnection>
   <Hostname/>
   <Port/>
   <EncryptionMethod/>
</ProtocolConnection>
```

 **ProtocolConnection**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Nombre de host (SOAP)](hostname-soap.md) <br/> |Representa la parte de nombre de host del nombre de equipo completo del equipo.  <br/> |
|[Puerto (SOAP)](port-soap.md) <br/> |Representa el número de puerto que se va a usar para el protocolo.  <br/> |
|[EncryptionMethod (SOAP)](encryptionmethod-soap.md) <br/> |Representa el método criptográfico que se usa para los protocolos POP, IMAP y SMTP.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ProtocolConnections (SOAP)](protocolconnections-soap.md) <br/> |Contiene cero o más conexiones de protocolo.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguna.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



[ProtocolConnectionCollectionSetting (SOAP)](protocolconnectioncollectionsetting-soap.md)

