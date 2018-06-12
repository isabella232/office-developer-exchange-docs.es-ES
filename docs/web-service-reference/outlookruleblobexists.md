---
title: OutlookRuleBlobExists
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OutlookRuleBlobExists
api_type:
- schema
ms.assetid: ae1bc448-deb9-4b5b-ab38-4b276abcb650
description: El elemento OutlookRuleBlobExists indica si existe un blob de regla de Microsoft Outlook en el buzón del usuario.
ms.openlocfilehash: a738377cd3c1d69b90ac39ca479b03b3220d5bc5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836679"
---
# <a name="outlookruleblobexists"></a><span data-ttu-id="867ca-103">OutlookRuleBlobExists</span><span class="sxs-lookup"><span data-stu-id="867ca-103">OutlookRuleBlobExists</span></span>

<span data-ttu-id="867ca-104">El elemento **OutlookRuleBlobExists** indica si existe un blob de regla de Microsoft Outlook en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="867ca-104">The **OutlookRuleBlobExists** element indicates whether a Microsoft Outlook rule blob exists in the user's mailbox.</span></span> 
  
[<span data-ttu-id="867ca-105">GetInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="867ca-105">GetInboxRulesResponse</span></span>](getinboxrulesresponse.md)
  
[<span data-ttu-id="867ca-106">OutlookRuleBlobExists</span><span class="sxs-lookup"><span data-stu-id="867ca-106">OutlookRuleBlobExists</span></span>](outlookruleblobexists.md)
  
```XML
<OutlookRuleBlobExists>true | false</OutlookRuleBlobExists>
```

 <span data-ttu-id="867ca-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="867ca-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="867ca-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="867ca-108">Attributes and elements</span></span>

<span data-ttu-id="867ca-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="867ca-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="867ca-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="867ca-110">Attributes</span></span>

<span data-ttu-id="867ca-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="867ca-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="867ca-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="867ca-112">Child elements</span></span>

<span data-ttu-id="867ca-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="867ca-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="867ca-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="867ca-114">Parent elements</span></span>

|<span data-ttu-id="867ca-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="867ca-115">**Element**</span></span>|<span data-ttu-id="867ca-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="867ca-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="867ca-117">GetInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="867ca-117">GetInboxRulesResponse</span></span>](getinboxrulesresponse.md) <br/> |<span data-ttu-id="867ca-118">Representa una respuesta a una solicitud de [operación GetInboxRules](getinboxrules-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="867ca-118">Represents a response to a [GetInboxRules operation](getinboxrules-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="867ca-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="867ca-119">Text value</span></span>

<span data-ttu-id="867ca-120">Un valor de texto de **true** indica que existe un blob de regla de Outlook.</span><span class="sxs-lookup"><span data-stu-id="867ca-120">A text value of **true** indicates that an Outlook rule blob exists.</span></span> <span data-ttu-id="867ca-121">Un valor de texto de **false** indica que no existe un blob de regla de Outlook.</span><span class="sxs-lookup"><span data-stu-id="867ca-121">A text value of **false** indicates that an Outlook rule blob does not exist.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="867ca-122">Notas</span><span class="sxs-lookup"><span data-stu-id="867ca-122">Remarks</span></span>

<span data-ttu-id="867ca-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="867ca-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="867ca-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="867ca-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="867ca-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="867ca-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="867ca-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="867ca-126">Schema Name</span></span>  <br/> |<span data-ttu-id="867ca-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="867ca-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="867ca-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="867ca-128">Validation File</span></span>  <br/> |<span data-ttu-id="867ca-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="867ca-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="867ca-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="867ca-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="867ca-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="867ca-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="867ca-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="867ca-132">See also</span></span>



- [<span data-ttu-id="867ca-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="867ca-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

