---
title: SID
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SID
api_type:
- schema
ms.assetid: 2f33b29b-163b-4106-a74d-6fb76ec38951
description: El elemento SID representa el formato de lenguaje de definición de descriptor de seguridad (SDDL) del identificador de seguridad (SID) para que la cuenta use para suplantar o delegar el acceso.
ms.openlocfilehash: 436f284b59d5146b481a25b7b0986db4aeee67ce
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59547060"
---
# <a name="sid"></a>SID

El **elemento SID** representa el formato de lenguaje de definición de descriptor de seguridad (SDDL) del identificador de seguridad (SID) para que la cuenta use para suplantar o delegar el acceso. 
  
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
|[ConnectingSID](connectingsid.md) <br/> |Representa una cuenta que se debe suplantar al usar el encabezado SOAP de ExchangeImpersonation.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[UserId](userid.md) <br/> |Identifica un usuario delegado o un usuario con permisos de acceso a carpetas.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto es una representación de cadena de un SID.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que se ejecuta Exchange Server con el rol de servidor acceso de cliente instalado.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

