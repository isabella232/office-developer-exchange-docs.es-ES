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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457385"
---
# <a name="delegateuserresponsemessagetype"></a><span data-ttu-id="dfa3c-103">DelegateUserResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="dfa3c-103">DelegateUserResponseMessageType</span></span>

<span data-ttu-id="dfa3c-104">El elemento **DelegateUserResponseMessageType** contiene el mensaje de respuesta para un solo usuario delegado.</span><span class="sxs-lookup"><span data-stu-id="dfa3c-104">The **DelegateUserResponseMessageType** element contains the response message for a single delegate user.</span></span> 
  
```xml
<DelegateUserResponseMessageType>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <DelegateUser/>
</DelegateUserResponseMessageType>
```

<span data-ttu-id="dfa3c-105">**DelegateUserResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="dfa3c-105">**DelegateUserResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="dfa3c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="dfa3c-106">Attributes and elements</span></span>

<span data-ttu-id="dfa3c-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="dfa3c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dfa3c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="dfa3c-108">Attributes</span></span>

<span data-ttu-id="dfa3c-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="dfa3c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dfa3c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dfa3c-110">Child elements</span></span>

|<span data-ttu-id="dfa3c-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="dfa3c-111">**Element**</span></span>|<span data-ttu-id="dfa3c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dfa3c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dfa3c-113">MessageText</span><span class="sxs-lookup"><span data-stu-id="dfa3c-113">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="dfa3c-114">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dfa3c-114">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="dfa3c-115">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="dfa3c-115">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="dfa3c-116">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dfa3c-116">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="dfa3c-117">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="dfa3c-117">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="dfa3c-118">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="dfa3c-118">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="dfa3c-119">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="dfa3c-119">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="dfa3c-120">MessageXml</span><span class="sxs-lookup"><span data-stu-id="dfa3c-120">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="dfa3c-121">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="dfa3c-121">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="dfa3c-122">DelegateUser</span><span class="sxs-lookup"><span data-stu-id="dfa3c-122">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="dfa3c-123">Identifica un único delegado que se devuelve en una respuesta de administración de delegado.</span><span class="sxs-lookup"><span data-stu-id="dfa3c-123">Identifies a single delegate that is returned in a delegate management response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dfa3c-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="dfa3c-124">Parent elements</span></span>

|<span data-ttu-id="dfa3c-125">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="dfa3c-125">**Element**</span></span>|<span data-ttu-id="dfa3c-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dfa3c-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dfa3c-127">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="dfa3c-127">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="dfa3c-128">Contiene los mensajes de respuesta para una solicitud de administración de un delegado de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="dfa3c-128">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dfa3c-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dfa3c-129">Remarks</span></span>

<span data-ttu-id="dfa3c-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con el rol de servidor acceso de clientes instalado.</span><span class="sxs-lookup"><span data-stu-id="dfa3c-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dfa3c-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="dfa3c-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dfa3c-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="dfa3c-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="dfa3c-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="dfa3c-133">Schema Name</span></span>  <br/> |<span data-ttu-id="dfa3c-134">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="dfa3c-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="dfa3c-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="dfa3c-135">Validation File</span></span>  <br/> |<span data-ttu-id="dfa3c-136">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="dfa3c-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dfa3c-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="dfa3c-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="dfa3c-138">Falso</span><span class="sxs-lookup"><span data-stu-id="dfa3c-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dfa3c-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="dfa3c-139">See also</span></span>

- [<span data-ttu-id="dfa3c-140">Operación AddDelegate</span><span class="sxs-lookup"><span data-stu-id="dfa3c-140">AddDelegate operation</span></span>](adddelegate-operation.md)  
- [<span data-ttu-id="dfa3c-141">Operación GetDelegate</span><span class="sxs-lookup"><span data-stu-id="dfa3c-141">GetDelegate operation</span></span>](getdelegate-operation.md) 
- [<span data-ttu-id="dfa3c-142">Operación UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="dfa3c-142">UpdateDelegate operation</span></span>](updatedelegate-operation.md)  
- [<span data-ttu-id="dfa3c-143">Operación RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="dfa3c-143">RemoveDelegate operation</span></span>](removedelegate-operation.md)
- [<span data-ttu-id="dfa3c-144">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="dfa3c-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

