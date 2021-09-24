---
title: SecurityIdentifier
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SecurityIdentifier
api_type:
- schema
ms.assetid: f7656729-f2c9-41cc-b1ec-60f480fc4dab
description: El elemento SecurityIdentifier representa el formato de lenguaje de definición de descriptor de seguridad (SDDL) de un identificador de seguridad (SID).
ms.openlocfilehash: 803c8c0efae1ccd6356d9ce3b5aa85e1d86aa565
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521608"
---
# <a name="securityidentifier"></a>SecurityIdentifier

El **elemento SecurityIdentifier** representa el formato de lenguaje de definición de descriptor de seguridad (SDDL) de un identificador de seguridad ( [SID](sid.md)).
  
```xml
<SecurityIdentifier/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GroupIdentifier](groupidentifier.md) <br/> |Representa un único identificador de seguridad y un atributo para un grupo de objetos de Active Directory del que la cuenta es miembro.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/SerializedSecurityContext/GroupSids/GroupIdentifier[i]` <br/> |
|[RestrictedGroupIdentifier](restrictedgroupidentifier.md) <br/> |Representa el identificador de seguridad del grupo y los atributos de un grupo restringido dentro de un token de usuario.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se usa en el encabezado Protocolo simple de acceso a objetos (SOAP).
  
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

