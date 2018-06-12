---
title: Recipients (ArrayOfRecipientsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Recipients
api_type:
- schema
ms.assetid: f4b71403-cbae-4176-8b2e-3597048c057b
description: El elemento de destinatarios representa una colección de los destinatarios que reciben una copia del mensaje.
ms.openlocfilehash: b24a029bfacd6cc40e85a201b8ca90efd7790e9f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836991"
---
# <a name="recipients-arrayofrecipientstype"></a><span data-ttu-id="bb1d5-103">Recipients (ArrayOfRecipientsType)</span><span class="sxs-lookup"><span data-stu-id="bb1d5-103">Recipients (ArrayOfRecipientsType)</span></span>

<span data-ttu-id="bb1d5-104">El elemento de **destinatarios** representa una colección de los destinatarios que reciben una copia del mensaje.</span><span class="sxs-lookup"><span data-stu-id="bb1d5-104">The **Recipients** element represents a collection of recipients that receive a copy of the message.</span></span> 
  
```XML
<Recipients>
   <Mailbox/>
</Recipients>
```

 <span data-ttu-id="bb1d5-105">**ArrayOfRecipientsType**</span><span class="sxs-lookup"><span data-stu-id="bb1d5-105">**ArrayOfRecipientsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bb1d5-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="bb1d5-106">Attributes and elements</span></span>

<span data-ttu-id="bb1d5-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="bb1d5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bb1d5-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="bb1d5-108">Attributes</span></span>

<span data-ttu-id="bb1d5-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bb1d5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bb1d5-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bb1d5-110">Child elements</span></span>

|<span data-ttu-id="bb1d5-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="bb1d5-111">**Element**</span></span>|<span data-ttu-id="bb1d5-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bb1d5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bb1d5-113">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="bb1d5-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="bb1d5-114">Identifica un objeto de Active Directory habilitados para correo.</span><span class="sxs-lookup"><span data-stu-id="bb1d5-114">Identifies a mail-enabled Active Directory object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bb1d5-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bb1d5-115">Parent elements</span></span>

|<span data-ttu-id="bb1d5-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="bb1d5-116">**Element**</span></span>|<span data-ttu-id="bb1d5-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bb1d5-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bb1d5-118">GetMailTips</span><span class="sxs-lookup"><span data-stu-id="bb1d5-118">GetMailTips</span></span>](getmailtips.md) <br/> |<span data-ttu-id="bb1d5-119">Contiene los destinatarios y los tipos de sugerencias de correo para recuperar.</span><span class="sxs-lookup"><span data-stu-id="bb1d5-119">Contains the recipients and types of mail tips to retrieve.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bb1d5-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="bb1d5-120">Text value</span></span>

<span data-ttu-id="bb1d5-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bb1d5-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bb1d5-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb1d5-122">Remarks</span></span>

<span data-ttu-id="bb1d5-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="bb1d5-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bb1d5-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="bb1d5-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bb1d5-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bb1d5-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bb1d5-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="bb1d5-126">Schema Name</span></span>  <br/> |<span data-ttu-id="bb1d5-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="bb1d5-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="bb1d5-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="bb1d5-128">Validation File</span></span>  <br/> |<span data-ttu-id="bb1d5-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bb1d5-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bb1d5-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="bb1d5-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="bb1d5-131">False</span><span class="sxs-lookup"><span data-stu-id="bb1d5-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bb1d5-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="bb1d5-132">See also</span></span>



- [<span data-ttu-id="bb1d5-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="bb1d5-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

