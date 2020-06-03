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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468407"
---
# <a name="maxrecipientspergetmailtipsrequest"></a><span data-ttu-id="365e7-103">MaxRecipientsPerGetMailTipsRequest</span><span class="sxs-lookup"><span data-stu-id="365e7-103">MaxRecipientsPerGetMailTipsRequest</span></span>

<span data-ttu-id="365e7-104">El elemento **MaxRecipientsPerGetMailTipsRequest** indica el número máximo de destinatarios que se pueden pasar a la [operación GetMailTips](getmailtips-operation.md).</span><span class="sxs-lookup"><span data-stu-id="365e7-104">The **MaxRecipientsPerGetMailTipsRequest** element indicates the maximum number of recipients that can be passed to the [GetMailTips operation](getmailtips-operation.md).</span></span>
  
```XML
<MaxRecipientsPerGetMailTipsRequest/>
```

 <span data-ttu-id="365e7-105">**int**</span><span class="sxs-lookup"><span data-stu-id="365e7-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="365e7-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="365e7-106">Attributes and elements</span></span>

<span data-ttu-id="365e7-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="365e7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="365e7-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="365e7-108">Attributes</span></span>

<span data-ttu-id="365e7-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="365e7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="365e7-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="365e7-110">Child elements</span></span>

<span data-ttu-id="365e7-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="365e7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="365e7-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="365e7-112">Parent elements</span></span>

|<span data-ttu-id="365e7-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="365e7-113">**Element**</span></span>|<span data-ttu-id="365e7-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="365e7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="365e7-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="365e7-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="365e7-116">Contiene información de configuración del servicio para el servicio de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="365e7-116">Contains service configuration information for the mail tips service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="365e7-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="365e7-117">Text value</span></span>

<span data-ttu-id="365e7-118">El valor de texto es un entero que representa el número máximo de destinatarios que se pueden pasar a la [operación GetMailTips](getmailtips-operation.md).</span><span class="sxs-lookup"><span data-stu-id="365e7-118">The text value is an integer that represents the maximum number of recipients that can be passed to the [GetMailTips operation](getmailtips-operation.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="365e7-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="365e7-119">Remarks</span></span>

<span data-ttu-id="365e7-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="365e7-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="365e7-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="365e7-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="365e7-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="365e7-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="365e7-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="365e7-123">Schema Name</span></span>  <br/> |<span data-ttu-id="365e7-124">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="365e7-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="365e7-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="365e7-125">Validation File</span></span>  <br/> |<span data-ttu-id="365e7-126">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="365e7-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="365e7-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="365e7-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="365e7-128">Falso</span><span class="sxs-lookup"><span data-stu-id="365e7-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="365e7-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="365e7-129">See also</span></span>



[<span data-ttu-id="365e7-130">Operación GetMailTips</span><span class="sxs-lookup"><span data-stu-id="365e7-130">GetMailTips operation</span></span>](getmailtips-operation.md)


- [<span data-ttu-id="365e7-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="365e7-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

