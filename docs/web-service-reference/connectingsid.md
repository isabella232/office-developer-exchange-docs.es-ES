---
title: ConnectingSID
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConnectingSID
api_type:
- schema
ms.assetid: 56d6aa52-8fa6-4773-9046-44a6f4f5d97c
description: El elemento ConnectingSID representa una cuenta que se suplanta cuando se usa el encabezado SOAP ExchangeImpersonation.
ms.openlocfilehash: f4edf63f129fc769f4a2d710a505b40da4057fab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459282"
---
# <a name="connectingsid"></a>ConnectingSID

El elemento **ConnectingSID** representa una cuenta que se suplanta cuando se usa el encabezado SOAP ExchangeImpersonation. 
  
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

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[PrincipalName](principalname.md) <br/> |Representa el nombre principal de usuario (UPN) de la cuenta que se va a usar para la suplantación. Debe ser el UPN del dominio en el que se encuentra la cuenta de usuario.  <br/> |
|[SID](sid.md) <br/> |Representa el formato de lenguaje de definición de descriptores de seguridad (SDDL) del identificador de seguridad (SID) de la cuenta que se va a usar para la suplantación.  <br/> |
|[PrimarySmtpAddress](primarysmtpaddress.md) <br/> |Representa la dirección de Protocolo simple de transferencia de correo (SMTP) principal de la cuenta que se va a usar para la suplantación de Exchange. Si se proporciona la dirección SMTP principal, la búsqueda del servicio de directorio de Active Directory adicional será más costosa para obtener el SID del usuario. Le recomendamos que use el SID o el UPN si están disponibles.  <br/> |
|[SmtpAddress](smtpaddress.md) <br/> |Representa la dirección del Protocolo simple de transferencia de correo (SMTP) de la cuenta que se va a usar para la suplantación de Exchange. Si se proporciona la dirección SMTP, el costo de la búsqueda en Active Directory será mayor para obtener el SID del usuario. Le recomendamos que use el SID o el UPN si están disponibles.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Se usa en el encabezado SOAP de una solicitud. Cuando este elemento está presente, el autor de la llamada está intentando suplantar la cuenta contenida en el elemento **ExchangeImpersonation** .  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/ExchangeImpersonation` <br/> |
   
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

- [Autorización de servidor a servidor en EWS](https://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

