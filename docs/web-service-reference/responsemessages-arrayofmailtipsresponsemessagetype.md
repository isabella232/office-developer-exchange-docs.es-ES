---
title: ResponseMessages (ArrayOfMailTipsResponseMessageType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResponseMessages
api_type:
- schema
ms.assetid: 00878187-fac2-45b9-ba1c-df7ffac71089
description: El elemento ResponseMessages representa una lista de los mensajes de respuesta de sugerencias de correo.
ms.openlocfilehash: 2db58029ead9332b832006bc81d751d77df54b07
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465453"
---
# <a name="responsemessages-arrayofmailtipsresponsemessagetype"></a><span data-ttu-id="3951c-103">ResponseMessages (ArrayOfMailTipsResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="3951c-103">ResponseMessages (ArrayOfMailTipsResponseMessageType)</span></span>

<span data-ttu-id="3951c-104">El elemento **ResponseMessages** representa una lista de los mensajes de respuesta de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="3951c-104">The **ResponseMessages** element represents a list of mail tips response messages.</span></span> 
  
```XML
<ResponseMessages>
   <MailTipsResponseMessageType/>
</ResponseMessages>
```

 <span data-ttu-id="3951c-105">**ArrayOfMailTipsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="3951c-105">**ArrayOfMailTipsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3951c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3951c-106">Attributes and elements</span></span>

<span data-ttu-id="3951c-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3951c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3951c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3951c-108">Attributes</span></span>

<span data-ttu-id="3951c-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3951c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3951c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3951c-110">Child elements</span></span>

|<span data-ttu-id="3951c-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3951c-111">**Element**</span></span>|<span data-ttu-id="3951c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3951c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3951c-113">MailTipsResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="3951c-113">MailTipsResponseMessageType</span></span>](mailtipsresponsemessagetype.md) <br/> |<span data-ttu-id="3951c-114">Representa la configuración de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="3951c-114">Represents mail tips settings.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3951c-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3951c-115">Parent elements</span></span>

|<span data-ttu-id="3951c-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3951c-116">**Element**</span></span>|<span data-ttu-id="3951c-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3951c-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3951c-118">GetMailTipsResponse</span><span class="sxs-lookup"><span data-stu-id="3951c-118">GetMailTipsResponse</span></span>](getmailtipsresponse.md) <br/> |<span data-ttu-id="3951c-119">Representa el mensaje de respuesta para la [operación GetMailTips](getmailtips-operation.md).</span><span class="sxs-lookup"><span data-stu-id="3951c-119">Represents the response message for the [GetMailTips operation](getmailtips-operation.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3951c-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3951c-120">Text value</span></span>

<span data-ttu-id="3951c-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3951c-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3951c-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3951c-122">Remarks</span></span>

<span data-ttu-id="3951c-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3951c-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3951c-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3951c-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3951c-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="3951c-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3951c-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3951c-126">Schema Name</span></span>  <br/> |<span data-ttu-id="3951c-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="3951c-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3951c-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3951c-128">Validation File</span></span>  <br/> |<span data-ttu-id="3951c-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="3951c-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3951c-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3951c-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="3951c-131">Falso</span><span class="sxs-lookup"><span data-stu-id="3951c-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3951c-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="3951c-132">See also</span></span>



[<span data-ttu-id="3951c-133">Operación GetMailTips</span><span class="sxs-lookup"><span data-stu-id="3951c-133">GetMailTips operation</span></span>](getmailtips-operation.md)


- [<span data-ttu-id="3951c-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="3951c-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

