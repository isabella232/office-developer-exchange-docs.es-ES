---
title: Posición
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 46726ebb-a403-4793-8378-282aa7dc39d0
description: El elemento de posición especifica la posición de una entidad extraída de un mensaje.
ms.openlocfilehash: 4bd8f3088891e918e13d5ef1ec8e3e5217cb3fa1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836853"
---
# <a name="position"></a><span data-ttu-id="c680c-103">Posición</span><span class="sxs-lookup"><span data-stu-id="c680c-103">Position</span></span>

<span data-ttu-id="c680c-104">El elemento de **posición** especifica la posición de una entidad extraída de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="c680c-104">The **Position** element specifies the position of an entity extracted from a message.</span></span> 
  
```XML
<Position> LatestReply | Other | Subject | Signature </Position>
```

 <span data-ttu-id="c680c-105">**EmailPositionType**</span><span class="sxs-lookup"><span data-stu-id="c680c-105">**EmailPositionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c680c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c680c-106">Attributes and elements</span></span>

<span data-ttu-id="c680c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c680c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c680c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c680c-108">Attributes</span></span>

<span data-ttu-id="c680c-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c680c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c680c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c680c-110">Child elements</span></span>

<span data-ttu-id="c680c-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c680c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c680c-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c680c-112">Parent elements</span></span>

<span data-ttu-id="c680c-113">[UrlEntity](urlentity.md) | [AddressEntity](addressentity.md) | [EmailAddressEntity](emailaddressentity.md) | [MeetingSuggestion](meetingsuggestion.md) | [contacto (ContactType)](contact-contacttype.md) | [teléfono (PhoneEntityType)](phone-phoneentitytype.md)  |  [ TaskSuggestion](tasksuggestion.md)</span><span class="sxs-lookup"><span data-stu-id="c680c-113">[UrlEntity](urlentity.md) | [AddressEntity](addressentity.md) | [EmailAddressEntity](emailaddressentity.md) | [MeetingSuggestion](meetingsuggestion.md) | [Contact (ContactType)](contact-contacttype.md) | [Phone (PhoneEntityType)](phone-phoneentitytype.md) | [TaskSuggestion](tasksuggestion.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="c680c-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c680c-114">Text value</span></span>

<span data-ttu-id="c680c-115">El valor de texto del elemento de **posición** es la ubicación donde se originó una entidad extraída en el mensaje de origen.</span><span class="sxs-lookup"><span data-stu-id="c680c-115">The text value of the **Position** element is the location where an extracted entity originated in the source message.</span></span> <span data-ttu-id="c680c-116">Los valores de texto para el elemento de **posición** son:</span><span class="sxs-lookup"><span data-stu-id="c680c-116">The text values for the **Position** element are:</span></span> 
  
- <span data-ttu-id="c680c-117">**LatestReply** - la entidad extraída se origina en la respuesta al mensaje más reciente.</span><span class="sxs-lookup"><span data-stu-id="c680c-117">**LatestReply** - the extracted entity originates from the latest reply to the message.</span></span> 
    
- <span data-ttu-id="c680c-118">**Otros** - la entidad extraída se origina desde una parte del mensaje no definida.</span><span class="sxs-lookup"><span data-stu-id="c680c-118">**Other** - the extracted entity originates from an undefined part of the message.</span></span> 
    
- <span data-ttu-id="c680c-119">**Asunto** : la entidad extraída se origina en el asunto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="c680c-119">**Subject** - the extracted entity originates from the message subject.</span></span> 
    
- <span data-ttu-id="c680c-120">**Firma** : la entidad extraída se origina en la firma del mensaje.</span><span class="sxs-lookup"><span data-stu-id="c680c-120">**Signature** - the extracted entity originates from the message signature.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c680c-121">Notas</span><span class="sxs-lookup"><span data-stu-id="c680c-121">Remarks</span></span>

<span data-ttu-id="c680c-122">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c680c-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c680c-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c680c-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c680c-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c680c-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c680c-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c680c-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c680c-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c680c-126">Schema name</span></span>  <br/> |<span data-ttu-id="c680c-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c680c-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="c680c-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c680c-128">Validation file</span></span>  <br/> |<span data-ttu-id="c680c-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c680c-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c680c-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c680c-130">Can be empty</span></span>  <br/> ||
   

