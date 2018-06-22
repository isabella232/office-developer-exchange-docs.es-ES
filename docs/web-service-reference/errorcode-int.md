---
title: ErrorCode (int)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 65537d96-edf9-41ee-9ad5-91ffe37e2269
description: El elemento ErrorCode especifica el código de error de una búsqueda con errores realizada en un buzón de correo.
ms.openlocfilehash: ed8a7771376f921303ea093f4be727c4146faa76
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764435"
---
# <a name="errorcode-int"></a><span data-ttu-id="118b3-103">ErrorCode (int)</span><span class="sxs-lookup"><span data-stu-id="118b3-103">ErrorCode (int)</span></span>

<span data-ttu-id="118b3-104">El elemento **ErrorCode** especifica el código de error de una búsqueda con errores realizada en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="118b3-104">The **ErrorCode** element specifies the error code of a failed search performed against a mailbox.</span></span> 
  
```XML
<ErrorCode></ErrorCode>
```

 <span data-ttu-id="118b3-105">**int**</span><span class="sxs-lookup"><span data-stu-id="118b3-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="118b3-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="118b3-106">Attributes and elements</span></span>

<span data-ttu-id="118b3-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="118b3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="118b3-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="118b3-108">Attributes</span></span>

<span data-ttu-id="118b3-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="118b3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="118b3-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="118b3-110">Child elements</span></span>

<span data-ttu-id="118b3-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="118b3-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="118b3-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="118b3-112">Parent elements</span></span>

|<span data-ttu-id="118b3-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="118b3-113">**Element**</span></span>|<span data-ttu-id="118b3-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="118b3-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="118b3-115">FailedMailbox</span><span class="sxs-lookup"><span data-stu-id="118b3-115">FailedMailbox</span></span>](failedmailbox.md) <br/> |<span data-ttu-id="118b3-116">Especifica el estado de retención del buzón.</span><span class="sxs-lookup"><span data-stu-id="118b3-116">Specifies the hold status of the mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="118b3-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="118b3-117">Text value</span></span>

<span data-ttu-id="118b3-118">El valor de texto del elemento **ErrorCode** es el código de error devuelto para una búsqueda con errores realizada en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="118b3-118">The text value of the **ErrorCode** element is the error code returned for a failed search performed against a mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="118b3-119">Notas</span><span class="sxs-lookup"><span data-stu-id="118b3-119">Remarks</span></span>

<span data-ttu-id="118b3-120">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="118b3-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="118b3-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="118b3-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="118b3-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="118b3-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="118b3-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="118b3-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="118b3-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="118b3-124">Schema Name</span></span>  <br/> |<span data-ttu-id="118b3-125">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="118b3-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="118b3-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="118b3-126">Validation File</span></span>  <br/> |<span data-ttu-id="118b3-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="118b3-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="118b3-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="118b3-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="118b3-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="118b3-129">See also</span></span>



- [<span data-ttu-id="118b3-130">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="118b3-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

