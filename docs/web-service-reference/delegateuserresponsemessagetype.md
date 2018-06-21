---
title: DelegateUserResponseMessageType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DelegateUserResponseMessageType
api_type:
- schema
ms.assetid: 3dc9552c-1e2d-40ac-a137-827883c2bb88
description: El elemento DelegateUserResponseMessageType contiene el mensaje de respuesta para un usuario delegado único.
ms.openlocfilehash: ac99e0ca219fc1f1e117f9288d895e27a1df4700
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/21/2018
ms.locfileid: "19764074"
---
# <a name="delegateuserresponsemessagetype"></a><span data-ttu-id="5a6ae-103">DelegateUserResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="5a6ae-103">DelegateUserResponseMessageType</span></span>

<span data-ttu-id="5a6ae-104">El elemento **DelegateUserResponseMessageType** contiene el mensaje de respuesta para un usuario delegado único.</span><span class="sxs-lookup"><span data-stu-id="5a6ae-104">The **DelegateUserResponseMessageType** element contains the response message for a single delegate user.</span></span> 
  
```xml
<DelegateUserResponseMessageType>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <DelegateUser/>
</DelegateUserResponseMessageType>
```

<span data-ttu-id="5a6ae-105">**DelegateUserResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="5a6ae-105">**DelegateUserResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="5a6ae-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5a6ae-106">Attributes and elements</span></span>

<span data-ttu-id="5a6ae-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5a6ae-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5a6ae-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5a6ae-108">Attributes</span></span>

<span data-ttu-id="5a6ae-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5a6ae-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5a6ae-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5a6ae-110">Child elements</span></span>

|<span data-ttu-id="5a6ae-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="5a6ae-111">**Element**</span></span>|<span data-ttu-id="5a6ae-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5a6ae-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5a6ae-113">MessageText</span><span class="sxs-lookup"><span data-stu-id="5a6ae-113">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="5a6ae-114">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5a6ae-114">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="5a6ae-115">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5a6ae-115">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="5a6ae-116">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5a6ae-116">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="5a6ae-117">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="5a6ae-117">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="5a6ae-118">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="5a6ae-118">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="5a6ae-119">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="5a6ae-119">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="5a6ae-120">MessageXml</span><span class="sxs-lookup"><span data-stu-id="5a6ae-120">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="5a6ae-121">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="5a6ae-121">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="5a6ae-122">UsuarioDelegado</span><span class="sxs-lookup"><span data-stu-id="5a6ae-122">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="5a6ae-123">Identifica a un delegado único que se devuelve en una respuesta de administración de delegado.</span><span class="sxs-lookup"><span data-stu-id="5a6ae-123">Identifies a single delegate that is returned in a delegate management response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5a6ae-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5a6ae-124">Parent elements</span></span>

|<span data-ttu-id="5a6ae-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="5a6ae-125">**Element**</span></span>|<span data-ttu-id="5a6ae-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5a6ae-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5a6ae-127">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="5a6ae-127">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="5a6ae-128">Contiene los mensajes de respuesta para una solicitud de administración de servicios Web de Exchange delegado.</span><span class="sxs-lookup"><span data-stu-id="5a6ae-128">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a6ae-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5a6ae-129">Remarks</span></span>

<span data-ttu-id="5a6ae-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con la función de servidor de acceso de cliente instalada.</span><span class="sxs-lookup"><span data-stu-id="5a6ae-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5a6ae-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5a6ae-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5a6ae-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5a6ae-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5a6ae-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5a6ae-133">Schema Name</span></span>  <br/> |<span data-ttu-id="5a6ae-134">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="5a6ae-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5a6ae-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5a6ae-135">Validation File</span></span>  <br/> |<span data-ttu-id="5a6ae-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5a6ae-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5a6ae-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5a6ae-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="5a6ae-138">False</span><span class="sxs-lookup"><span data-stu-id="5a6ae-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5a6ae-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a6ae-139">See also</span></span>

- [<span data-ttu-id="5a6ae-140">Operación AddDelegate</span><span class="sxs-lookup"><span data-stu-id="5a6ae-140">AddDelegate operation</span></span>](adddelegate-operation.md)  
- [<span data-ttu-id="5a6ae-141">Operación GetDelegate</span><span class="sxs-lookup"><span data-stu-id="5a6ae-141">GetDelegate operation</span></span>](getdelegate-operation.md) 
- [<span data-ttu-id="5a6ae-142">Operación UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="5a6ae-142">UpdateDelegate operation</span></span>](updatedelegate-operation.md)  
- [<span data-ttu-id="5a6ae-143">Operación RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="5a6ae-143">RemoveDelegate operation</span></span>](removedelegate-operation.md)
- [<span data-ttu-id="5a6ae-144">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="5a6ae-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

