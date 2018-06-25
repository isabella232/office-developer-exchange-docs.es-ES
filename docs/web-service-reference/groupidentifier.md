---
title: GroupIdentifier
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupIdentifier
api_type:
- schema
ms.assetid: bdc6fc1e-4979-42da-a35b-e3017988c7d3
description: El elemento GroupIdentifier representa un identificador de seguridad único y un atributo para un grupo de objetos de servicio de directorio de Active Directory de que la cuenta es miembro.
ms.openlocfilehash: d73d72979762238ca09496cfbd6636b4ff44a969
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835767"
---
# <a name="groupidentifier"></a>GroupIdentifier

El elemento **GroupIdentifier** representa un identificador de seguridad único y un atributo para un grupo de objetos de servicio de directorio de Active Directory de que la cuenta es miembro. 
  
```xml
<GroupIdentifier>
   <SecurityIdentifier/>
</GroupIdentifier>
```

 **SidAndAttributesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**Attributes** <br/> |Contiene los atributos de grupo.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[SecurityIdentifier](securityidentifier.md) <br/> |Representa el formato de idioma (SDDL) de definición de descriptor de seguridad de un identificador de seguridad ([SID](sid.md)) que representa el grupo.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[GroupSids](groupsids.md) <br/> |Representa una colección de identificadores de seguridad de objeto de grupo de Active Directory que componen un símbolo (token) de cuenta para la serialización de token. No se admite la serialización de token.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

