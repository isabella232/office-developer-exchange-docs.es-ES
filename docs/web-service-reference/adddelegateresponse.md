---
title: AddDelegateResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AddDelegateResponse
api_type:
- schema
ms.assetid: d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429
description: El elemento AddDelegateResponse contiene el estado y el resultado de una solicitud de operación AddDelegate.
ms.openlocfilehash: a1d56e9994b3a7916fe0fbe40be1e6d8ff473730
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763392"
---
# <a name="adddelegateresponse"></a><span data-ttu-id="1be1a-103">AddDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="1be1a-103">AddDelegateResponse</span></span>

<span data-ttu-id="1be1a-104">El elemento **AddDelegateResponse** contiene el estado y el resultado de una solicitud de [operación AddDelegate](adddelegate-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="1be1a-104">The **AddDelegateResponse** element contains the status and result of an [AddDelegate operation](adddelegate-operation.md) request.</span></span> 
  
```xml
<AddDelegateResponse>
   <ResponseMessages/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</AddDelegateResponse>
```

 <span data-ttu-id="1be1a-105">**AddDelegateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="1be1a-105">**AddDelegateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1be1a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1be1a-106">Attributes and elements</span></span>

<span data-ttu-id="1be1a-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1be1a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1be1a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1be1a-108">Attributes</span></span>

<span data-ttu-id="1be1a-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1be1a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1be1a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1be1a-110">Child elements</span></span>

|<span data-ttu-id="1be1a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="1be1a-111">**Element**</span></span>|<span data-ttu-id="1be1a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1be1a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1be1a-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="1be1a-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="1be1a-114">Contiene los mensajes de respuesta para una solicitud de administración de servicios Web de Exchange delegado.</span><span class="sxs-lookup"><span data-stu-id="1be1a-114">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
|[<span data-ttu-id="1be1a-115">MessageText</span><span class="sxs-lookup"><span data-stu-id="1be1a-115">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="1be1a-116">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1be1a-116">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="1be1a-117">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="1be1a-117">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="1be1a-118">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1be1a-118">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="1be1a-119">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="1be1a-119">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="1be1a-120">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="1be1a-120">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="1be1a-121">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="1be1a-121">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="1be1a-122">MessageXml</span><span class="sxs-lookup"><span data-stu-id="1be1a-122">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="1be1a-123">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="1be1a-123">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1be1a-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1be1a-124">Parent elements</span></span>

<span data-ttu-id="1be1a-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1be1a-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1be1a-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1be1a-126">Remarks</span></span>

<span data-ttu-id="1be1a-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="1be1a-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1be1a-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1be1a-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1be1a-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1be1a-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1be1a-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1be1a-130">Schema Name</span></span>  <br/> |<span data-ttu-id="1be1a-131">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="1be1a-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1be1a-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1be1a-132">Validation File</span></span>  <br/> |<span data-ttu-id="1be1a-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1be1a-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1be1a-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1be1a-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="1be1a-135">False</span><span class="sxs-lookup"><span data-stu-id="1be1a-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1be1a-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="1be1a-136">See also</span></span>

- [<span data-ttu-id="1be1a-137">Operación AddDelegate</span><span class="sxs-lookup"><span data-stu-id="1be1a-137">AddDelegate operation</span></span>](adddelegate-operation.md)
- [<span data-ttu-id="1be1a-138">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="1be1a-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="1be1a-139">Adición de delegados</span><span class="sxs-lookup"><span data-stu-id="1be1a-139">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

