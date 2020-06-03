---
title: IsArchive
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b89d8a78-5c18-4547-aaf4-4b16a93190a7
description: El elemento IsArchive especifica un valor booleano que indica si el buzón es un buzón de archivo.
ms.openlocfilehash: 6d0be0eb283de3f4d8f786ff96f4a0d4f49e2009
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526518"
---
# <a name="isarchive"></a><span data-ttu-id="3b772-103">IsArchive</span><span class="sxs-lookup"><span data-stu-id="3b772-103">IsArchive</span></span>

<span data-ttu-id="3b772-104">El elemento **IsArchive** especifica un valor booleano que indica si el buzón es un buzón de archivo.</span><span class="sxs-lookup"><span data-stu-id="3b772-104">The **IsArchive** element specifies a Boolean value that indicates whether the mailbox is an archive mailbox.</span></span> 
  
```XML
<IsArchive>true | false</IsArchive>
```

 <span data-ttu-id="3b772-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="3b772-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3b772-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3b772-106">Attributes and elements</span></span>

<span data-ttu-id="3b772-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3b772-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3b772-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3b772-108">Attributes</span></span>

<span data-ttu-id="3b772-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3b772-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3b772-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3b772-110">Child elements</span></span>

<span data-ttu-id="3b772-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3b772-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3b772-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3b772-112">Parent elements</span></span>

<span data-ttu-id="3b772-113">[FailedMailbox](failedmailbox.md)  |  [RetentionPolicyTag](retentionpolicytag.md)</span><span class="sxs-lookup"><span data-stu-id="3b772-113">[FailedMailbox](failedmailbox.md) | [RetentionPolicyTag](retentionpolicytag.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="3b772-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3b772-114">Text value</span></span>

<span data-ttu-id="3b772-115">Un valor de texto de **true** para el elemento **IsArchive** indica que el buzón de destino es un buzón de archivo.</span><span class="sxs-lookup"><span data-stu-id="3b772-115">A text value of **true** for the **IsArchive** element indicates that the target mailbox is an archive mailbox.</span></span> <span data-ttu-id="3b772-116">Un valor de **false** indica que el buzón de correo de destino no es un buzón de archivo.</span><span class="sxs-lookup"><span data-stu-id="3b772-116">A value of **false** indicates that the target mailbox is not an archive mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3b772-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3b772-117">Remarks</span></span>

<span data-ttu-id="3b772-118">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3b772-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3b772-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3b772-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3b772-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3b772-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3b772-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="3b772-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3b772-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3b772-122">Schema Name</span></span>  <br/> |<span data-ttu-id="3b772-123">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="3b772-123">Type schema</span></span>  <br/> |
|<span data-ttu-id="3b772-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3b772-124">Validation File</span></span>  <br/> |<span data-ttu-id="3b772-125">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="3b772-125">types.xsd</span></span>  <br/> |
|<span data-ttu-id="3b772-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3b772-126">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="3b772-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b772-127">See also</span></span>



- [<span data-ttu-id="3b772-128">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="3b772-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

