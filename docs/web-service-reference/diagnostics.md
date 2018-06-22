---
title: Diagnósticos
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Diagnostics
api_type:
- schema
ms.assetid: fecea440-970a-49da-9796-534ca470cbd6
description: El elemento de diagnóstico proporciona información de rendimiento y control de tiempo que se usa para la creación de informes en un centro de datos.
ms.openlocfilehash: 2b9cac54a683967ec274b8681fb9a0c8a844205e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764144"
---
# <a name="diagnostics"></a><span data-ttu-id="b8cc6-103">Diagnósticos</span><span class="sxs-lookup"><span data-stu-id="b8cc6-103">Diagnostics</span></span>

<span data-ttu-id="b8cc6-104">El elemento de **diagnóstico** proporciona información de rendimiento y control de tiempo que se usa para la creación de informes en un centro de datos.</span><span class="sxs-lookup"><span data-stu-id="b8cc6-104">The **Diagnostics** element provides timing and performance information that is used for reporting in a DataCenter.</span></span> 
  
```XML
<Diagnostics>
   <String/>
</Diagnostics>

```

 <span data-ttu-id="b8cc6-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="b8cc6-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b8cc6-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b8cc6-106">Attributes and elements</span></span>

<span data-ttu-id="b8cc6-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b8cc6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b8cc6-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b8cc6-108">Attributes</span></span>

<span data-ttu-id="b8cc6-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b8cc6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b8cc6-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b8cc6-110">Child elements</span></span>

|<span data-ttu-id="b8cc6-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b8cc6-111">**Element**</span></span>|<span data-ttu-id="b8cc6-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b8cc6-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b8cc6-113">String</span><span class="sxs-lookup"><span data-stu-id="b8cc6-113">String</span></span>](string.md) <br/> |<span data-ttu-id="b8cc6-114">Contiene una cadena que se usa en los elementos, contactos, tareas y las conversaciones.</span><span class="sxs-lookup"><span data-stu-id="b8cc6-114">Contains a string that is used by items, contacts, tasks, and conversations.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b8cc6-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b8cc6-115">Parent elements</span></span>

|<span data-ttu-id="b8cc6-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="b8cc6-116">**Element**</span></span>|<span data-ttu-id="b8cc6-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b8cc6-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b8cc6-118">FindMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="b8cc6-118">FindMessageTrackingReportResponse</span></span>](findmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="b8cc6-119">Contiene el estado y el resultado de una única solicitud de [operación FindMessageTrackingReport](findmessagetrackingreport-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="b8cc6-119">Contains the status and result of a single [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="b8cc6-120">GetMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="b8cc6-120">GetMessageTrackingReportResponse</span></span>](getmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="b8cc6-121">Contiene la respuesta de la [operación de GetMessageTrackingReport](getmessagetrackingreport-operation.md).</span><span class="sxs-lookup"><span data-stu-id="b8cc6-121">Contains the response for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b8cc6-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b8cc6-122">Text value</span></span>

<span data-ttu-id="b8cc6-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b8cc6-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b8cc6-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8cc6-124">Remarks</span></span>

<span data-ttu-id="b8cc6-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b8cc6-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b8cc6-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b8cc6-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b8cc6-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b8cc6-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b8cc6-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b8cc6-128">Schema Name</span></span>  <br/> |<span data-ttu-id="b8cc6-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="b8cc6-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b8cc6-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b8cc6-130">Validation File</span></span>  <br/> |<span data-ttu-id="b8cc6-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b8cc6-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b8cc6-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b8cc6-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="b8cc6-133">False</span><span class="sxs-lookup"><span data-stu-id="b8cc6-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b8cc6-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="b8cc6-134">See also</span></span>

- [<span data-ttu-id="b8cc6-135">Operación FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="b8cc6-135">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)
- [<span data-ttu-id="b8cc6-136">Operación GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="b8cc6-136">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)
- [<span data-ttu-id="b8cc6-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="b8cc6-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

