---
title: DeleteItemResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteItemResponse
api_type:
- schema
ms.assetid: 86463d66-fe47-4a19-a81b-e24841e816ab
description: El elemento DeleteItemResponse define una respuesta a una única solicitud DeleteItem.
ms.openlocfilehash: 8a35033c744fbcb0829d2c79a8d79557f77137bb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764103"
---
# <a name="deleteitemresponse"></a><span data-ttu-id="aadb8-103">DeleteItemResponse</span><span class="sxs-lookup"><span data-stu-id="aadb8-103">DeleteItemResponse</span></span>

<span data-ttu-id="aadb8-104">El elemento **DeleteItemResponse** define una respuesta a una única solicitud DeleteItem.</span><span class="sxs-lookup"><span data-stu-id="aadb8-104">The **DeleteItemResponse** element defines a response to a single DeleteItem request.</span></span> 
  
```xml
<DeleteItemResponse>
   <ResponseMessages/>
</DeleteItemResponse>
```

 <span data-ttu-id="aadb8-105">**DeleteItemResponseType**</span><span class="sxs-lookup"><span data-stu-id="aadb8-105">**DeleteItemResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aadb8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="aadb8-106">Attributes and elements</span></span>

<span data-ttu-id="aadb8-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="aadb8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aadb8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="aadb8-108">Attributes</span></span>

<span data-ttu-id="aadb8-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="aadb8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aadb8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="aadb8-110">Child elements</span></span>

|<span data-ttu-id="aadb8-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="aadb8-111">**Element**</span></span>|<span data-ttu-id="aadb8-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aadb8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aadb8-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="aadb8-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="aadb8-114">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="aadb8-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="aadb8-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="aadb8-115">Parent elements</span></span>

<span data-ttu-id="aadb8-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="aadb8-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aadb8-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aadb8-117">Remarks</span></span>

<span data-ttu-id="aadb8-118">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="aadb8-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aadb8-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="aadb8-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aadb8-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="aadb8-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="aadb8-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="aadb8-121">Schema Name</span></span>  <br/> |<span data-ttu-id="aadb8-122">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="aadb8-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="aadb8-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="aadb8-123">Validation File</span></span>  <br/> |<span data-ttu-id="aadb8-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="aadb8-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="aadb8-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="aadb8-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="aadb8-126">False</span><span class="sxs-lookup"><span data-stu-id="aadb8-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aadb8-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="aadb8-127">See also</span></span>

- [<span data-ttu-id="aadb8-128">Operación DeleteItem</span><span class="sxs-lookup"><span data-stu-id="aadb8-128">DeleteItem operation</span></span>](deleteitem-operation.md)  
- [<span data-ttu-id="aadb8-129">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="aadb8-129">DeleteItem</span></span>](deleteitem.md)
- [<span data-ttu-id="aadb8-130">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="aadb8-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

