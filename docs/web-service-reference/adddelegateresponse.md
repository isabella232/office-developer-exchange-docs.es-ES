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
ms.openlocfilehash: 1c38563ab38facf89fd5eab119542374949244c2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466461"
---
# <a name="adddelegateresponse"></a><span data-ttu-id="4b973-103">AddDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="4b973-103">AddDelegateResponse</span></span>

<span data-ttu-id="4b973-104">El elemento **AddDelegateResponse** contiene el estado y el resultado de una solicitud de [operación AddDelegate](adddelegate-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="4b973-104">The **AddDelegateResponse** element contains the status and result of an [AddDelegate operation](adddelegate-operation.md) request.</span></span> 
  
```xml
<AddDelegateResponse>
   <ResponseMessages/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</AddDelegateResponse>
```

 <span data-ttu-id="4b973-105">**AddDelegateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="4b973-105">**AddDelegateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4b973-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4b973-106">Attributes and elements</span></span>

<span data-ttu-id="4b973-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4b973-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4b973-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4b973-108">Attributes</span></span>

<span data-ttu-id="4b973-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="4b973-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4b973-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4b973-110">Child elements</span></span>

|<span data-ttu-id="4b973-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4b973-111">**Element**</span></span>|<span data-ttu-id="4b973-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4b973-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4b973-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="4b973-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="4b973-114">Contiene los mensajes de respuesta para una solicitud de administración de un delegado de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4b973-114">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
|[<span data-ttu-id="4b973-115">MessageText</span><span class="sxs-lookup"><span data-stu-id="4b973-115">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="4b973-116">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4b973-116">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="4b973-117">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="4b973-117">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="4b973-118">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4b973-118">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="4b973-119">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="4b973-119">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="4b973-120">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="4b973-120">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="4b973-121">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="4b973-121">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="4b973-122">MessageXml</span><span class="sxs-lookup"><span data-stu-id="4b973-122">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="4b973-123">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="4b973-123">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4b973-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4b973-124">Parent elements</span></span>

<span data-ttu-id="4b973-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4b973-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4b973-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4b973-126">Remarks</span></span>

<span data-ttu-id="4b973-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="4b973-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4b973-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4b973-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4b973-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="4b973-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4b973-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4b973-130">Schema Name</span></span>  <br/> |<span data-ttu-id="4b973-131">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="4b973-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4b973-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4b973-132">Validation File</span></span>  <br/> |<span data-ttu-id="4b973-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="4b973-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4b973-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4b973-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="4b973-135">Falso</span><span class="sxs-lookup"><span data-stu-id="4b973-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4b973-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b973-136">See also</span></span>

- [<span data-ttu-id="4b973-137">Operación AddDelegate</span><span class="sxs-lookup"><span data-stu-id="4b973-137">AddDelegate operation</span></span>](adddelegate-operation.md)
- [<span data-ttu-id="4b973-138">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="4b973-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="4b973-139">Adición de delegados</span><span class="sxs-lookup"><span data-stu-id="4b973-139">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

