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
description: El elemento DiagnosticsLevel representa la información de tiempo y de rendimiento que se usará para derivar el informe.
ms.openlocfilehash: 3060d4f1b8449a5870d964bdfcdbf0d503905abc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467833"
---
# <a name="diagnosticslevel"></a><span data-ttu-id="5dc14-103">DiagnosticsLevel</span><span class="sxs-lookup"><span data-stu-id="5dc14-103">DiagnosticsLevel</span></span>

<span data-ttu-id="5dc14-104">El elemento **DiagnosticsLevel** representa la información de tiempo y de rendimiento que se usará para derivar el informe.</span><span class="sxs-lookup"><span data-stu-id="5dc14-104">The **DiagnosticsLevel** element represents timing and performance information that will be used to derive the report.</span></span> 
  
```XML
<DiagnosticsLevel/>
```

 <span data-ttu-id="5dc14-105">**string**</span><span class="sxs-lookup"><span data-stu-id="5dc14-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5dc14-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5dc14-106">Attributes and elements</span></span>

<span data-ttu-id="5dc14-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5dc14-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5dc14-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5dc14-108">Attributes</span></span>

<span data-ttu-id="5dc14-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5dc14-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5dc14-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5dc14-110">Child elements</span></span>

<span data-ttu-id="5dc14-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5dc14-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5dc14-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5dc14-112">Parent elements</span></span>

|<span data-ttu-id="5dc14-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5dc14-113">**Element**</span></span>|<span data-ttu-id="5dc14-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5dc14-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5dc14-115">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="5dc14-115">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="5dc14-116">Contiene los criterios para los tipos de mensajes que se van a buscar.</span><span class="sxs-lookup"><span data-stu-id="5dc14-116">Contains criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="5dc14-117">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="5dc14-117">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="5dc14-118">Contiene la solicitud de la [operación GetMessageTrackingReport](getmessagetrackingreport-operation.md) para recuperar el informe completo de seguimiento de mensajes del identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="5dc14-118">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5dc14-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5dc14-119">Text value</span></span>

<span data-ttu-id="5dc14-120">Si se usa este elemento, se necesita un valor de texto que represente una cadena.</span><span class="sxs-lookup"><span data-stu-id="5dc14-120">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5dc14-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5dc14-121">Remarks</span></span>

<span data-ttu-id="5dc14-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="5dc14-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5dc14-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5dc14-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5dc14-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="5dc14-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5dc14-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5dc14-125">Schema Name</span></span>  <br/> |<span data-ttu-id="5dc14-126">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="5dc14-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5dc14-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5dc14-127">Validation File</span></span>  <br/> |<span data-ttu-id="5dc14-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="5dc14-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5dc14-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5dc14-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="5dc14-130">Falso</span><span class="sxs-lookup"><span data-stu-id="5dc14-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5dc14-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="5dc14-131">See also</span></span>

- [<span data-ttu-id="5dc14-132">Operación GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="5dc14-132">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)
- [<span data-ttu-id="5dc14-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="5dc14-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

