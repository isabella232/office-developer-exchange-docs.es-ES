---
title: ConvertIdResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConvertIdResponse
api_type:
- schema
ms.assetid: ac1f044f-04a4-42ef-b762-cac5cd37894d
description: El elemento ConvertIdResponse contiene una respuesta a una solicitud ConvertId. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 690f0f2109dfc36dd8f359b7cef1e65beb47fc6e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44452527"
---
# <a name="convertidresponse"></a><span data-ttu-id="45f5a-104">ConvertIdResponse</span><span class="sxs-lookup"><span data-stu-id="45f5a-104">ConvertIdResponse</span></span>

<span data-ttu-id="45f5a-105">El elemento **ConvertIdResponse** contiene una respuesta a una solicitud ConvertId.</span><span class="sxs-lookup"><span data-stu-id="45f5a-105">The **ConvertIdResponse** element contains a response to a ConvertId request.</span></span> <span data-ttu-id="45f5a-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="45f5a-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<ConvertIdResponse>
   <ResponseMessages/>
</ConvertIdResponse>
```

 <span data-ttu-id="45f5a-107">**ConvertIdResponseType**</span><span class="sxs-lookup"><span data-stu-id="45f5a-107">**ConvertIdResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="45f5a-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="45f5a-108">Attributes and elements</span></span>

<span data-ttu-id="45f5a-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="45f5a-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="45f5a-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="45f5a-110">Attributes</span></span>

<span data-ttu-id="45f5a-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="45f5a-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="45f5a-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="45f5a-112">Child elements</span></span>

|<span data-ttu-id="45f5a-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="45f5a-113">**Element**</span></span>|<span data-ttu-id="45f5a-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="45f5a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="45f5a-115">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="45f5a-115">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="45f5a-116">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="45f5a-116">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="45f5a-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="45f5a-117">Parent elements</span></span>

<span data-ttu-id="45f5a-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="45f5a-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="45f5a-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="45f5a-119">Remarks</span></span>

<span data-ttu-id="45f5a-120">Los mensajes de respuesta que se encuentran en el elemento [ResponseMessages](responsemessages.md) serán instancias de ConvertIdResponseMessageType.</span><span class="sxs-lookup"><span data-stu-id="45f5a-120">The response messages that are contained within the [ResponseMessages](responsemessages.md) element will be instances of ConvertIdResponseMessageType.</span></span> 
  
<span data-ttu-id="45f5a-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="45f5a-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="45f5a-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="45f5a-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="45f5a-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="45f5a-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="45f5a-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="45f5a-124">Schema Name</span></span>  <br/> |<span data-ttu-id="45f5a-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="45f5a-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="45f5a-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="45f5a-126">Validation File</span></span>  <br/> |<span data-ttu-id="45f5a-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="45f5a-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="45f5a-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="45f5a-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="45f5a-129">Falso</span><span class="sxs-lookup"><span data-stu-id="45f5a-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="45f5a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="45f5a-130">See also</span></span>



[<span data-ttu-id="45f5a-131">Operación ConvertId</span><span class="sxs-lookup"><span data-stu-id="45f5a-131">ConvertId operation</span></span>](convertid-operation.md)


- [<span data-ttu-id="45f5a-132">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="45f5a-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="45f5a-133">Convertir identificadores</span><span class="sxs-lookup"><span data-stu-id="45f5a-133">Converting Identifiers</span></span>](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

