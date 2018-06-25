---
title: Companies
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Companies
api_type:
- schema
ms.assetid: 5d9ea76f-e14d-4424-8842-0c3cc3305119
description: El elemento de compañías representa la colección de las empresas que están asociados con un contacto o una tarea.
ms.openlocfilehash: 5b8ac20d4a02017881f941d12380fe29078f51cc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763748"
---
# <a name="companies"></a><span data-ttu-id="3a1d5-103">Companies</span><span class="sxs-lookup"><span data-stu-id="3a1d5-103">Companies</span></span>

<span data-ttu-id="3a1d5-104">El elemento de **compañías** representa la colección de las empresas que están asociados con un contacto o una tarea.</span><span class="sxs-lookup"><span data-stu-id="3a1d5-104">The **Companies** element represents the collection of companies that are associated with a contact or task.</span></span> 
  
```xml
<Companies>
   <String/>
</Companies>
```

 <span data-ttu-id="3a1d5-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="3a1d5-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3a1d5-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3a1d5-106">Attributes and elements</span></span>

<span data-ttu-id="3a1d5-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3a1d5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3a1d5-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3a1d5-108">Attributes</span></span>

<span data-ttu-id="3a1d5-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3a1d5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3a1d5-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3a1d5-110">Child elements</span></span>

|<span data-ttu-id="3a1d5-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3a1d5-111">**Element**</span></span>|<span data-ttu-id="3a1d5-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3a1d5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a1d5-113">String</span><span class="sxs-lookup"><span data-stu-id="3a1d5-113">String</span></span>](string.md) <br/> |<span data-ttu-id="3a1d5-114">Representa el nombre de una compañía.</span><span class="sxs-lookup"><span data-stu-id="3a1d5-114">Represents the name of a company.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3a1d5-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3a1d5-115">Parent elements</span></span>

|<span data-ttu-id="3a1d5-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="3a1d5-116">**Element**</span></span>|<span data-ttu-id="3a1d5-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3a1d5-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a1d5-118">Contact</span><span class="sxs-lookup"><span data-stu-id="3a1d5-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="3a1d5-119">Representa un contacto en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3a1d5-119">Represents a contact in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3a1d5-120">Tarea</span><span class="sxs-lookup"><span data-stu-id="3a1d5-120">Task</span></span>](task.md) <br/> |<span data-ttu-id="3a1d5-121">Representa una tarea en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3a1d5-121">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a1d5-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3a1d5-122">Remarks</span></span>

<span data-ttu-id="3a1d5-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="3a1d5-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3a1d5-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3a1d5-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3a1d5-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3a1d5-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3a1d5-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3a1d5-126">Schema name</span></span>  <br/> |<span data-ttu-id="3a1d5-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="3a1d5-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="3a1d5-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3a1d5-128">Validation file</span></span>  <br/> |<span data-ttu-id="3a1d5-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3a1d5-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3a1d5-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3a1d5-130">Can be empty</span></span>  <br/> |<span data-ttu-id="3a1d5-131">False</span><span class="sxs-lookup"><span data-stu-id="3a1d5-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3a1d5-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a1d5-132">See also</span></span>



- [<span data-ttu-id="3a1d5-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3a1d5-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

