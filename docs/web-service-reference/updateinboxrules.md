---
title: UpdateInboxRules
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateInboxRules
api_type:
- schema
ms.assetid: d220064f-ff4d-4537-8077-adf94f2cbdbd
description: El elemento UpdateInboxRules define una solicitud para actualizar las reglas de la bandeja de entrada en un buzón de correo en el almacén del servidor.
ms.openlocfilehash: d604604d582d28c07eaa75d3239082d1b6735e65
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456363"
---
# <a name="updateinboxrules"></a><span data-ttu-id="eb44d-103">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="eb44d-103">UpdateInboxRules</span></span>

<span data-ttu-id="eb44d-104">El elemento **UpdateInboxRules** define una solicitud para actualizar las reglas de la bandeja de entrada en un buzón de correo en el almacén del servidor.</span><span class="sxs-lookup"><span data-stu-id="eb44d-104">The **UpdateInboxRules** element defines a request to update the Inbox rules in a mailbox in the server store.</span></span> 
  
```XML
<UpdateInboxRules>
   <MailboxSmtpAddress/>
   <RemoveOutlookRuleBlob/>
   <Operations/>
</UpdateInboxRules>
```

 <span data-ttu-id="eb44d-105">**UpdateInboxRulesRequestType**</span><span class="sxs-lookup"><span data-stu-id="eb44d-105">**UpdateInboxRulesRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eb44d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="eb44d-106">Attributes and elements</span></span>

<span data-ttu-id="eb44d-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="eb44d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eb44d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="eb44d-108">Attributes</span></span>

<span data-ttu-id="eb44d-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="eb44d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eb44d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="eb44d-110">Child elements</span></span>

|<span data-ttu-id="eb44d-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="eb44d-111">**Element**</span></span>|<span data-ttu-id="eb44d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="eb44d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eb44d-113">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="eb44d-113">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md) <br/> |<span data-ttu-id="eb44d-114">Representa la dirección SMTP del usuario cuyas reglas de la bandeja de entrada se van a crear, modificar o eliminar.</span><span class="sxs-lookup"><span data-stu-id="eb44d-114">Represents the SMTP address of the user whose Inbox rules are to be created, modified, or deleted.</span></span>  <br/> |
|[<span data-ttu-id="eb44d-115">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="eb44d-115">RemoveOutlookRuleBlob</span></span>](removeoutlookruleblob.md) <br/> |<span data-ttu-id="eb44d-116">Indica si se quita el BLOB de reglas de Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="eb44d-116">Indicates whether to remove the Microsoft Outlook rule blob.</span></span>  <br/> |
|[<span data-ttu-id="eb44d-117">Operations</span><span class="sxs-lookup"><span data-stu-id="eb44d-117">Operations</span></span>](operations.md) <br/> |<span data-ttu-id="eb44d-118">Contiene una matriz de operaciones de regla que se pueden realizar en una bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="eb44d-118">Contains an array of rule operations that can be performed on an Inbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="eb44d-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="eb44d-119">Parent elements</span></span>

<span data-ttu-id="eb44d-120">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="eb44d-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="eb44d-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="eb44d-121">Text value</span></span>

<span data-ttu-id="eb44d-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="eb44d-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eb44d-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="eb44d-123">Remarks</span></span>

<span data-ttu-id="eb44d-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="eb44d-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eb44d-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="eb44d-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb44d-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="eb44d-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="eb44d-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="eb44d-127">Schema Name</span></span>  <br/> |<span data-ttu-id="eb44d-128">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="eb44d-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="eb44d-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="eb44d-129">Validation File</span></span>  <br/> |<span data-ttu-id="eb44d-130">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="eb44d-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="eb44d-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="eb44d-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="eb44d-132">Verdadero</span><span class="sxs-lookup"><span data-stu-id="eb44d-132">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eb44d-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb44d-133">See also</span></span>



[<span data-ttu-id="eb44d-134">Operación de UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="eb44d-134">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)


- [<span data-ttu-id="eb44d-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="eb44d-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

