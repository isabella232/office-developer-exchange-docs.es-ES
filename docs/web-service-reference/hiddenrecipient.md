---
title: HiddenRecipient
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HiddenRecipient
api_type:
- schema
ms.assetid: a8209f75-0070-4424-8dcd-273cfd192728
description: El elemento HiddenRecipient indica que el destinatario fue agregado por una directiva de la organización que debe ocultarse a los usuarios sin privilegios.
ms.openlocfilehash: bfe57fabc02ff00c801672b71ccdb0bf1b916bd9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457644"
---
# <a name="hiddenrecipient"></a><span data-ttu-id="0d16d-103">HiddenRecipient</span><span class="sxs-lookup"><span data-stu-id="0d16d-103">HiddenRecipient</span></span>

<span data-ttu-id="0d16d-104">El elemento **HiddenRecipient** indica que el destinatario fue agregado por una directiva de la organización que debe ocultarse a los usuarios sin privilegios.</span><span class="sxs-lookup"><span data-stu-id="0d16d-104">The **HiddenRecipient** element indicates that the recipient was added by an organization policy that should be hidden from unprivileged users.</span></span> 
  
```XML
<HiddenRecipient>true | false</HiddenRecipient>
```

 <span data-ttu-id="0d16d-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="0d16d-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0d16d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0d16d-106">Attributes and elements</span></span>

<span data-ttu-id="0d16d-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0d16d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0d16d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0d16d-108">Attributes</span></span>

<span data-ttu-id="0d16d-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0d16d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0d16d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0d16d-110">Child elements</span></span>

<span data-ttu-id="0d16d-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0d16d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0d16d-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0d16d-112">Parent elements</span></span>

|<span data-ttu-id="0d16d-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0d16d-113">**Element**</span></span>|<span data-ttu-id="0d16d-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0d16d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d16d-115">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="0d16d-115">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="0d16d-116">Contiene información de un evento único para un destinatario.</span><span class="sxs-lookup"><span data-stu-id="0d16d-116">Contains information for a single event for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0d16d-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0d16d-117">Text value</span></span>

<span data-ttu-id="0d16d-118">Este elemento puede ser **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="0d16d-118">This element can be either **true** or **false**.</span></span> <span data-ttu-id="0d16d-119">Un valor de **true** indica que una directiva de organización agregó al usuario; un valor de **false** indica que el usuario no fue agregado por una directiva de organización.</span><span class="sxs-lookup"><span data-stu-id="0d16d-119">A value of **true** indicates that the user was added by an organization policy; a value of **false** indicates that the user was not added by an organization policy.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0d16d-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0d16d-120">Remarks</span></span>

<span data-ttu-id="0d16d-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0d16d-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0d16d-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0d16d-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0d16d-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="0d16d-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0d16d-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0d16d-124">Schema Name</span></span>  <br/> |<span data-ttu-id="0d16d-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="0d16d-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="0d16d-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0d16d-126">Validation File</span></span>  <br/> |<span data-ttu-id="0d16d-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="0d16d-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0d16d-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0d16d-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="0d16d-129">Falso</span><span class="sxs-lookup"><span data-stu-id="0d16d-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0d16d-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d16d-130">See also</span></span>



- [<span data-ttu-id="0d16d-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0d16d-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

