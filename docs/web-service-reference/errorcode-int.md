---
title: ErrorCode (int)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 65537d96-edf9-41ee-9ad5-91ffe37e2269
description: El elemento ErrorCode especifica el código de error de una búsqueda fallida realizada en un buzón.
ms.openlocfilehash: 24170a56e5fa23c3811fcbd27f0240e6ba3c87b7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460669"
---
# <a name="errorcode-int"></a><span data-ttu-id="04fd2-103">ErrorCode (int)</span><span class="sxs-lookup"><span data-stu-id="04fd2-103">ErrorCode (int)</span></span>

<span data-ttu-id="04fd2-104">El elemento **ErrorCode** especifica el código de error de una búsqueda fallida realizada en un buzón.</span><span class="sxs-lookup"><span data-stu-id="04fd2-104">The **ErrorCode** element specifies the error code of a failed search performed against a mailbox.</span></span> 
  
```XML
<ErrorCode></ErrorCode>
```

 <span data-ttu-id="04fd2-105">**int**</span><span class="sxs-lookup"><span data-stu-id="04fd2-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="04fd2-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="04fd2-106">Attributes and elements</span></span>

<span data-ttu-id="04fd2-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="04fd2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="04fd2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="04fd2-108">Attributes</span></span>

<span data-ttu-id="04fd2-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="04fd2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="04fd2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="04fd2-110">Child elements</span></span>

<span data-ttu-id="04fd2-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="04fd2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="04fd2-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="04fd2-112">Parent elements</span></span>

|<span data-ttu-id="04fd2-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="04fd2-113">**Element**</span></span>|<span data-ttu-id="04fd2-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="04fd2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="04fd2-115">FailedMailbox</span><span class="sxs-lookup"><span data-stu-id="04fd2-115">FailedMailbox</span></span>](failedmailbox.md) <br/> |<span data-ttu-id="04fd2-116">Especifica el estado de suspensión del buzón.</span><span class="sxs-lookup"><span data-stu-id="04fd2-116">Specifies the hold status of the mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="04fd2-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="04fd2-117">Text value</span></span>

<span data-ttu-id="04fd2-118">El valor de texto del elemento **ErrorCode** es el código de error devuelto para una búsqueda fallida realizada en un buzón.</span><span class="sxs-lookup"><span data-stu-id="04fd2-118">The text value of the **ErrorCode** element is the error code returned for a failed search performed against a mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="04fd2-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="04fd2-119">Remarks</span></span>

<span data-ttu-id="04fd2-120">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="04fd2-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="04fd2-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="04fd2-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="04fd2-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="04fd2-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="04fd2-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="04fd2-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="04fd2-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="04fd2-124">Schema Name</span></span>  <br/> |<span data-ttu-id="04fd2-125">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="04fd2-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="04fd2-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="04fd2-126">Validation File</span></span>  <br/> |<span data-ttu-id="04fd2-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="04fd2-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="04fd2-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="04fd2-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="04fd2-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="04fd2-129">See also</span></span>



- [<span data-ttu-id="04fd2-130">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="04fd2-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

