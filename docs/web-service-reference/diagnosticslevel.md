---
title: DiagnosticsLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DiagnosticsLevel
api_type:
- schema
ms.assetid: 66794226-f5e0-44f0-8a0e-1f194bb0ba0f
description: El elemento DiagnosticsLevel representa la información de rendimiento y control de tiempo que se utilizará para derivar el informe.
ms.openlocfilehash: 9205625bb6cf38e370e29d96770eb293ed9277f7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764146"
---
# <a name="diagnosticslevel"></a><span data-ttu-id="d6eb8-103">DiagnosticsLevel</span><span class="sxs-lookup"><span data-stu-id="d6eb8-103">DiagnosticsLevel</span></span>

<span data-ttu-id="d6eb8-104">El elemento **DiagnosticsLevel** representa la información de rendimiento y control de tiempo que se utilizará para derivar el informe.</span><span class="sxs-lookup"><span data-stu-id="d6eb8-104">The **DiagnosticsLevel** element represents timing and performance information that will be used to derive the report.</span></span> 
  
```XML
<DiagnosticsLevel/>
```

 <span data-ttu-id="d6eb8-105">**string**</span><span class="sxs-lookup"><span data-stu-id="d6eb8-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d6eb8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d6eb8-106">Attributes and elements</span></span>

<span data-ttu-id="d6eb8-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d6eb8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d6eb8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d6eb8-108">Attributes</span></span>

<span data-ttu-id="d6eb8-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d6eb8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d6eb8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d6eb8-110">Child elements</span></span>

<span data-ttu-id="d6eb8-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d6eb8-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d6eb8-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d6eb8-112">Parent elements</span></span>

|<span data-ttu-id="d6eb8-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d6eb8-113">**Element**</span></span>|<span data-ttu-id="d6eb8-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d6eb8-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d6eb8-115">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="d6eb8-115">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="d6eb8-116">Contiene los criterios para los tipos de mensajes para buscar.</span><span class="sxs-lookup"><span data-stu-id="d6eb8-116">Contains criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="d6eb8-117">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="d6eb8-117">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="d6eb8-118">Contiene la solicitud para la [operación de GetMessageTrackingReport](getmessagetrackingreport-operation.md) recuperar el mensaje completo informe de seguimiento para el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="d6eb8-118">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d6eb8-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d6eb8-119">Text value</span></span>

<span data-ttu-id="d6eb8-120">Si se usa este elemento, es necesario un valor de texto que representa una cadena.</span><span class="sxs-lookup"><span data-stu-id="d6eb8-120">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d6eb8-121">Notas</span><span class="sxs-lookup"><span data-stu-id="d6eb8-121">Remarks</span></span>

<span data-ttu-id="d6eb8-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d6eb8-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d6eb8-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d6eb8-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d6eb8-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d6eb8-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d6eb8-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d6eb8-125">Schema Name</span></span>  <br/> |<span data-ttu-id="d6eb8-126">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="d6eb8-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d6eb8-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d6eb8-127">Validation File</span></span>  <br/> |<span data-ttu-id="d6eb8-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d6eb8-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d6eb8-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d6eb8-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="d6eb8-130">False</span><span class="sxs-lookup"><span data-stu-id="d6eb8-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d6eb8-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="d6eb8-131">See also</span></span>

- [<span data-ttu-id="d6eb8-132">Operación GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="d6eb8-132">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)
- [<span data-ttu-id="d6eb8-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d6eb8-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

