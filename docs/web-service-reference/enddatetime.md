---
title: EndDateTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EndDateTime
api_type:
- schema
ms.assetid: 54d14e47-a8f7-400b-a859-c7ea7ce4c6a4
description: El elemento EndDateTime especifica la fecha de finalización y la hora para una regla o una búsqueda.
ms.openlocfilehash: ad596c6441e7bdb10b4e886a8d0f3ba183c43c3e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764409"
---
# <a name="enddatetime"></a><span data-ttu-id="b0ddc-103">EndDateTime</span><span class="sxs-lookup"><span data-stu-id="b0ddc-103">EndDateTime</span></span>

<span data-ttu-id="b0ddc-104">El elemento **EndDateTime** especifica la fecha de finalización y la hora para una regla o una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="b0ddc-104">The **EndDateTime** element specifies the end date and time for a rule or a search.</span></span> 
  
```XML
<EndDateTime/>
```

 <span data-ttu-id="b0ddc-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="b0ddc-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b0ddc-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b0ddc-106">Attributes and elements</span></span>

<span data-ttu-id="b0ddc-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b0ddc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b0ddc-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b0ddc-108">Attributes</span></span>

<span data-ttu-id="b0ddc-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b0ddc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b0ddc-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b0ddc-110">Child elements</span></span>

<span data-ttu-id="b0ddc-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b0ddc-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b0ddc-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b0ddc-112">Parent elements</span></span>

|<span data-ttu-id="b0ddc-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b0ddc-113">**Element**</span></span>|<span data-ttu-id="b0ddc-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b0ddc-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b0ddc-115">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="b0ddc-115">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="b0ddc-116">Contiene los criterios para los tipos de mensajes para buscar.</span><span class="sxs-lookup"><span data-stu-id="b0ddc-116">Contains criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="b0ddc-117">WithinDateRange</span><span class="sxs-lookup"><span data-stu-id="b0ddc-117">WithinDateRange</span></span>](withindaterange.md) <br/> |<span data-ttu-id="b0ddc-118">Especifica el intervalo de fechas dentro del cual los mensajes entrantes tienen que se han recibido en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="b0ddc-118">Specifies the date range within which incoming messages have to have been received in order for the condition or exception to apply.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b0ddc-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b0ddc-119">Text value</span></span>

<span data-ttu-id="b0ddc-120">Si se usa este elemento, es necesario un valor de texto que representa un fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="b0ddc-120">A text value that represents a date/time is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b0ddc-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b0ddc-121">Remarks</span></span>

<span data-ttu-id="b0ddc-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b0ddc-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b0ddc-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b0ddc-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b0ddc-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b0ddc-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b0ddc-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b0ddc-125">Schema Name</span></span>  <br/> |<span data-ttu-id="b0ddc-126">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="b0ddc-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b0ddc-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b0ddc-127">Validation File</span></span>  <br/> |<span data-ttu-id="b0ddc-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b0ddc-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b0ddc-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b0ddc-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="b0ddc-130">False</span><span class="sxs-lookup"><span data-stu-id="b0ddc-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b0ddc-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0ddc-131">See also</span></span>



- [<span data-ttu-id="b0ddc-132">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="b0ddc-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

