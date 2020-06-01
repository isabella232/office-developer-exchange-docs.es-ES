---
title: Position
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 46726ebb-a403-4793-8378-282aa7dc39d0
description: El elemento Position especifica la posición de una entidad extraída de un mensaje.
ms.openlocfilehash: 9acd965c3e0c29f3fa91df338c0671749192b38b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465425"
---
# <a name="position"></a><span data-ttu-id="8bbaa-103">Position</span><span class="sxs-lookup"><span data-stu-id="8bbaa-103">Position</span></span>

<span data-ttu-id="8bbaa-104">El elemento **Position** especifica la posición de una entidad extraída de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="8bbaa-104">The **Position** element specifies the position of an entity extracted from a message.</span></span> 
  
```XML
<Position> LatestReply | Other | Subject | Signature </Position>
```

 <span data-ttu-id="8bbaa-105">**EmailPositionType**</span><span class="sxs-lookup"><span data-stu-id="8bbaa-105">**EmailPositionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8bbaa-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8bbaa-106">Attributes and elements</span></span>

<span data-ttu-id="8bbaa-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8bbaa-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8bbaa-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8bbaa-108">Attributes</span></span>

<span data-ttu-id="8bbaa-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8bbaa-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8bbaa-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8bbaa-110">Child elements</span></span>

<span data-ttu-id="8bbaa-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8bbaa-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8bbaa-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8bbaa-112">Parent elements</span></span>

<span data-ttu-id="8bbaa-113">[UrlEntity](urlentity.md)  |  [AddressEntity](addressentity.md)  |  [EmailAddressEntity](emailaddressentity.md)  |  [MeetingSuggestion](meetingsuggestion.md)  |  [Contacto (ContactType)](contact-contacttype.md)  |  [Teléfono (PhoneEntityType)](phone-phoneentitytype.md)  |  [TaskSuggestion](tasksuggestion.md)</span><span class="sxs-lookup"><span data-stu-id="8bbaa-113">[UrlEntity](urlentity.md) | [AddressEntity](addressentity.md) | [EmailAddressEntity](emailaddressentity.md) | [MeetingSuggestion](meetingsuggestion.md) | [Contact (ContactType)](contact-contacttype.md) | [Phone (PhoneEntityType)](phone-phoneentitytype.md) | [TaskSuggestion](tasksuggestion.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="8bbaa-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="8bbaa-114">Text value</span></span>

<span data-ttu-id="8bbaa-115">El valor de texto del elemento **Position** es la ubicación en la que se originó una entidad extraída en el mensaje de origen.</span><span class="sxs-lookup"><span data-stu-id="8bbaa-115">The text value of the **Position** element is the location where an extracted entity originated in the source message.</span></span> <span data-ttu-id="8bbaa-116">Los valores de texto para el elemento **Position** son:</span><span class="sxs-lookup"><span data-stu-id="8bbaa-116">The text values for the **Position** element are:</span></span> 
  
- <span data-ttu-id="8bbaa-117">**LatestReply** : la entidad extraída se origina desde la última respuesta al mensaje.</span><span class="sxs-lookup"><span data-stu-id="8bbaa-117">**LatestReply** - the extracted entity originates from the latest reply to the message.</span></span> 
    
- <span data-ttu-id="8bbaa-118">**Otro** : la entidad extraída se origina a partir de una parte indefinida del mensaje.</span><span class="sxs-lookup"><span data-stu-id="8bbaa-118">**Other** - the extracted entity originates from an undefined part of the message.</span></span> 
    
- <span data-ttu-id="8bbaa-119">**Asunto** : la entidad extraída se origina desde el asunto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="8bbaa-119">**Subject** - the extracted entity originates from the message subject.</span></span> 
    
- <span data-ttu-id="8bbaa-120">**Signature** : la entidad extraída se origina desde la firma del mensaje.</span><span class="sxs-lookup"><span data-stu-id="8bbaa-120">**Signature** - the extracted entity originates from the message signature.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8bbaa-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8bbaa-121">Remarks</span></span>

<span data-ttu-id="8bbaa-122">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8bbaa-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8bbaa-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="8bbaa-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8bbaa-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8bbaa-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8bbaa-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="8bbaa-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8bbaa-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8bbaa-126">Schema name</span></span>  <br/> |<span data-ttu-id="8bbaa-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="8bbaa-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="8bbaa-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8bbaa-128">Validation file</span></span>  <br/> |<span data-ttu-id="8bbaa-129">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="8bbaa-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8bbaa-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8bbaa-130">Can be empty</span></span>  <br/> ||
   

