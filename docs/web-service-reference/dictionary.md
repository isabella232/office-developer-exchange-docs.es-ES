---
title: Dictionary
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Dictionary
api_type:
- schema
ms.assetid: 8309e468-115b-4d6e-b33c-c4719dcecc4c
description: El elemento Dictionary define un conjunto de entradas de diccionario (propiedad) para un objeto de configuración de usuario.
ms.openlocfilehash: 151abfe7a9a9ae05b8b61af87c33675e025920ec
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764151"
---
# <a name="dictionary"></a><span data-ttu-id="d29d8-103">Dictionary</span><span class="sxs-lookup"><span data-stu-id="d29d8-103">Dictionary</span></span>

<span data-ttu-id="d29d8-104">El elemento **Dictionary** define un conjunto de entradas de diccionario (propiedad) para un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="d29d8-104">The **Dictionary** element defines a set of dictionary property entries for a user configuration object.</span></span> 
  
```xml
<Dictionary>
   <DictionaryEntry/>
</Dictionary>
```

 <span data-ttu-id="d29d8-105">**UserConfigurationDictionaryType**</span><span class="sxs-lookup"><span data-stu-id="d29d8-105">**UserConfigurationDictionaryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d29d8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d29d8-106">Attributes and elements</span></span>

<span data-ttu-id="d29d8-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d29d8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d29d8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d29d8-108">Attributes</span></span>

<span data-ttu-id="d29d8-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d29d8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d29d8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d29d8-110">Child elements</span></span>

|<span data-ttu-id="d29d8-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d29d8-111">**Element**</span></span>|<span data-ttu-id="d29d8-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d29d8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d29d8-113">DictionaryEntry</span><span class="sxs-lookup"><span data-stu-id="d29d8-113">DictionaryEntry</span></span>](dictionaryentry.md) <br/> |<span data-ttu-id="d29d8-114">Especifica el contenido de una propiedad de entrada único diccionario.</span><span class="sxs-lookup"><span data-stu-id="d29d8-114">Specifies the contents of a single dictionary entry property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d29d8-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d29d8-115">Parent elements</span></span>

|<span data-ttu-id="d29d8-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="d29d8-116">**Element**</span></span>|<span data-ttu-id="d29d8-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d29d8-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d29d8-118">UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="d29d8-118">UserConfiguration</span></span>](userconfiguration.md) <br/> |<span data-ttu-id="d29d8-119">Define un objeto de configuración de usuario único.</span><span class="sxs-lookup"><span data-stu-id="d29d8-119">Defines a single user configuration object.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d29d8-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d29d8-120">Text value</span></span>

<span data-ttu-id="d29d8-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d29d8-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d29d8-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d29d8-122">Remarks</span></span>

<span data-ttu-id="d29d8-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d29d8-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d29d8-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d29d8-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d29d8-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d29d8-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d29d8-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d29d8-126">Schema Name</span></span>  <br/> |<span data-ttu-id="d29d8-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d29d8-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="d29d8-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d29d8-128">Validation File</span></span>  <br/> |<span data-ttu-id="d29d8-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d29d8-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d29d8-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d29d8-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="d29d8-131">False</span><span class="sxs-lookup"><span data-stu-id="d29d8-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d29d8-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="d29d8-132">See also</span></span>

- [<span data-ttu-id="d29d8-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d29d8-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

