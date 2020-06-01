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
description: El elemento MaxRecipientsPerGetMailTipsRequest indica el número máximo de destinatarios que se pueden pasar a la operación GetMailTips.
ms.openlocfilehash: cec343182b364fce040d5e32928cbeb569a22124
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468407"
---
# <a name="maxrecipientspergetmailtipsrequest"></a><span data-ttu-id="e2469-103">MaxRecipientsPerGetMailTipsRequest</span><span class="sxs-lookup"><span data-stu-id="e2469-103">MaxRecipientsPerGetMailTipsRequest</span></span>

<span data-ttu-id="e2469-104">El elemento **MaxRecipientsPerGetMailTipsRequest** indica el número máximo de destinatarios que se pueden pasar a la [operación GetMailTips](getmailtips-operation.md).</span><span class="sxs-lookup"><span data-stu-id="e2469-104">The **MaxRecipientsPerGetMailTipsRequest** element indicates the maximum number of recipients that can be passed to the [GetMailTips operation](getmailtips-operation.md).</span></span>
  
```XML
<MaxRecipientsPerGetMailTipsRequest/>
```

 <span data-ttu-id="e2469-105">**int**</span><span class="sxs-lookup"><span data-stu-id="e2469-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e2469-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e2469-106">Attributes and elements</span></span>

<span data-ttu-id="e2469-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e2469-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e2469-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e2469-108">Attributes</span></span>

<span data-ttu-id="e2469-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e2469-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e2469-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e2469-110">Child elements</span></span>

<span data-ttu-id="e2469-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e2469-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e2469-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e2469-112">Parent elements</span></span>

|<span data-ttu-id="e2469-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e2469-113">**Element**</span></span>|<span data-ttu-id="e2469-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e2469-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e2469-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="e2469-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="e2469-116">Contiene información de configuración del servicio para el servicio de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="e2469-116">Contains service configuration information for the mail tips service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e2469-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e2469-117">Text value</span></span>

<span data-ttu-id="e2469-118">El valor de texto es un entero que representa el número máximo de destinatarios que se pueden pasar a la [operación GetMailTips](getmailtips-operation.md).</span><span class="sxs-lookup"><span data-stu-id="e2469-118">The text value is an integer that represents the maximum number of recipients that can be passed to the [GetMailTips operation](getmailtips-operation.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e2469-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e2469-119">Remarks</span></span>

<span data-ttu-id="e2469-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e2469-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e2469-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e2469-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e2469-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="e2469-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e2469-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e2469-123">Schema Name</span></span>  <br/> |<span data-ttu-id="e2469-124">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e2469-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="e2469-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e2469-125">Validation File</span></span>  <br/> |<span data-ttu-id="e2469-126">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="e2469-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e2469-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e2469-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="e2469-128">Falso</span><span class="sxs-lookup"><span data-stu-id="e2469-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e2469-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2469-129">See also</span></span>



[<span data-ttu-id="e2469-130">Operación GetMailTips</span><span class="sxs-lookup"><span data-stu-id="e2469-130">GetMailTips operation</span></span>](getmailtips-operation.md)


- [<span data-ttu-id="e2469-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e2469-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

