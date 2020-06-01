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
description: El elemento Recipients representa una colección de destinatarios que reciben una copia del mensaje.
ms.openlocfilehash: 0e18152a8143b888ad27f48137c06613694f5713
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463877"
---
# <a name="recipients-arrayofrecipientstype"></a><span data-ttu-id="bf328-103">Recipients (ArrayOfRecipientsType)</span><span class="sxs-lookup"><span data-stu-id="bf328-103">Recipients (ArrayOfRecipientsType)</span></span>

<span data-ttu-id="bf328-104">El elemento **Recipients** representa una colección de destinatarios que reciben una copia del mensaje.</span><span class="sxs-lookup"><span data-stu-id="bf328-104">The **Recipients** element represents a collection of recipients that receive a copy of the message.</span></span> 
  
```XML
<Recipients>
   <Mailbox/>
</Recipients>
```

 <span data-ttu-id="bf328-105">**ArrayOfRecipientsType**</span><span class="sxs-lookup"><span data-stu-id="bf328-105">**ArrayOfRecipientsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bf328-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="bf328-106">Attributes and elements</span></span>

<span data-ttu-id="bf328-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="bf328-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bf328-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="bf328-108">Attributes</span></span>

<span data-ttu-id="bf328-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="bf328-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bf328-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bf328-110">Child elements</span></span>

|<span data-ttu-id="bf328-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bf328-111">**Element**</span></span>|<span data-ttu-id="bf328-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bf328-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bf328-113">Buzón</span><span class="sxs-lookup"><span data-stu-id="bf328-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="bf328-114">Identifica un objeto de Active Directory habilitado para correo.</span><span class="sxs-lookup"><span data-stu-id="bf328-114">Identifies a mail-enabled Active Directory object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bf328-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bf328-115">Parent elements</span></span>

|<span data-ttu-id="bf328-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bf328-116">**Element**</span></span>|<span data-ttu-id="bf328-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bf328-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bf328-118">GetMailTips</span><span class="sxs-lookup"><span data-stu-id="bf328-118">GetMailTips</span></span>](getmailtips.md) <br/> |<span data-ttu-id="bf328-119">Contiene los destinatarios y los tipos de sugerencias de correo que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="bf328-119">Contains the recipients and types of mail tips to retrieve.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bf328-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="bf328-120">Text value</span></span>

<span data-ttu-id="bf328-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bf328-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bf328-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bf328-122">Remarks</span></span>

<span data-ttu-id="bf328-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="bf328-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bf328-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="bf328-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bf328-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="bf328-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bf328-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="bf328-126">Schema Name</span></span>  <br/> |<span data-ttu-id="bf328-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="bf328-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="bf328-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="bf328-128">Validation File</span></span>  <br/> |<span data-ttu-id="bf328-129">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="bf328-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bf328-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="bf328-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="bf328-131">Falso</span><span class="sxs-lookup"><span data-stu-id="bf328-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bf328-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf328-132">See also</span></span>



- [<span data-ttu-id="bf328-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="bf328-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

