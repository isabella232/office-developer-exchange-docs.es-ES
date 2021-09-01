---
title: DirectReports
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ab88739f-9018-4887-ae46-f1471242628c
description: El elemento DirectReports contiene información SMTP que identifica los informes directos de un contacto.
ms.openlocfilehash: 216f6e99a3caf46f9d3bc792dcb4641c3681a9fb
ms.sourcegitcommit: 63e48eaf2891a6db1a718b55cd69e3a0433c4a9c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2021
ms.locfileid: "58851110"
---
# <a name="directreports"></a>DirectReports

El **elemento DirectReports** contiene información SMTP que identifica los informes directos de un contacto. 
  
```XML
<DirectReports>
   <Mailbox/>
</DirectReports>
```

 **SingleRecipientType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Buzón](mailbox.md) <br/> |Identifica un objeto de servicio de directorio de Active Directory habilitado para correo.  <br/> |
     
### <a name="parent-elements"></a>Elementos principales

|**Nombre del elemento**|**Descripción**|
|:-----|:-----|
|[Contact](contact.md) <br/> |Representa el elemento de contacto en Exchange almacén.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
Este elemento se introdujo en Exchange Server 2010 Service Pack 2 (SP2).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)
- [Creación de contactos (Exchange Web Services)](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)

