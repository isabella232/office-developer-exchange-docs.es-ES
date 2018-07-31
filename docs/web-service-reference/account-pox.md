---
title: Account (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 488fdbdc-e9d9-4301-91ab-e22eb42e549e
description: El elemento de cuenta especifica la configuración de cuenta para el usuario o contiene las respuestas de error.
ms.openlocfilehash: 6cd87e678b3a524a69f6dca4d6999a3cff22fa57
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353346"
---
# <a name="account-pox"></a>Account (POX)

El elemento de **cuenta** especifica la configuración de cuenta para el usuario o contiene las respuestas de error. 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[AccountType (POX)](accounttype-pox.md) <br/> |Representa el tipo de cuenta.  <br/> |
|[Action (POX)](action-pox.md) <br/> |Proporciona información que se utiliza para determinar si se requiere otra solicitud de detección automática para devolver la información de configuración de usuario.  <br/> |
|[MicrosoftOnline (POX)](microsoftonline-pox.md) <br/> |Contiene un valor que indica si el buzón del usuario está hospedado en Exchange Online o Exchange Online como parte de Office 365.  <br/> |
|[RedirectUrl (POX)](redirecturl-pox.md) <br/> |Contiene la dirección URL del equipo que ejecuta Exchange Server que tiene el rol de servidor de acceso de cliente instalado que se debe usar para obtener la configuración de detección automática.  <br/> |
|[RedirectAddr (POX)](redirectaddr-pox.md) <br/> |Especifica la dirección de correo electrónico que se debe usar para una solicitud de detección automática subsiguiente.  <br/> |
|[Image (POX)](image-pox.md) <br/> |Contiene la ruta de acceso de una imagen que se usa para personalizar la marca de la experiencia de configuración.  <br/> |
|[ServiceHome (POX)](servicehome-pox.md) <br/> |Contiene la dirección URL de la página principal del proveedor de servicios Internet (ISP).  <br/> |
|[Protocol (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar a un cliente con el servidor de acceso de cliente.  <br/> |
|[PublicFolderInformation (POX)](publicfolderinformation-pox.md) <br/> |Contiene información que los clientes pueden usar para enviar una solicitud de detección automática para detectar información de carpetas públicas para el usuario.  <br/> |
|[Error (POX)](error-pox.md) <br/> |Contiene una respuesta de error de detección automática.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Response (POX)](response-pox.md) <br/> |Contiene la respuesta del servicio Detección automática.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos de Autodiscover XML POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

