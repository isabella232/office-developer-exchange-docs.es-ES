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
description: El elemento ReportTemplate representa el tipo de informe que se va a obtener.
ms.openlocfilehash: 22f14d326032a30e5cb4c2c9e1aff390d98e95e0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528702"
---
# <a name="reporttemplate"></a><span data-ttu-id="149a0-103">ReportTemplate</span><span class="sxs-lookup"><span data-stu-id="149a0-103">ReportTemplate</span></span>

<span data-ttu-id="149a0-104">El elemento **ReportTemplate** representa el tipo de informe que se va a obtener.</span><span class="sxs-lookup"><span data-stu-id="149a0-104">The **ReportTemplate** element represents the type of report to get.</span></span> 
  
```xml
<ReportTemplate>Summary or RecipientPath</ReportTemplate>
```

 <span data-ttu-id="149a0-105">**MessageTrackingReportTemplateType**</span><span class="sxs-lookup"><span data-stu-id="149a0-105">**MessageTrackingReportTemplateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="149a0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="149a0-106">Attributes and elements</span></span>

<span data-ttu-id="149a0-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="149a0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="149a0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="149a0-108">Attributes</span></span>

<span data-ttu-id="149a0-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="149a0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="149a0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="149a0-110">Child elements</span></span>

<span data-ttu-id="149a0-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="149a0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="149a0-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="149a0-112">Parent elements</span></span>

|<span data-ttu-id="149a0-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="149a0-113">**Element**</span></span>|<span data-ttu-id="149a0-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="149a0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="149a0-115">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="149a0-115">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="149a0-116">Contiene la solicitud de la [operación GetMessageTrackingReport](getmessagetrackingreport-operation.md) para recuperar el informe completo de seguimiento de mensajes del identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="149a0-116">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="149a0-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="149a0-117">Text value</span></span>

<span data-ttu-id="149a0-118">En la siguiente tabla se enumeran los valores posibles para el elemento **ReportTemplate** .</span><span class="sxs-lookup"><span data-stu-id="149a0-118">The following table lists the possible values for the **ReportTemplate** element.</span></span> 
  
<span data-ttu-id="149a0-119">**Valores del elemento ReportTemplate**</span><span class="sxs-lookup"><span data-stu-id="149a0-119">**ReportTemplate element values**</span></span>

|<span data-ttu-id="149a0-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="149a0-120">**Value**</span></span>|<span data-ttu-id="149a0-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="149a0-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="149a0-122">Resumen</span><span class="sxs-lookup"><span data-stu-id="149a0-122">Summary</span></span>  <br/> |<span data-ttu-id="149a0-123">Especifica que el informe mostrará todos los destinatarios del mensaje y el estado de entrega del mensaje a cada destinatario.</span><span class="sxs-lookup"><span data-stu-id="149a0-123">Specifies that the report will display all the recipients of the message and the delivery status of the message to each recipient.</span></span>  <br/> |
|<span data-ttu-id="149a0-124">RecipientPath</span><span class="sxs-lookup"><span data-stu-id="149a0-124">RecipientPath</span></span>  <br/> |<span data-ttu-id="149a0-125">Especifica que, para un único destinatario, el informe mostrará un historial completo de los eventos que se produjeron.</span><span class="sxs-lookup"><span data-stu-id="149a0-125">Specifies that for a single recipient, the report will display a full history of the events that occurred.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="149a0-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="149a0-126">Remarks</span></span>

<span data-ttu-id="149a0-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="149a0-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="149a0-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="149a0-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="149a0-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="149a0-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="149a0-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="149a0-130">Schema Name</span></span>  <br/> |<span data-ttu-id="149a0-131">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="149a0-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="149a0-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="149a0-132">Validation File</span></span>  <br/> |<span data-ttu-id="149a0-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="149a0-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="149a0-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="149a0-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="149a0-135">Falso</span><span class="sxs-lookup"><span data-stu-id="149a0-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="149a0-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="149a0-136">See also</span></span>



- [<span data-ttu-id="149a0-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="149a0-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

