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
description: El elemento UnknownEntry representa una sola entrada de permiso desconocida que no se puede resolver contra el servicio de directorio de Active Directory. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 452857690f719ba3ee9dffa29e576ca4f3b2b945
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459401"
---
# <a name="unknownentry"></a><span data-ttu-id="f695c-104">UnknownEntry</span><span class="sxs-lookup"><span data-stu-id="f695c-104">UnknownEntry</span></span>

<span data-ttu-id="f695c-105">El elemento **UnknownEntry** representa una sola entrada de permiso desconocida que no se puede resolver contra el servicio de directorio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f695c-105">The **UnknownEntry** element represents a single unknown permission entry that cannot be resolved against the Active Directory directory service.</span></span> <span data-ttu-id="f695c-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f695c-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<UnknownEntry/>
```

 <span data-ttu-id="f695c-107">**string**</span><span class="sxs-lookup"><span data-stu-id="f695c-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f695c-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f695c-108">Attributes and elements</span></span>

<span data-ttu-id="f695c-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f695c-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f695c-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="f695c-110">Attributes</span></span>

<span data-ttu-id="f695c-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f695c-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f695c-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f695c-112">Child elements</span></span>

<span data-ttu-id="f695c-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f695c-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f695c-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f695c-114">Parent elements</span></span>

|<span data-ttu-id="f695c-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f695c-115">**Element**</span></span>|<span data-ttu-id="f695c-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f695c-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f695c-117">UnknownEntries</span><span class="sxs-lookup"><span data-stu-id="f695c-117">UnknownEntries</span></span>](unknownentries.md) <br/> |<span data-ttu-id="f695c-118">Contiene una matriz de entradas de permisos desconocidos que no se pueden resolver en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f695c-118">Contains an array of unknown permission entries that cannot be resolved against Active Directory.</span></span> <span data-ttu-id="f695c-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="f695c-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f695c-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f695c-120">Text value</span></span>

<span data-ttu-id="f695c-121">El valor de texto representa una entrada de permiso que no se puede resolver en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f695c-121">The text value represents a permission entry that cannot be resolved against Active Directory.</span></span> <span data-ttu-id="f695c-122">El valor de texto representa un identificador de seguridad (SID).</span><span class="sxs-lookup"><span data-stu-id="f695c-122">The text value represents a security identifier (SID).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f695c-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f695c-123">Remarks</span></span>

<span data-ttu-id="f695c-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="f695c-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f695c-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f695c-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f695c-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="f695c-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f695c-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f695c-127">Schema Name</span></span>  <br/> |<span data-ttu-id="f695c-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f695c-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="f695c-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f695c-129">Validation File</span></span>  <br/> |<span data-ttu-id="f695c-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="f695c-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f695c-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f695c-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="f695c-132">Falso</span><span class="sxs-lookup"><span data-stu-id="f695c-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f695c-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="f695c-133">See also</span></span>



- [<span data-ttu-id="f695c-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f695c-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="f695c-135">Configuración de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="f695c-135">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

