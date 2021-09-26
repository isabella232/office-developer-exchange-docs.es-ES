---
title: DocumentSharingLocation (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 21bc388c-33be-422b-a89d-30ade0fae8f1
description: El elemento DocumentSharingLocation contiene información de ubicación y metadatos para una ubicación de uso compartido de documentos.
ms.openlocfilehash: f4011dfb846d314d926ba644f4ddc2176283008a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541486"
---
# <a name="documentsharinglocation-soap"></a>DocumentSharingLocation (SOAP)

El **elemento DocumentSharingLocation** contiene información de ubicación y metadatos para una ubicación de uso compartido de documentos. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ServiceUrl (SOAP)](serviceurl-soap.md) <br/> |Representa la dirección URL del servicio web de uso compartido de documentos.  <br/> |
|[LocationUrl (SOAP)](locationurl-soap.md) <br/> |Representa la dirección URL de la ubicación de uso compartido de documentos.  <br/> |
|[DisplayName (SOAP)](displayname-soap.md) <br/> |Representa el nombre de la ubicación de uso compartido de documentos que se usará en la interfaz de usuario.  <br/> |
|[SupportedFileExtensions (SOAP)](supportedfileextensions-soap.md) <br/> |Representa las extensiones de archivo que se pueden almacenar en la ubicación de uso compartido de documentos.  <br/> |
|[ExternalAccessAllowed (SOAP)](externalaccessallowed-soap.md) <br/> |Indica si la ubicación de uso compartido de documentos está disponible para las conexiones externas.  <br/> |
|[AnonymousAccessAllowed (SOAP)](anonymousaccessallowed-soap.md) <br/> |Indica si el acceso a la ubicación de uso compartido requiere un usuario autenticado.  <br/> |
|[CanModifyPermissions (SOAP)](canmodifypermissions-soap.md) <br/> |Indica si el usuario puede modificar los permisos de acceso a la ubicación de uso compartido de documentos.  <br/> |
|[IsDefault (SOAP)](isdefault-soap.md) <br/> |Indica si la ubicación de uso compartido de documentos es la ubicación de uso compartido predeterminada del usuario.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DocumentSharingLocations (SOAP)](documentsharinglocations-soap.md) <br/> |Contiene una lista de ubicaciones de uso compartido de documentos y metadatos.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguna.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)
- [Referencia del servicio web de Detección automática para Exchange](autodiscover-web-service-reference-for-exchange.md)
- [Elementos XML de detección automática soap para Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

