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
ms.openlocfilehash: a8944be111a8dcbe914601ffc4e31794422d58aa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44441579"
---
# <a name="isquickcontact"></a><span data-ttu-id="25428-103">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="25428-103">IsQuickContact</span></span>

<span data-ttu-id="25428-104">El elemento **IsQuickContact** especifica un valor booleano que indica si el contacto subyacente es un contacto rápido.</span><span class="sxs-lookup"><span data-stu-id="25428-104">The **IsQuickContact** element specifies a Boolean value that indicates whether the underlying contact is a quick contact.</span></span> 
  
```XML
<IsQuickContact>true | false</IsQuickContact>
```

 <span data-ttu-id="25428-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="25428-105">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="25428-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="25428-106">Attributes and elements</span></span>

<span data-ttu-id="25428-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="25428-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="25428-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="25428-108">Attributes</span></span>

<span data-ttu-id="25428-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="25428-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="25428-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="25428-110">Child elements</span></span>

<span data-ttu-id="25428-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="25428-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="25428-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="25428-112">Parent elements</span></span>

|<span data-ttu-id="25428-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="25428-113">**Element**</span></span>|<span data-ttu-id="25428-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="25428-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="25428-115">Atribución (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="25428-115">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md) <br/> |<span data-ttu-id="25428-116">Especifica una instancia de una matriz de atributos para un elemento de **rol** .</span><span class="sxs-lookup"><span data-stu-id="25428-116">Specifies an instance in an array of attributes for a **Persona** element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="25428-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="25428-117">Text value</span></span>

<span data-ttu-id="25428-118">Un valor de texto de **true** para el elemento **IsQuickContact** indica que el contacto es un contacto rápido.</span><span class="sxs-lookup"><span data-stu-id="25428-118">A text value of **true** for the **IsQuickContact** element indicates that the contact is a quick contact.</span></span> <span data-ttu-id="25428-119">Un valor de **false** indica que el contacto no es un contacto rápido.</span><span class="sxs-lookup"><span data-stu-id="25428-119">A value of **false** indicates that the contact is not a quick contact.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="25428-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="25428-120">Remarks</span></span>

<span data-ttu-id="25428-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="25428-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="25428-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="25428-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="25428-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="25428-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="25428-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="25428-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="25428-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="25428-125">Schema Name</span></span>  <br/> |<span data-ttu-id="25428-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="25428-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="25428-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="25428-127">Validation File</span></span>  <br/> |<span data-ttu-id="25428-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="25428-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="25428-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="25428-129">Can Be Empty</span></span>  <br/> |<span data-ttu-id="25428-130">false</span><span class="sxs-lookup"><span data-stu-id="25428-130">false</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="25428-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="25428-131">See also</span></span>



- [<span data-ttu-id="25428-132">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="25428-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

