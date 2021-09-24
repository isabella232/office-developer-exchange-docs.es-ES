---
title: ExchangeImpersonation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ExchangeImpersonation
api_type:
- schema
ms.assetid: d8cbac49-47d0-4745-a2a7-545d33f8da93
description: El elemento ExchangeImpersonation se usa en el encabezado SOAP de una solicitud. Cuando este elemento está presente, el autor de la llamada intenta suplantar la cuenta contenida en el elemento ExchangeImpersonation.
ms.openlocfilehash: 88a0ae18a869c14b9ae3ef2eb3cdfc189c8c60ea
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59530769"
---
# <a name="exchangeimpersonation"></a>ExchangeImpersonation

El **elemento ExchangeImpersonation** se usa en el encabezado SOAP de una solicitud. Cuando este elemento está presente, el autor de la llamada intenta suplantar la cuenta contenida en el **elemento ExchangeImpersonation.** 
  
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

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ConnectingSID](connectingsid.md) <br/> |Representa una cuenta que se va a suplantar cuando se usa el encabezado SOAP de ExchangeImpersonation.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

La cuenta de llamada debe tener el derecho de suplantación **ms-exch-en** el servidor de acceso de cliente y el **derecho ms-exch-MayImpersonate** en la base de datos de buzones de correo que contiene el buzón que se suplanta o el objeto User/Contact de Active Directory. 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Autorización de servidor a servidor en EWS](https://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

