---
title: DocumentSharingLocation (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21bc388c-33be-422b-a89d-30ade0fae8f1
description: El elemento DocumentSharingLocation contiene la ubicación y la información de metadatos de un documento de ubicación de uso compartido.
ms.openlocfilehash: d258efecb46d570138c7c2c78ed9d2fa9a275103
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764256"
---
# <a name="documentsharinglocation-soap"></a>DocumentSharingLocation (SOAP)

El elemento **DocumentSharingLocation** contiene la ubicación y la información de metadatos de un documento de ubicación de uso compartido. 
  
```XML
<DocumentSharingLocation>
   <ServiceUrl />
   <LocationUrl />
   <DisplayName />
   <SupportedFileExtensions />
   <ExternalAccessAllowed />
   <AnonymousAccessAllowed />
   <CanModifyPermissions />
   <IsDefault />
</DocumentSharingLocation>
```

 **DocumentSharingLocation**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[ServiceUrl (SOAP)](serviceurl-soap.md) <br/> |Representa la dirección URL del servicio web de uso compartido de documento.  <br/> |
|[LocationUrl (SOAP)](locationurl-soap.md) <br/> |Representa la dirección URL de la ubicación de uso compartido de documentos.  <br/> |
|[DisplayName (SOAP)](displayname-soap.md) <br/> |Representa el nombre del documento de ubicación que se usará en la interfaz de usuario de uso compartido.  <br/> |
|[SupportedFileExtensions (SOAP)](supportedfileextensions-soap.md) <br/> |Representa las extensiones de archivo que se pueden almacenar en la ubicación de uso compartido de documentos.  <br/> |
|[ExternalAccessAllowed (SOAP)](externalaccessallowed-soap.md) <br/> |Indica si el documento en la ubicación de uso compartido está disponible a fuera de las conexiones.  <br/> |
|[AnonymousAccessAllowed (SOAP)](anonymousaccessallowed-soap.md) <br/> |Indica si el acceso a la ubicación de uso compartido requiere un usuario autenticado.  <br/> |
|[CanModifyPermissions (SOAP)](canmodifypermissions-soap.md) <br/> |Indica si el usuario puede modificar los permisos de acceso a la ubicación de uso compartido de documentos.  <br/> |
|[IsDefault (SOAP)](isdefault-soap.md) <br/> |Indica si el documento en la ubicación de uso compartido es la predeterminada del usuario ubicación de uso compartido.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[DocumentSharingLocations (SOAP)](documentsharinglocations-soap.md) <br/> |Contiene una lista de uso compartido de las ubicaciones y los metadatos del documento.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)
- [Referencia de servicio web de detección automática para Exchange](autodiscover-web-service-reference-for-exchange.md)
- [Elementos de Autodiscover XML SOAP para Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

