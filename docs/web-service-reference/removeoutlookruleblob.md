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
description: El elemento RemoveOutlookRuleBlob indica si se debe quitar el blob de regla de Microsoft Outlook.
ms.openlocfilehash: 45336e296c39161704ce6e0d51fba1d2c61797b1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837102"
---
# <a name="removeoutlookruleblob"></a><span data-ttu-id="2f257-103">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="2f257-103">RemoveOutlookRuleBlob</span></span>

<span data-ttu-id="2f257-104">El elemento **RemoveOutlookRuleBlob** indica si se debe quitar el blob de regla de Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="2f257-104">The **RemoveOutlookRuleBlob** element indicates whether to remove the Microsoft Outlook rule blob.</span></span> 
  
[<span data-ttu-id="2f257-105">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="2f257-105">UpdateInboxRules</span></span>](updateinboxrules.md)
  
[<span data-ttu-id="2f257-106">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="2f257-106">RemoveOutlookRuleBlob</span></span>](removeoutlookruleblob.md)
  
```XML
<RemoveOutlookRuleBlob>true | false</RemoveOutlookRuleBlob>
```

 <span data-ttu-id="2f257-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="2f257-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2f257-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2f257-108">Attributes and elements</span></span>

<span data-ttu-id="2f257-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2f257-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2f257-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="2f257-110">Attributes</span></span>

<span data-ttu-id="2f257-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2f257-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2f257-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2f257-112">Child elements</span></span>

<span data-ttu-id="2f257-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2f257-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2f257-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2f257-114">Parent elements</span></span>

|<span data-ttu-id="2f257-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="2f257-115">**Element**</span></span>|<span data-ttu-id="2f257-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2f257-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f257-117">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="2f257-117">UpdateInboxRules</span></span>](updateinboxrules.md) <br/> |<span data-ttu-id="2f257-118">Define una solicitud para actualizar las reglas de bandeja de entrada en un buzón en el almacén del servidor.</span><span class="sxs-lookup"><span data-stu-id="2f257-118">Defines a request to update the Inbox rules in a mailbox in the server store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2f257-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="2f257-119">Text value</span></span>

<span data-ttu-id="2f257-120">Un valor de texto de **true** indica que se debe quitar el blob de regla de Outlook.</span><span class="sxs-lookup"><span data-stu-id="2f257-120">A text value of **true** indicates that the Outlook rule blob should be removed.</span></span> <span data-ttu-id="2f257-121">Un valor de texto de **false** indica que no se debe quitar el blob de regla de Outlook.</span><span class="sxs-lookup"><span data-stu-id="2f257-121">A text value of **false** indicates that the Outlook rule blob should not be removed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2f257-122">Notas</span><span class="sxs-lookup"><span data-stu-id="2f257-122">Remarks</span></span>

<span data-ttu-id="2f257-123">Este elemento se establece en **true** para permitir una actualización de la regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="2f257-123">Set this element to **true** to allow for an Inbox rule update.</span></span> 
  
<span data-ttu-id="2f257-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="2f257-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2f257-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2f257-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f257-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2f257-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2f257-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2f257-127">Schema Name</span></span>  <br/> |<span data-ttu-id="2f257-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="2f257-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="2f257-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2f257-129">Validation File</span></span>  <br/> |<span data-ttu-id="2f257-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2f257-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2f257-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2f257-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="2f257-132">Verdadero</span><span class="sxs-lookup"><span data-stu-id="2f257-132">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2f257-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="2f257-133">See also</span></span>



[<span data-ttu-id="2f257-134">Operación de UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="2f257-134">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)


- [<span data-ttu-id="2f257-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="2f257-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

