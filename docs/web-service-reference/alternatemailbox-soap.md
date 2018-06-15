---
title: AlternateMailbox (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: d913a70d-5a85-4b6e-becc-2fb9334b6088
description: El elemento AlternateMailbox representa un buzón de alternativo.
ms.openlocfilehash: 8eb53e4846ad55916e2c5876606c00c0f2e371ac
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19763483"
---
# <a name="alternatemailbox-soap"></a>AlternateMailbox (SOAP)

El elemento **AlternateMailbox** representa un buzón de alternativo. 
  
```XML
<AlternateMailbox>
   <Type/>
   <DisplayName/>
   <LegacyDN/>
   <Server/>
   <SmtpAddress/>
</AlternateMailbox>
```

 **AlternateMailbox**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Tipo (SOAP)](type-soap.md) <br/> |Representa el tipo de buzón de correo alternativas.  <br/> |
|[DisplayName (SOAP)](displayname-soap.md) <br/> |Representa el nombre para mostrar de buzón de correo alternativas.  <br/> |
|[LegacyDN (SOAP)](legacydn-soap.md) <br/> |Representa el nombre distintivo heredado de buzón de correo alternativas.  <br/> |
|[Servidor (SOAP)](server-soap.md) <br/> |Representa el servidor de buzones alternativas.  <br/> |
|[SmtpAddress (SOAP)](smtpaddress-soap.md) <br/> |Representa la dirección SMTP del buzón de correo alternativa.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[AlternateMailboxes (SOAP)](alternatemailboxes-soap.md) <br/> |Representa una colección de buzones de correo alternativas.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también

- [AlternateMailboxCollectionSetting (SOAP)](alternatemailboxcollectionsetting-soap.md)

