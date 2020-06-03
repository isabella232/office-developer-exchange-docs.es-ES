---
title: MessageTrackingReportId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MessageTrackingReportId
api_type:
- schema
ms.assetid: 9c604ca3-10fe-4760-b7fd-8b52f1a0c712
description: El elemento MessageTrackingReportId representa el mensaje por su identificador de mensaje, la organización donde se encontró el mensaje, el servidor en el que se envió el mensaje y un identificador interno que identifica de forma única el mensaje.
ms.openlocfilehash: d6e92593d55608e260634602c2aab694804d716d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460599"
---
# <a name="messagetrackingreportid"></a><span data-ttu-id="fa603-103">MessageTrackingReportId</span><span class="sxs-lookup"><span data-stu-id="fa603-103">MessageTrackingReportId</span></span>

<span data-ttu-id="fa603-104">El elemento **MessageTrackingReportId** representa el mensaje por su identificador de mensaje, la organización donde se encontró el mensaje, el servidor en el que se envió el mensaje y un identificador interno que identifica de forma única el mensaje.</span><span class="sxs-lookup"><span data-stu-id="fa603-104">The **MessageTrackingReportId** element represents the message by its message ID, the organization where the message was found, the server on which the message was submitted, and an internal ID that uniquely identifies the message.</span></span> 
  
```XML
<MessageTrackingReportId/>
```

 <span data-ttu-id="fa603-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="fa603-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fa603-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fa603-106">Attributes and elements</span></span>

<span data-ttu-id="fa603-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fa603-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa603-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="fa603-108">Attributes</span></span>

<span data-ttu-id="fa603-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fa603-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fa603-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fa603-110">Child elements</span></span>

<span data-ttu-id="fa603-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fa603-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fa603-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fa603-112">Parent elements</span></span>

|<span data-ttu-id="fa603-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fa603-113">**Element**</span></span>|<span data-ttu-id="fa603-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fa603-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa603-115">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="fa603-115">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="fa603-116">Contiene la solicitud de la [operación GetMessageTrackingReport](getmessagetrackingreport-operation.md) para recuperar el informe completo de seguimiento de mensajes del identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="fa603-116">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
|[<span data-ttu-id="fa603-117">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="fa603-117">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="fa603-118">Contiene un único resultado de mensaje para un elemento [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="fa603-118">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fa603-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="fa603-119">Text value</span></span>

<span data-ttu-id="fa603-120">Si se usa este elemento, se necesita un valor de texto que represente una cadena.</span><span class="sxs-lookup"><span data-stu-id="fa603-120">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fa603-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fa603-121">Remarks</span></span>

<span data-ttu-id="fa603-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="fa603-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fa603-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fa603-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa603-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="fa603-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fa603-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fa603-125">Schema Name</span></span>  <br/> |<span data-ttu-id="fa603-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="fa603-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="fa603-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fa603-127">Validation File</span></span>  <br/> |<span data-ttu-id="fa603-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="fa603-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fa603-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fa603-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="fa603-130">Falso</span><span class="sxs-lookup"><span data-stu-id="fa603-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fa603-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa603-131">See also</span></span>



[<span data-ttu-id="fa603-132">Operación GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="fa603-132">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="fa603-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="fa603-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

