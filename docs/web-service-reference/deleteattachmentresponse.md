---
title: DeleteAttachmentResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteAttachmentResponse
api_type:
- schema
ms.assetid: 24099a88-4ab6-4bf3-8ed5-efec8e07b9b9
description: El DeleteAttachmentResponse define una respuesta a una solicitud de DeleteAttachment.
ms.openlocfilehash: f1a6b0ebba7257d02ceeea024486dc002d299dff
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764077"
---
# <a name="deleteattachmentresponse"></a><span data-ttu-id="c713f-103">DeleteAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="c713f-103">DeleteAttachmentResponse</span></span>

<span data-ttu-id="c713f-104">El **DeleteAttachmentResponse** define una respuesta a una solicitud de DeleteAttachment.</span><span class="sxs-lookup"><span data-stu-id="c713f-104">The **DeleteAttachmentResponse** defines a response to a DeleteAttachment request.</span></span> 
  
```xml
<DeleteAttachmentResponse>
   <ResponseMessages/>
</DeleteAttachmentResponse>
```

<span data-ttu-id="c713f-105">**DeleteAttachmentResponseType**</span><span class="sxs-lookup"><span data-stu-id="c713f-105">**DeleteAttachmentResponseType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c713f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c713f-106">Attributes and elements</span></span>

<span data-ttu-id="c713f-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c713f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c713f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c713f-108">Attributes</span></span>

<span data-ttu-id="c713f-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c713f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c713f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c713f-110">Child elements</span></span>

|<span data-ttu-id="c713f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c713f-111">**Element**</span></span>|<span data-ttu-id="c713f-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c713f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c713f-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c713f-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="c713f-114">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c713f-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c713f-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c713f-115">Parent elements</span></span>

<span data-ttu-id="c713f-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c713f-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c713f-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c713f-117">Remarks</span></span>

<span data-ttu-id="c713f-118">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="c713f-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c713f-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c713f-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c713f-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c713f-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c713f-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c713f-121">Schema name</span></span>  <br/> |<span data-ttu-id="c713f-122">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="c713f-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c713f-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c713f-123">Validation file</span></span>  <br/> |<span data-ttu-id="c713f-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c713f-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c713f-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c713f-125">Can be empty</span></span>  <br/> |<span data-ttu-id="c713f-126">False</span><span class="sxs-lookup"><span data-stu-id="c713f-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c713f-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="c713f-127">See also</span></span>

- [<span data-ttu-id="c713f-128">Operación DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="c713f-128">DeleteAttachment operation</span></span>](deleteattachment-operation.md)  
- [<span data-ttu-id="c713f-129">DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="c713f-129">DeleteAttachment</span></span>](deleteattachment.md)
- [<span data-ttu-id="c713f-130">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c713f-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

