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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835958"
---
# <a name="invalidrecipient-mailtips"></a><span data-ttu-id="230a9-103">InvalidRecipient (sugerencias de correo electrónico)</span><span class="sxs-lookup"><span data-stu-id="230a9-103">InvalidRecipient (MailTips)</span></span>

<span data-ttu-id="230a9-104">El elemento **InvalidRecipient** indica si el destinatario no es válido.</span><span class="sxs-lookup"><span data-stu-id="230a9-104">The **InvalidRecipient** element indicates whether the recipient is invalid.</span></span> 
  
```XML
<InvalidRecipient>true | false</InvalidRecipient>
```

 <span data-ttu-id="230a9-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="230a9-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="230a9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="230a9-106">Attributes and elements</span></span>

<span data-ttu-id="230a9-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="230a9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="230a9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="230a9-108">Attributes</span></span>

<span data-ttu-id="230a9-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="230a9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="230a9-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="230a9-110">Child elements</span></span>

<span data-ttu-id="230a9-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="230a9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="230a9-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="230a9-112">Parent elements</span></span>

|<span data-ttu-id="230a9-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="230a9-113">**Element**</span></span>|<span data-ttu-id="230a9-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="230a9-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="230a9-115">Sugerencias de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="230a9-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="230a9-116">Representa los valores de distintos tipos de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="230a9-116">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="230a9-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="230a9-117">Text value</span></span>

<span data-ttu-id="230a9-118">El valor de texto de este elemento es **true** si el destinatario no es válido.</span><span class="sxs-lookup"><span data-stu-id="230a9-118">The text value of this element is **true** if the recipient is invalid.</span></span> <span data-ttu-id="230a9-119">El valor es **false** si el destinatario no es válido.</span><span class="sxs-lookup"><span data-stu-id="230a9-119">The value is **false** if the recipient is not invalid.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="230a9-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="230a9-120">Remarks</span></span>

<span data-ttu-id="230a9-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="230a9-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="230a9-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="230a9-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="230a9-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="230a9-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="230a9-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="230a9-124">Schema Name</span></span>  <br/> |<span data-ttu-id="230a9-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="230a9-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="230a9-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="230a9-126">Validation File</span></span>  <br/> |<span data-ttu-id="230a9-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="230a9-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="230a9-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="230a9-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="230a9-129">False</span><span class="sxs-lookup"><span data-stu-id="230a9-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="230a9-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="230a9-130">See also</span></span>



- [<span data-ttu-id="230a9-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="230a9-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

