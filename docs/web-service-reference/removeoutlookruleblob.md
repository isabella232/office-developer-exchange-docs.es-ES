---
title: RemoveOutlookRuleBlob
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RemoveOutlookRuleBlob
api_type:
- schema
ms.assetid: 69614475-8bd3-4475-b988-614fe9cad8ef
description: El elemento RemoveOutlookRuleBlob indica si se va a quitar el blob de Outlook microsoft.
ms.openlocfilehash: 92fd4e22ce0551c7922036e68fc0c6822a006b89
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525599"
---
# <a name="removeoutlookruleblob"></a>RemoveOutlookRuleBlob

El **elemento RemoveOutlookRuleBlob** indica si se va a quitar el blob de Outlook microsoft. 
  
[UpdateInboxRules](updateinboxrules.md)
  
[RemoveOutlookRuleBlob](removeoutlookruleblob.md)
  
```XML
<RemoveOutlookRuleBlob>true | false</RemoveOutlookRuleBlob>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[UpdateInboxRules](updateinboxrules.md) <br/> |Define una solicitud para actualizar las reglas de la Bandeja de entrada en un buzón en el almacén del servidor.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto **de true** indica que se debe quitar Outlook blob de regla. Un valor de texto **de false** indica que el blob Outlook regla no debe quitarse. 
  
## <a name="remarks"></a>Comentarios

Establezca este elemento en **true para** permitir una actualización de regla de bandeja de entrada. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación de UpdateInboxRules](updateinboxrules-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

