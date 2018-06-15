---
title: MaxMessageSize
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MaxMessageSize
api_type:
- schema
ms.assetid: bb98ac72-9409-4332-81bb-ee3bebb9a00e
description: El elemento MaxMessageSize representa el tamaño máximo de mensaje que puede aceptar un destinatario.
ms.openlocfilehash: 13a5679a03420655356269a7e8b5e22950724164
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836383"
---
# <a name="maxmessagesize"></a><span data-ttu-id="2d4eb-103">MaxMessageSize</span><span class="sxs-lookup"><span data-stu-id="2d4eb-103">MaxMessageSize</span></span>

<span data-ttu-id="2d4eb-104">El elemento **MaxMessageSize** representa el tamaño máximo de mensaje que puede aceptar un destinatario.</span><span class="sxs-lookup"><span data-stu-id="2d4eb-104">The **MaxMessageSize** element represents the maximum message size a recipient can accept.</span></span> 
  
```XML
<MaxMessageSize/>
```

 <span data-ttu-id="2d4eb-105">**int**</span><span class="sxs-lookup"><span data-stu-id="2d4eb-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2d4eb-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2d4eb-106">Attributes and elements</span></span>

<span data-ttu-id="2d4eb-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2d4eb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2d4eb-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2d4eb-108">Attributes</span></span>

<span data-ttu-id="2d4eb-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2d4eb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2d4eb-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2d4eb-110">Child elements</span></span>

<span data-ttu-id="2d4eb-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2d4eb-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2d4eb-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2d4eb-112">Parent elements</span></span>

|<span data-ttu-id="2d4eb-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="2d4eb-113">**Element**</span></span>|<span data-ttu-id="2d4eb-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2d4eb-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2d4eb-115">Sugerencias de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="2d4eb-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="2d4eb-116">Representa los valores de distintos tipos de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="2d4eb-116">Represents values for various types of mail tips.</span></span>  <br/> |
|[<span data-ttu-id="2d4eb-117">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="2d4eb-117">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="2d4eb-118">Contiene información de configuración de servicio para el servicio de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="2d4eb-118">Contains service configuration information for the mail tips service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2d4eb-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="2d4eb-119">Text value</span></span>

<span data-ttu-id="2d4eb-120">El valor de texto es un número entero que representa el tamaño máximo de mensaje un destinatario puede aceptar.</span><span class="sxs-lookup"><span data-stu-id="2d4eb-120">The text value is an integer that represents the maximum message size a recipient can accept.</span></span> <span data-ttu-id="2d4eb-121">Este valor se puede medir en kilobytes o megabytes.</span><span class="sxs-lookup"><span data-stu-id="2d4eb-121">This value can be measured in kilobytes or megabytes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2d4eb-122">Notas</span><span class="sxs-lookup"><span data-stu-id="2d4eb-122">Remarks</span></span>

<span data-ttu-id="2d4eb-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="2d4eb-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2d4eb-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2d4eb-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2d4eb-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2d4eb-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2d4eb-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2d4eb-126">Schema Name</span></span>  <br/> |<span data-ttu-id="2d4eb-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="2d4eb-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="2d4eb-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2d4eb-128">Validation File</span></span>  <br/> |<span data-ttu-id="2d4eb-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2d4eb-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2d4eb-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2d4eb-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="2d4eb-131">False</span><span class="sxs-lookup"><span data-stu-id="2d4eb-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2d4eb-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="2d4eb-132">See also</span></span>



- [<span data-ttu-id="2d4eb-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="2d4eb-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
