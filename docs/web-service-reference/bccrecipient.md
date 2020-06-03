---
title: BccRecipient
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BccRecipient
api_type:
- schema
ms.assetid: 4ef0cff5-8a5a-4d76-9d2b-938774d8fc1b
description: El elemento BccRecipient representa un destinatario que recibe una copia oculta (CCO) de un mensaje de correo electrónico.
ms.openlocfilehash: 8296af1d74338bdfb1f4cb7bc7449ad91a9cd531
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461530"
---
# <a name="bccrecipient"></a><span data-ttu-id="e46b7-103">BccRecipient</span><span class="sxs-lookup"><span data-stu-id="e46b7-103">BccRecipient</span></span>

<span data-ttu-id="e46b7-104">El elemento **BccRecipient** representa un destinatario que recibe una copia oculta (CCO) de un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="e46b7-104">The **BccRecipient** element represents a recipient to receive a blind carbon copy (Bcc) of an e-mail message.</span></span> 
  
```XML
<BccRecipient>true | false</BccRecipient>
```

 <span data-ttu-id="e46b7-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="e46b7-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e46b7-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e46b7-106">Attributes and elements</span></span>

<span data-ttu-id="e46b7-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e46b7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e46b7-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e46b7-108">Attributes</span></span>

<span data-ttu-id="e46b7-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e46b7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e46b7-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e46b7-110">Child elements</span></span>

<span data-ttu-id="e46b7-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e46b7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e46b7-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e46b7-112">Parent elements</span></span>

|<span data-ttu-id="e46b7-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e46b7-113">**Element**</span></span>|<span data-ttu-id="e46b7-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e46b7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e46b7-115">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="e46b7-115">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="e46b7-116">Contiene información de un evento único para un destinatario.</span><span class="sxs-lookup"><span data-stu-id="e46b7-116">Contains information for a single event for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e46b7-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e46b7-117">Text value</span></span>

<span data-ttu-id="e46b7-118">Este elemento puede ser **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="e46b7-118">This element can be either **true** or **false**.</span></span> <span data-ttu-id="e46b7-119">Un valor de **true** indica que el destinatario ha copiado el carbono ciego; un valor de **false** indica que el destinatario no es una copia oculta.</span><span class="sxs-lookup"><span data-stu-id="e46b7-119">A value of **true** indicates that the recipient is blind carbon copied; a value of **false** indicates that the recipient is not blind carbon copied.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e46b7-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e46b7-120">Remarks</span></span>

<span data-ttu-id="e46b7-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e46b7-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e46b7-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e46b7-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e46b7-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="e46b7-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e46b7-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e46b7-124">Schema Name</span></span>  <br/> |<span data-ttu-id="e46b7-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e46b7-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="e46b7-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e46b7-126">Validation File</span></span>  <br/> |<span data-ttu-id="e46b7-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="e46b7-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e46b7-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e46b7-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="e46b7-129">Falso</span><span class="sxs-lookup"><span data-stu-id="e46b7-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e46b7-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="e46b7-130">See also</span></span>



- [<span data-ttu-id="e46b7-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e46b7-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

