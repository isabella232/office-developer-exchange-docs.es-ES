---
title: GetUserSettingsRequest (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 832a9211-d2d5-4a49-bcb3-1dc6dc3904ed
description: El elemento GetUserSettingsRequest representa una solicitud para recuperar la configuración especificada para uno o varios usuarios.
ms.openlocfilehash: ccbcd67d4fdcb98be08acfecbf2ae066a91d65d2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59547396"
---
# <a name="getusersettingsrequest-soap"></a>GetUserSettingsRequest (SOAP)

El **elemento GetUserSettingsRequest** representa una solicitud para recuperar la configuración especificada para uno o varios usuarios. 
  
```XML
<GetUserSettingsRequest>
   <Users/>
   <RequestedSettings/>
   <RequestedVersion/>
</GetUserSettingsRequest>
```

 **GetUserSettingsRequest**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Users (SOAP)](users-soap.md) <br/> |Representa una colección de direcciones de correo electrónico de los usuarios para los que se debe recuperar la configuración.  <br/> |
|[RequestedSettings (SOAP)](requestedsettings-soap.md) <br/> |Contiene los nombres de las opciones de configuración solicitadas.  <br/> |
|[RequestedVersion (SOAP)](requestedversion-soap.md) <br/> |Especifica la versión de servidor específica que el proveedor desea usar.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguna.
  
## <a name="text-value"></a>Valor de texto

Ninguna.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Consulte también



[Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)

