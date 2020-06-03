---
title: Idioma (DiscoverySearchConfigurationType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 34eab81c-d832-4925-9f76-d69f24b36931
description: El elemento Language (DiscoverySearchConfigurationType) identifica la referencia cultural que se va a usar para el formato específico de la referencia cultural de los intervalos de fechas. También especifica el idioma usado en una consulta de búsqueda.
ms.openlocfilehash: 3cf85525147bec5d6dfc6fe2b2af5916d42c44be
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463289"
---
# <a name="language-discoverysearchconfigurationtype"></a><span data-ttu-id="69bd1-104">Idioma (DiscoverySearchConfigurationType)</span><span class="sxs-lookup"><span data-stu-id="69bd1-104">Language (DiscoverySearchConfigurationType)</span></span>

<span data-ttu-id="69bd1-105">El elemento **Language (DiscoverySearchConfigurationType)** identifica la referencia cultural que se va a usar para el formato específico de la referencia cultural de los intervalos de fechas.</span><span class="sxs-lookup"><span data-stu-id="69bd1-105">The **Language (DiscoverySearchConfigurationType)** element identifies the culture to be used for the culture-specific format of date ranges.</span></span> <span data-ttu-id="69bd1-106">También especifica el idioma usado en una consulta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="69bd1-106">It also specifies the language used in a search query.</span></span> 
  
```XML
<Language />
```

 <span data-ttu-id="69bd1-107">**string**</span><span class="sxs-lookup"><span data-stu-id="69bd1-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="69bd1-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="69bd1-108">Attributes and elements</span></span>

<span data-ttu-id="69bd1-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="69bd1-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="69bd1-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="69bd1-110">Attributes</span></span>

<span data-ttu-id="69bd1-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="69bd1-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="69bd1-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="69bd1-112">Child elements</span></span>

<span data-ttu-id="69bd1-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="69bd1-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="69bd1-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="69bd1-114">Parent elements</span></span>

[<span data-ttu-id="69bd1-115">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="69bd1-115">DiscoverySearchConfiguration</span></span>](discoverysearchconfiguration.md)
  
## <a name="text-value"></a><span data-ttu-id="69bd1-116">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="69bd1-116">Text value</span></span>

<span data-ttu-id="69bd1-117">El valor de texto del elemento **Language (DiscoverySearchConfigurationType)** es una referencia cultural o un lenguaje.</span><span class="sxs-lookup"><span data-stu-id="69bd1-117">The text value of the **Language (DiscoverySearchConfigurationType)** element is a culture or language.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="69bd1-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="69bd1-118">Remarks</span></span>

<span data-ttu-id="69bd1-119">Este elemento especifica el formato de los intervalos de fechas especificados en la [operación SearchMailboxes](searchmailboxes-operation.md) o en la [operación SetHoldOnMailboxes](setholdonmailboxes-operation.md).</span><span class="sxs-lookup"><span data-stu-id="69bd1-119">This element specifies the format of date ranges specified in the [SearchMailboxes operation](searchmailboxes-operation.md) or the [SetHoldOnMailboxes operation](setholdonmailboxes-operation.md).</span></span>
  
<span data-ttu-id="69bd1-120">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="69bd1-120">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="69bd1-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="69bd1-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="69bd1-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="69bd1-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="69bd1-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="69bd1-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="69bd1-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="69bd1-124">Schema Name</span></span>  <br/> |<span data-ttu-id="69bd1-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="69bd1-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="69bd1-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="69bd1-126">Validation File</span></span>  <br/> |<span data-ttu-id="69bd1-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="69bd1-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="69bd1-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="69bd1-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="69bd1-129">Verdadero</span><span class="sxs-lookup"><span data-stu-id="69bd1-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="69bd1-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="69bd1-130">See also</span></span>



[<span data-ttu-id="69bd1-131">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="69bd1-131">DiscoverySearchConfiguration</span></span>](discoverysearchconfiguration.md)


- [<span data-ttu-id="69bd1-132">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="69bd1-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

