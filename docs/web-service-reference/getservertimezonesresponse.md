---
title: GetServerTimeZonesResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetServerTimeZonesResponse
api_type:
- schema
ms.assetid: 97c94d32-10f1-4c3e-ab20-9fd7e8257e50
description: El elemento GetServerTimeZonesResponse define una respuesta a una solicitud de operación GetServerTimeZones.
ms.openlocfilehash: 5a8dbe19055e3b697149c10df610d081cb65430b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460928"
---
# <a name="getservertimezonesresponse"></a><span data-ttu-id="e0af5-103">GetServerTimeZonesResponse</span><span class="sxs-lookup"><span data-stu-id="e0af5-103">GetServerTimeZonesResponse</span></span>

<span data-ttu-id="e0af5-104">El elemento **GetServerTimeZonesResponse** define una respuesta a una solicitud de [operación GetServerTimeZones](getservertimezones-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0af5-104">The **GetServerTimeZonesResponse** element defines a response to a [GetServerTimeZones operation](getservertimezones-operation.md) request.</span></span> 
  
```XML
<GetServerTimeZonesResponse>
   <ResponseMessages/>
</GetServerTimeZonesResponse>
```

 <span data-ttu-id="e0af5-105">**GetServerTimeZonesResponseType**</span><span class="sxs-lookup"><span data-stu-id="e0af5-105">**GetServerTimeZonesResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e0af5-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e0af5-106">Attributes and elements</span></span>

<span data-ttu-id="e0af5-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e0af5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e0af5-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e0af5-108">Attributes</span></span>

<span data-ttu-id="e0af5-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e0af5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e0af5-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e0af5-110">Child elements</span></span>

|<span data-ttu-id="e0af5-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e0af5-111">**Element**</span></span>|<span data-ttu-id="e0af5-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e0af5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e0af5-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e0af5-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="e0af5-114">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e0af5-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e0af5-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e0af5-115">Parent elements</span></span>

<span data-ttu-id="e0af5-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e0af5-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e0af5-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e0af5-117">Remarks</span></span>

<span data-ttu-id="e0af5-118">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e0af5-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e0af5-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e0af5-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0af5-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="e0af5-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e0af5-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e0af5-121">Schema Name</span></span>  <br/> |<span data-ttu-id="e0af5-122">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="e0af5-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e0af5-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e0af5-123">Validation File</span></span>  <br/> |<span data-ttu-id="e0af5-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="e0af5-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e0af5-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e0af5-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="e0af5-126">Falso</span><span class="sxs-lookup"><span data-stu-id="e0af5-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e0af5-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0af5-127">See also</span></span>



- [<span data-ttu-id="e0af5-128">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e0af5-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

