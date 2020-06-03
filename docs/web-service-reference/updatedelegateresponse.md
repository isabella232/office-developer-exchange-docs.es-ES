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
ms.openlocfilehash: 9f11d87ac07dd51a5231d4546fac92e7ca95ad4b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465054"
---
# <a name="updatedelegateresponse"></a><span data-ttu-id="25848-103">UpdateDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="25848-103">UpdateDelegateResponse</span></span>

<span data-ttu-id="25848-104">El elemento **UpdateDelegateResponse** contiene el estado y el resultado de una solicitud de [operación UpdateDelegate](updatedelegate-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="25848-104">The **UpdateDelegateResponse** element contains the status and result of an [UpdateDelegate operation](updatedelegate-operation.md) request.</span></span> 
  
```xml
<UpdateDelegateResponseMessage>
   <ResponseMessages/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</UpdateDelegateResponseMessage>
```

 <span data-ttu-id="25848-105">**UpdateDelegateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="25848-105">**UpdateDelegateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="25848-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="25848-106">Attributes and elements</span></span>

<span data-ttu-id="25848-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="25848-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="25848-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="25848-108">Attributes</span></span>

<span data-ttu-id="25848-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="25848-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="25848-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="25848-110">Child elements</span></span>

|<span data-ttu-id="25848-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="25848-111">**Element**</span></span>|<span data-ttu-id="25848-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="25848-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="25848-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="25848-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="25848-114">Contiene los mensajes de respuesta para una solicitud de administración de un delegado de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="25848-114">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
|[<span data-ttu-id="25848-115">MessageText</span><span class="sxs-lookup"><span data-stu-id="25848-115">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="25848-116">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="25848-116">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="25848-117">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="25848-117">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="25848-118">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="25848-118">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="25848-119">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="25848-119">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="25848-120">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="25848-120">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="25848-121">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="25848-121">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="25848-122">MessageXml</span><span class="sxs-lookup"><span data-stu-id="25848-122">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="25848-123">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="25848-123">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="25848-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="25848-124">Parent elements</span></span>

<span data-ttu-id="25848-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="25848-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="25848-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="25848-126">Remarks</span></span>

<span data-ttu-id="25848-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="25848-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="25848-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="25848-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="25848-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="25848-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="25848-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="25848-130">Schema Name</span></span>  <br/> |<span data-ttu-id="25848-131">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="25848-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="25848-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="25848-132">Validation File</span></span>  <br/> |<span data-ttu-id="25848-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="25848-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="25848-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="25848-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="25848-135">Falso</span><span class="sxs-lookup"><span data-stu-id="25848-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="25848-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="25848-136">See also</span></span>



[<span data-ttu-id="25848-137">Operación UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="25848-137">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="25848-138">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="25848-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

