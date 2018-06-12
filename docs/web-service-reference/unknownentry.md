---
title: UnknownEntry
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnknownEntry
api_type:
- schema
ms.assetid: 3cb4c62e-052a-4326-8639-8c41dfd047b2
description: El elemento UnknownEntry representa una entrada de permiso desconocido único que no se puede resolver con el servicio de directorio de Active Directory. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 11939ad39c83ac2d15ec7fface6f530d3f60e12a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840786"
---
# <a name="unknownentry"></a><span data-ttu-id="eb889-104">UnknownEntry</span><span class="sxs-lookup"><span data-stu-id="eb889-104">UnknownEntry</span></span>

<span data-ttu-id="eb889-105">El elemento **UnknownEntry** representa una entrada de permiso desconocido único que no se puede resolver con el servicio de directorio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="eb889-105">The **UnknownEntry** element represents a single unknown permission entry that cannot be resolved against the Active Directory directory service.</span></span> <span data-ttu-id="eb889-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="eb889-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<UnknownEntry/>
```

 <span data-ttu-id="eb889-107">**string**</span><span class="sxs-lookup"><span data-stu-id="eb889-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eb889-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="eb889-108">Attributes and elements</span></span>

<span data-ttu-id="eb889-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="eb889-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eb889-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="eb889-110">Attributes</span></span>

<span data-ttu-id="eb889-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="eb889-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eb889-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="eb889-112">Child elements</span></span>

<span data-ttu-id="eb889-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="eb889-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="eb889-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="eb889-114">Parent elements</span></span>

|<span data-ttu-id="eb889-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="eb889-115">**Element**</span></span>|<span data-ttu-id="eb889-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="eb889-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eb889-117">UnknownEntries</span><span class="sxs-lookup"><span data-stu-id="eb889-117">UnknownEntries</span></span>](unknownentries.md) <br/> |<span data-ttu-id="eb889-118">Contiene una matriz de las entradas de permiso desconocido que no se puede resolver en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="eb889-118">Contains an array of unknown permission entries that cannot be resolved against Active Directory.</span></span> <span data-ttu-id="eb889-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="eb889-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="eb889-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="eb889-120">Text value</span></span>

<span data-ttu-id="eb889-121">El valor de texto representa una entrada de permiso que no se puede resolver en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="eb889-121">The text value represents a permission entry that cannot be resolved against Active Directory.</span></span> <span data-ttu-id="eb889-122">El valor de texto representa un identificador de seguridad (SID).</span><span class="sxs-lookup"><span data-stu-id="eb889-122">The text value represents a security identifier (SID).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eb889-123">Notas</span><span class="sxs-lookup"><span data-stu-id="eb889-123">Remarks</span></span>

<span data-ttu-id="eb889-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="eb889-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eb889-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="eb889-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb889-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="eb889-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="eb889-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="eb889-127">Schema Name</span></span>  <br/> |<span data-ttu-id="eb889-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="eb889-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="eb889-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="eb889-129">Validation File</span></span>  <br/> |<span data-ttu-id="eb889-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="eb889-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="eb889-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="eb889-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="eb889-132">False</span><span class="sxs-lookup"><span data-stu-id="eb889-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eb889-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="eb889-133">See also</span></span>



- [<span data-ttu-id="eb889-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="eb889-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="eb889-135">Establecimiento de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="eb889-135">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

