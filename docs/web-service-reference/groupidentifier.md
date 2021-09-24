---
title: GroupIdentifier
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GroupIdentifier
api_type:
- schema
ms.assetid: bdc6fc1e-4979-42da-a35b-e3017988c7d3
description: El elemento GroupIdentifier representa un único identificador de seguridad y un atributo para un grupo de objetos de servicio de directorio de Active Directory del que la cuenta es miembro.
ms.openlocfilehash: c96d0ca673d9b488266f08abbbd6546aaeb9f5a9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59533162"
---
# <a name="groupidentifier"></a>GroupIdentifier

El **elemento GroupIdentifier** representa un único identificador de seguridad y un atributo para un grupo de objetos de servicio de directorio de Active Directory del que la cuenta es miembro. 
  
```xml
<GroupIdentifier>
   <SecurityIdentifier/>
</GroupIdentifier>
```

 **SidAndAttributesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**Atributos** <br/> |Contiene atributos de grupo.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SecurityIdentifier](securityidentifier.md) <br/> |Representa el formato de lenguaje de definición de descriptor de seguridad (SDDL) de un identificador de seguridad ([SID](sid.md)) que representa el grupo.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GroupSids](groupsids.md) <br/> |Representa una colección de identificadores de seguridad de objetos de grupo de Active Directory que representan un token de cuenta para la serialización de tokens. No se admite la serialización de tokens.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

