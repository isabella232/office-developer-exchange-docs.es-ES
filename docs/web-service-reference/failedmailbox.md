---
title: FailedMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3d4c9816-54bb-4932-b4ba-f057c9173a1a
description: El elemento FailedMailbox especifica el mensaje de error de un buzón en el que se produjo un error en la búsqueda.
ms.openlocfilehash: 404084bc342eb555db61c4216e936bee6ced9c36
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461964"
---
# <a name="failedmailbox"></a><span data-ttu-id="c1c7e-103">FailedMailbox</span><span class="sxs-lookup"><span data-stu-id="c1c7e-103">FailedMailbox</span></span>

<span data-ttu-id="c1c7e-104">El elemento **FailedMailbox** especifica el mensaje de error de un buzón en el que se produjo un error en la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c1c7e-104">The **FailedMailbox** element specifies the error message for a mailbox that failed on search.</span></span> 
  
```XML
<FailedMailbox>
    <Mailbox/>
    <ErrorCode/>
    <ErrorMessage/>
    <IsArchive/>
</FailedMailbox>
```

 <span data-ttu-id="c1c7e-105">**FailedSearchMailboxType**</span><span class="sxs-lookup"><span data-stu-id="c1c7e-105">**FailedSearchMailboxType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c1c7e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c1c7e-106">Attributes and elements</span></span>

<span data-ttu-id="c1c7e-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c1c7e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1c7e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c1c7e-108">Attributes</span></span>

<span data-ttu-id="c1c7e-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c1c7e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c1c7e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c1c7e-110">Child elements</span></span>

|<span data-ttu-id="c1c7e-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c1c7e-111">**Element**</span></span>|<span data-ttu-id="c1c7e-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c1c7e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1c7e-113">Mailbox (cadena)</span><span class="sxs-lookup"><span data-stu-id="c1c7e-113">Mailbox (string)</span></span>](mailbox-string.md) <br/> |<span data-ttu-id="c1c7e-114">Contiene un identificador para el buzón.</span><span class="sxs-lookup"><span data-stu-id="c1c7e-114">Contains an identifier for the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="c1c7e-115">ErrorCode (int)</span><span class="sxs-lookup"><span data-stu-id="c1c7e-115">ErrorCode (int)</span></span>](errorcode-int.md) <br/> |<span data-ttu-id="c1c7e-116">Especifica el código de error del buzón de correo que produjo el error en la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c1c7e-116">Specifies the error code of the mailbox that failed the search.</span></span>  <br/> |
|[<span data-ttu-id="c1c7e-117">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="c1c7e-117">ErrorMessage</span></span>](errormessage.md) <br/> |<span data-ttu-id="c1c7e-118">Representa el motivo del error de validación.</span><span class="sxs-lookup"><span data-stu-id="c1c7e-118">Represents the reason for the validation error.</span></span>  <br/> |
|[<span data-ttu-id="c1c7e-119">IsArchive</span><span class="sxs-lookup"><span data-stu-id="c1c7e-119">IsArchive</span></span>](isarchive.md) <br/> |<span data-ttu-id="c1c7e-120">Especifica un valor booleano que indica si el buzón es un archivo.</span><span class="sxs-lookup"><span data-stu-id="c1c7e-120">Specifies a Boolean value that indicates whether the mailbox is an archive.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c1c7e-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c1c7e-121">Parent elements</span></span>

|<span data-ttu-id="c1c7e-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c1c7e-122">**Element**</span></span>|<span data-ttu-id="c1c7e-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c1c7e-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1c7e-124">FailedMailboxes</span><span class="sxs-lookup"><span data-stu-id="c1c7e-124">FailedMailboxes</span></span>](failedmailboxes.md) <br/> |<span data-ttu-id="c1c7e-125">Especifica una matriz de buzones con error.</span><span class="sxs-lookup"><span data-stu-id="c1c7e-125">Specifies an array of failed mailboxes.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c1c7e-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c1c7e-126">Remarks</span></span>

<span data-ttu-id="c1c7e-127">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c1c7e-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c1c7e-128">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c1c7e-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1c7e-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c1c7e-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1c7e-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1c7e-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c1c7e-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c1c7e-131">Schema Name</span></span>  <br/> |<span data-ttu-id="c1c7e-132">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="c1c7e-132">Type schema</span></span>  <br/> |
|<span data-ttu-id="c1c7e-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c1c7e-133">Validation File</span></span>  <br/> |<span data-ttu-id="c1c7e-134">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c1c7e-134">types.xsd</span></span>  <br/> |
|<span data-ttu-id="c1c7e-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c1c7e-135">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="c1c7e-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1c7e-136">See also</span></span>



- [<span data-ttu-id="c1c7e-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c1c7e-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

