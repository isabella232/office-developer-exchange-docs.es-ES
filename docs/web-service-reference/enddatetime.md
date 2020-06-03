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
description: El elemento EndDateTime especifica la fecha y hora de finalización de una regla o búsqueda.
ms.openlocfilehash: 9556e4c1ef405ae66a71d19d99d9a71a61f54efc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460137"
---
# <a name="enddatetime"></a><span data-ttu-id="94b85-103">EndDateTime</span><span class="sxs-lookup"><span data-stu-id="94b85-103">EndDateTime</span></span>

<span data-ttu-id="94b85-104">El elemento **EndDateTime** especifica la fecha y hora de finalización de una regla o búsqueda.</span><span class="sxs-lookup"><span data-stu-id="94b85-104">The **EndDateTime** element specifies the end date and time for a rule or a search.</span></span> 
  
```XML
<EndDateTime/>
```

 <span data-ttu-id="94b85-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="94b85-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="94b85-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="94b85-106">Attributes and elements</span></span>

<span data-ttu-id="94b85-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="94b85-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="94b85-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="94b85-108">Attributes</span></span>

<span data-ttu-id="94b85-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="94b85-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="94b85-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="94b85-110">Child elements</span></span>

<span data-ttu-id="94b85-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="94b85-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="94b85-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="94b85-112">Parent elements</span></span>

|<span data-ttu-id="94b85-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="94b85-113">**Element**</span></span>|<span data-ttu-id="94b85-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="94b85-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="94b85-115">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="94b85-115">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="94b85-116">Contiene los criterios para los tipos de mensajes que se van a buscar.</span><span class="sxs-lookup"><span data-stu-id="94b85-116">Contains criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="94b85-117">WithinDateRange</span><span class="sxs-lookup"><span data-stu-id="94b85-117">WithinDateRange</span></span>](withindaterange.md) <br/> |<span data-ttu-id="94b85-118">Especifica el intervalo de fechas en el que se deben recibir los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="94b85-118">Specifies the date range within which incoming messages have to have been received in order for the condition or exception to apply.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="94b85-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="94b85-119">Text value</span></span>

<span data-ttu-id="94b85-120">Si se usa este elemento, es necesario un valor de texto que represente una fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="94b85-120">A text value that represents a date/time is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="94b85-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="94b85-121">Remarks</span></span>

<span data-ttu-id="94b85-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="94b85-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="94b85-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="94b85-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="94b85-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="94b85-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="94b85-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="94b85-125">Schema Name</span></span>  <br/> |<span data-ttu-id="94b85-126">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="94b85-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="94b85-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="94b85-127">Validation File</span></span>  <br/> |<span data-ttu-id="94b85-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="94b85-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="94b85-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="94b85-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="94b85-130">Falso</span><span class="sxs-lookup"><span data-stu-id="94b85-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="94b85-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="94b85-131">See also</span></span>



- [<span data-ttu-id="94b85-132">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="94b85-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

