---
title: CreateContents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateContents
api_type:
- schema
ms.assetid: 8a9cd241-0d73-4be8-a563-a945898d1a0e
description: El elemento CreateContents indica si un cliente puede crear una tabla de contenido. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: f84ffdd2e6b485436d9e4ccd5f03a6e2c57fcfd1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763921"
---
# <a name="createcontents"></a><span data-ttu-id="82112-104">CreateContents</span><span class="sxs-lookup"><span data-stu-id="82112-104">CreateContents</span></span>

<span data-ttu-id="82112-105">El elemento **CreateContents** indica si un cliente puede crear una tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="82112-105">The **CreateContents** element indicates whether a client can create a contents table.</span></span> <span data-ttu-id="82112-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="82112-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<CreateContents>true or false</CreateContents>
```

 <span data-ttu-id="82112-107">**boolean**</span><span class="sxs-lookup"><span data-stu-id="82112-107">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="82112-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="82112-108">Attributes and elements</span></span>

<span data-ttu-id="82112-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="82112-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="82112-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="82112-110">Attributes</span></span>

<span data-ttu-id="82112-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="82112-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="82112-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="82112-112">Child elements</span></span>

<span data-ttu-id="82112-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="82112-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="82112-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="82112-114">Parent elements</span></span>

|<span data-ttu-id="82112-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="82112-115">**Element**</span></span>|<span data-ttu-id="82112-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="82112-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="82112-117">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="82112-117">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="82112-118">Contiene los derechos del cliente en función de la configuración de permisos para el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="82112-118">Contains the rights of the client based on the permission settings for the item or folder.</span></span> <span data-ttu-id="82112-119">Este elemento fue introducido inExchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="82112-119">This element was introduced inExchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="82112-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="82112-120">Text value</span></span>

<span data-ttu-id="82112-121">Un valor de texto de **true** indica que un cliente puede crear una tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="82112-121">A text value of **true** indicates that a client can create a contents table.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="82112-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="82112-122">Remarks</span></span>

<span data-ttu-id="82112-123">Esta propiedad sólo se utiliza en objetos folder.</span><span class="sxs-lookup"><span data-stu-id="82112-123">This property is only used on folder objects.</span></span>
  
<span data-ttu-id="82112-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="82112-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="82112-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="82112-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="82112-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="82112-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="82112-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="82112-127">Schema Name</span></span>  <br/> |<span data-ttu-id="82112-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="82112-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="82112-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="82112-129">Validation File</span></span>  <br/> |<span data-ttu-id="82112-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="82112-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="82112-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="82112-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="82112-132">False</span><span class="sxs-lookup"><span data-stu-id="82112-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="82112-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="82112-133">See also</span></span>



- [<span data-ttu-id="82112-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="82112-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="82112-135">Establecimiento de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="82112-135">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

