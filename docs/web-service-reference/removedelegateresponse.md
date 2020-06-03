---
title: RemoveDelegateResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RemoveDelegateResponse
api_type:
- schema
ms.assetid: eef56c53-d0a7-4342-9ce6-4dbb6b1a1369
description: El elemento RemoveDelegateResponse contiene el estado y el resultado de una solicitud de operación RemoveDelegate.
ms.openlocfilehash: 4c7a8b81528435b72576c116bc97f611544c24d6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468939"
---
# <a name="removedelegateresponse"></a><span data-ttu-id="e641d-103">RemoveDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="e641d-103">RemoveDelegateResponse</span></span>

<span data-ttu-id="e641d-104">El elemento **RemoveDelegateResponse** contiene el estado y el resultado de una solicitud de [operación RemoveDelegate](removedelegate-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="e641d-104">The **RemoveDelegateResponse** element contains the status and result of a [RemoveDelegate operation](removedelegate-operation.md) request.</span></span> 
  
```xml
<RemoveDelegateResponse>
   <ResponseMessages/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</RemoveDelegateResponse>
```

 <span data-ttu-id="e641d-105">**RemoveDelegateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="e641d-105">**RemoveDelegateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e641d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e641d-106">Attributes and elements</span></span>

<span data-ttu-id="e641d-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e641d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e641d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e641d-108">Attributes</span></span>

<span data-ttu-id="e641d-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e641d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e641d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e641d-110">Child elements</span></span>

|<span data-ttu-id="e641d-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e641d-111">**Element**</span></span>|<span data-ttu-id="e641d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e641d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e641d-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="e641d-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="e641d-114">Contiene los mensajes de respuesta para una solicitud de administración de un delegado de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e641d-114">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
|[<span data-ttu-id="e641d-115">MessageText</span><span class="sxs-lookup"><span data-stu-id="e641d-115">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="e641d-116">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e641d-116">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="e641d-117">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e641d-117">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="e641d-118">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e641d-118">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="e641d-119">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="e641d-119">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="e641d-120">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="e641d-120">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="e641d-121">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="e641d-121">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="e641d-122">MessageXml</span><span class="sxs-lookup"><span data-stu-id="e641d-122">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="e641d-123">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="e641d-123">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e641d-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e641d-124">Parent elements</span></span>

<span data-ttu-id="e641d-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e641d-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e641d-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e641d-126">Remarks</span></span>

<span data-ttu-id="e641d-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="e641d-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e641d-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e641d-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e641d-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="e641d-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e641d-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e641d-130">Schema Name</span></span>  <br/> |<span data-ttu-id="e641d-131">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="e641d-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e641d-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e641d-132">Validation File</span></span>  <br/> |<span data-ttu-id="e641d-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="e641d-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e641d-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e641d-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="e641d-135">Falso</span><span class="sxs-lookup"><span data-stu-id="e641d-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e641d-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="e641d-136">See also</span></span>



[<span data-ttu-id="e641d-137">Operación RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="e641d-137">RemoveDelegate operation</span></span>](removedelegate-operation.md)


- [<span data-ttu-id="e641d-138">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e641d-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

