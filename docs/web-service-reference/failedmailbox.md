---
title: FailedMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3d4c9816-54bb-4932-b4ba-f057c9173a1a
description: El elemento FailedMailbox especifica el mensaje de error para un buzón de correo con errores en la búsqueda.
ms.openlocfilehash: a4f5cd975eba121dd1d8d918b638d34f907588a8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764580"
---
# <a name="failedmailbox"></a><span data-ttu-id="2e28e-103">FailedMailbox</span><span class="sxs-lookup"><span data-stu-id="2e28e-103">FailedMailbox</span></span>

<span data-ttu-id="2e28e-104">El elemento **FailedMailbox** especifica el mensaje de error para un buzón de correo con errores en la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="2e28e-104">The **FailedMailbox** element specifies the error message for a mailbox that failed on search.</span></span> 
  
```XML
<FailedMailbox>
    <Mailbox/>
    <ErrorCode/>
    <ErrorMessage/>
    <IsArchive/>
</FailedMailbox>
```

 <span data-ttu-id="2e28e-105">**FailedSearchMailboxType**</span><span class="sxs-lookup"><span data-stu-id="2e28e-105">**FailedSearchMailboxType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2e28e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2e28e-106">Attributes and elements</span></span>

<span data-ttu-id="2e28e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2e28e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2e28e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2e28e-108">Attributes</span></span>

<span data-ttu-id="2e28e-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2e28e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2e28e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2e28e-110">Child elements</span></span>

|<span data-ttu-id="2e28e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="2e28e-111">**Element**</span></span>|<span data-ttu-id="2e28e-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2e28e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e28e-113">Buzón de correo (cadena)</span><span class="sxs-lookup"><span data-stu-id="2e28e-113">Mailbox (string)</span></span>](mailbox-string.md) <br/> |<span data-ttu-id="2e28e-114">Contiene un identificador para el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="2e28e-114">Contains an identifier for the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="2e28e-115">ErrorCode (int)</span><span class="sxs-lookup"><span data-stu-id="2e28e-115">ErrorCode (int)</span></span>](errorcode-int.md) <br/> |<span data-ttu-id="2e28e-116">Especifica el código de error del buzón al que no se pudo la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="2e28e-116">Specifies the error code of the mailbox that failed the search.</span></span>  <br/> |
|[<span data-ttu-id="2e28e-117">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="2e28e-117">ErrorMessage</span></span>](errormessage.md) <br/> |<span data-ttu-id="2e28e-118">Representa el motivo del error de validación.</span><span class="sxs-lookup"><span data-stu-id="2e28e-118">Represents the reason for the validation error.</span></span>  <br/> |
|[<span data-ttu-id="2e28e-119">IsArchive</span><span class="sxs-lookup"><span data-stu-id="2e28e-119">IsArchive</span></span>](isarchive.md) <br/> |<span data-ttu-id="2e28e-120">Especifica un valor booleano que indica si el buzón de correo es un archivo.</span><span class="sxs-lookup"><span data-stu-id="2e28e-120">Specifies a Boolean value that indicates whether the mailbox is an archive.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2e28e-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2e28e-121">Parent elements</span></span>

|<span data-ttu-id="2e28e-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="2e28e-122">**Element**</span></span>|<span data-ttu-id="2e28e-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2e28e-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e28e-124">FailedMailboxes</span><span class="sxs-lookup"><span data-stu-id="2e28e-124">FailedMailboxes</span></span>](failedmailboxes.md) <br/> |<span data-ttu-id="2e28e-125">Especifica una matriz de los buzones de correo con errores.</span><span class="sxs-lookup"><span data-stu-id="2e28e-125">Specifies an array of failed mailboxes.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e28e-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2e28e-126">Remarks</span></span>

<span data-ttu-id="2e28e-127">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2e28e-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2e28e-128">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="2e28e-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2e28e-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2e28e-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2e28e-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2e28e-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2e28e-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2e28e-131">Schema Name</span></span>  <br/> |<span data-ttu-id="2e28e-132">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="2e28e-132">Type schema</span></span>  <br/> |
|<span data-ttu-id="2e28e-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2e28e-133">Validation File</span></span>  <br/> |<span data-ttu-id="2e28e-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2e28e-134">types.xsd</span></span>  <br/> |
|<span data-ttu-id="2e28e-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2e28e-135">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="2e28e-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e28e-136">See also</span></span>



- [<span data-ttu-id="2e28e-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="2e28e-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

