---
title: ResponseMessages (ArrayOfServiceConfigurationResponseMessageType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResponseMessages
api_type:
- schema
ms.assetid: c7cfa0d1-fcb2-441f-8489-3a549da33b34
description: El elemento ResponseMessages contiene una matriz de los mensajes de respuesta de configuración de servicio.
ms.openlocfilehash: af8a6db8d6e9d3ec76b532a81ef2a7392dcfde7a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837194"
---
# <a name="responsemessages-arrayofserviceconfigurationresponsemessagetype"></a><span data-ttu-id="a2444-103">ResponseMessages (ArrayOfServiceConfigurationResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="a2444-103">ResponseMessages (ArrayOfServiceConfigurationResponseMessageType)</span></span>

<span data-ttu-id="a2444-104">El elemento **ResponseMessages** contiene una matriz de los mensajes de respuesta de configuración de servicio.</span><span class="sxs-lookup"><span data-stu-id="a2444-104">The **ResponseMessages** element contains an array of service configuration response messages.</span></span> 
  
```XML
<ResponseMessages>
   <ServiceConfigurationResponseMessageType/>
</ResponseMessages>
```

 <span data-ttu-id="a2444-105">**ArrayOfServiceConfigurationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="a2444-105">**ArrayOfServiceConfigurationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a2444-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a2444-106">Attributes and elements</span></span>

<span data-ttu-id="a2444-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a2444-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a2444-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a2444-108">Attributes</span></span>

<span data-ttu-id="a2444-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a2444-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a2444-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a2444-110">Child elements</span></span>

|<span data-ttu-id="a2444-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a2444-111">**Element**</span></span>|<span data-ttu-id="a2444-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a2444-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a2444-113">ServiceConfigurationResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="a2444-113">ServiceConfigurationResponseMessageType</span></span>](serviceconfigurationresponsemessagetype.md) <br/> |<span data-ttu-id="a2444-114">Contiene la configuración del servicio.</span><span class="sxs-lookup"><span data-stu-id="a2444-114">Contains service configuration settings.</span></span> <span data-ttu-id="a2444-115">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="a2444-115">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a2444-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a2444-116">Parent elements</span></span>

|<span data-ttu-id="a2444-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="a2444-117">**Element**</span></span>|<span data-ttu-id="a2444-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a2444-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a2444-119">GetServiceConfigurationResponse</span><span class="sxs-lookup"><span data-stu-id="a2444-119">GetServiceConfigurationResponse</span></span>](getserviceconfigurationresponse.md) <br/> |<span data-ttu-id="a2444-120">Define una respuesta a una solicitud de GetServiceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a2444-120">Defines a response to a GetServiceConfiguration request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a2444-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a2444-121">Text value</span></span>

<span data-ttu-id="a2444-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a2444-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a2444-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a2444-123">Remarks</span></span>

<span data-ttu-id="a2444-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a2444-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a2444-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a2444-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a2444-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a2444-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a2444-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a2444-127">Schema Name</span></span>  <br/> |<span data-ttu-id="a2444-128">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="a2444-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a2444-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a2444-129">Validation File</span></span>  <br/> |<span data-ttu-id="a2444-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a2444-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a2444-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a2444-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="a2444-132">False</span><span class="sxs-lookup"><span data-stu-id="a2444-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a2444-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2444-133">See also</span></span>



- [<span data-ttu-id="a2444-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="a2444-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

