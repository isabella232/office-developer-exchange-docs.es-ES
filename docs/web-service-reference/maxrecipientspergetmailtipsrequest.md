---
title: MaxRecipientsPerGetMailTipsRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MaxRecipientsPerGetMailTipsRequest
api_type:
- schema
ms.assetid: 8ff5df18-1989-4217-b4c0-599232911d0c
description: El elemento MaxRecipientsPerGetMailTipsRequest indica el número máximo de destinatarios que se pueden pasar a la operación de GetMailTips.
ms.openlocfilehash: 4c873fe534582e582bf5b1c1d5fd2789616e056a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836386"
---
# <a name="maxrecipientspergetmailtipsrequest"></a><span data-ttu-id="75faa-103">MaxRecipientsPerGetMailTipsRequest</span><span class="sxs-lookup"><span data-stu-id="75faa-103">MaxRecipientsPerGetMailTipsRequest</span></span>

<span data-ttu-id="75faa-104">El elemento **MaxRecipientsPerGetMailTipsRequest** indica el número máximo de destinatarios que se pueden pasar a la [operación de GetMailTips](getmailtips-operation.md).</span><span class="sxs-lookup"><span data-stu-id="75faa-104">The **MaxRecipientsPerGetMailTipsRequest** element indicates the maximum number of recipients that can be passed to the [GetMailTips operation](getmailtips-operation.md).</span></span>
  
```XML
<MaxRecipientsPerGetMailTipsRequest/>
```

 <span data-ttu-id="75faa-105">**int**</span><span class="sxs-lookup"><span data-stu-id="75faa-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="75faa-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="75faa-106">Attributes and elements</span></span>

<span data-ttu-id="75faa-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="75faa-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="75faa-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="75faa-108">Attributes</span></span>

<span data-ttu-id="75faa-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="75faa-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="75faa-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="75faa-110">Child elements</span></span>

<span data-ttu-id="75faa-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="75faa-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="75faa-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="75faa-112">Parent elements</span></span>

|<span data-ttu-id="75faa-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="75faa-113">**Element**</span></span>|<span data-ttu-id="75faa-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="75faa-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="75faa-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="75faa-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="75faa-116">Contiene información de configuración de servicio para el servicio de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="75faa-116">Contains service configuration information for the mail tips service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="75faa-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="75faa-117">Text value</span></span>

<span data-ttu-id="75faa-118">El valor de texto es un entero que representa el número máximo de destinatarios que se pueden pasar a la [operación de GetMailTips](getmailtips-operation.md).</span><span class="sxs-lookup"><span data-stu-id="75faa-118">The text value is an integer that represents the maximum number of recipients that can be passed to the [GetMailTips operation](getmailtips-operation.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="75faa-119">Notas</span><span class="sxs-lookup"><span data-stu-id="75faa-119">Remarks</span></span>

<span data-ttu-id="75faa-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="75faa-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="75faa-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="75faa-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="75faa-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="75faa-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="75faa-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="75faa-123">Schema Name</span></span>  <br/> |<span data-ttu-id="75faa-124">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="75faa-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="75faa-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="75faa-125">Validation File</span></span>  <br/> |<span data-ttu-id="75faa-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="75faa-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="75faa-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="75faa-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="75faa-128">False</span><span class="sxs-lookup"><span data-stu-id="75faa-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="75faa-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="75faa-129">See also</span></span>



[<span data-ttu-id="75faa-130">Operación GetMailTips</span><span class="sxs-lookup"><span data-stu-id="75faa-130">GetMailTips operation</span></span>](getmailtips-operation.md)


- [<span data-ttu-id="75faa-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="75faa-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

