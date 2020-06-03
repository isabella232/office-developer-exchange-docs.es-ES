---
title: AssistantPhoneNumbers
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f9bd9ac1-7db3-44ea-9117-18488dddde15
description: El elemento AssistantPhoneNumbers especifica una matriz de números de teléfono de asistentes y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: a72c8d646750b5d7cf9ebca13a51f4df84bf7bdb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464486"
---
# <a name="assistantphonenumbers"></a><span data-ttu-id="665e7-103">AssistantPhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="665e7-103">AssistantPhoneNumbers</span></span>

<span data-ttu-id="665e7-104">El elemento **AssistantPhoneNumbers** especifica una matriz de números de teléfono de asistentes y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="665e7-104">The **AssistantPhoneNumbers** element specifies an array of assistant phone numbers and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<AssistantPhoneNumbers>
    <PhoneNumberAttributedValue></PhoneNumberAttributedValue>
</AssistantPhoneNumbers>
```

 <span data-ttu-id="665e7-105">**ArrayOfPhoneNumberAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="665e7-105">**ArrayOfPhoneNumberAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="665e7-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="665e7-106">Attributes and elements</span></span>

<span data-ttu-id="665e7-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="665e7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="665e7-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="665e7-108">Attributes</span></span>

<span data-ttu-id="665e7-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="665e7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="665e7-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="665e7-110">Child elements</span></span>

|<span data-ttu-id="665e7-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="665e7-111">**Element**</span></span>|<span data-ttu-id="665e7-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="665e7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="665e7-113">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="665e7-113">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md) <br/> |<span data-ttu-id="665e7-114">Especifica una instancia de una matriz de números de teléfono y sus atribuciones asociadas.</span><span class="sxs-lookup"><span data-stu-id="665e7-114">Specifies an instance of an array of phone numbers and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="665e7-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="665e7-115">Parent elements</span></span>

|<span data-ttu-id="665e7-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="665e7-116">**Element**</span></span>|<span data-ttu-id="665e7-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="665e7-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="665e7-118">Rol</span><span class="sxs-lookup"><span data-stu-id="665e7-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="665e7-119">Especifica un conjunto de datos de rol devueltos por una solicitud **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="665e7-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="665e7-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="665e7-120">Remarks</span></span>

<span data-ttu-id="665e7-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="665e7-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="665e7-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="665e7-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="665e7-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="665e7-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="665e7-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="665e7-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="665e7-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="665e7-125">Schema Name</span></span>  <br/> |<span data-ttu-id="665e7-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="665e7-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="665e7-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="665e7-127">Validation File</span></span>  <br/> |<span data-ttu-id="665e7-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="665e7-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="665e7-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="665e7-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="665e7-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="665e7-130">See also</span></span>

- [<span data-ttu-id="665e7-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="665e7-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

