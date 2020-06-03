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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461383"
---
# <a name="discoverysearchconfigurations"></a><span data-ttu-id="cd919-103">DiscoverySearchConfigurations</span><span class="sxs-lookup"><span data-stu-id="cd919-103">DiscoverySearchConfigurations</span></span>

<span data-ttu-id="cd919-104">El elemento **DiscoverySearchConfigurations** especifica una matriz de elementos **DiscoverySearchConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="cd919-104">The **DiscoverySearchConfigurations** element specifies an array of **DiscoverySearchConfiguration** elements.</span></span> 
  
```XML
<DiscoverySearchConfigurations>
    <DiscoverySearchConfiguration></DiscoverySearchConfiguration>
</DiscoverySearchConfigurations>
```

 <span data-ttu-id="cd919-105">**ArrayOfDiscoverySearchConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="cd919-105">**ArrayOfDiscoverySearchConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cd919-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cd919-106">Attributes and elements</span></span>

<span data-ttu-id="cd919-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cd919-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cd919-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="cd919-108">Attributes</span></span>

<span data-ttu-id="cd919-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cd919-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cd919-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cd919-110">Child elements</span></span>

|<span data-ttu-id="cd919-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cd919-111">**Element**</span></span>|<span data-ttu-id="cd919-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cd919-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cd919-113">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd919-113">DiscoverySearchConfiguration</span></span>](discoverysearchconfiguration.md) <br/> |<span data-ttu-id="cd919-114">Especifica la configuración de la búsqueda de exhibición de documentos electrónicos.</span><span class="sxs-lookup"><span data-stu-id="cd919-114">Specifies the configuration for eDiscovery search.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cd919-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cd919-115">Parent elements</span></span>

|<span data-ttu-id="cd919-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cd919-116">**Element**</span></span>|<span data-ttu-id="cd919-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cd919-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cd919-118">GetDiscoverySearchConfigurationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="cd919-118">GetDiscoverySearchConfigurationResponseMessage</span></span>](getdiscoverysearchconfigurationresponsemessage.md) <br/> |<span data-ttu-id="cd919-119">Especifica el mensaje de respuesta para una solicitud de **GetDiscoverySearchConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="cd919-119">Specifies the response message for a **GetDiscoverySearchConfiguration** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd919-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cd919-120">Remarks</span></span>

<span data-ttu-id="cd919-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="cd919-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="cd919-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="cd919-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cd919-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cd919-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cd919-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="cd919-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cd919-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cd919-125">Schema Name</span></span>  <br/> |<span data-ttu-id="cd919-126">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="cd919-126">Message schema</span></span>  <br/> |
|<span data-ttu-id="cd919-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cd919-127">Validation File</span></span>  <br/> |<span data-ttu-id="cd919-128">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="cd919-128">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cd919-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cd919-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="cd919-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd919-130">See also</span></span>

- [<span data-ttu-id="cd919-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="cd919-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

