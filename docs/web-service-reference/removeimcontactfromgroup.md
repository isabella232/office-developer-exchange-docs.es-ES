---
title: RemoveImContactFromGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a62b0640-9800-45a6-a297-2105ff36881e
description: El elemento RemoveImContactFromGroup define una solicitud para quitar un contacto de mensajería instantánea de un grupo de mensajería instantánea.
ms.openlocfilehash: 379994ad5832b05e9f7da61d752f7660a6eec5ad
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466965"
---
# <a name="removeimcontactfromgroup"></a>RemoveImContactFromGroup

El elemento **RemoveImContactFromGroup** define una solicitud para quitar un contacto de mensajería instantánea de un grupo de mensajería instantánea. 
  
```XML
<RemoveImContactFromGroup>
   <ContactId/>
   <GroupId/>
</RemoveImContactFromGroup>
```

 **RemoveImContactFromGroupType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

[ContactId](contactid.md)  |  [GROUPID](groupid.md)
  
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> ||
   

