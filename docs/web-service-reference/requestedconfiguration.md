---
title: RequestedConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RequestedConfiguration
api_type:
- schema
ms.assetid: 24921387-f676-49e6-8d7a-ef3115024866
description: El elemento RequestedConfiguration contiene las configuraciones del servicio solicitado.
ms.openlocfilehash: 1edc6394360250c9a9810fe614c975cb48eba3f0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837130"
---
# <a name="requestedconfiguration"></a><span data-ttu-id="a3ae8-103">RequestedConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3ae8-103">RequestedConfiguration</span></span>

<span data-ttu-id="a3ae8-104">El elemento **RequestedConfiguration** contiene las configuraciones del servicio solicitado.</span><span class="sxs-lookup"><span data-stu-id="a3ae8-104">The **RequestedConfiguration** element contains the requested service configurations.</span></span> 
  
```XML
<RequestedConfiguration>
   <ConfigurationName/>
</RequestedConfiguration>
```

 <span data-ttu-id="a3ae8-105">**ArrayOfServiceConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="a3ae8-105">**ArrayOfServiceConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a3ae8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a3ae8-106">Attributes and elements</span></span>

<span data-ttu-id="a3ae8-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a3ae8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a3ae8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a3ae8-108">Attributes</span></span>

<span data-ttu-id="a3ae8-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a3ae8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a3ae8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a3ae8-110">Child elements</span></span>

|<span data-ttu-id="a3ae8-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a3ae8-111">**Element**</span></span>|<span data-ttu-id="a3ae8-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a3ae8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a3ae8-113">ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="a3ae8-113">ConfigurationName</span></span>](configurationname.md) <br/> |<span data-ttu-id="a3ae8-114">Especifica las configuraciones de servicio solicitado por su nombre.</span><span class="sxs-lookup"><span data-stu-id="a3ae8-114">Specifies the requested service configurations by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a3ae8-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a3ae8-115">Parent elements</span></span>

|<span data-ttu-id="a3ae8-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="a3ae8-116">**Element**</span></span>|<span data-ttu-id="a3ae8-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a3ae8-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a3ae8-118">GetServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3ae8-118">GetServiceConfiguration</span></span>](getserviceconfiguration.md) <br/> |<span data-ttu-id="a3ae8-119">Define una solicitud GetServiceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a3ae8-119">Defines a GetServiceConfiguration request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a3ae8-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a3ae8-120">Text value</span></span>

<span data-ttu-id="a3ae8-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a3ae8-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a3ae8-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3ae8-122">Remarks</span></span>

<span data-ttu-id="a3ae8-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a3ae8-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a3ae8-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a3ae8-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a3ae8-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a3ae8-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a3ae8-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a3ae8-126">Schema Name</span></span>  <br/> |<span data-ttu-id="a3ae8-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="a3ae8-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a3ae8-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a3ae8-128">Validation File</span></span>  <br/> |<span data-ttu-id="a3ae8-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a3ae8-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a3ae8-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a3ae8-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="a3ae8-131">False</span><span class="sxs-lookup"><span data-stu-id="a3ae8-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a3ae8-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="a3ae8-132">See also</span></span>



- [<span data-ttu-id="a3ae8-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="a3ae8-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

