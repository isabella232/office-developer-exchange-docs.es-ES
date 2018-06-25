---
title: AssistantPhoneNumbers
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f9bd9ac1-7db3-44ea-9117-18488dddde15
description: El elemento AssistantPhoneNumbers especifica una matriz de números de teléfono del Ayudante y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: 747835102af28d94d60b763fdbc5b2ea0947d47e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763563"
---
# <a name="assistantphonenumbers"></a><span data-ttu-id="68bcb-103">AssistantPhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="68bcb-103">AssistantPhoneNumbers</span></span>

<span data-ttu-id="68bcb-104">El elemento **AssistantPhoneNumbers** especifica una matriz de números de teléfono del Ayudante y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="68bcb-104">The **AssistantPhoneNumbers** element specifies an array of assistant phone numbers and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<AssistantPhoneNumbers>
    <PhoneNumberAttributedValue></PhoneNumberAttributedValue>
</AssistantPhoneNumbers>
```

 <span data-ttu-id="68bcb-105">**ArrayOfPhoneNumberAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="68bcb-105">**ArrayOfPhoneNumberAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="68bcb-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="68bcb-106">Attributes and elements</span></span>

<span data-ttu-id="68bcb-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="68bcb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="68bcb-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="68bcb-108">Attributes</span></span>

<span data-ttu-id="68bcb-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="68bcb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="68bcb-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="68bcb-110">Child elements</span></span>

|<span data-ttu-id="68bcb-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="68bcb-111">**Element**</span></span>|<span data-ttu-id="68bcb-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="68bcb-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="68bcb-113">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="68bcb-113">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md) <br/> |<span data-ttu-id="68bcb-114">Especifica una instancia de una matriz de números de teléfono y sus atribuciones asociados.</span><span class="sxs-lookup"><span data-stu-id="68bcb-114">Specifies an instance of an array of phone numbers and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="68bcb-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="68bcb-115">Parent elements</span></span>

|<span data-ttu-id="68bcb-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="68bcb-116">**Element**</span></span>|<span data-ttu-id="68bcb-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="68bcb-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="68bcb-118">Rol</span><span class="sxs-lookup"><span data-stu-id="68bcb-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="68bcb-119">Especifica un conjunto de datos de rol devueltos por una solicitud de **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="68bcb-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68bcb-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="68bcb-120">Remarks</span></span>

<span data-ttu-id="68bcb-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="68bcb-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="68bcb-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="68bcb-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="68bcb-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="68bcb-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68bcb-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="68bcb-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="68bcb-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="68bcb-125">Schema Name</span></span>  <br/> |<span data-ttu-id="68bcb-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="68bcb-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="68bcb-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="68bcb-127">Validation File</span></span>  <br/> |<span data-ttu-id="68bcb-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="68bcb-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="68bcb-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="68bcb-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="68bcb-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="68bcb-130">See also</span></span>

- [<span data-ttu-id="68bcb-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="68bcb-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

