---
title: CreateHierarchy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateHierarchy
api_type:
- schema
ms.assetid: 630b5610-1c19-4d4a-a5df-8cebb9afd2f4
description: El elemento CreateHierarchy indica si un cliente puede crear una tabla de jerarquía. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: a5b428fe453dbc31761309b017367a7d25a01b76
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763939"
---
# <a name="createhierarchy"></a><span data-ttu-id="4846d-104">CreateHierarchy</span><span class="sxs-lookup"><span data-stu-id="4846d-104">CreateHierarchy</span></span>

<span data-ttu-id="4846d-105">El elemento **CreateHierarchy** indica si un cliente puede crear una tabla de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="4846d-105">The **CreateHierarchy** element indicates whether a client can create a hierarchy table.</span></span> <span data-ttu-id="4846d-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="4846d-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<CreateHierarchy>true or false</CreateHierarchy>
```

 <span data-ttu-id="4846d-107">**boolean**</span><span class="sxs-lookup"><span data-stu-id="4846d-107">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4846d-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4846d-108">Attributes and elements</span></span>

<span data-ttu-id="4846d-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4846d-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4846d-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="4846d-110">Attributes</span></span>

<span data-ttu-id="4846d-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4846d-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4846d-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4846d-112">Child elements</span></span>

<span data-ttu-id="4846d-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4846d-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4846d-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4846d-114">Parent elements</span></span>

|<span data-ttu-id="4846d-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="4846d-115">**Element**</span></span>|<span data-ttu-id="4846d-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4846d-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4846d-117">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="4846d-117">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="4846d-118">Contiene los derechos del cliente en función de la configuración de permisos para el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="4846d-118">Contains the rights of the client based on the permission settings for the item or folder.</span></span> <span data-ttu-id="4846d-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="4846d-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4846d-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="4846d-120">Text value</span></span>

<span data-ttu-id="4846d-121">Un valor de texto de **true** indica que un cliente puede crear una tabla de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="4846d-121">A text value of **true** indicates that a client can create a hierarchy table.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4846d-122">Notas</span><span class="sxs-lookup"><span data-stu-id="4846d-122">Remarks</span></span>

<span data-ttu-id="4846d-123">Esta propiedad sólo se utiliza en objetos folder.</span><span class="sxs-lookup"><span data-stu-id="4846d-123">This property is only used on folder objects.</span></span>
  
<span data-ttu-id="4846d-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="4846d-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4846d-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4846d-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4846d-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4846d-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4846d-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4846d-127">Schema Name</span></span>  <br/> |<span data-ttu-id="4846d-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4846d-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="4846d-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4846d-129">Validation File</span></span>  <br/> |<span data-ttu-id="4846d-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4846d-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4846d-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4846d-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="4846d-132">False</span><span class="sxs-lookup"><span data-stu-id="4846d-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4846d-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="4846d-133">See also</span></span>



- [<span data-ttu-id="4846d-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="4846d-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="4846d-135">Establecimiento de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="4846d-135">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

