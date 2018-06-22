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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764151"
---
# <a name="dictionary"></a><span data-ttu-id="673db-103">Dictionary</span><span class="sxs-lookup"><span data-stu-id="673db-103">Dictionary</span></span>

<span data-ttu-id="673db-104">El elemento **Dictionary** define un conjunto de entradas de diccionario (propiedad) para un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="673db-104">The **Dictionary** element defines a set of dictionary property entries for a user configuration object.</span></span> 
  
```xml
<Dictionary>
   <DictionaryEntry/>
</Dictionary>
```

 <span data-ttu-id="673db-105">**UserConfigurationDictionaryType**</span><span class="sxs-lookup"><span data-stu-id="673db-105">**UserConfigurationDictionaryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="673db-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="673db-106">Attributes and elements</span></span>

<span data-ttu-id="673db-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="673db-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="673db-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="673db-108">Attributes</span></span>

<span data-ttu-id="673db-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="673db-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="673db-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="673db-110">Child elements</span></span>

|<span data-ttu-id="673db-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="673db-111">**Element**</span></span>|<span data-ttu-id="673db-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="673db-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="673db-113">DictionaryEntry</span><span class="sxs-lookup"><span data-stu-id="673db-113">DictionaryEntry</span></span>](dictionaryentry.md) <br/> |<span data-ttu-id="673db-114">Especifica el contenido de una propiedad de entrada único diccionario.</span><span class="sxs-lookup"><span data-stu-id="673db-114">Specifies the contents of a single dictionary entry property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="673db-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="673db-115">Parent elements</span></span>

|<span data-ttu-id="673db-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="673db-116">**Element**</span></span>|<span data-ttu-id="673db-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="673db-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="673db-118">UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="673db-118">UserConfiguration</span></span>](userconfiguration.md) <br/> |<span data-ttu-id="673db-119">Define un objeto de configuración de usuario único.</span><span class="sxs-lookup"><span data-stu-id="673db-119">Defines a single user configuration object.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="673db-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="673db-120">Text value</span></span>

<span data-ttu-id="673db-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="673db-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="673db-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="673db-122">Remarks</span></span>

<span data-ttu-id="673db-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="673db-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="673db-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="673db-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="673db-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="673db-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="673db-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="673db-126">Schema Name</span></span>  <br/> |<span data-ttu-id="673db-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="673db-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="673db-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="673db-128">Validation File</span></span>  <br/> |<span data-ttu-id="673db-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="673db-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="673db-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="673db-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="673db-131">False</span><span class="sxs-lookup"><span data-stu-id="673db-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="673db-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="673db-132">See also</span></span>

- [<span data-ttu-id="673db-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="673db-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

