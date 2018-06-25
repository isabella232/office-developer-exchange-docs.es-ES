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
description: El elemento HiddenRecipient indica que el destinatario se ha agregado una directiva de la organización que debería estar oculto de los usuarios sin privilegios.
ms.openlocfilehash: 73b2e3e39c675cf3e2bc56105b1e76009d4a2451
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835810"
---
# <a name="hiddenrecipient"></a><span data-ttu-id="56833-103">HiddenRecipient</span><span class="sxs-lookup"><span data-stu-id="56833-103">HiddenRecipient</span></span>

<span data-ttu-id="56833-104">El elemento **HiddenRecipient** indica que el destinatario se ha agregado una directiva de la organización que debería estar oculto de los usuarios sin privilegios.</span><span class="sxs-lookup"><span data-stu-id="56833-104">The **HiddenRecipient** element indicates that the recipient was added by an organization policy that should be hidden from unprivileged users.</span></span> 
  
```XML
<HiddenRecipient>true | false</HiddenRecipient>
```

 <span data-ttu-id="56833-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="56833-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="56833-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="56833-106">Attributes and elements</span></span>

<span data-ttu-id="56833-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="56833-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="56833-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="56833-108">Attributes</span></span>

<span data-ttu-id="56833-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="56833-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="56833-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="56833-110">Child elements</span></span>

<span data-ttu-id="56833-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="56833-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="56833-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="56833-112">Parent elements</span></span>

|<span data-ttu-id="56833-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="56833-113">**Element**</span></span>|<span data-ttu-id="56833-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="56833-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="56833-115">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="56833-115">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="56833-116">Contiene información de un solo evento de un destinatario.</span><span class="sxs-lookup"><span data-stu-id="56833-116">Contains information for a single event for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="56833-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="56833-117">Text value</span></span>

<span data-ttu-id="56833-118">Este elemento puede ser **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="56833-118">This element can be either **true** or **false**.</span></span> <span data-ttu-id="56833-119">Un valor de **true** indica que el usuario se ha agregado una directiva de la organización; un valor de **false** indica que el usuario no se ha agregado una directiva de la organización.</span><span class="sxs-lookup"><span data-stu-id="56833-119">A value of **true** indicates that the user was added by an organization policy; a value of **false** indicates that the user was not added by an organization policy.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="56833-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="56833-120">Remarks</span></span>

<span data-ttu-id="56833-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="56833-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="56833-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="56833-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="56833-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="56833-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="56833-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="56833-124">Schema Name</span></span>  <br/> |<span data-ttu-id="56833-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="56833-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="56833-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="56833-126">Validation File</span></span>  <br/> |<span data-ttu-id="56833-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="56833-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="56833-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="56833-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="56833-129">False</span><span class="sxs-lookup"><span data-stu-id="56833-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="56833-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="56833-130">See also</span></span>



- [<span data-ttu-id="56833-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="56833-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

