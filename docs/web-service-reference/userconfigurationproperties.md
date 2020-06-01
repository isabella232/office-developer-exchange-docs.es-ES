---
title: UserConfigurationProperties
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserConfigurationProperties
api_type:
- schema
ms.assetid: c143a6ec-62ad-4d48-b844-b1ad88054bc1
description: El elemento UserConfigurationProperties especifica los tipos de propiedad que se van a obtener en una operación GetUserConfiguration.
ms.openlocfilehash: af6bee64516a7410d96ecc7581e8e819f550ddc1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466496"
---
# <a name="userconfigurationproperties"></a><span data-ttu-id="e07c9-103">UserConfigurationProperties</span><span class="sxs-lookup"><span data-stu-id="e07c9-103">UserConfigurationProperties</span></span>

<span data-ttu-id="e07c9-104">El elemento **UserConfigurationProperties** especifica los tipos de propiedad que se van a obtener en una operación GetUserConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e07c9-104">The **UserConfigurationProperties** element specifies the property types to get in a GetUserConfiguration operation.</span></span> 
  
```xml
<UserConfigurationProperties>Id | Dictionary | XmlData | BinaryData | All</UserConfigurationProperties>
```

 <span data-ttu-id="e07c9-105">**UserConfigurationPropertyType**</span><span class="sxs-lookup"><span data-stu-id="e07c9-105">**UserConfigurationPropertyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e07c9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e07c9-106">Attributes and elements</span></span>

<span data-ttu-id="e07c9-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e07c9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e07c9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e07c9-108">Attributes</span></span>

<span data-ttu-id="e07c9-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e07c9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e07c9-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e07c9-110">Child elements</span></span>

<span data-ttu-id="e07c9-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e07c9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e07c9-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e07c9-112">Parent elements</span></span>

|<span data-ttu-id="e07c9-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e07c9-113">**Element**</span></span>|<span data-ttu-id="e07c9-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e07c9-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e07c9-115">GetUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="e07c9-115">GetUserConfiguration</span></span>](getuserconfiguration.md) <br/> |<span data-ttu-id="e07c9-116">Especifica una solicitud para obtener un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="e07c9-116">Specifies a request to get a user configuration object.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e07c9-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e07c9-117">Text value</span></span>

<span data-ttu-id="e07c9-118">En la siguiente tabla se enumeran los valores posibles para el elemento **UserConfigurationProperties** .</span><span class="sxs-lookup"><span data-stu-id="e07c9-118">The following table lists the possible values for the **UserConfigurationProperties** element.</span></span> 
  
|<span data-ttu-id="e07c9-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e07c9-119">**Value**</span></span>|<span data-ttu-id="e07c9-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e07c9-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e07c9-121">Id</span><span class="sxs-lookup"><span data-stu-id="e07c9-121">Id</span></span>  <br/> |<span data-ttu-id="e07c9-122">Especifica la propiedad de identificador.</span><span class="sxs-lookup"><span data-stu-id="e07c9-122">Specifies the identifier property.</span></span>  <br/> |
|<span data-ttu-id="e07c9-123">Dictionary</span><span class="sxs-lookup"><span data-stu-id="e07c9-123">Dictionary</span></span>  <br/> |<span data-ttu-id="e07c9-124">Especifica los tipos de propiedades de diccionario.</span><span class="sxs-lookup"><span data-stu-id="e07c9-124">Specifies dictionary property types.</span></span>  <br/> |
|<span data-ttu-id="e07c9-125">XmlData</span><span class="sxs-lookup"><span data-stu-id="e07c9-125">XmlData</span></span>  <br/> |<span data-ttu-id="e07c9-126">Especifica los tipos de propiedades de datos XML.</span><span class="sxs-lookup"><span data-stu-id="e07c9-126">Specifies XML data property types.</span></span>  <br/> |
|<span data-ttu-id="e07c9-127">BinaryData</span><span class="sxs-lookup"><span data-stu-id="e07c9-127">BinaryData</span></span>  <br/> |<span data-ttu-id="e07c9-128">Especifica los tipos de propiedades de datos binarios.</span><span class="sxs-lookup"><span data-stu-id="e07c9-128">Specifies binary data property types.</span></span>  <br/> |
|<span data-ttu-id="e07c9-129">Todo</span><span class="sxs-lookup"><span data-stu-id="e07c9-129">All</span></span>  <br/> |<span data-ttu-id="e07c9-130">Especifica los tipos de propiedad de identificador, diccionario, datos XML y datos binarios.</span><span class="sxs-lookup"><span data-stu-id="e07c9-130">Specifies the identifier, dictionary, XML data, and binary data property types.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e07c9-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e07c9-131">Remarks</span></span>

<span data-ttu-id="e07c9-132">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e07c9-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e07c9-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e07c9-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e07c9-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="e07c9-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e07c9-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e07c9-135">Schema Name</span></span>  <br/> |<span data-ttu-id="e07c9-136">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="e07c9-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e07c9-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e07c9-137">Validation File</span></span>  <br/> |<span data-ttu-id="e07c9-138">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="e07c9-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e07c9-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e07c9-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="e07c9-140">Falso</span><span class="sxs-lookup"><span data-stu-id="e07c9-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e07c9-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="e07c9-141">See also</span></span>



- [<span data-ttu-id="e07c9-142">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e07c9-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

