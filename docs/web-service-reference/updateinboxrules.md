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
description: El elemento UpdateInboxRules define una solicitud para actualizar las reglas de bandeja de entrada en un buzón en el almacén del servidor.
ms.openlocfilehash: 73af3efcbf4320604576b724acf18530b8b86b26
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840830"
---
# <a name="updateinboxrules"></a><span data-ttu-id="00037-103">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="00037-103">UpdateInboxRules</span></span>

<span data-ttu-id="00037-104">El elemento **UpdateInboxRules** define una solicitud para actualizar las reglas de bandeja de entrada en un buzón en el almacén del servidor.</span><span class="sxs-lookup"><span data-stu-id="00037-104">The **UpdateInboxRules** element defines a request to update the Inbox rules in a mailbox in the server store.</span></span> 
  
```XML
<UpdateInboxRules>
   <MailboxSmtpAddress/>
   <RemoveOutlookRuleBlob/>
   <Operations/>
</UpdateInboxRules>
```

 <span data-ttu-id="00037-105">**UpdateInboxRulesRequestType**</span><span class="sxs-lookup"><span data-stu-id="00037-105">**UpdateInboxRulesRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="00037-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="00037-106">Attributes and elements</span></span>

<span data-ttu-id="00037-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="00037-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="00037-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="00037-108">Attributes</span></span>

<span data-ttu-id="00037-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="00037-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="00037-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="00037-110">Child elements</span></span>

|<span data-ttu-id="00037-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="00037-111">**Element**</span></span>|<span data-ttu-id="00037-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="00037-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="00037-113">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="00037-113">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md) <br/> |<span data-ttu-id="00037-114">Representa la dirección SMTP del usuario cuyas reglas de bandeja de entrada que se van a crear, modificar o eliminar.</span><span class="sxs-lookup"><span data-stu-id="00037-114">Represents the SMTP address of the user whose Inbox rules are to be created, modified, or deleted.</span></span>  <br/> |
|[<span data-ttu-id="00037-115">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="00037-115">RemoveOutlookRuleBlob</span></span>](removeoutlookruleblob.md) <br/> |<span data-ttu-id="00037-116">Indica si se debe quitar el blob de regla de Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="00037-116">Indicates whether to remove the Microsoft Outlook rule blob.</span></span>  <br/> |
|[<span data-ttu-id="00037-117">Operations</span><span class="sxs-lookup"><span data-stu-id="00037-117">Operations</span></span>](operations.md) <br/> |<span data-ttu-id="00037-118">Contiene una matriz de las operaciones de la regla que se puede realizar en una bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="00037-118">Contains an array of rule operations that can be performed on an Inbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="00037-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="00037-119">Parent elements</span></span>

<span data-ttu-id="00037-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="00037-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="00037-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="00037-121">Text value</span></span>

<span data-ttu-id="00037-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="00037-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="00037-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00037-123">Remarks</span></span>

<span data-ttu-id="00037-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="00037-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="00037-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="00037-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="00037-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="00037-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="00037-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="00037-127">Schema Name</span></span>  <br/> |<span data-ttu-id="00037-128">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="00037-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="00037-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="00037-129">Validation File</span></span>  <br/> |<span data-ttu-id="00037-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="00037-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="00037-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="00037-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="00037-132">Verdadero</span><span class="sxs-lookup"><span data-stu-id="00037-132">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="00037-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="00037-133">See also</span></span>



[<span data-ttu-id="00037-134">Operación de UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="00037-134">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)


- [<span data-ttu-id="00037-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="00037-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

