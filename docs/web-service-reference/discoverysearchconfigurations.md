---
title: DiscoverySearchConfigurations
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f04b14c9-384c-4016-b113-52a49e15e73b
description: El elemento DiscoverySearchConfigurations especifica una matriz de elementos de DiscoverySearchConfiguration.
ms.openlocfilehash: a95bb35b88114e8e72e22de424679993fd4eef2a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764212"
---
# <a name="discoverysearchconfigurations"></a><span data-ttu-id="2b4d5-103">DiscoverySearchConfigurations</span><span class="sxs-lookup"><span data-stu-id="2b4d5-103">DiscoverySearchConfigurations</span></span>

<span data-ttu-id="2b4d5-104">El elemento **DiscoverySearchConfigurations** especifica una matriz de elementos de **DiscoverySearchConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="2b4d5-104">The **DiscoverySearchConfigurations** element specifies an array of **DiscoverySearchConfiguration** elements.</span></span> 
  
```XML
<DiscoverySearchConfigurations>
    <DiscoverySearchConfiguration></DiscoverySearchConfiguration>
</DiscoverySearchConfigurations>
```

 <span data-ttu-id="2b4d5-105">**ArrayOfDiscoverySearchConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="2b4d5-105">**ArrayOfDiscoverySearchConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2b4d5-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2b4d5-106">Attributes and elements</span></span>

<span data-ttu-id="2b4d5-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2b4d5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2b4d5-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2b4d5-108">Attributes</span></span>

<span data-ttu-id="2b4d5-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2b4d5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2b4d5-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2b4d5-110">Child elements</span></span>

|<span data-ttu-id="2b4d5-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="2b4d5-111">**Element**</span></span>|<span data-ttu-id="2b4d5-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2b4d5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2b4d5-113">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b4d5-113">DiscoverySearchConfiguration</span></span>](discoverysearchconfiguration.md) <br/> |<span data-ttu-id="2b4d5-114">Especifica la configuración para la búsqueda de exhibición de documentos electrónicos.</span><span class="sxs-lookup"><span data-stu-id="2b4d5-114">Specifies the configuration for eDiscovery search.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2b4d5-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2b4d5-115">Parent elements</span></span>

|<span data-ttu-id="2b4d5-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="2b4d5-116">**Element**</span></span>|<span data-ttu-id="2b4d5-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2b4d5-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2b4d5-118">GetDiscoverySearchConfigurationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2b4d5-118">GetDiscoverySearchConfigurationResponseMessage</span></span>](getdiscoverysearchconfigurationresponsemessage.md) <br/> |<span data-ttu-id="2b4d5-119">Especifica el mensaje de respuesta de una solicitud de **GetDiscoverySearchConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="2b4d5-119">Specifies the response message for a **GetDiscoverySearchConfiguration** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b4d5-120">Notas</span><span class="sxs-lookup"><span data-stu-id="2b4d5-120">Remarks</span></span>

<span data-ttu-id="2b4d5-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2b4d5-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2b4d5-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="2b4d5-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2b4d5-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2b4d5-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2b4d5-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2b4d5-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2b4d5-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2b4d5-125">Schema Name</span></span>  <br/> |<span data-ttu-id="2b4d5-126">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="2b4d5-126">Message schema</span></span>  <br/> |
|<span data-ttu-id="2b4d5-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2b4d5-127">Validation File</span></span>  <br/> |<span data-ttu-id="2b4d5-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2b4d5-128">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2b4d5-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2b4d5-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="2b4d5-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="2b4d5-130">See also</span></span>

- [<span data-ttu-id="2b4d5-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="2b4d5-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

