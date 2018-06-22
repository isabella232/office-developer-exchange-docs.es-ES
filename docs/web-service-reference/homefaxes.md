---
title: HomeFaxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 459ddb1c-8cff-4125-b6fa-dc93c183dee8
description: El elemento HomeFaxes especifica una matriz de números de fax del domicilio particular y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: dd2cd8bba2c4cc7d08e88787d648e96ea996a251
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835840"
---
# <a name="homefaxes"></a><span data-ttu-id="4cb8a-103">HomeFaxes</span><span class="sxs-lookup"><span data-stu-id="4cb8a-103">HomeFaxes</span></span>

<span data-ttu-id="4cb8a-104">El elemento **HomeFaxes** especifica una matriz de números de fax del domicilio particular y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="4cb8a-104">The **HomeFaxes** element specifies an array of home fax numbers and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<HomeFaxes>
    <PhoneNumberAttributedValue/>
</HomeFaxes>
```

 <span data-ttu-id="4cb8a-105">**ArrayOfPhoneNumberAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="4cb8a-105">**ArrayOfPhoneNumberAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4cb8a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4cb8a-106">Attributes and elements</span></span>

<span data-ttu-id="4cb8a-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4cb8a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4cb8a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4cb8a-108">Attributes</span></span>

<span data-ttu-id="4cb8a-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4cb8a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4cb8a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4cb8a-110">Child elements</span></span>

|<span data-ttu-id="4cb8a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4cb8a-111">**Element**</span></span>|<span data-ttu-id="4cb8a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4cb8a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4cb8a-113">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="4cb8a-113">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md) <br/> |<span data-ttu-id="4cb8a-114">Contiene un número de teléfono único de atributos para un rol.</span><span class="sxs-lookup"><span data-stu-id="4cb8a-114">Contains a single attributed phone number for a persona.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4cb8a-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4cb8a-115">Parent elements</span></span>

|<span data-ttu-id="4cb8a-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="4cb8a-116">**Element**</span></span>|<span data-ttu-id="4cb8a-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4cb8a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4cb8a-118">Rol</span><span class="sxs-lookup"><span data-stu-id="4cb8a-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="4cb8a-119">Especifica un conjunto de datos de rol devueltos por una solicitud de **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="4cb8a-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4cb8a-120">Notas</span><span class="sxs-lookup"><span data-stu-id="4cb8a-120">Remarks</span></span>

<span data-ttu-id="4cb8a-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4cb8a-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="4cb8a-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="4cb8a-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4cb8a-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4cb8a-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4cb8a-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4cb8a-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4cb8a-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4cb8a-125">Schema Name</span></span>  <br/> |<span data-ttu-id="4cb8a-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="4cb8a-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="4cb8a-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4cb8a-127">Validation File</span></span>  <br/> |<span data-ttu-id="4cb8a-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4cb8a-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="4cb8a-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4cb8a-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="4cb8a-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="4cb8a-130">See also</span></span>



- [<span data-ttu-id="4cb8a-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="4cb8a-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

