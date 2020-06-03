---
title: UnsubscribeResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnsubscribeResponse
api_type:
- schema
ms.assetid: 125e0326-6522-42cd-b20e-6977e6fde249
description: El elemento UnsubscribeResponse define una respuesta a una solicitud unsubscribe.
ms.openlocfilehash: 1a8ddf93499acb7aa369ec9e91a7106e5cb4bd53
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467203"
---
# <a name="unsubscriberesponse"></a><span data-ttu-id="9a990-103">UnsubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="9a990-103">UnsubscribeResponse</span></span>

<span data-ttu-id="9a990-104">El elemento **UnsubscribeResponse** define una respuesta a una solicitud unsubscribe.</span><span class="sxs-lookup"><span data-stu-id="9a990-104">The **UnsubscribeResponse** element defines a response to an Unsubscribe request.</span></span> 
  
```xml
<UnsubscribeResponse>
   <ResponseMessages/>
</UnsubscribeResponse>
```

 <span data-ttu-id="9a990-105">**UnsubscribeResponseType**</span><span class="sxs-lookup"><span data-stu-id="9a990-105">**UnsubscribeResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9a990-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9a990-106">Attributes and elements</span></span>

<span data-ttu-id="9a990-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9a990-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9a990-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="9a990-108">Attributes</span></span>

<span data-ttu-id="9a990-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="9a990-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9a990-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9a990-110">Child elements</span></span>

|<span data-ttu-id="9a990-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9a990-111">**Element**</span></span>|<span data-ttu-id="9a990-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9a990-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9a990-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9a990-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="9a990-114">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="9a990-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9a990-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9a990-115">Parent elements</span></span>

<span data-ttu-id="9a990-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9a990-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9a990-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9a990-117">Remarks</span></span>

<span data-ttu-id="9a990-118">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="9a990-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9a990-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9a990-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9a990-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="9a990-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9a990-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9a990-121">Schema name</span></span>  <br/> |<span data-ttu-id="9a990-122">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="9a990-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9a990-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9a990-123">Validation file</span></span>  <br/> |<span data-ttu-id="9a990-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="9a990-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9a990-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9a990-125">Can be empty</span></span>  <br/> |<span data-ttu-id="9a990-126">Falso</span><span class="sxs-lookup"><span data-stu-id="9a990-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9a990-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a990-127">See also</span></span>



- [<span data-ttu-id="9a990-128">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="9a990-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

