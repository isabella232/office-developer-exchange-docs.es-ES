---
title: Emails2
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6ad95936-f61b-431a-9d86-df160b5d4b2d
description: El elemento Emails2 contiene una matriz de valores de EmailAddressAttributedValue y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: 1767d6bfaee335717e33e0345c605025a073335c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764353"
---
# <a name="emails2"></a><span data-ttu-id="c5699-103">Emails2</span><span class="sxs-lookup"><span data-stu-id="c5699-103">Emails2</span></span>

<span data-ttu-id="c5699-104">El elemento **Emails2** contiene una matriz de valores de **EmailAddressAttributedValue** y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="c5699-104">The **Emails2** element contains an array of **EmailAddressAttributedValue** values and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<Emails2>
    <EmailAddressAttributedValue></EmailAddressAttributedValue>
</Emails2>
```

 <span data-ttu-id="c5699-105">**ArrayOfEmailAddressAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="c5699-105">**ArrayOfEmailAddressAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c5699-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c5699-106">Attributes and elements</span></span>

<span data-ttu-id="c5699-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c5699-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c5699-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c5699-108">Attributes</span></span>

<span data-ttu-id="c5699-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c5699-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c5699-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c5699-110">Child elements</span></span>

|<span data-ttu-id="c5699-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c5699-111">**Element**</span></span>|<span data-ttu-id="c5699-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c5699-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c5699-113">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="c5699-113">EmailAddressAttributedValue</span></span>](emailaddressattributedvalue.md) <br/> |<span data-ttu-id="c5699-114">Especifica una instancia de una matriz de direcciones de correo electrónico y sus atribuciones asociados.</span><span class="sxs-lookup"><span data-stu-id="c5699-114">Specifies an instance of an array of email addresses and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c5699-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c5699-115">Parent elements</span></span>

|<span data-ttu-id="c5699-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="c5699-116">**Element**</span></span>|<span data-ttu-id="c5699-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c5699-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c5699-118">Rol</span><span class="sxs-lookup"><span data-stu-id="c5699-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="c5699-119">Especifica un conjunto de datos de rol devueltos por una solicitud de **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="c5699-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5699-120">Notas</span><span class="sxs-lookup"><span data-stu-id="c5699-120">Remarks</span></span>

<span data-ttu-id="c5699-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c5699-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c5699-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c5699-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c5699-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c5699-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c5699-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c5699-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c5699-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c5699-125">Schema Name</span></span>  <br/> |<span data-ttu-id="c5699-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="c5699-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="c5699-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c5699-127">Validation File</span></span>  <br/> |<span data-ttu-id="c5699-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c5699-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="c5699-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c5699-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="c5699-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="c5699-130">See also</span></span>



- [<span data-ttu-id="c5699-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c5699-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

