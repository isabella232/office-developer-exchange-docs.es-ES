---
title: ExchangeImpersonation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExchangeImpersonation
api_type:
- schema
ms.assetid: d8cbac49-47d0-4745-a2a7-545d33f8da93
description: El elemento ExchangeImpersonation se usa en el encabezado SOAP de una solicitud. Cuando este elemento está presente, el autor de la llamada está intentando suplantar la cuenta contenida en el elemento ExchangeImpersonation.
ms.openlocfilehash: 188219d95453dc45378c6ca65ab93c2de7db4eac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463352"
---
# <a name="exchangeimpersonation"></a>ExchangeImpersonation

El elemento **ExchangeImpersonation** se usa en el encabezado SOAP de una solicitud. Cuando este elemento está presente, el autor de la llamada está intentando suplantar la cuenta contenida en el elemento **ExchangeImpersonation** . 
  
[ExchangeImpersonation](exchangeimpersonation.md)
  
```xml
<ExchangeImpersonation>
   <ConnectingSID/>
</ExchangeImpersonation>
```

 **ExchangeImpersonationType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ConnectingSID](connectingsid.md) <br/> |Representa una cuenta que se va a suplantar cuando se usa el encabezado SOAP ExchangeImpersonation.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

La cuenta de llamada debe tener el derecho **MS-Exch-Impersonation** en el servidor de acceso de cliente y el derecho **MS-Exch-MayImpersonate** en la base de datos de buzones de correo que contiene el buzón de correo para la suplantación o el objeto de contacto o de usuario de Active Directory. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Autorización de servidor a servidor en EWS](https://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

