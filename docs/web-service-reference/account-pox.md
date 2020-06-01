---
title: Cuenta (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 488fdbdc-e9d9-4301-91ab-e22eb42e549e
description: El elemento Account especifica la configuración de la cuenta para el usuario o contiene respuestas de error.
ms.openlocfilehash: ffd8ebe4b7bd9d4b3f6a9b42fc557ac6189a068d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462321"
---
# <a name="account-pox"></a>Cuenta (POX)

El elemento **account** especifica la configuración de la cuenta para el usuario o contiene respuestas de error. 
  
- [Detección automática (POX)](autodiscover-pox.md)
- [Respuesta (POX)](response-pox.md)
- [Cuenta (POX)](account-pox.md)
  
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

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AccountType (POX)](accounttype-pox.md) <br/> |Representa el tipo de cuenta.  <br/> |
|[Acción (POX)](action-pox.md) <br/> |Proporciona información que se usa para determinar si se requiere otra solicitud de detección automática para devolver la información de configuración del usuario.  <br/> |
|[MicrosoftOnline (POX)](microsoftonline-pox.md) <br/> |Contiene un valor que indica si el buzón del usuario está hospedado en Exchange online o Exchange online como parte de Office 365.  <br/> |
|[RedirectUrl (POX)](redirecturl-pox.md) <br/> |Contiene la dirección URL del equipo que ejecuta Exchange Server y que tiene instalado el rol de servidor acceso de clientes que se debe usar para obtener la configuración de detección automática.  <br/> |
|[RedirectAddr (POX)](redirectaddr-pox.md) <br/> |Especifica la dirección de correo electrónico que se debe usar para una solicitud de detección automática posterior.  <br/> |
|[Imagen (POX)](image-pox.md) <br/> |Contiene la ruta de acceso de una imagen que se usa para personalizar la experiencia de configuración.  <br/> |
|[ServiceHome (POX)](servicehome-pox.md) <br/> |Contiene la dirección URL de la Página principal del proveedor de servicios de Internet (ISP).  <br/> |
|[Protocolo (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al servidor de acceso de cliente.  <br/> |
|[PublicFolderInformation (POX)](publicfolderinformation-pox.md) <br/> |Contiene información que los clientes pueden usar para enviar una solicitud de detección automática para detectar la información de las carpetas públicas del usuario.  <br/> |
|[Error (POX)](error-pox.md) <br/> |Contiene una respuesta de error de detección automática.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Respuesta (POX)](response-pox.md) <br/> |Contiene la respuesta del servicio Detección automática.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

