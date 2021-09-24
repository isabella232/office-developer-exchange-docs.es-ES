---
title: GetServiceConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetServiceConfiguration
api_type:
- schema
ms.assetid: acbb29e4-d853-4302-8e32-7018775d54e4
description: El elemento GetServiceConfiguration define una solicitud GetServiceConfiguration.
ms.openlocfilehash: fdc4fd84c658dd0cd2ecabe7fefc06113bca173a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59533437"
---
# <a name="getserviceconfiguration"></a>GetServiceConfiguration

El **elemento GetServiceConfiguration** define una solicitud GetServiceConfiguration. 
  
```XML
<GetServiceConfiguration>
   <ActingAs/>
   <RequestedConfiguration/>
</GetServiceConfiguration>
```

 **GetServiceConfigurationType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ActingAs](actingas.md) <br/> |Identifica a quién envía el autor de la llamada. Este elemento es opcional. Si este elemento no está presente, se supone que el usuario autenticado es el remitente. El **elemento ActingAs** debe incluirse para solicitar sugerencias de remitente. Un error ErrorInvalidArgument se puede devolver en una respuesta si falta el elemento **ActingAs,** no incluye un tipo de enrutamiento, no incluye una dirección de correo electrónico, contiene una dirección de correo electrónico no válida, no resuelve a un usuario de Servicios de dominio de Active Directory (AD DS) o resuelve a varios usuarios en AD DS.  <br/> |
|[RequestedConfiguration](requestedconfiguration.md) <br/> |Contiene las configuraciones de servicio solicitadas. Se requiere este elemento.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

