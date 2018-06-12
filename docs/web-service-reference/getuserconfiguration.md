---
title: GetUserConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetUserConfiguration
api_type:
- schema
ms.assetid: 4044c0a1-cd88-41ae-9cc4-a7cf2b279094
description: El elemento GetUserConfiguration representan una solicitud para obtener un objeto de configuración de usuario.
ms.openlocfilehash: 81f2ca4995de69d6547412ec699a2ceaddcce385
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835688"
---
# <a name="getuserconfiguration"></a><span data-ttu-id="eb415-103">GetUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb415-103">GetUserConfiguration</span></span>

<span data-ttu-id="eb415-104">El elemento **GetUserConfiguration** representan una solicitud para obtener un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="eb415-104">The **GetUserConfiguration** element represent a request to get a user configuration object.</span></span> 
  
```XML
<GetUserConfiguration>
   <UserConfigurationName/>
   <UserConfigurationProperties/>
</GetUserConfiguration>
```

 <span data-ttu-id="eb415-105">**GetUserConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="eb415-105">**GetUserConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eb415-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="eb415-106">Attributes and elements</span></span>

<span data-ttu-id="eb415-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="eb415-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eb415-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="eb415-108">Attributes</span></span>

<span data-ttu-id="eb415-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="eb415-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eb415-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="eb415-110">Child elements</span></span>

|<span data-ttu-id="eb415-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="eb415-111">**Element**</span></span>|<span data-ttu-id="eb415-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="eb415-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eb415-113">UserConfigurationName</span><span class="sxs-lookup"><span data-stu-id="eb415-113">UserConfigurationName</span></span>](userconfigurationname.md) <br/> |<span data-ttu-id="eb415-114">Representa el nombre de un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="eb415-114">Represents the name of a user configuration object.</span></span> <span data-ttu-id="eb415-115">Este elemento debe estar presente en una solicitud de GetUserConfiguration.</span><span class="sxs-lookup"><span data-stu-id="eb415-115">This element must be present in a GetUserConfiguration request.</span></span>  <br/> |
|[<span data-ttu-id="eb415-116">UserConfigurationProperties</span><span class="sxs-lookup"><span data-stu-id="eb415-116">UserConfigurationProperties</span></span>](userconfigurationproperties.md) <br/> |<span data-ttu-id="eb415-117">Especifica los tipos de propiedad de configuración de usuario para devolver.</span><span class="sxs-lookup"><span data-stu-id="eb415-117">Specifies the user configuration property types to return.</span></span> <span data-ttu-id="eb415-118">Este elemento debe estar presente en una solicitud de GetUserConfiguration.</span><span class="sxs-lookup"><span data-stu-id="eb415-118">This element must be present in a GetUserConfiguration request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="eb415-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="eb415-119">Parent elements</span></span>

<span data-ttu-id="eb415-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="eb415-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="eb415-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="eb415-121">Text value</span></span>

<span data-ttu-id="eb415-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="eb415-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eb415-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eb415-123">Remarks</span></span>

<span data-ttu-id="eb415-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="eb415-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eb415-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="eb415-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb415-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="eb415-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="eb415-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="eb415-127">Schema Name</span></span>  <br/> |<span data-ttu-id="eb415-128">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="eb415-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="eb415-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="eb415-129">Validation File</span></span>  <br/> |<span data-ttu-id="eb415-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="eb415-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="eb415-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="eb415-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="eb415-132">False</span><span class="sxs-lookup"><span data-stu-id="eb415-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eb415-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="eb415-133">See also</span></span>



- [<span data-ttu-id="eb415-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="eb415-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

