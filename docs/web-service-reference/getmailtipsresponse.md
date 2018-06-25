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
ms.openlocfilehash: e7a18e8818761af931d32b26aeaf58a2853fa684
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764903"
---
# <a name="getmailtipsresponse"></a><span data-ttu-id="91645-103">GetMailTipsResponse</span><span class="sxs-lookup"><span data-stu-id="91645-103">GetMailTipsResponse</span></span>

<span data-ttu-id="91645-104">El elemento **GetMailTipsResponse** representa el mensaje de respuesta para una [operación de GetMailTips](getmailtips-operation.md).</span><span class="sxs-lookup"><span data-stu-id="91645-104">The **GetMailTipsResponse** element represents the response message for a [GetMailTips operation](getmailtips-operation.md).</span></span>
  
```XML
<GetMailTipsResponse>
   <ResponseMessages/>
</GetMailTipsResponse>
```

 <span data-ttu-id="91645-105">**GetMailTipsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="91645-105">**GetMailTipsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="91645-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="91645-106">Attributes and elements</span></span>

<span data-ttu-id="91645-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="91645-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="91645-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="91645-108">Attributes</span></span>

<span data-ttu-id="91645-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="91645-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="91645-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="91645-110">Child elements</span></span>

|<span data-ttu-id="91645-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="91645-111">**Element**</span></span>|<span data-ttu-id="91645-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="91645-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="91645-113">ResponseMessages (ArrayOfMailTipsResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="91645-113">ResponseMessages (ArrayOfMailTipsResponseMessageType)</span></span>](responsemessages-arrayofmailtipsresponsemessagetype.md) <br/> |<span data-ttu-id="91645-114">Representa una lista de los mensajes de respuesta de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="91645-114">Represents a list of mail tips response messages.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="91645-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="91645-115">Parent elements</span></span>

<span data-ttu-id="91645-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="91645-116">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="91645-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="91645-117">Text value</span></span>

<span data-ttu-id="91645-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="91645-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="91645-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="91645-119">Remarks</span></span>

<span data-ttu-id="91645-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="91645-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="91645-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="91645-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="91645-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="91645-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="91645-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="91645-123">Schema Name</span></span>  <br/> |<span data-ttu-id="91645-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="91645-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="91645-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="91645-125">Validation File</span></span>  <br/> |<span data-ttu-id="91645-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="91645-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="91645-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="91645-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="91645-128">False</span><span class="sxs-lookup"><span data-stu-id="91645-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="91645-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="91645-129">See also</span></span>



[<span data-ttu-id="91645-130">Operación GetMailTips</span><span class="sxs-lookup"><span data-stu-id="91645-130">GetMailTips operation</span></span>](getmailtips-operation.md)


- [<span data-ttu-id="91645-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="91645-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

