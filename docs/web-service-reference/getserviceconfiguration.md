---
title: GetServiceConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetServiceConfiguration
api_type:
- schema
ms.assetid: acbb29e4-d853-4302-8e32-7018775d54e4
description: El elemento GetServiceConfiguration define una solicitud de GetServiceConfiguration.
ms.openlocfilehash: e9357a9e3be22e129c4910c01231f9dbd22a2dbe
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457875"
---
# <a name="getserviceconfiguration"></a>GetServiceConfiguration

El elemento **GetServiceConfiguration** define una solicitud de GetServiceConfiguration. 
  
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

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Acciones](actingas.md) <br/> |Identifica quién envía el autor de la llamada. Este elemento es opcional. Si este elemento no está presente, se supone que el usuario autenticado es el remitente. El elemento **actual** debe incluirse para solicitar sugerencias de remitente. Se puede devolver un error ErrorInvalidArgument en una respuesta si falta el elemento **actuaas** , no incluye un tipo de enrutamiento, no incluye una dirección de correo electrónico, contiene una dirección de correo electrónico no válida, no se resuelve como un usuario de los servicios de dominio de Active Directory (AD DS) o se resuelve en varios usuarios en AD DS.  <br/> |
|[RequestedConfiguration](requestedconfiguration.md) <br/> |Contiene las configuraciones de servicio solicitadas. Se requiere este elemento.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguna.
  
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

