---
title: InternalDomains (SmtpDomainList)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InternalDomains
api_type:
- schema
ms.assetid: 0f2cbb05-338d-4302-8871-a06e78b33f98
description: El elemento InternalDomains identifica la lista de dominios SMTP internos de la organización.
ms.openlocfilehash: f37a31f4348a7eb0024656489f249dec349bc67b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835953"
---
# <a name="internaldomains-smtpdomainlist"></a>InternalDomains (SmtpDomainList)

El elemento **InternalDomains** identifica la lista de dominios SMTP internos de la organización. 
  
```XML
<InternalDomains>
   <Domain/>
</InternalDomains>
```

 **SmtpDomainList**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Domain](domain.md) <br/> |Identifica un único dominio SMTP.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[MailTipsConfiguration (MailTipsServiceConfiguration)](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |Contiene información de configuración de servicio para el servicio de sugerencias de correo.  <br/> |
|[ProtectionRulesConfiguration](protectionrulesconfiguration.md) <br/> |Contiene información de configuración de servicio para el servicio de protección de las reglas.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Se requiere este elemento. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

