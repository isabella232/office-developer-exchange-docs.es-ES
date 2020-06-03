---
title: Diagnóstico
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
description: El elemento Diagnostics proporciona información sobre el rendimiento y el tiempo que se usa para los informes en un centro de datos.
ms.openlocfilehash: 9eb46ef7ceb877372aff9b029190af8c8d8115cd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467840"
---
# <a name="diagnostics"></a><span data-ttu-id="51f3d-103">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="51f3d-103">Diagnostics</span></span>

<span data-ttu-id="51f3d-104">El elemento **Diagnostics** proporciona información sobre el rendimiento y el tiempo que se usa para los informes en un centro de datos.</span><span class="sxs-lookup"><span data-stu-id="51f3d-104">The **Diagnostics** element provides timing and performance information that is used for reporting in a DataCenter.</span></span> 
  
```XML
<Diagnostics>
   <String/>
</Diagnostics>

```

 <span data-ttu-id="51f3d-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="51f3d-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="51f3d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="51f3d-106">Attributes and elements</span></span>

<span data-ttu-id="51f3d-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="51f3d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="51f3d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="51f3d-108">Attributes</span></span>

<span data-ttu-id="51f3d-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="51f3d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="51f3d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="51f3d-110">Child elements</span></span>

|<span data-ttu-id="51f3d-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="51f3d-111">**Element**</span></span>|<span data-ttu-id="51f3d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="51f3d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="51f3d-113">String</span><span class="sxs-lookup"><span data-stu-id="51f3d-113">String</span></span>](string.md) <br/> |<span data-ttu-id="51f3d-114">Contiene una cadena que usan los elementos, contactos, tareas y conversaciones.</span><span class="sxs-lookup"><span data-stu-id="51f3d-114">Contains a string that is used by items, contacts, tasks, and conversations.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="51f3d-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="51f3d-115">Parent elements</span></span>

|<span data-ttu-id="51f3d-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="51f3d-116">**Element**</span></span>|<span data-ttu-id="51f3d-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="51f3d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="51f3d-118">FindMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="51f3d-118">FindMessageTrackingReportResponse</span></span>](findmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="51f3d-119">Contiene el estado y el resultado de una sola solicitud de [operación FindMessageTrackingReport](findmessagetrackingreport-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="51f3d-119">Contains the status and result of a single [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="51f3d-120">GetMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="51f3d-120">GetMessageTrackingReportResponse</span></span>](getmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="51f3d-121">Contiene la respuesta para la [operación GetMessageTrackingReport](getmessagetrackingreport-operation.md).</span><span class="sxs-lookup"><span data-stu-id="51f3d-121">Contains the response for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="51f3d-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="51f3d-122">Text value</span></span>

<span data-ttu-id="51f3d-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="51f3d-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="51f3d-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="51f3d-124">Remarks</span></span>

<span data-ttu-id="51f3d-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="51f3d-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="51f3d-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="51f3d-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="51f3d-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="51f3d-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="51f3d-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="51f3d-128">Schema Name</span></span>  <br/> |<span data-ttu-id="51f3d-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="51f3d-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="51f3d-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="51f3d-130">Validation File</span></span>  <br/> |<span data-ttu-id="51f3d-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="51f3d-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="51f3d-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="51f3d-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="51f3d-133">Falso</span><span class="sxs-lookup"><span data-stu-id="51f3d-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="51f3d-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="51f3d-134">See also</span></span>

- [<span data-ttu-id="51f3d-135">Operación FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="51f3d-135">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)
- [<span data-ttu-id="51f3d-136">Operación GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="51f3d-136">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)
- [<span data-ttu-id="51f3d-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="51f3d-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

