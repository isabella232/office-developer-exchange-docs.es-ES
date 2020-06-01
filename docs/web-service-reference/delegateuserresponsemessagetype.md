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
description: El elemento DelegateUserResponseMessageType contiene el mensaje de respuesta para un solo usuario delegado.
ms.openlocfilehash: d7addac2ef05d50e0043490ac20d299ece7d577b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457385"
---
# <a name="delegateuserresponsemessagetype"></a><span data-ttu-id="42450-103">DelegateUserResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="42450-103">DelegateUserResponseMessageType</span></span>

<span data-ttu-id="42450-104">El elemento **DelegateUserResponseMessageType** contiene el mensaje de respuesta para un solo usuario delegado.</span><span class="sxs-lookup"><span data-stu-id="42450-104">The **DelegateUserResponseMessageType** element contains the response message for a single delegate user.</span></span> 
  
```xml
<DelegateUserResponseMessageType>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <DelegateUser/>
</DelegateUserResponseMessageType>
```

<span data-ttu-id="42450-105">**DelegateUserResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="42450-105">**DelegateUserResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="42450-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="42450-106">Attributes and elements</span></span>

<span data-ttu-id="42450-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="42450-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="42450-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="42450-108">Attributes</span></span>

<span data-ttu-id="42450-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="42450-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="42450-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="42450-110">Child elements</span></span>

|<span data-ttu-id="42450-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="42450-111">**Element**</span></span>|<span data-ttu-id="42450-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="42450-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="42450-113">MessageText</span><span class="sxs-lookup"><span data-stu-id="42450-113">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="42450-114">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="42450-114">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="42450-115">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="42450-115">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="42450-116">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="42450-116">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="42450-117">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="42450-117">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="42450-118">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="42450-118">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="42450-119">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="42450-119">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="42450-120">MessageXml</span><span class="sxs-lookup"><span data-stu-id="42450-120">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="42450-121">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="42450-121">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="42450-122">DelegateUser</span><span class="sxs-lookup"><span data-stu-id="42450-122">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="42450-123">Identifica un único delegado que se devuelve en una respuesta de administración de delegado.</span><span class="sxs-lookup"><span data-stu-id="42450-123">Identifies a single delegate that is returned in a delegate management response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="42450-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="42450-124">Parent elements</span></span>

|<span data-ttu-id="42450-125">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="42450-125">**Element**</span></span>|<span data-ttu-id="42450-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="42450-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="42450-127">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="42450-127">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="42450-128">Contiene los mensajes de respuesta para una solicitud de administración de un delegado de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="42450-128">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="42450-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="42450-129">Remarks</span></span>

<span data-ttu-id="42450-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con el rol de servidor acceso de clientes instalado.</span><span class="sxs-lookup"><span data-stu-id="42450-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="42450-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="42450-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="42450-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="42450-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="42450-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="42450-133">Schema Name</span></span>  <br/> |<span data-ttu-id="42450-134">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="42450-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="42450-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="42450-135">Validation File</span></span>  <br/> |<span data-ttu-id="42450-136">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="42450-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="42450-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="42450-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="42450-138">Falso</span><span class="sxs-lookup"><span data-stu-id="42450-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="42450-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="42450-139">See also</span></span>

- [<span data-ttu-id="42450-140">Operación AddDelegate</span><span class="sxs-lookup"><span data-stu-id="42450-140">AddDelegate operation</span></span>](adddelegate-operation.md)  
- [<span data-ttu-id="42450-141">Operación GetDelegate</span><span class="sxs-lookup"><span data-stu-id="42450-141">GetDelegate operation</span></span>](getdelegate-operation.md) 
- [<span data-ttu-id="42450-142">Operación UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="42450-142">UpdateDelegate operation</span></span>](updatedelegate-operation.md)  
- [<span data-ttu-id="42450-143">Operación RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="42450-143">RemoveDelegate operation</span></span>](removedelegate-operation.md)
- [<span data-ttu-id="42450-144">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="42450-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

