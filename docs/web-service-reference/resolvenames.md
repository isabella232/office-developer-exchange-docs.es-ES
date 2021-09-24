---
title: ResolveNames
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ResolveNames
api_type:
- schema
ms.assetid: c85207e1-1315-443b-94ec-2b58f405076b
description: El elemento ResolveNames define una solicitud para resolver nombres ambiguos.
ms.openlocfilehash: 8fbf933593b43de656bf8731aa86cc8c8eb76bb4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514147"
---
# <a name="resolvenames"></a>ResolveNames

El **elemento ResolveNames** define una solicitud para resolver nombres ambiguos. 
  
```XML
<ResolveNames ReturnFullContactData="" SearchScope="" ContactDataShape="">
   <ParentFolderIds/>
   <UnresolvedEntry/>
</ResolveNames>
```

 **ResolveNamesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**ReturnFullContactData** <br/> |Describe si se devuelven los detalles de contacto completos de los contactos públicos para un nombre resuelto en la respuesta. Este atributo es necesario para los contactos públicos. Este valor no afecta a los contactos privados ni a las listas de distribución privadas, para las que [ItemId](itemid.md) siempre se devuelve.  <br/> |
|**SearchScope** <br/> |Identifica el orden y el ámbito de una búsqueda ResolveNames.  <br/> |
|ContactDataShape  <br/> |Identifica el conjunto de propiedades devuelto para los contactos. Este atributo se introdujo en Exchange Server 2010 Service Pack 2 (SP2).  <br/> |
   
#### <a name="returnfullcontactdata-attribute-values"></a>Valores de atributo ReturnFullContactData

|**Valor**|**Descripción**|
|:-----|:-----|
|True  <br/> |Se devuelven los detalles de contacto completos de los contactos públicos.  <br/> |
|Falso  <br/> |No se devuelven los detalles de contacto completos de los contactos públicos.  <br/> |
   
#### <a name="searchscope-attribute-values"></a>Valores de atributo SearchScope

|**Valor**|**Descripción**|
|:-----|:-----|
|ActiveDirectory  <br/> |Solo se busca en el servicio de directorio de Active Directory.  <br/> |
|ActiveDirectoryContacts  <br/> |Primero se busca en Active Directory y, a continuación, se buscan las carpetas de contacto especificadas en la [propiedad ParentFolderIds.](parentfolderids.md)  <br/> |
|Contactos  <br/> |Solo se buscan las carpetas de contacto identificadas por la [propiedad ParentFolderIds.](parentfolderids.md)  <br/> |
|ContactsActiveDirectory  <br/> |Primero se buscan las carpetas de contactos identificadas por la [propiedad ParentFolderIds](parentfolderids.md) y, a continuación, se busca en Active Directory.  <br/> |
   
#### <a name="contactdatashape-attribute-values"></a>Valores de atributo ContactDataShape

|**Valor**|**Descripción**|
|:-----|:-----|
|IdOnly  <br/> |Se devuelve la propiedad identificador del elemento de contacto.  <br/> |
|Predeterminado  <br/> |Se devuelve el conjunto predeterminado de propiedades del elemento de contacto. Para obtener más información, vea [Formas de respuesta en EWS](https://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx).  <br/> |
|AllProperties  <br/> |Se devuelve el conjunto AllProperties de propiedades de elemento de contacto. Para obtener más información, vea [Formas de respuesta en EWS](https://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx).  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ParentFolderIds](parentfolderids.md) <br/> |Contiene una matriz de identificadores de carpeta de contactos que se buscarían si el atributo **SearchScope** se establece en ActiveDirectoryContacts, Contacts o ContactsActiveDirectory. La matriz ParentFolderIds solo puede contener un único identificador de carpeta de contactos. Si el **elemento ParentFolderIds** no está presente, se busca en la carpeta Contacts predeterminada.  <br/> El identificador de carpeta se puede usar para delegar el acceso.  <br/> Las búsquedas de Active Directory se realizan mediante listas de control de acceso (ACL). Es posible que algunos usuarios no tengan los derechos para ver algunos objetos de Active Directory.  <br/> Este elemento es opcional.  <br/> |
|[UnresolvedEntry](unresolvedentry.md) <br/> |Contiene el nombre de una lista de contactos o distribución que se debe resolver.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre del esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación ResolveNames](resolvenames-operation.md)
  
[ResolveNamesType](https://msdn.microsoft.com/library/ExchangeWebServices.ResolveNamesType.aspx)
  
[ResolveNamesSearchScopeType](https://msdn.microsoft.com/library/ExchangeWebServices.ResolveNamesSearchScopeType.aspx)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


[Uso de la resolución de nombres](https://msdn.microsoft.com/library/9257fb07-89d2-46eb-b885-e2173fe6fbc1%28Office.15%29.aspx)

