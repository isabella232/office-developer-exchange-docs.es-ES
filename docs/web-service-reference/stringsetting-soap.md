---
title: StringSetting (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: bf7096d8-42d4-4bf5-bbdd-851af2754000
description: El elemento StringSetting representa una configuración de usuario, el valor de los cuales es de tipo string.
ms.openlocfilehash: af2c8ed243182e3491723be172ae162554250951
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837606"
---
# <a name="stringsetting-soap"></a><span data-ttu-id="9b638-103">StringSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9b638-103">StringSetting (SOAP)</span></span>

<span data-ttu-id="9b638-104">El elemento **StringSetting** representa una configuración de usuario, el valor de los cuales es de tipo string.</span><span class="sxs-lookup"><span data-stu-id="9b638-104">The **StringSetting** element represents a user setting the value of which is of type string.</span></span> 
  
```XML
<StringSetting>
   <Name/>
   <Value/>
</StringSetting>
```

 <span data-ttu-id="9b638-105">**StringSetting**</span><span class="sxs-lookup"><span data-stu-id="9b638-105">**StringSetting**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9b638-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9b638-106">Attributes and elements</span></span>

<span data-ttu-id="9b638-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9b638-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9b638-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="9b638-108">Attributes</span></span>

<span data-ttu-id="9b638-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9b638-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9b638-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9b638-110">Child elements</span></span>

|<span data-ttu-id="9b638-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="9b638-111">**Element**</span></span>|<span data-ttu-id="9b638-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9b638-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9b638-113">Nombre (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9b638-113">Name (SOAP)</span></span>](name-soap.md) <br/> |<span data-ttu-id="9b638-114">Representa un nombre de la configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="9b638-114">Represents a user setting name.</span></span>  <br/> |
|[<span data-ttu-id="9b638-115">Valor (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9b638-115">Value (SOAP)</span></span>](value-soap.md) <br/> |<span data-ttu-id="9b638-116">Representa un valor de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="9b638-116">Represents a user setting value.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9b638-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9b638-117">Parent elements</span></span>

<span data-ttu-id="9b638-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9b638-118">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="9b638-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="9b638-119">Text value</span></span>

<span data-ttu-id="9b638-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9b638-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9b638-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9b638-121">Remarks</span></span>

<span data-ttu-id="9b638-122">El tipo de **StringSetting** extiende el tipo de **UserSetting** .</span><span class="sxs-lookup"><span data-stu-id="9b638-122">The **StringSetting** type extends the **UserSetting** type.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="9b638-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9b638-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9b638-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9b638-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="9b638-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9b638-125">Schema Name</span></span>  <br/> |<span data-ttu-id="9b638-126">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="9b638-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="9b638-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9b638-127">Validation File</span></span>  <br/> |<span data-ttu-id="9b638-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9b638-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9b638-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9b638-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="9b638-130">Verdadero</span><span class="sxs-lookup"><span data-stu-id="9b638-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9b638-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b638-131">See also</span></span>



[<span data-ttu-id="9b638-132">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9b638-132">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="9b638-133">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9b638-133">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
  
[<span data-ttu-id="9b638-134">Operación GetFederationInformation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9b638-134">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

