---
title: Children
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Children
api_type:
- schema
ms.assetid: ceaffddd-f9bc-43ea-b348-a20fdade738f
description: El elemento de elementos secundarios contiene los nombres de los elementos secundarios de un contacto.
ms.openlocfilehash: 9b1e06529fcf74850755daefc299242cfbf81f1e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763736"
---
# <a name="children"></a><span data-ttu-id="aef1f-103">Children</span><span class="sxs-lookup"><span data-stu-id="aef1f-103">Children</span></span>

<span data-ttu-id="aef1f-104">El elemento de **elementos secundarios** contiene los nombres de los elementos secundarios de un contacto.</span><span class="sxs-lookup"><span data-stu-id="aef1f-104">The **Children** element contains the names of a contact's children.</span></span> 
  
```xml
<Children>
   <String/>
</Children>
```

 <span data-ttu-id="aef1f-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="aef1f-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aef1f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="aef1f-106">Attributes and elements</span></span>

<span data-ttu-id="aef1f-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="aef1f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aef1f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="aef1f-108">Attributes</span></span>

<span data-ttu-id="aef1f-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="aef1f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aef1f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="aef1f-110">Child elements</span></span>

|<span data-ttu-id="aef1f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="aef1f-111">**Element**</span></span>|<span data-ttu-id="aef1f-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aef1f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aef1f-113">String</span><span class="sxs-lookup"><span data-stu-id="aef1f-113">String</span></span>](string.md) <br/> |<span data-ttu-id="aef1f-114">Contiene el nombre del elemento secundario de un contacto.</span><span class="sxs-lookup"><span data-stu-id="aef1f-114">Contains the name of a contact's child.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="aef1f-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="aef1f-115">Parent elements</span></span>

|<span data-ttu-id="aef1f-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="aef1f-116">**Element**</span></span>|<span data-ttu-id="aef1f-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aef1f-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aef1f-118">Contact</span><span class="sxs-lookup"><span data-stu-id="aef1f-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="aef1f-119">Representa un contacto en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="aef1f-119">Represents a contact in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aef1f-120">Notas</span><span class="sxs-lookup"><span data-stu-id="aef1f-120">Remarks</span></span>

<span data-ttu-id="aef1f-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="aef1f-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aef1f-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="aef1f-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aef1f-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="aef1f-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="aef1f-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="aef1f-124">Schema name</span></span>  <br/> |<span data-ttu-id="aef1f-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="aef1f-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="aef1f-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="aef1f-126">Validation file</span></span>  <br/> |<span data-ttu-id="aef1f-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="aef1f-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="aef1f-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="aef1f-128">Can be empty</span></span>  <br/> |<span data-ttu-id="aef1f-129">False</span><span class="sxs-lookup"><span data-stu-id="aef1f-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aef1f-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="aef1f-130">See also</span></span>



- [<span data-ttu-id="aef1f-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="aef1f-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

