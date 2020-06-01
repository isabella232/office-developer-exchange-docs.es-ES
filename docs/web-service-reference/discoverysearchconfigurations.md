---
title: DiscoverySearchConfigurations
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f04b14c9-384c-4016-b113-52a49e15e73b
description: El elemento DiscoverySearchConfigurations especifica una matriz de elementos DiscoverySearchConfiguration.
ms.openlocfilehash: 6af4c8198f2ad73f8b39f9718e11b88aa8075c39
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461383"
---
# <a name="discoverysearchconfigurations"></a><span data-ttu-id="374cb-103">DiscoverySearchConfigurations</span><span class="sxs-lookup"><span data-stu-id="374cb-103">DiscoverySearchConfigurations</span></span>

<span data-ttu-id="374cb-104">El elemento **DiscoverySearchConfigurations** especifica una matriz de elementos **DiscoverySearchConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="374cb-104">The **DiscoverySearchConfigurations** element specifies an array of **DiscoverySearchConfiguration** elements.</span></span> 
  
```XML
<DiscoverySearchConfigurations>
    <DiscoverySearchConfiguration></DiscoverySearchConfiguration>
</DiscoverySearchConfigurations>
```

 <span data-ttu-id="374cb-105">**ArrayOfDiscoverySearchConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="374cb-105">**ArrayOfDiscoverySearchConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="374cb-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="374cb-106">Attributes and elements</span></span>

<span data-ttu-id="374cb-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="374cb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="374cb-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="374cb-108">Attributes</span></span>

<span data-ttu-id="374cb-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="374cb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="374cb-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="374cb-110">Child elements</span></span>

|<span data-ttu-id="374cb-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="374cb-111">**Element**</span></span>|<span data-ttu-id="374cb-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="374cb-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="374cb-113">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="374cb-113">DiscoverySearchConfiguration</span></span>](discoverysearchconfiguration.md) <br/> |<span data-ttu-id="374cb-114">Especifica la configuración de la búsqueda de exhibición de documentos electrónicos.</span><span class="sxs-lookup"><span data-stu-id="374cb-114">Specifies the configuration for eDiscovery search.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="374cb-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="374cb-115">Parent elements</span></span>

|<span data-ttu-id="374cb-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="374cb-116">**Element**</span></span>|<span data-ttu-id="374cb-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="374cb-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="374cb-118">GetDiscoverySearchConfigurationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="374cb-118">GetDiscoverySearchConfigurationResponseMessage</span></span>](getdiscoverysearchconfigurationresponsemessage.md) <br/> |<span data-ttu-id="374cb-119">Especifica el mensaje de respuesta para una solicitud de **GetDiscoverySearchConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="374cb-119">Specifies the response message for a **GetDiscoverySearchConfiguration** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="374cb-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="374cb-120">Remarks</span></span>

<span data-ttu-id="374cb-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="374cb-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="374cb-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="374cb-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="374cb-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="374cb-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="374cb-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="374cb-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="374cb-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="374cb-125">Schema Name</span></span>  <br/> |<span data-ttu-id="374cb-126">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="374cb-126">Message schema</span></span>  <br/> |
|<span data-ttu-id="374cb-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="374cb-127">Validation File</span></span>  <br/> |<span data-ttu-id="374cb-128">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="374cb-128">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="374cb-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="374cb-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="374cb-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="374cb-130">See also</span></span>

- [<span data-ttu-id="374cb-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="374cb-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

