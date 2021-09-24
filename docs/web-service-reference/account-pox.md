---
title: Account (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 488fdbdc-e9d9-4301-91ab-e22eb42e549e
description: El elemento Account especifica la configuración de la cuenta para el usuario o contiene respuestas de error.
ms.openlocfilehash: 89799ab62a2aa4945b0e8f3209ab1fbc7d2fa2e6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59534056"
---
# <a name="account-pox"></a>Account (POX)

El **elemento Account** especifica la configuración de la cuenta para el usuario o contiene respuestas de error. 
  
- [AutoDiscover (POX)](autodiscover-pox.md)
- [Response (POX)](response-pox.md)
- [Account (POX)](account-pox.md)
  
```XML
<Account>
   <AccountType/>
   <Action/>
   <MicrosoftOnline/>
   <RedirectURL/>
   <RedirectAddr/>
   <Image/>
   <ServiceHome/>
   <Protocol/>
   <PublicFolderInformation/>
</Account>
```

<br/>

```XML
<Account> 
    <Error/> 
</Account>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AccountType (POX)](accounttype-pox.md) <br/> |Representa el tipo de cuenta.  <br/> |
|[Action (POX)](action-pox.md) <br/> |Proporciona información que se usa para determinar si es necesaria otra solicitud de detección automática para devolver la información de configuración del usuario.  <br/> |
|[MicrosoftOnline (POX)](microsoftonline-pox.md) <br/> |Contiene un valor que indica si el buzón del usuario está hospedado en Exchange Online o Exchange Online como parte de Office 365.  <br/> |
|[RedirectUrl (POX)](redirecturl-pox.md) <br/> |Contiene la dirección URL del equipo que ejecuta Exchange Server que tiene instalado el rol de servidor Acceso de cliente que se debe usar para obtener la configuración de detección automática.  <br/> |
|[RedirectAddr (POX)](redirectaddr-pox.md) <br/> |Especifica la dirección de correo electrónico que se debe usar para una solicitud de detección automática posterior.  <br/> |
|[Image (POX)](image-pox.md) <br/> |Contiene la ruta de acceso de una imagen que se usa para marcar la experiencia de configuración.  <br/> |
|[ServiceHome (POX)](servicehome-pox.md) <br/> |Contiene la dirección URL de la página principal del proveedor de servicios de Internet (ISP).  <br/> |
|[Protocol (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al servidor de acceso de cliente.  <br/> |
|[PublicFolderInformation (POX)](publicfolderinformation-pox.md) <br/> |Contiene información que los clientes pueden usar para enviar una solicitud de detección automática para detectar información de carpetas públicas para el usuario.  <br/> |
|[Error (POX)](error-pox.md) <br/> |Contiene una respuesta de error de detección automática.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Response (POX)](response-pox.md) <br/> |Contiene la respuesta del servicio de detección automática.  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

