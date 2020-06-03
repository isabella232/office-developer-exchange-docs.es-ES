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
description: El elemento ResponseMessages contiene una matriz de mensajes de respuesta de configuración del servicio.
ms.openlocfilehash: cf271224141ffeb6dc00069abf430ab33d3ca2fa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457455"
---
# <a name="responsemessages-arrayofserviceconfigurationresponsemessagetype"></a><span data-ttu-id="2f114-103">ResponseMessages (ArrayOfServiceConfigurationResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="2f114-103">ResponseMessages (ArrayOfServiceConfigurationResponseMessageType)</span></span>

<span data-ttu-id="2f114-104">El elemento **ResponseMessages** contiene una matriz de mensajes de respuesta de configuración del servicio.</span><span class="sxs-lookup"><span data-stu-id="2f114-104">The **ResponseMessages** element contains an array of service configuration response messages.</span></span> 
  
```XML
<ResponseMessages>
   <ServiceConfigurationResponseMessageType/>
</ResponseMessages>
```

 <span data-ttu-id="2f114-105">**ArrayOfServiceConfigurationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2f114-105">**ArrayOfServiceConfigurationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2f114-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2f114-106">Attributes and elements</span></span>

<span data-ttu-id="2f114-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2f114-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2f114-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2f114-108">Attributes</span></span>

<span data-ttu-id="2f114-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2f114-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2f114-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2f114-110">Child elements</span></span>

|<span data-ttu-id="2f114-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2f114-111">**Element**</span></span>|<span data-ttu-id="2f114-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2f114-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f114-113">ServiceConfigurationResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="2f114-113">ServiceConfigurationResponseMessageType</span></span>](serviceconfigurationresponsemessagetype.md) <br/> |<span data-ttu-id="2f114-114">Contiene las opciones de configuración del servicio.</span><span class="sxs-lookup"><span data-stu-id="2f114-114">Contains service configuration settings.</span></span> <span data-ttu-id="2f114-115">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="2f114-115">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2f114-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2f114-116">Parent elements</span></span>

|<span data-ttu-id="2f114-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2f114-117">**Element**</span></span>|<span data-ttu-id="2f114-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2f114-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f114-119">GetServiceConfigurationResponse</span><span class="sxs-lookup"><span data-stu-id="2f114-119">GetServiceConfigurationResponse</span></span>](getserviceconfigurationresponse.md) <br/> |<span data-ttu-id="2f114-120">Define una respuesta a una solicitud GetServiceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2f114-120">Defines a response to a GetServiceConfiguration request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2f114-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="2f114-121">Text value</span></span>

<span data-ttu-id="2f114-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2f114-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2f114-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2f114-123">Remarks</span></span>

<span data-ttu-id="2f114-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="2f114-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2f114-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2f114-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f114-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="2f114-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2f114-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2f114-127">Schema Name</span></span>  <br/> |<span data-ttu-id="2f114-128">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="2f114-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2f114-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2f114-129">Validation File</span></span>  <br/> |<span data-ttu-id="2f114-130">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="2f114-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2f114-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2f114-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="2f114-132">Falso</span><span class="sxs-lookup"><span data-stu-id="2f114-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2f114-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f114-133">See also</span></span>



- [<span data-ttu-id="2f114-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2f114-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

