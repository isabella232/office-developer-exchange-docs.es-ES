---
title: UpdateDelegateResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateDelegateResponse
api_type:
- schema
ms.assetid: cd336add-fbcc-4f61-9867-d4c08a60e142
description: El elemento UpdateDelegateResponse contiene el estado y el resultado de una solicitud de operación UpdateDelegate.
ms.openlocfilehash: b90dd7d8011cf75831481b8f2b92df80d9a67d31
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840798"
---
# <a name="updatedelegateresponse"></a><span data-ttu-id="0b21d-103">UpdateDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="0b21d-103">UpdateDelegateResponse</span></span>

<span data-ttu-id="0b21d-104">El elemento **UpdateDelegateResponse** contiene el estado y el resultado de una solicitud de [operación UpdateDelegate](updatedelegate-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="0b21d-104">The **UpdateDelegateResponse** element contains the status and result of an [UpdateDelegate operation](updatedelegate-operation.md) request.</span></span> 
  
```xml
<UpdateDelegateResponseMessage>
   <ResponseMessages/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</UpdateDelegateResponseMessage>
```

 <span data-ttu-id="0b21d-105">**UpdateDelegateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="0b21d-105">**UpdateDelegateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0b21d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0b21d-106">Attributes and elements</span></span>

<span data-ttu-id="0b21d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0b21d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0b21d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0b21d-108">Attributes</span></span>

<span data-ttu-id="0b21d-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0b21d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0b21d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0b21d-110">Child elements</span></span>

|<span data-ttu-id="0b21d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="0b21d-111">**Element**</span></span>|<span data-ttu-id="0b21d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0b21d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0b21d-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="0b21d-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="0b21d-114">Contiene los mensajes de respuesta para una solicitud de administración de servicios Web de Exchange delegado.</span><span class="sxs-lookup"><span data-stu-id="0b21d-114">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
|[<span data-ttu-id="0b21d-115">MessageText</span><span class="sxs-lookup"><span data-stu-id="0b21d-115">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="0b21d-116">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0b21d-116">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="0b21d-117">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0b21d-117">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="0b21d-118">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0b21d-118">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="0b21d-119">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0b21d-119">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="0b21d-120">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="0b21d-120">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="0b21d-121">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="0b21d-121">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="0b21d-122">MessageXml</span><span class="sxs-lookup"><span data-stu-id="0b21d-122">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="0b21d-123">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="0b21d-123">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0b21d-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0b21d-124">Parent elements</span></span>

<span data-ttu-id="0b21d-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0b21d-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0b21d-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0b21d-126">Remarks</span></span>

<span data-ttu-id="0b21d-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="0b21d-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0b21d-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0b21d-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0b21d-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0b21d-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0b21d-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0b21d-130">Schema Name</span></span>  <br/> |<span data-ttu-id="0b21d-131">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="0b21d-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0b21d-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0b21d-132">Validation File</span></span>  <br/> |<span data-ttu-id="0b21d-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0b21d-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0b21d-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0b21d-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="0b21d-135">False</span><span class="sxs-lookup"><span data-stu-id="0b21d-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0b21d-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b21d-136">See also</span></span>



[<span data-ttu-id="0b21d-137">Operación UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="0b21d-137">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="0b21d-138">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="0b21d-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

