---
title: MSExchangeCertificate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c514f22f-be3e-4cad-ac56-bdff6bafcee6
description: El elemento MSExchangeCertificate contiene un valor que codifica el certificado de Microsoft Exchange de un contacto.
ms.openlocfilehash: 60bbcfb45e52dc92140d03cdd24a251ea84217b1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465677"
---
# <a name="msexchangecertificate"></a>MSExchangeCertificate

El elemento **MSExchangeCertificate** contiene un valor que codifica el certificado de Microsoft Exchange de un contacto. 
  
```XML
<MSExchangeCertificate/>
```

 **ArrayOfBinaryType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Nombre del elemento**|**Descripción**|
|:-----|:-----|
|[Base64Binary](base64binary.md) <br/> |Contiene un valor codificado en Base64.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Nombre del elemento**|**Descripción**|
|:-----|:-----|
|[Contacto](contact.md) <br/> |Representa un elemento de contacto en el almacén de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
Este elemento se introdujo en Exchange Server 2010 Service Pack 2 (SP2).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


[Creación de contactos (servicios Web de Exchange)](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)

