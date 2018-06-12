---
title: ResolveNames
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResolveNames
api_type:
- schema
ms.assetid: c85207e1-1315-443b-94ec-2b58f405076b
description: El elemento ResolveNames define una solicitud para resolver nombres ambiguos.
ms.openlocfilehash: e97b6e78d99cf8ffa3d680907916882d40963f59
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837172"
---
# <a name="resolvenames"></a>ResolveNames

El elemento **ResolveNames** define una solicitud para resolver nombres ambiguos. 
  
```XML
<ResolveNames ReturnFullContactData="" SearchScope="" ContactDataShape="">
   <ParentFolderIds/>
   <UnresolvedEntry/>
</ResolveNames>
```

 **ResolveNamesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**ReturnFullContactData** <br/> |Describe si se devuelven los detalles de contacto para los contactos para un nombre resuelto en la respuesta. Este atributo es necesario para los contactos. Este valor no afecta a los contactos privados y listas de distribución privadas, para que siempre se devuelve [ItemId](itemid.md) .  <br/> |
|**SearchScope** <br/> |Identifica la orden y el ámbito de una búsqueda ResolveNames.  <br/> |
|ContactDataShape  <br/> |Identifica la propiedad establecida devuelta para los contactos. Este atributo se introdujo en Exchange Server 2010 Service Pack 2 (SP2).  <br/> |
   
#### <a name="returnfullcontactdata-attribute-values"></a>Valores de atributo de ReturnFullContactData

|**Valor**|**Descripción**|
|:-----|:-----|
|True  <br/> |Se devuelven detalles de contacto para los contactos.  <br/> |
|False  <br/> |No se devuelven datos de contacto completos para los contactos.  <br/> |
   
#### <a name="searchscope-attribute-values"></a>Valores de atributo de SearchScope

|**Valor**|**Descripción**|
|:-----|:-----|
|ActiveDirectory  <br/> |Se busca en sólo el servicio de directorio de Active Directory.  <br/> |
|ActiveDirectoryContacts  <br/> |Active Directory se busca en primer lugar y, a continuación, se buscan las carpetas de contactos que se especifican en la propiedad [ParentFolderIds](parentfolderids.md) .  <br/> |
|Contacts  <br/> |Se buscan sólo las carpetas de contactos que se identifican mediante la propiedad [ParentFolderIds](parentfolderids.md) .  <br/> |
|ContactsActiveDirectory  <br/> |Carpetas de contactos que se identifican mediante la propiedad [ParentFolderIds](parentfolderids.md) se buscan en primer lugar y, a continuación, se busca en Active Directory.  <br/> |
   
#### <a name="contactdatashape-attribute-values"></a>Valores de atributo de ContactDataShape

|**Valor**|**Descripción**|
|:-----|:-----|
|IdOnly  <br/> |Se devuelve la propiedad de identificador de elemento de contacto.  <br/> |
|Default  <br/> |Se devuelve el conjunto predeterminado de propiedades de elemento de contacto. Para obtener más información, vea [las formas de respuesta de EWS](http://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx).  <br/> |
|AllProperties  <br/> |Se devuelven el conjunto de AllProperties de propiedades de elemento de contacto. Para obtener más información, vea [las formas de respuesta de EWS](http://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx).  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[ParentFolderIds](parentfolderids.md) <br/> |Contiene una matriz de identificadores de la carpeta de contactos que se debería buscar si se establece el atributo **SearchScope** en ActiveDirectoryContacts, contactos o ContactsActiveDirectory. La matriz de ParentFolderIds sólo puede contener un identificador único de carpeta de contactos. Si el elemento **ParentFolderIds** no está presente, se busca en la carpeta Contactos predeterminada.  <br/> El identificador de la carpeta se puede usar para el acceso de delegado.  <br/> Búsquedas en Active Directory se realizan mediante el uso de listas de control de acceso (ACL). Algunos usuarios no puedan tener los derechos para ver algunos objetos de Active Directory.  <br/> Este elemento es opcional.  <br/> |
|[UnresolvedEntry](unresolvedentry.md) <br/> |Contiene el nombre de un contacto o lista de distribución para resolver.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Observaciones

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación ResolveNames](resolvenames-operation.md)
  
[ResolveNamesType](https://msdn.microsoft.com/library/ExchangeWebServices.ResolveNamesType.aspx)
  
[ResolveNamesSearchScopeType](https://msdn.microsoft.com/library/ExchangeWebServices.ResolveNamesSearchScopeType.aspx)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


[Uso de la resolución de nombres](http://msdn.microsoft.com/library/9257fb07-89d2-46eb-b885-e2173fe6fbc1%28Office.15%29.aspx)

