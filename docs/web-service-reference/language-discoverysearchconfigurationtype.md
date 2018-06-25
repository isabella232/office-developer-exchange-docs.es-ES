---
title: Idioma (DiscoverySearchConfigurationType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 34eab81c-d832-4925-9f76-d69f24b36931
description: El elemento de idioma (DiscoverySearchConfigurationType) identifica la referencia cultural que se usará para el formato de referencias culturales específicas de los intervalos de fechas. También especifica el lenguaje utilizado en una consulta de búsqueda.
ms.openlocfilehash: 1e904ac4d7f525b2d12cfe83f0da33b9ed474066
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836197"
---
# <a name="language-discoverysearchconfigurationtype"></a><span data-ttu-id="81c30-104">Idioma (DiscoverySearchConfigurationType)</span><span class="sxs-lookup"><span data-stu-id="81c30-104">Language (DiscoverySearchConfigurationType)</span></span>

<span data-ttu-id="81c30-105">El elemento de **idioma (DiscoverySearchConfigurationType)** identifica la referencia cultural que se usará para el formato de referencias culturales específicas de los intervalos de fechas.</span><span class="sxs-lookup"><span data-stu-id="81c30-105">The **Language (DiscoverySearchConfigurationType)** element identifies the culture to be used for the culture-specific format of date ranges.</span></span> <span data-ttu-id="81c30-106">También especifica el lenguaje utilizado en una consulta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="81c30-106">It also specifies the language used in a search query.</span></span> 
  
```XML
<Language />
```

 <span data-ttu-id="81c30-107">**string**</span><span class="sxs-lookup"><span data-stu-id="81c30-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="81c30-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="81c30-108">Attributes and elements</span></span>

<span data-ttu-id="81c30-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="81c30-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="81c30-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="81c30-110">Attributes</span></span>

<span data-ttu-id="81c30-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="81c30-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="81c30-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="81c30-112">Child elements</span></span>

<span data-ttu-id="81c30-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="81c30-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="81c30-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="81c30-114">Parent elements</span></span>

[<span data-ttu-id="81c30-115">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="81c30-115">DiscoverySearchConfiguration</span></span>](discoverysearchconfiguration.md)
  
## <a name="text-value"></a><span data-ttu-id="81c30-116">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="81c30-116">Text value</span></span>

<span data-ttu-id="81c30-117">El valor de texto del elemento de **idioma (DiscoverySearchConfigurationType)** es un idioma o referencia cultural.</span><span class="sxs-lookup"><span data-stu-id="81c30-117">The text value of the **Language (DiscoverySearchConfigurationType)** element is a culture or language.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="81c30-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="81c30-118">Remarks</span></span>

<span data-ttu-id="81c30-119">Este elemento especifica el formato de los intervalos de fechas especificado en la [operación de SearchMailboxes](searchmailboxes-operation.md) o la [operación SetHoldOnMailboxes](setholdonmailboxes-operation.md).</span><span class="sxs-lookup"><span data-stu-id="81c30-119">This element specifies the format of date ranges specified in the [SearchMailboxes operation](searchmailboxes-operation.md) or the [SetHoldOnMailboxes operation](setholdonmailboxes-operation.md).</span></span>
  
<span data-ttu-id="81c30-120">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="81c30-120">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="81c30-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="81c30-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="81c30-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="81c30-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="81c30-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="81c30-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="81c30-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="81c30-124">Schema Name</span></span>  <br/> |<span data-ttu-id="81c30-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="81c30-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="81c30-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="81c30-126">Validation File</span></span>  <br/> |<span data-ttu-id="81c30-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="81c30-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="81c30-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="81c30-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="81c30-129">Verdadero</span><span class="sxs-lookup"><span data-stu-id="81c30-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="81c30-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="81c30-130">See also</span></span>



[<span data-ttu-id="81c30-131">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="81c30-131">DiscoverySearchConfiguration</span></span>](discoverysearchconfiguration.md)


- [<span data-ttu-id="81c30-132">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="81c30-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

