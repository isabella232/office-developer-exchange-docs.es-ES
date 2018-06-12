---
title: HasPicture
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HasPicture
api_type:
- schema
ms.assetid: 922a43fe-01bd-49f2-9261-e00e4699b8da
description: El elemento HasPicture indica si el elemento de contacto tiene un archivo adjunto que representa la imagen del contacto.
ms.openlocfilehash: 8f6890ec2bcc9a961f69331fb20f5cad8a59bf38
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835806"
---
# <a name="haspicture"></a><span data-ttu-id="840a5-103">HasPicture</span><span class="sxs-lookup"><span data-stu-id="840a5-103">HasPicture</span></span>

<span data-ttu-id="840a5-104">El elemento **HasPicture** indica si el elemento de contacto tiene un archivo adjunto que representa la imagen del contacto.</span><span class="sxs-lookup"><span data-stu-id="840a5-104">The **HasPicture** element indicates whether the contact item has a file attachment that represents the contact's picture.</span></span> 
  
[<span data-ttu-id="840a5-105">Contact</span><span class="sxs-lookup"><span data-stu-id="840a5-105">Contact</span></span>](contact.md)
  
[<span data-ttu-id="840a5-106">HasPicture</span><span class="sxs-lookup"><span data-stu-id="840a5-106">HasPicture</span></span>](haspicture.md)
  
```xml
<HasPicture>true or false</HasPicture>
```

 <span data-ttu-id="840a5-107">**boolean**</span><span class="sxs-lookup"><span data-stu-id="840a5-107">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="840a5-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="840a5-108">Attributes and elements</span></span>

<span data-ttu-id="840a5-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="840a5-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="840a5-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="840a5-110">Attributes</span></span>

<span data-ttu-id="840a5-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="840a5-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="840a5-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="840a5-112">Child elements</span></span>

<span data-ttu-id="840a5-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="840a5-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="840a5-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="840a5-114">Parent elements</span></span>

|<span data-ttu-id="840a5-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="840a5-115">**Element**</span></span>|<span data-ttu-id="840a5-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="840a5-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="840a5-117">Contact</span><span class="sxs-lookup"><span data-stu-id="840a5-117">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="840a5-118">Representa un elemento de contacto en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="840a5-118">Represents a contact item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="840a5-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="840a5-119">Text value</span></span>

<span data-ttu-id="840a5-120">El valor de texto del elemento **HasPicture** puede ser **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="840a5-120">The text value of the **HasPicture** element can be either **true** or **false**.</span></span> <span data-ttu-id="840a5-121">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="840a5-121">The default value is **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="840a5-122">Notas</span><span class="sxs-lookup"><span data-stu-id="840a5-122">Remarks</span></span>

<span data-ttu-id="840a5-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="840a5-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="840a5-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="840a5-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="840a5-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="840a5-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="840a5-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="840a5-126">Schema Name</span></span>  <br/> |<span data-ttu-id="840a5-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="840a5-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="840a5-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="840a5-128">Validation File</span></span>  <br/> |<span data-ttu-id="840a5-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="840a5-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="840a5-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="840a5-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="840a5-131">False</span><span class="sxs-lookup"><span data-stu-id="840a5-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="840a5-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="840a5-132">See also</span></span>



- [<span data-ttu-id="840a5-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="840a5-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

