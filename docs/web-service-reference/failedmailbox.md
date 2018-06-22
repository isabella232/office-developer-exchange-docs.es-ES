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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764580"
---
# <a name="failedmailbox"></a><span data-ttu-id="abc56-103">FailedMailbox</span><span class="sxs-lookup"><span data-stu-id="abc56-103">FailedMailbox</span></span>

<span data-ttu-id="abc56-104">El elemento **FailedMailbox** especifica el mensaje de error para un buzón de correo con errores en la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="abc56-104">The **FailedMailbox** element specifies the error message for a mailbox that failed on search.</span></span> 
  
```XML
<FailedMailbox>
    <Mailbox/>
    <ErrorCode/>
    <ErrorMessage/>
    <IsArchive/>
</FailedMailbox>
```

 <span data-ttu-id="abc56-105">**FailedSearchMailboxType**</span><span class="sxs-lookup"><span data-stu-id="abc56-105">**FailedSearchMailboxType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="abc56-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="abc56-106">Attributes and elements</span></span>

<span data-ttu-id="abc56-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="abc56-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="abc56-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="abc56-108">Attributes</span></span>

<span data-ttu-id="abc56-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="abc56-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="abc56-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="abc56-110">Child elements</span></span>

|<span data-ttu-id="abc56-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="abc56-111">**Element**</span></span>|<span data-ttu-id="abc56-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="abc56-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="abc56-113">Buzón de correo (cadena)</span><span class="sxs-lookup"><span data-stu-id="abc56-113">Mailbox (string)</span></span>](mailbox-string.md) <br/> |<span data-ttu-id="abc56-114">Contiene un identificador para el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="abc56-114">Contains an identifier for the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="abc56-115">ErrorCode (int)</span><span class="sxs-lookup"><span data-stu-id="abc56-115">ErrorCode (int)</span></span>](errorcode-int.md) <br/> |<span data-ttu-id="abc56-116">Especifica el código de error del buzón al que no se pudo la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="abc56-116">Specifies the error code of the mailbox that failed the search.</span></span>  <br/> |
|[<span data-ttu-id="abc56-117">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="abc56-117">ErrorMessage</span></span>](errormessage.md) <br/> |<span data-ttu-id="abc56-118">Representa el motivo del error de validación.</span><span class="sxs-lookup"><span data-stu-id="abc56-118">Represents the reason for the validation error.</span></span>  <br/> |
|[<span data-ttu-id="abc56-119">IsArchive</span><span class="sxs-lookup"><span data-stu-id="abc56-119">IsArchive</span></span>](isarchive.md) <br/> |<span data-ttu-id="abc56-120">Especifica un valor booleano que indica si el buzón de correo es un archivo.</span><span class="sxs-lookup"><span data-stu-id="abc56-120">Specifies a Boolean value that indicates whether the mailbox is an archive.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="abc56-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="abc56-121">Parent elements</span></span>

|<span data-ttu-id="abc56-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="abc56-122">**Element**</span></span>|<span data-ttu-id="abc56-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="abc56-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="abc56-124">FailedMailboxes</span><span class="sxs-lookup"><span data-stu-id="abc56-124">FailedMailboxes</span></span>](failedmailboxes.md) <br/> |<span data-ttu-id="abc56-125">Especifica una matriz de los buzones de correo con errores.</span><span class="sxs-lookup"><span data-stu-id="abc56-125">Specifies an array of failed mailboxes.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="abc56-126">Notas</span><span class="sxs-lookup"><span data-stu-id="abc56-126">Remarks</span></span>

<span data-ttu-id="abc56-127">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="abc56-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="abc56-128">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="abc56-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="abc56-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="abc56-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="abc56-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="abc56-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="abc56-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="abc56-131">Schema Name</span></span>  <br/> |<span data-ttu-id="abc56-132">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="abc56-132">Type schema</span></span>  <br/> |
|<span data-ttu-id="abc56-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="abc56-133">Validation File</span></span>  <br/> |<span data-ttu-id="abc56-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="abc56-134">types.xsd</span></span>  <br/> |
|<span data-ttu-id="abc56-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="abc56-135">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="abc56-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="abc56-136">See also</span></span>



- [<span data-ttu-id="abc56-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="abc56-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

