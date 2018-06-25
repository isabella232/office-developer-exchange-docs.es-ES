---
title: FileAsMapping
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FileAsMapping
api_type:
- schema
ms.assetid: 2c98e7c6-09b0-47b3-bbf7-8c4ef9510280
description: El elemento FileAsMapping define cómo construir lo que se muestra para un contacto.
ms.openlocfilehash: 1ba0ae0daa56a72c29d8c0ccad64e3edae5f0b84
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764602"
---
# <a name="fileasmapping"></a><span data-ttu-id="762a1-103">FileAsMapping</span><span class="sxs-lookup"><span data-stu-id="762a1-103">FileAsMapping</span></span>

<span data-ttu-id="762a1-104">El elemento **FileAsMapping** define cómo construir lo que se muestra para un contacto.</span><span class="sxs-lookup"><span data-stu-id="762a1-104">The **FileAsMapping** element defines how to construct what is displayed for a contact.</span></span> 
  
```xml
<FileAsMapping/>
```

 <span data-ttu-id="762a1-105">**FileAsMappingType**</span><span class="sxs-lookup"><span data-stu-id="762a1-105">**FileAsMappingType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="762a1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="762a1-106">Attributes and elements</span></span>

<span data-ttu-id="762a1-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="762a1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="762a1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="762a1-108">Attributes</span></span>

<span data-ttu-id="762a1-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="762a1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="762a1-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="762a1-110">Child elements</span></span>

<span data-ttu-id="762a1-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="762a1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="762a1-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="762a1-112">Parent elements</span></span>

|<span data-ttu-id="762a1-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="762a1-113">**Element**</span></span>|<span data-ttu-id="762a1-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="762a1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="762a1-115">Contact</span><span class="sxs-lookup"><span data-stu-id="762a1-115">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="762a1-116">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="762a1-116">Represents an Exchange contact item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="762a1-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="762a1-117">Text value</span></span>

<span data-ttu-id="762a1-118">El valor de texto para este elemento está restringido a uno de los siguientes valores de cadena:</span><span class="sxs-lookup"><span data-stu-id="762a1-118">The text value for this element is restricted to one of the following string values:</span></span>
  
- <span data-ttu-id="762a1-119">None</span><span class="sxs-lookup"><span data-stu-id="762a1-119">None</span></span>
    
- <span data-ttu-id="762a1-120">LastCommaFirst</span><span class="sxs-lookup"><span data-stu-id="762a1-120">LastCommaFirst</span></span>
    
- <span data-ttu-id="762a1-121">FirstSpaceLast</span><span class="sxs-lookup"><span data-stu-id="762a1-121">FirstSpaceLast</span></span>
    
- <span data-ttu-id="762a1-122">Compañía</span><span class="sxs-lookup"><span data-stu-id="762a1-122">Company</span></span>
    
- <span data-ttu-id="762a1-123">LastCommaFirstCompany</span><span class="sxs-lookup"><span data-stu-id="762a1-123">LastCommaFirstCompany</span></span>
    
- <span data-ttu-id="762a1-124">CompanyLastFirst</span><span class="sxs-lookup"><span data-stu-id="762a1-124">CompanyLastFirst</span></span>
    
- <span data-ttu-id="762a1-125">ApellidosNombre</span><span class="sxs-lookup"><span data-stu-id="762a1-125">LastFirst</span></span>
    
- <span data-ttu-id="762a1-126">LastFirstCompany</span><span class="sxs-lookup"><span data-stu-id="762a1-126">LastFirstCompany</span></span>
    
- <span data-ttu-id="762a1-127">CompanyLastCommaFirst</span><span class="sxs-lookup"><span data-stu-id="762a1-127">CompanyLastCommaFirst</span></span>
    
- <span data-ttu-id="762a1-128">LastFirstSuffix</span><span class="sxs-lookup"><span data-stu-id="762a1-128">LastFirstSuffix</span></span>
    
- <span data-ttu-id="762a1-129">LastSpaceFirstCompany</span><span class="sxs-lookup"><span data-stu-id="762a1-129">LastSpaceFirstCompany</span></span>
    
- <span data-ttu-id="762a1-130">CompanyLastSpaceFirst</span><span class="sxs-lookup"><span data-stu-id="762a1-130">CompanyLastSpaceFirst</span></span>
    
- <span data-ttu-id="762a1-131">LastSpaceFirst</span><span class="sxs-lookup"><span data-stu-id="762a1-131">LastSpaceFirst</span></span>
    
- <span data-ttu-id="762a1-132">DisplayName</span><span class="sxs-lookup"><span data-stu-id="762a1-132">DisplayName</span></span>
    
- <span data-ttu-id="762a1-133">FirstName</span><span class="sxs-lookup"><span data-stu-id="762a1-133">FirstName</span></span>
    
- <span data-ttu-id="762a1-134">LastFirstMiddleSuffix</span><span class="sxs-lookup"><span data-stu-id="762a1-134">LastFirstMiddleSuffix</span></span>
    
- <span data-ttu-id="762a1-135">LastName</span><span class="sxs-lookup"><span data-stu-id="762a1-135">LastName</span></span>
    
- <span data-ttu-id="762a1-136">Empty</span><span class="sxs-lookup"><span data-stu-id="762a1-136">Empty</span></span>
    
## <a name="remarks"></a><span data-ttu-id="762a1-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="762a1-137">Remarks</span></span>

<span data-ttu-id="762a1-138">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="762a1-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="762a1-139">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="762a1-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="762a1-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="762a1-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="762a1-141">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="762a1-141">Schema name</span></span>  <br/> |<span data-ttu-id="762a1-142">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="762a1-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="762a1-143">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="762a1-143">Validation file</span></span>  <br/> |<span data-ttu-id="762a1-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="762a1-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="762a1-145">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="762a1-145">Can be empty</span></span>  <br/> |<span data-ttu-id="762a1-146">False</span><span class="sxs-lookup"><span data-stu-id="762a1-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="762a1-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="762a1-147">See also</span></span>



- [<span data-ttu-id="762a1-148">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="762a1-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="762a1-149">Creación de contactos (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="762a1-149">Creating Contacts (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[<span data-ttu-id="762a1-150">Actualizar contactos</span><span class="sxs-lookup"><span data-stu-id="762a1-150">Updating Contacts</span></span>](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[<span data-ttu-id="762a1-151">Eliminación de contactos</span><span class="sxs-lookup"><span data-stu-id="762a1-151">Deleting Contacts</span></span>](http://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

