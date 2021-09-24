---
title: Reglas
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Rules
api_type:
- schema
ms.assetid: 53f59054-8f68-4eaa-be9c-ccfc9383bcf2
description: El elemento Rules contiene una matriz de reglas de protección.
ms.openlocfilehash: 492111e53c01a0848bd87c460670f35c524baf31
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517864"
---
# <a name="rules"></a>Rules

El **elemento Rules** contiene una matriz de reglas de protección. 
  
```xml
<Rules>   <Rule/></Rules>
```

 **ArrayOfProtectionRulesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Rule](rule.md) <br/> |Contiene una sola regla de protección. Este elemento puede producirse cero o más veces. Este elemento se produce cero veces cuando la organización no define reglas de protección. Se produce una o más veces si la organización define al menos una regla.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ProtectionRulesConfiguration](protectionrulesconfiguration.md) <br/> |Contiene la configuración del servicio de reglas de protección.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

