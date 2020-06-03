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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467672"
---
# <a name="removeoutlookruleblob"></a><span data-ttu-id="d7424-103">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="d7424-103">RemoveOutlookRuleBlob</span></span>

<span data-ttu-id="d7424-104">El elemento **RemoveOutlookRuleBlob** indica si se debe quitar el objeto binario de la regla de Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="d7424-104">The **RemoveOutlookRuleBlob** element indicates whether to remove the Microsoft Outlook rule blob.</span></span> 
  
[<span data-ttu-id="d7424-105">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="d7424-105">UpdateInboxRules</span></span>](updateinboxrules.md)
  
[<span data-ttu-id="d7424-106">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="d7424-106">RemoveOutlookRuleBlob</span></span>](removeoutlookruleblob.md)
  
```XML
<RemoveOutlookRuleBlob>true | false</RemoveOutlookRuleBlob>
```

 <span data-ttu-id="d7424-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="d7424-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d7424-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d7424-108">Attributes and elements</span></span>

<span data-ttu-id="d7424-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d7424-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d7424-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="d7424-110">Attributes</span></span>

<span data-ttu-id="d7424-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d7424-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d7424-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d7424-112">Child elements</span></span>

<span data-ttu-id="d7424-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d7424-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d7424-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d7424-114">Parent elements</span></span>

|<span data-ttu-id="d7424-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d7424-115">**Element**</span></span>|<span data-ttu-id="d7424-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d7424-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d7424-117">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="d7424-117">UpdateInboxRules</span></span>](updateinboxrules.md) <br/> |<span data-ttu-id="d7424-118">Define una solicitud para actualizar las reglas de la bandeja de entrada en un buzón de correo en el almacén del servidor.</span><span class="sxs-lookup"><span data-stu-id="d7424-118">Defines a request to update the Inbox rules in a mailbox in the server store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d7424-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d7424-119">Text value</span></span>

<span data-ttu-id="d7424-120">Un valor de texto de **true** indica que se debe quitar el BLOB de regla de Outlook.</span><span class="sxs-lookup"><span data-stu-id="d7424-120">A text value of **true** indicates that the Outlook rule blob should be removed.</span></span> <span data-ttu-id="d7424-121">Un valor de texto **falso** indica que el BLOB de la regla de Outlook no se debe quitar.</span><span class="sxs-lookup"><span data-stu-id="d7424-121">A text value of **false** indicates that the Outlook rule blob should not be removed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d7424-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d7424-122">Remarks</span></span>

<span data-ttu-id="d7424-123">Establezca este elemento en **true** para permitir una actualización de la regla de la bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="d7424-123">Set this element to **true** to allow for an Inbox rule update.</span></span> 
  
<span data-ttu-id="d7424-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d7424-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d7424-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d7424-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d7424-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="d7424-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d7424-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d7424-127">Schema Name</span></span>  <br/> |<span data-ttu-id="d7424-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d7424-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="d7424-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d7424-129">Validation File</span></span>  <br/> |<span data-ttu-id="d7424-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="d7424-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d7424-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d7424-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="d7424-132">Verdadero</span><span class="sxs-lookup"><span data-stu-id="d7424-132">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d7424-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7424-133">See also</span></span>



[<span data-ttu-id="d7424-134">Operación de UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="d7424-134">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)


- [<span data-ttu-id="d7424-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d7424-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

