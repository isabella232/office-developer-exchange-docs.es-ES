---
title: UpdateInboxRules
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UpdateInboxRules
api_type:
- schema
ms.assetid: d220064f-ff4d-4537-8077-adf94f2cbdbd
description: El elemento UpdateInboxRules define una solicitud para actualizar las reglas de la Bandeja de entrada en un buzón del almacén de servidores.
ms.openlocfilehash: 823763efc9f9dfe621ccf05356f7e0f3c7bace14
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541716"
---
# <a name="updateinboxrules"></a>UpdateInboxRules

El **elemento UpdateInboxRules** define una solicitud para actualizar las reglas de la Bandeja de entrada en un buzón del almacén de servidores. 
  
```XML
<UpdateInboxRules>
   <MailboxSmtpAddress/>
   <RemoveOutlookRuleBlob/>
   <Operations/>
</UpdateInboxRules>
```

 **UpdateInboxRulesRequestType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MailboxSmtpAddress](mailboxsmtpaddress.md) <br/> |Representa la dirección SMTP del usuario cuyas reglas de bandeja de entrada deben crearse, modificarse o eliminarse.  <br/> |
|[RemoveOutlookRuleBlob](removeoutlookruleblob.md) <br/> |Indica si se va a quitar el blob de Outlook microsoft.  <br/> |
|[Operations](operations.md) <br/> |Contiene una matriz de operaciones de regla que se pueden realizar en una Bandeja de entrada.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguna.
  
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Consulte también



[Operación de UpdateInboxRules](updateinboxrules-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

