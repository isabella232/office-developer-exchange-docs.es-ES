---
title: ConnectingSID
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ConnectingSID
api_type:
- schema
ms.assetid: 56d6aa52-8fa6-4773-9046-44a6f4f5d97c
description: El elemento ConnectingSID representa una cuenta que se va a suplantar cuando se usa el encabezado SOAP de ExchangeImpersonation.
ms.openlocfilehash: 21cfcfc3590ea5a8b8ca5b53dfdb403e108e37f7
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515974"
---
# <a name="connectingsid"></a>ConnectingSID

El **elemento ConnectingSID** representa una cuenta que se va a suplantar cuando se usa el encabezado SOAP de ExchangeImpersonation. 
  
- [ExchangeImpersonation](exchangeimpersonation.md) 
- [ConnectingSID](connectingsid.md)
  
```xml
<ConnectingSID>
   <PrincipalName/>
</ConnectingSID>
```

```xml
<ConnectingSID>
   <SmtpAddress/>
</ConnectingSID>
```

```xml
<ConnectingSID>
    <SID/> 
</ConnectingSID>
```

```xml
<ConnectingSID>
   <PrimarySmtpAddress/>
</ConnectingSID>
```

**ConnectingSIDType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[PrincipalName](principalname.md) <br/> |Representa el nombre principal de usuario (UPN) de la cuenta que se usará para la suplantación. Este debe ser el UPN del dominio donde existe la cuenta de usuario.  <br/> |
|[SID](sid.md) <br/> |Representa el formato de lenguaje de definición de descriptor de seguridad (SDDL) del identificador de seguridad (SID) de la cuenta que se usará para la suplantación.  <br/> |
|[PrimarySmtpAddress](primarysmtpaddress.md) <br/> |Representa la dirección principal del Protocolo simple de transferencia de correo (SMTP) de la cuenta que se usará para Exchange suplantación. Si se proporciona la dirección SMTP principal, tendrá un costo adicional de búsqueda del servicio de directorio de Active Directory para obtener el SID del usuario. Se recomienda usar el SID o UPN si están disponibles.  <br/> |
|[SmtpAddress](smtpaddress.md) <br/> |Representa la dirección del Protocolo simple de transferencia de correo (SMTP) de la cuenta que se usará para Exchange suplantación. Si se proporciona la dirección SMTP, costará una búsqueda adicional de Active Directory para obtener el SID del usuario. Se recomienda usar el SID o UPN si están disponibles.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Se usa en el encabezado SOAP de una solicitud. Cuando este elemento está presente, el autor de la llamada intenta suplantar la cuenta contenida en el **elemento ExchangeImpersonation.**  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/ExchangeImpersonation` <br/> |
   
## <a name="remarks"></a>Comentarios

La cuenta de llamada debe tener el derecho **ms-exch-suplantación** en el servidor de acceso de cliente y el **derecho ms-exch-MayImpersonate** en la base de datos de buzones de correo que contiene el buzón que se suplanta o el usuario de Active Directory o el objeto de contacto. 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Autorización de servidor a servidor en EWS](https://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

