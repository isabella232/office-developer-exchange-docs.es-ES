---
title: PhysicalAddresses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PhysicalAddresses
api_type:
- schema
ms.assetid: 5276c5f2-9e08-43af-a0b2-da4ff1dcae2d
description: El elemento PhysicalAddresses contiene una colección de direcciones físicas que están asociados con un contacto.
ms.openlocfilehash: d4d5232312c735e389e9f5b0dbcb74f8614b6906
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836814"
---
# <a name="physicaladdresses"></a><span data-ttu-id="c4f02-103">PhysicalAddresses</span><span class="sxs-lookup"><span data-stu-id="c4f02-103">PhysicalAddresses</span></span>

<span data-ttu-id="c4f02-104">El elemento **PhysicalAddresses** contiene una colección de direcciones físicas que están asociados con un contacto.</span><span class="sxs-lookup"><span data-stu-id="c4f02-104">The **PhysicalAddresses** element contains a collection of physical addresses that are associated with a contact.</span></span> 
  
```xml
<PhysicalAddresses>
   <Entry/>
</PhysicalAddresses>
```

 <span data-ttu-id="c4f02-105">**PhysicalAddressDictionaryType**</span><span class="sxs-lookup"><span data-stu-id="c4f02-105">**PhysicalAddressDictionaryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c4f02-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c4f02-106">Attributes and elements</span></span>

<span data-ttu-id="c4f02-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c4f02-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c4f02-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c4f02-108">Attributes</span></span>

<span data-ttu-id="c4f02-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c4f02-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c4f02-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c4f02-110">Child elements</span></span>

|<span data-ttu-id="c4f02-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c4f02-111">**Element**</span></span>|<span data-ttu-id="c4f02-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c4f02-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c4f02-113">Entrada (PhysicalAddress)</span><span class="sxs-lookup"><span data-stu-id="c4f02-113">Entry (PhysicalAddress)</span></span>](entry-physicaladdress.md) <br/> |<span data-ttu-id="c4f02-114">Describe una sola dirección física para un elemento de contacto.</span><span class="sxs-lookup"><span data-stu-id="c4f02-114">Describes a single physical address for a contact item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c4f02-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c4f02-115">Parent elements</span></span>

|<span data-ttu-id="c4f02-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="c4f02-116">**Element**</span></span>|<span data-ttu-id="c4f02-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c4f02-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c4f02-118">Contact</span><span class="sxs-lookup"><span data-stu-id="c4f02-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="c4f02-119">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c4f02-119">Represents an Exchange contact item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4f02-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c4f02-120">Remarks</span></span>

<span data-ttu-id="c4f02-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="c4f02-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c4f02-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c4f02-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c4f02-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c4f02-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c4f02-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c4f02-124">Schema name</span></span>  <br/> |<span data-ttu-id="c4f02-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c4f02-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="c4f02-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c4f02-126">Validation file</span></span>  <br/> |<span data-ttu-id="c4f02-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c4f02-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c4f02-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c4f02-128">Can be empty</span></span>  <br/> |<span data-ttu-id="c4f02-129">False</span><span class="sxs-lookup"><span data-stu-id="c4f02-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c4f02-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4f02-130">See also</span></span>



- [<span data-ttu-id="c4f02-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c4f02-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="c4f02-132">Creación de contactos (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="c4f02-132">Creating Contacts (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[<span data-ttu-id="c4f02-133">Actualizar contactos</span><span class="sxs-lookup"><span data-stu-id="c4f02-133">Updating Contacts</span></span>](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[<span data-ttu-id="c4f02-134">Eliminación de contactos</span><span class="sxs-lookup"><span data-stu-id="c4f02-134">Deleting Contacts</span></span>](http://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

