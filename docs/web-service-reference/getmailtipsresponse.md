---
title: GetMailTipsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetMailTipsResponse
api_type:
- schema
ms.assetid: fe270e34-566e-4f9e-9e73-fbf38e06436d
description: El elemento GetMailTipsResponse representa el mensaje de respuesta para una operación de GetMailTips.
ms.openlocfilehash: 2c0dcfe4e2deddcf9a6f4bb9d68d59115c171796
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458610"
---
# <a name="getmailtipsresponse"></a><span data-ttu-id="e0767-103">GetMailTipsResponse</span><span class="sxs-lookup"><span data-stu-id="e0767-103">GetMailTipsResponse</span></span>

<span data-ttu-id="e0767-104">El elemento **GetMailTipsResponse** representa el mensaje de respuesta para una [operación de GetMailTips](getmailtips-operation.md).</span><span class="sxs-lookup"><span data-stu-id="e0767-104">The **GetMailTipsResponse** element represents the response message for a [GetMailTips operation](getmailtips-operation.md).</span></span>
  
```XML
<GetMailTipsResponse>
   <ResponseMessages/>
</GetMailTipsResponse>
```

 <span data-ttu-id="e0767-105">**GetMailTipsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="e0767-105">**GetMailTipsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e0767-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e0767-106">Attributes and elements</span></span>

<span data-ttu-id="e0767-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e0767-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e0767-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e0767-108">Attributes</span></span>

<span data-ttu-id="e0767-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e0767-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e0767-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e0767-110">Child elements</span></span>

|<span data-ttu-id="e0767-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e0767-111">**Element**</span></span>|<span data-ttu-id="e0767-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e0767-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e0767-113">ResponseMessages (ArrayOfMailTipsResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="e0767-113">ResponseMessages (ArrayOfMailTipsResponseMessageType)</span></span>](responsemessages-arrayofmailtipsresponsemessagetype.md) <br/> |<span data-ttu-id="e0767-114">Representa una lista de los mensajes de respuesta de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="e0767-114">Represents a list of mail tips response messages.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e0767-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e0767-115">Parent elements</span></span>

<span data-ttu-id="e0767-116">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e0767-116">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="e0767-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e0767-117">Text value</span></span>

<span data-ttu-id="e0767-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e0767-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e0767-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e0767-119">Remarks</span></span>

<span data-ttu-id="e0767-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e0767-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e0767-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e0767-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0767-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="e0767-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e0767-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e0767-123">Schema Name</span></span>  <br/> |<span data-ttu-id="e0767-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="e0767-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e0767-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e0767-125">Validation File</span></span>  <br/> |<span data-ttu-id="e0767-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="e0767-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e0767-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e0767-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="e0767-128">Falso</span><span class="sxs-lookup"><span data-stu-id="e0767-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e0767-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0767-129">See also</span></span>



[<span data-ttu-id="e0767-130">Operación GetMailTips</span><span class="sxs-lookup"><span data-stu-id="e0767-130">GetMailTips operation</span></span>](getmailtips-operation.md)


- [<span data-ttu-id="e0767-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e0767-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

