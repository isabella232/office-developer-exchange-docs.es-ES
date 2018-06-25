---
title: Contactos
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Contacts
api_type:
- schema
ms.assetid: 0cc67cdf-9707-45e7-92c6-fa83a016cdbe
description: El elemento de contactos contiene una lista de contactos que están asociados con una tarea.
ms.openlocfilehash: da7963d30f58f7da52e76e3f7f1d0f7fd68abf74
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763788"
---
# <a name="contacts"></a><span data-ttu-id="4feae-103">Contactos</span><span class="sxs-lookup"><span data-stu-id="4feae-103">Contacts</span></span>

<span data-ttu-id="4feae-104">El elemento de **contactos** contiene una lista de contactos que están asociados con una tarea.</span><span class="sxs-lookup"><span data-stu-id="4feae-104">The **Contacts** element contains a list of contacts that are associated with a task.</span></span> 
  
```xml
<Contacts>
   <String/>
</Contacts>
```

 <span data-ttu-id="4feae-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="4feae-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4feae-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4feae-106">Attributes and elements</span></span>

<span data-ttu-id="4feae-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4feae-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4feae-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4feae-108">Attributes</span></span>

<span data-ttu-id="4feae-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4feae-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4feae-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4feae-110">Child elements</span></span>

|<span data-ttu-id="4feae-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4feae-111">**Element**</span></span>|<span data-ttu-id="4feae-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4feae-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4feae-113">String</span><span class="sxs-lookup"><span data-stu-id="4feae-113">String</span></span>](string.md) <br/> |<span data-ttu-id="4feae-114">Representa una lista separada por comas de nombres de los contactos.</span><span class="sxs-lookup"><span data-stu-id="4feae-114">Represents a comma-separated list of contact names.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4feae-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4feae-115">Parent elements</span></span>

|<span data-ttu-id="4feae-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="4feae-116">**Element**</span></span>|<span data-ttu-id="4feae-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4feae-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4feae-118">Tarea</span><span class="sxs-lookup"><span data-stu-id="4feae-118">Task</span></span>](task.md) <br/> |<span data-ttu-id="4feae-119">Representa una tarea en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4feae-119">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4feae-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4feae-120">Remarks</span></span>

<span data-ttu-id="4feae-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="4feae-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4feae-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4feae-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4feae-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4feae-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4feae-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4feae-124">Schema name</span></span>  <br/> |<span data-ttu-id="4feae-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4feae-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="4feae-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4feae-126">Validation file</span></span>  <br/> |<span data-ttu-id="4feae-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4feae-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4feae-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4feae-128">Can be empty</span></span>  <br/> |<span data-ttu-id="4feae-129">False</span><span class="sxs-lookup"><span data-stu-id="4feae-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4feae-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="4feae-130">See also</span></span>



- [<span data-ttu-id="4feae-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="4feae-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

