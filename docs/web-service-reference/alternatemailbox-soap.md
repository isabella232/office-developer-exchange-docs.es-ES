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
description: El elemento AlternateMailbox representa un buzón de correo alternativo.
ms.openlocfilehash: 9019f85a373cc186cc9dadddceee3dc9d11b3854
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466160"
---
# <a name="alternatemailbox-soap"></a>AlternateMailbox (SOAP)

El elemento **AlternateMailbox** representa un buzón de correo alternativo. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Tipo (SOAP)](type-soap.md) <br/> |Representa el tipo de buzón alternativo.  <br/> |
|[DisplayName (SOAP)](displayname-soap.md) <br/> |Representa el nombre para mostrar del buzón alternativo.  <br/> |
|[LegacyDN (SOAP)](legacydn-soap.md) <br/> |Representa el nombre distintivo heredado de buzón alternativo.  <br/> |
|[Servidor (SOAP)](server-soap.md) <br/> |Representa el servidor de buzones de correo alternativo.  <br/> |
|[SmtpAddress (SOAP)](smtpaddress-soap.md) <br/> |Representa la dirección SMTP de buzón alternativa.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AlternateMailboxes (SOAP)](alternatemailboxes-soap.md) <br/> |Representa una colección de buzones de correo alternativos.  <br/> |
   
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

- [AlternateMailboxCollectionSetting (SOAP)](alternatemailboxcollectionsetting-soap.md)

