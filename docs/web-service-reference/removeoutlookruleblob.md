---
title: RemoveOutlookRuleBlob
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RemoveOutlookRuleBlob
api_type:
- schema
ms.assetid: 69614475-8bd3-4475-b988-614fe9cad8ef
description: El elemento RemoveOutlookRuleBlob indica si se debe quitar el objeto binario de la regla de Microsoft Outlook.
ms.openlocfilehash: b4202ab52bf16d1ad1546ec963cd8b9dacd2bd63
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467672"
---
# <a name="removeoutlookruleblob"></a>RemoveOutlookRuleBlob

El elemento **RemoveOutlookRuleBlob** indica si se debe quitar el objeto binario de la regla de Microsoft Outlook. 
  
[UpdateInboxRules](updateinboxrules.md)
  
[RemoveOutlookRuleBlob](removeoutlookruleblob.md)
  
```XML
<RemoveOutlookRuleBlob>true | false</RemoveOutlookRuleBlob>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[UpdateInboxRules](updateinboxrules.md) <br/> |Define una solicitud para actualizar las reglas de la bandeja de entrada en un buzón de correo en el almacén del servidor.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto de **true** indica que se debe quitar el BLOB de regla de Outlook. Un valor de texto **falso** indica que el BLOB de la regla de Outlook no se debe quitar. 
  
## <a name="remarks"></a>Comentarios

Establezca este elemento en **true** para permitir una actualización de la regla de la bandeja de entrada. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación de UpdateInboxRules](updateinboxrules-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

