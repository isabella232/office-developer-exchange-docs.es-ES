---
title: SID
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SID
api_type:
- schema
ms.assetid: 2f33b29b-163b-4106-a74d-6fb76ec38951
description: El elemento SID representa el formato de lenguaje de definición de descriptores de seguridad (SDDL) del identificador de seguridad (SID) de la cuenta que se va a usar para la suplantación o el acceso delegado.
ms.openlocfilehash: 0e3f740e9a056f7c0042049d97757b5f2d3c441d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468050"
---
# <a name="sid"></a>SID

El elemento **SID** representa el formato de lenguaje de definición de descriptores de seguridad (SDDL) del identificador de seguridad (SID) de la cuenta que se va a usar para la suplantación o el acceso delegado. 
  
```xml
<SID/>
```

 **SIDType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ConnectingSID](connectingsid.md) <br/> |Representa una cuenta que se va a suplantar al usar el encabezado SOAP ExchangeImpersonation.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[UserId](userid.md) <br/> |Identifica un usuario delegado o un usuario con permisos de acceso a la carpeta.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto es una representación de cadena de un SID.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con el rol de servidor acceso de clientes instalado.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

