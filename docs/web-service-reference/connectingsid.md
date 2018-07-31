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
description: El elemento ConnectingSID representa una cuenta para suplantar a cuando se usa el encabezado SOAP ExchangeImpersonation.
ms.openlocfilehash: a30f11721506989a84f52dd04c328974f4483956
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354340"
---
# <a name="connectingsid"></a>ConnectingSID

El elemento **ConnectingSID** representa una cuenta para suplantar a cuando se usa el encabezado SOAP ExchangeImpersonation. 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[PrincipalName](principalname.md) <br/> |Representa el nombre principal de usuario (UPN) de la cuenta a utilizar para la suplantación. Debe ser el UPN para el dominio donde se encuentra la cuenta de usuario.  <br/> |
|[SID](sid.md) <br/> |Representa el formulario de idioma (SDDL) de definición de descriptor de seguridad del identificador de seguridad (SID) para que la cuenta a utilizar para la suplantación.  <br/> |
|[PrimarySmtpAddress](primarysmtpaddress.md) <br/> |Representa la dirección de Protocolo Simple de transferencia de correo (SMTP) principal de la cuenta que se usará para la suplantación de Exchange. Si se proporciona la dirección SMTP principal, costo una búsqueda de servicio de directorio de Active Directory adicional con el fin de obtener al SID del usuario. Se recomienda usar el SID o el UPN si están disponibles.  <br/> |
|[SmtpAddress](smtpaddress.md) <br/> |Representa la dirección de Protocolo Simple de transferencia de correo (SMTP) de la cuenta que se usará para la suplantación de Exchange. Si se proporciona la dirección SMTP, costo una búsqueda de Active Directory adicional con el fin de obtener al SID del usuario. Se recomienda usar el SID o el UPN si están disponibles.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Se usa en el encabezado SOAP de una solicitud. Cuando este elemento está presente, el autor de la llamada está intentando suplantar la cuenta que está incluida dentro del elemento **ExchangeImpersonation** .  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/ExchangeImpersonation` <br/> |
   
## <a name="remarks"></a>Comentarios

La cuenta que realiza la llamada debe tener la **ms-exch-impersonation** derecha en el servidor de acceso de cliente y el **ms-exch-MayImpersonate** derecho en ya sea la base de datos de buzón de correo que contiene el buzón de correo para suplantar o el usuario de Active Directory o contacto objeto. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Autorización de servidor a servidor en EWS](http://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

