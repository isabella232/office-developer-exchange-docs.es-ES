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
description: El elemento RequestedConfiguration contiene las configuraciones de servicio solicitadas.
ms.openlocfilehash: bbc503e6d6f7c56c785365924106bc2468965d0b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457154"
---
# <a name="requestedconfiguration"></a><span data-ttu-id="aa8ab-103">RequestedConfiguration</span><span class="sxs-lookup"><span data-stu-id="aa8ab-103">RequestedConfiguration</span></span>

<span data-ttu-id="aa8ab-104">El elemento **RequestedConfiguration** contiene las configuraciones de servicio solicitadas.</span><span class="sxs-lookup"><span data-stu-id="aa8ab-104">The **RequestedConfiguration** element contains the requested service configurations.</span></span> 
  
```XML
<RequestedConfiguration>
   <ConfigurationName/>
</RequestedConfiguration>
```

 <span data-ttu-id="aa8ab-105">**ArrayOfServiceConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="aa8ab-105">**ArrayOfServiceConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aa8ab-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="aa8ab-106">Attributes and elements</span></span>

<span data-ttu-id="aa8ab-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="aa8ab-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aa8ab-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="aa8ab-108">Attributes</span></span>

<span data-ttu-id="aa8ab-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="aa8ab-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aa8ab-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="aa8ab-110">Child elements</span></span>

|<span data-ttu-id="aa8ab-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="aa8ab-111">**Element**</span></span>|<span data-ttu-id="aa8ab-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aa8ab-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aa8ab-113">ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="aa8ab-113">ConfigurationName</span></span>](configurationname.md) <br/> |<span data-ttu-id="aa8ab-114">Especifica las configuraciones de servicio solicitadas por nombre.</span><span class="sxs-lookup"><span data-stu-id="aa8ab-114">Specifies the requested service configurations by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="aa8ab-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="aa8ab-115">Parent elements</span></span>

|<span data-ttu-id="aa8ab-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="aa8ab-116">**Element**</span></span>|<span data-ttu-id="aa8ab-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aa8ab-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aa8ab-118">GetServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="aa8ab-118">GetServiceConfiguration</span></span>](getserviceconfiguration.md) <br/> |<span data-ttu-id="aa8ab-119">Define una solicitud de GetServiceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="aa8ab-119">Defines a GetServiceConfiguration request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="aa8ab-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="aa8ab-120">Text value</span></span>

<span data-ttu-id="aa8ab-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="aa8ab-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aa8ab-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aa8ab-122">Remarks</span></span>

<span data-ttu-id="aa8ab-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="aa8ab-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aa8ab-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="aa8ab-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aa8ab-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="aa8ab-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="aa8ab-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="aa8ab-126">Schema Name</span></span>  <br/> |<span data-ttu-id="aa8ab-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="aa8ab-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="aa8ab-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="aa8ab-128">Validation File</span></span>  <br/> |<span data-ttu-id="aa8ab-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="aa8ab-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="aa8ab-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="aa8ab-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="aa8ab-131">Falso</span><span class="sxs-lookup"><span data-stu-id="aa8ab-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aa8ab-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa8ab-132">See also</span></span>



- [<span data-ttu-id="aa8ab-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="aa8ab-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

