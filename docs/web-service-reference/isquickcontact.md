---
title: IsQuickContact
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c9542d6-ef72-4743-828a-bb671e783836
description: El elemento IsQuickContact especifica un valor booleano que indica si el contacto subyacente es un contacto rápido.
ms.openlocfilehash: 979dbd3c0358eacd443eed79b258f7dd6bb9bc7d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836092"
---
# <a name="isquickcontact"></a><span data-ttu-id="feab9-103">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="feab9-103">IsQuickContact</span></span>

<span data-ttu-id="feab9-104">El elemento **IsQuickContact** especifica un valor booleano que indica si el contacto subyacente es un contacto rápido.</span><span class="sxs-lookup"><span data-stu-id="feab9-104">The **IsQuickContact** element specifies a Boolean value that indicates whether the underlying contact is a quick contact.</span></span> 
  
```XML
<IsQuickContact>true | false</IsQuickContact>
```

 <span data-ttu-id="feab9-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="feab9-105">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="feab9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="feab9-106">Attributes and elements</span></span>

<span data-ttu-id="feab9-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="feab9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="feab9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="feab9-108">Attributes</span></span>

<span data-ttu-id="feab9-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="feab9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="feab9-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="feab9-110">Child elements</span></span>

<span data-ttu-id="feab9-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="feab9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="feab9-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="feab9-112">Parent elements</span></span>

|<span data-ttu-id="feab9-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="feab9-113">**Element**</span></span>|<span data-ttu-id="feab9-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="feab9-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="feab9-115">Atribución (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="feab9-115">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md) <br/> |<span data-ttu-id="feab9-116">Especifica una instancia de una matriz de atributos de un elemento de la **Persona** .</span><span class="sxs-lookup"><span data-stu-id="feab9-116">Specifies an instance in an array of attributes for a **Persona** element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="feab9-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="feab9-117">Text value</span></span>

<span data-ttu-id="feab9-118">Un valor de texto de **true** para el elemento **IsQuickContact** indica que el contacto es un contacto rápido.</span><span class="sxs-lookup"><span data-stu-id="feab9-118">A text value of **true** for the **IsQuickContact** element indicates that the contact is a quick contact.</span></span> <span data-ttu-id="feab9-119">Un valor de **false** indica que el contacto no es un contacto rápido.</span><span class="sxs-lookup"><span data-stu-id="feab9-119">A value of **false** indicates that the contact is not a quick contact.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="feab9-120">Notas</span><span class="sxs-lookup"><span data-stu-id="feab9-120">Remarks</span></span>

<span data-ttu-id="feab9-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="feab9-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="feab9-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="feab9-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="feab9-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="feab9-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="feab9-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="feab9-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="feab9-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="feab9-125">Schema Name</span></span>  <br/> |<span data-ttu-id="feab9-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="feab9-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="feab9-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="feab9-127">Validation File</span></span>  <br/> |<span data-ttu-id="feab9-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="feab9-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="feab9-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="feab9-129">Can Be Empty</span></span>  <br/> |<span data-ttu-id="feab9-130">falso</span><span class="sxs-lookup"><span data-stu-id="feab9-130">false</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="feab9-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="feab9-131">See also</span></span>



- [<span data-ttu-id="feab9-132">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="feab9-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

