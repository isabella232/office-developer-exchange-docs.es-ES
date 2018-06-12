---
title: InvalidRecipient (sugerencias de correo electrónico)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InvalidRecipient
api_type:
- schema
ms.assetid: 48959a99-bb0d-4004-963e-5a5baaa96476
description: El elemento InvalidRecipient indica si el destinatario no es válido.
ms.openlocfilehash: addb86ece2be3091ac55a52ee2f16f5c5f72ae41
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835958"
---
# <a name="invalidrecipient-mailtips"></a><span data-ttu-id="6361a-103">InvalidRecipient (sugerencias de correo electrónico)</span><span class="sxs-lookup"><span data-stu-id="6361a-103">InvalidRecipient (MailTips)</span></span>

<span data-ttu-id="6361a-104">El elemento **InvalidRecipient** indica si el destinatario no es válido.</span><span class="sxs-lookup"><span data-stu-id="6361a-104">The **InvalidRecipient** element indicates whether the recipient is invalid.</span></span> 
  
```XML
<InvalidRecipient>true | false</InvalidRecipient>
```

 <span data-ttu-id="6361a-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="6361a-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6361a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6361a-106">Attributes and elements</span></span>

<span data-ttu-id="6361a-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6361a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6361a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6361a-108">Attributes</span></span>

<span data-ttu-id="6361a-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6361a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6361a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6361a-110">Child elements</span></span>

<span data-ttu-id="6361a-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6361a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6361a-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6361a-112">Parent elements</span></span>

|<span data-ttu-id="6361a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6361a-113">**Element**</span></span>|<span data-ttu-id="6361a-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6361a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6361a-115">Sugerencias de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="6361a-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="6361a-116">Representa los valores de distintos tipos de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="6361a-116">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6361a-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="6361a-117">Text value</span></span>

<span data-ttu-id="6361a-118">El valor de texto de este elemento es **true** si el destinatario no es válido.</span><span class="sxs-lookup"><span data-stu-id="6361a-118">The text value of this element is **true** if the recipient is invalid.</span></span> <span data-ttu-id="6361a-119">El valor es **false** si el destinatario no es válido.</span><span class="sxs-lookup"><span data-stu-id="6361a-119">The value is **false** if the recipient is not invalid.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6361a-120">Notas</span><span class="sxs-lookup"><span data-stu-id="6361a-120">Remarks</span></span>

<span data-ttu-id="6361a-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="6361a-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6361a-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6361a-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6361a-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6361a-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6361a-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6361a-124">Schema Name</span></span>  <br/> |<span data-ttu-id="6361a-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="6361a-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="6361a-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6361a-126">Validation File</span></span>  <br/> |<span data-ttu-id="6361a-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6361a-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6361a-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6361a-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="6361a-129">False</span><span class="sxs-lookup"><span data-stu-id="6361a-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6361a-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="6361a-130">See also</span></span>



- [<span data-ttu-id="6361a-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="6361a-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

