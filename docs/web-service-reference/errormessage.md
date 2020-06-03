---
title: ErrorMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0cec33a6-4b10-4259-8ac3-3f39a642b34c
description: El elemento ErrorMessage representa el motivo del error de validación.
ms.openlocfilehash: a35dc6af12e71c8437c13024a254000e8f477a15
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526196"
---
# <a name="errormessage"></a><span data-ttu-id="d1f2b-103">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="d1f2b-103">ErrorMessage</span></span>

<span data-ttu-id="d1f2b-104">El elemento **errorMessage** representa el motivo del error de validación.</span><span class="sxs-lookup"><span data-stu-id="d1f2b-104">The **ErrorMessage** element represents the reason for the validation error.</span></span> 
  
```XML
<ErrorMessage/>
```

 <span data-ttu-id="d1f2b-105">**String**</span><span class="sxs-lookup"><span data-stu-id="d1f2b-105">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d1f2b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d1f2b-106">Attributes and elements</span></span>

<span data-ttu-id="d1f2b-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d1f2b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d1f2b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d1f2b-108">Attributes</span></span>

<span data-ttu-id="d1f2b-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d1f2b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d1f2b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d1f2b-110">Child elements</span></span>

<span data-ttu-id="d1f2b-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d1f2b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d1f2b-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d1f2b-112">Parent elements</span></span>

|<span data-ttu-id="d1f2b-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d1f2b-113">**Element**</span></span>|<span data-ttu-id="d1f2b-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d1f2b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d1f2b-115">Error</span><span class="sxs-lookup"><span data-stu-id="d1f2b-115">Error</span></span>](error.md) <br/> |<span data-ttu-id="d1f2b-116">Representa un error de validación único en un valor de propiedad de regla, un valor de propiedad de predicado o un valor de propiedad de acción específicos.</span><span class="sxs-lookup"><span data-stu-id="d1f2b-116">Represents a single validation error on a particular rule property value, predicate property value, or action property value.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d1f2b-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d1f2b-117">Text value</span></span>

<span data-ttu-id="d1f2b-118">Mensaje de error asociado al error de validación de regla.</span><span class="sxs-lookup"><span data-stu-id="d1f2b-118">The error message associated with the rule validation error.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d1f2b-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d1f2b-119">Remarks</span></span>

<span data-ttu-id="d1f2b-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d1f2b-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d1f2b-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d1f2b-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d1f2b-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="d1f2b-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d1f2b-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d1f2b-123">Schema Name</span></span>  <br/> |<span data-ttu-id="d1f2b-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="d1f2b-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d1f2b-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d1f2b-125">Validation File</span></span>  <br/> |<span data-ttu-id="d1f2b-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d1f2b-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d1f2b-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d1f2b-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="d1f2b-128">Verdadero</span><span class="sxs-lookup"><span data-stu-id="d1f2b-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d1f2b-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1f2b-129">See also</span></span>



- [<span data-ttu-id="d1f2b-130">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d1f2b-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

