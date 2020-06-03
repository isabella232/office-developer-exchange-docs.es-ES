---
title: DiscoverySearchConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 085384f9-dca4-4534-82e2-dd782471d0da
description: El elemento DiscoverySearchConfiguration especifica la configuración de la búsqueda de exhibición de documentos electrónicos.
ms.openlocfilehash: 8819d951f35ccc215bdf0128d2a16b60bbf20f2a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529059"
---
# <a name="discoverysearchconfiguration"></a><span data-ttu-id="7e6a7-103">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e6a7-103">DiscoverySearchConfiguration</span></span>

<span data-ttu-id="7e6a7-104">El elemento **DiscoverySearchConfiguration** especifica la configuración de la búsqueda de exhibición de documentos electrónicos.</span><span class="sxs-lookup"><span data-stu-id="7e6a7-104">The **DiscoverySearchConfiguration** element specifies the configuration for eDiscovery search.</span></span> 
  
```XML
<DiscoverySearchConfiguration>
    <SearchId></SearchId>
    <SearchQuery></SearchQuery>
    <SearchableMailboxes></SearchableMailboxes>
</DiscoverySearchConfiguration>
```

 <span data-ttu-id="7e6a7-105">**DiscoverySearchConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="7e6a7-105">**DiscoverySearchConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7e6a7-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7e6a7-106">Attributes and elements</span></span>

<span data-ttu-id="7e6a7-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7e6a7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7e6a7-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7e6a7-108">Attributes</span></span>

<span data-ttu-id="7e6a7-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7e6a7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7e6a7-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7e6a7-110">Child elements</span></span>

|<span data-ttu-id="7e6a7-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7e6a7-111">**Element**</span></span>|<span data-ttu-id="7e6a7-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7e6a7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7e6a7-113">SearchId</span><span class="sxs-lookup"><span data-stu-id="7e6a7-113">SearchId</span></span>](searchid.md) <br/> |<span data-ttu-id="7e6a7-114">Especifica el identificador de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="7e6a7-114">Specifies the identifier of the search.</span></span>  <br/> |
|[<span data-ttu-id="7e6a7-115">SearchQuery</span><span class="sxs-lookup"><span data-stu-id="7e6a7-115">SearchQuery</span></span>](searchquery.md) <br/> |<span data-ttu-id="7e6a7-116">Especifica el nombre de una consulta de búsqueda de exhibición de documentos electrónicos.</span><span class="sxs-lookup"><span data-stu-id="7e6a7-116">Specifies the name of an eDiscovery search query.</span></span>  <br/> |
|[<span data-ttu-id="7e6a7-117">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="7e6a7-117">SearchableMailboxes</span></span>](searchablemailboxes.md) <br/> |<span data-ttu-id="7e6a7-118">Contiene una lista de los buzones devueltos por una solicitud **GetSearchableMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="7e6a7-118">Contains a list of the mailboxes returned from a **GetSearchableMailboxes** request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7e6a7-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7e6a7-119">Parent elements</span></span>

|<span data-ttu-id="7e6a7-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7e6a7-120">**Element**</span></span>|<span data-ttu-id="7e6a7-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7e6a7-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7e6a7-122">DiscoverySearchConfigurations</span><span class="sxs-lookup"><span data-stu-id="7e6a7-122">DiscoverySearchConfigurations</span></span>](discoverysearchconfigurations.md) <br/> |<span data-ttu-id="7e6a7-123">Especifica una matriz de elementos **DiscoverySearchConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="7e6a7-123">Specifies an array of **DiscoverySearchConfiguration** elements.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7e6a7-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7e6a7-124">Remarks</span></span>

<span data-ttu-id="7e6a7-125">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7e6a7-125">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7e6a7-126">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="7e6a7-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7e6a7-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7e6a7-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7e6a7-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="7e6a7-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7e6a7-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7e6a7-129">Schema Name</span></span>  <br/> |<span data-ttu-id="7e6a7-130">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="7e6a7-130">Message schema</span></span>  <br/> |
|<span data-ttu-id="7e6a7-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7e6a7-131">Validation File</span></span>  <br/> |<span data-ttu-id="7e6a7-132">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="7e6a7-132">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7e6a7-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7e6a7-133">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="7e6a7-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e6a7-134">See also</span></span>

- [<span data-ttu-id="7e6a7-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="7e6a7-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

