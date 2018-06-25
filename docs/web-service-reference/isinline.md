---
title: IsInline
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsInline
api_type:
- schema
ms.assetid: 5e7712c8-372a-4a16-be64-360c5ff3961a
description: El elemento IsInline indica si los datos adjuntos aparecen en línea dentro de un elemento.
ms.openlocfilehash: f2f9093777a3914de067ef63827de6cf354fc12d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836042"
---
# <a name="isinline"></a><span data-ttu-id="41398-103">IsInline</span><span class="sxs-lookup"><span data-stu-id="41398-103">IsInline</span></span>

<span data-ttu-id="41398-104">El elemento **IsInline** indica si los datos adjuntos aparecen en línea dentro de un elemento.</span><span class="sxs-lookup"><span data-stu-id="41398-104">The **IsInline** element represents whether the attachment appears inline within an item.</span></span> 
  
```xml
<IsInline>true or false</IsInline>
```

 <span data-ttu-id="41398-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="41398-105">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="41398-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="41398-106">Attributes and elements</span></span>

<span data-ttu-id="41398-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="41398-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="41398-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="41398-108">Attributes</span></span>

<span data-ttu-id="41398-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="41398-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="41398-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="41398-110">Child elements</span></span>

<span data-ttu-id="41398-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="41398-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="41398-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="41398-112">Parent elements</span></span>

|<span data-ttu-id="41398-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="41398-113">**Element**</span></span>|<span data-ttu-id="41398-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="41398-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="41398-115">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="41398-115">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="41398-116">Representa un archivo que se adjunta a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="41398-116">Represents a file that is attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="41398-117">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="41398-117">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="41398-118">Representa un elemento de Exchange que está vinculado a otro elemento de Exchange.</span><span class="sxs-lookup"><span data-stu-id="41398-118">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="41398-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="41398-119">Text value</span></span>

<span data-ttu-id="41398-120">Este elemento puede ser **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="41398-120">This element can be either **true** or **false**.</span></span> <span data-ttu-id="41398-121">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="41398-121">The default value is **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="41398-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="41398-122">Remarks</span></span>

<span data-ttu-id="41398-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="41398-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="41398-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="41398-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="41398-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="41398-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="41398-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="41398-126">Schema Name</span></span>  <br/> |<span data-ttu-id="41398-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="41398-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="41398-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="41398-128">Validation File</span></span>  <br/> |<span data-ttu-id="41398-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="41398-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="41398-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="41398-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="41398-131">False</span><span class="sxs-lookup"><span data-stu-id="41398-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="41398-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="41398-132">See also</span></span>



- [<span data-ttu-id="41398-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="41398-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

