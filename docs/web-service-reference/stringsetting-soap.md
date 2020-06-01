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
description: El elemento StringSetting representa una configuración de usuario cuyo valor es de tipo String.
ms.openlocfilehash: 215d1187c0968577e894c9f9cddea050789697b9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463079"
---
# <a name="stringsetting-soap"></a><span data-ttu-id="b39ba-103">StringSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b39ba-103">StringSetting (SOAP)</span></span>

<span data-ttu-id="b39ba-104">El elemento **StringSetting** representa una configuración de usuario cuyo valor es de tipo String.</span><span class="sxs-lookup"><span data-stu-id="b39ba-104">The **StringSetting** element represents a user setting the value of which is of type string.</span></span> 
  
```XML
<StringSetting>
   <Name/>
   <Value/>
</StringSetting>
```

 <span data-ttu-id="b39ba-105">**StringSetting**</span><span class="sxs-lookup"><span data-stu-id="b39ba-105">**StringSetting**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b39ba-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b39ba-106">Attributes and elements</span></span>

<span data-ttu-id="b39ba-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b39ba-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b39ba-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b39ba-108">Attributes</span></span>

<span data-ttu-id="b39ba-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b39ba-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b39ba-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b39ba-110">Child elements</span></span>

|<span data-ttu-id="b39ba-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b39ba-111">**Element**</span></span>|<span data-ttu-id="b39ba-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b39ba-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b39ba-113">Name (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b39ba-113">Name (SOAP)</span></span>](name-soap.md) <br/> |<span data-ttu-id="b39ba-114">Representa un nombre de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="b39ba-114">Represents a user setting name.</span></span>  <br/> |
|[<span data-ttu-id="b39ba-115">Valor (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b39ba-115">Value (SOAP)</span></span>](value-soap.md) <br/> |<span data-ttu-id="b39ba-116">Representa un valor de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="b39ba-116">Represents a user setting value.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b39ba-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b39ba-117">Parent elements</span></span>

<span data-ttu-id="b39ba-118">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b39ba-118">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="b39ba-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b39ba-119">Text value</span></span>

<span data-ttu-id="b39ba-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b39ba-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b39ba-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b39ba-121">Remarks</span></span>

<span data-ttu-id="b39ba-122">El tipo **StringSetting** amplía el tipo **UserSetting** .</span><span class="sxs-lookup"><span data-stu-id="b39ba-122">The **StringSetting** type extends the **UserSetting** type.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="b39ba-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b39ba-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b39ba-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="b39ba-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="b39ba-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b39ba-125">Schema Name</span></span>  <br/> |<span data-ttu-id="b39ba-126">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="b39ba-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="b39ba-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b39ba-127">Validation File</span></span>  <br/> |<span data-ttu-id="b39ba-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="b39ba-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b39ba-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b39ba-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="b39ba-130">Verdadero</span><span class="sxs-lookup"><span data-stu-id="b39ba-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b39ba-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="b39ba-131">See also</span></span>



[<span data-ttu-id="b39ba-132">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b39ba-132">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="b39ba-133">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b39ba-133">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
  
[<span data-ttu-id="b39ba-134">Operación GetFederationInformation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b39ba-134">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

