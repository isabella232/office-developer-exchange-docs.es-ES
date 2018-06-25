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
description: El elemento ProtocolConnection representa la conexión de protocolo del cliente de servidor Web.
ms.openlocfilehash: 8b5396821cd959e41d24fcf7a94c519f9c634a1f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836915"
---
# <a name="protocolconnection-soap"></a>ProtocolConnection (SOAP)

El elemento **ProtocolConnection** representa la conexión de protocolo del cliente de servidor Web. 
  
```XML
<ProtocolConnection>
   <Hostname/>
   <Port/>
   <EncryptionMethod/>
</ProtocolConnection>
```

 **ProtocolConnection**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Nombre de host (SOAP)](hostname-soap.md) <br/> |Representa la parte del nombre completo del equipo del equipo en el nombre de host.  <br/> |
|[Puerto (SOAP)](port-soap.md) <br/> |Representa el número de puerto que se usará para el protocolo.  <br/> |
|[EncryptionMethod (SOAP)](encryptionmethod-soap.md) <br/> |Representa el método de cifrado que se usa para los protocolos POP, IMAP y SMTP.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ProtocolConnections (SOAP)](protocolconnections-soap.md) <br/> |Contiene cero o más conexiones de protocolo.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



[ProtocolConnectionCollectionSetting (SOAP)](protocolconnectioncollectionsetting-soap.md)

