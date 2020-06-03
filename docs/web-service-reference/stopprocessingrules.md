---
title: StopProcessingRules
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StopProcessingRules
api_type:
- schema
ms.assetid: 5b89a2cb-ab26-444d-b3dd-2b3858872d63
description: El elemento StopProcessingRules indica si las reglas posteriores se deben evaluar.
ms.openlocfilehash: 9f068fd6290a39bbab6e3c1e29066c4fefefc64b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467903"
---
# <a name="stopprocessingrules"></a><span data-ttu-id="d75ec-103">StopProcessingRules</span><span class="sxs-lookup"><span data-stu-id="d75ec-103">StopProcessingRules</span></span>

<span data-ttu-id="d75ec-104">El elemento **StopProcessingRules** indica si las reglas posteriores se deben evaluar.</span><span class="sxs-lookup"><span data-stu-id="d75ec-104">The **StopProcessingRules** element indicates whether subsequent rules are to be evaluated.</span></span> 
  
```XML
<StopProcessingRules>true | false</StopProcessingRules>
```

 <span data-ttu-id="d75ec-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="d75ec-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d75ec-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d75ec-106">Attributes and elements</span></span>

<span data-ttu-id="d75ec-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d75ec-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d75ec-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d75ec-108">Attributes</span></span>

<span data-ttu-id="d75ec-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d75ec-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d75ec-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d75ec-110">Child elements</span></span>

<span data-ttu-id="d75ec-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d75ec-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d75ec-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d75ec-112">Parent elements</span></span>

|<span data-ttu-id="d75ec-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d75ec-113">**Element**</span></span>|<span data-ttu-id="d75ec-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d75ec-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d75ec-115">Actions</span><span class="sxs-lookup"><span data-stu-id="d75ec-115">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="d75ec-116">Representa el conjunto de acciones que se pueden realizar en un mensaje cuando se cumplen las condiciones.</span><span class="sxs-lookup"><span data-stu-id="d75ec-116">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d75ec-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d75ec-117">Text value</span></span>

<span data-ttu-id="d75ec-118">Un valor de texto de **true** indica que no se deben procesar las reglas posteriores.</span><span class="sxs-lookup"><span data-stu-id="d75ec-118">A text value of **true** indicates that subsequent rules should not be processed.</span></span> <span data-ttu-id="d75ec-119">Un valor de **false** indica que las reglas posteriores deben seguir evaluándose.</span><span class="sxs-lookup"><span data-stu-id="d75ec-119">A value of **false** indicates that subsequent rules should continue to be evaluated.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d75ec-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d75ec-120">Remarks</span></span>

<span data-ttu-id="d75ec-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d75ec-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d75ec-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d75ec-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d75ec-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="d75ec-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d75ec-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d75ec-124">Schema Name</span></span>  <br/> |<span data-ttu-id="d75ec-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="d75ec-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d75ec-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d75ec-126">Validation File</span></span>  <br/> |<span data-ttu-id="d75ec-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d75ec-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d75ec-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d75ec-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="d75ec-129">Verdadero</span><span class="sxs-lookup"><span data-stu-id="d75ec-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d75ec-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="d75ec-130">See also</span></span>



- [<span data-ttu-id="d75ec-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d75ec-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

