---
title: OldItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OldItemId
api_type:
- schema
ms.assetid: fb57deee-9cc3-4730-9805-ff34f39e3ab7
description: El elemento OldItemId contiene el identificador único del elemento que se ha copiado o movido.
ms.openlocfilehash: 9fab14478ffbb2dd8ad013d59520af943584f2eb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467469"
---
# <a name="olditemid"></a>OldItemId

El elemento **OldItemId** contiene el identificador único del elemento que se ha copiado o movido. 
  
```xml
<OldItemId Id="" ChangeKey=""/>
```

 **ItemIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**Id** <br/> |Contiene una cadena que identifica un elemento en el almacén de Exchange. Este atributo es obligatorio.  <br/> |
|**ChangeKey** <br/> |Contiene una cadena que identifica una versión de un elemento identificado por el atributo id. Este atributo es opcional. Use este atributo para asegurarse de que se usa la versión correcta de un elemento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CopiedEvent](copiedevent.md) <br/> |Representa un evento en el que se copia un elemento o una carpeta.  <br/> |
|[MovedEvent](movedevent.md) <br/> |Representa un evento en el que se mueve un elemento o una carpeta de una carpeta principal a otra carpeta principal.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación subscribe](subscribe-operation.md)
  
[Operación GetEvents](getevents-operation.md)
  
[Operación unsubscribe](unsubscribe-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

