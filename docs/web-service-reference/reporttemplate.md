---
title: ReportTemplate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReportTemplate
api_type:
- schema
ms.assetid: f528eee6-d5af-4745-8b00-a9834bf34be6
description: El elemento ReportTemplate representa el tipo de informe que desea obtener.
ms.openlocfilehash: 70aab69f4d20ad9fd7e878c7fccd16e261c9b94c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837118"
---
# <a name="reporttemplate"></a><span data-ttu-id="38f94-103">ReportTemplate</span><span class="sxs-lookup"><span data-stu-id="38f94-103">ReportTemplate</span></span>

<span data-ttu-id="38f94-104">El elemento **ReportTemplate** representa el tipo de informe que desea obtener.</span><span class="sxs-lookup"><span data-stu-id="38f94-104">The **ReportTemplate** element represents the type of report to get.</span></span> 
  
```xml
<ReportTemplate>Summary or RecipientPath</ReportTemplate>
```

 <span data-ttu-id="38f94-105">**MessageTrackingReportTemplateType**</span><span class="sxs-lookup"><span data-stu-id="38f94-105">**MessageTrackingReportTemplateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="38f94-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="38f94-106">Attributes and elements</span></span>

<span data-ttu-id="38f94-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="38f94-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="38f94-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="38f94-108">Attributes</span></span>

<span data-ttu-id="38f94-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="38f94-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="38f94-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="38f94-110">Child elements</span></span>

<span data-ttu-id="38f94-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="38f94-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="38f94-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="38f94-112">Parent elements</span></span>

|<span data-ttu-id="38f94-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="38f94-113">**Element**</span></span>|<span data-ttu-id="38f94-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="38f94-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="38f94-115">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="38f94-115">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="38f94-116">Contiene la solicitud para la [operación de GetMessageTrackingReport](getmessagetrackingreport-operation.md) recuperar el mensaje completo informe de seguimiento para el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="38f94-116">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="38f94-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="38f94-117">Text value</span></span>

<span data-ttu-id="38f94-118">En la siguiente tabla se enumera los valores posibles para el elemento **ReportTemplate** .</span><span class="sxs-lookup"><span data-stu-id="38f94-118">The following table lists the possible values for the **ReportTemplate** element.</span></span> 
  
<span data-ttu-id="38f94-119">**Valores de elemento ReportTemplate**</span><span class="sxs-lookup"><span data-stu-id="38f94-119">**ReportTemplate element values**</span></span>

|<span data-ttu-id="38f94-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="38f94-120">**Value**</span></span>|<span data-ttu-id="38f94-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="38f94-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="38f94-122">Resumen</span><span class="sxs-lookup"><span data-stu-id="38f94-122">Summary</span></span>  <br/> |<span data-ttu-id="38f94-123">Especifica que el informe mostrará todos los destinatarios del mensaje y el estado de entrega del mensaje a cada destinatario.</span><span class="sxs-lookup"><span data-stu-id="38f94-123">Specifies that the report will display all the recipients of the message and the delivery status of the message to each recipient.</span></span>  <br/> |
|<span data-ttu-id="38f94-124">RecipientPath</span><span class="sxs-lookup"><span data-stu-id="38f94-124">RecipientPath</span></span>  <br/> |<span data-ttu-id="38f94-125">Especifica para un solo destinatario, el informe mostrará un historial completo de los eventos que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="38f94-125">Specifies that for a single recipient, the report will display a full history of the events that occurred.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38f94-126">Notas</span><span class="sxs-lookup"><span data-stu-id="38f94-126">Remarks</span></span>

<span data-ttu-id="38f94-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="38f94-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="38f94-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="38f94-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="38f94-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="38f94-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="38f94-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="38f94-130">Schema Name</span></span>  <br/> |<span data-ttu-id="38f94-131">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="38f94-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="38f94-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="38f94-132">Validation File</span></span>  <br/> |<span data-ttu-id="38f94-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="38f94-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="38f94-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="38f94-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="38f94-135">False</span><span class="sxs-lookup"><span data-stu-id="38f94-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="38f94-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="38f94-136">See also</span></span>



- [<span data-ttu-id="38f94-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="38f94-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

