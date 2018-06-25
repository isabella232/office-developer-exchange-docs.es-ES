---
title: Leído
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Read
api_type:
- schema
ms.assetid: b14637e9-1695-4b7e-b078-ae527c2e4303
description: El elemento de lectura indica si un cliente puede leer una carpeta o un elemento. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: cd9c2c9802c78b202418e3947f5b5718b0f676cc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836948"
---
# <a name="read"></a><span data-ttu-id="ced4c-104">Leído</span><span class="sxs-lookup"><span data-stu-id="ced4c-104">Read</span></span>

<span data-ttu-id="ced4c-105">El elemento de **lectura** indica si un cliente puede leer una carpeta o un elemento.</span><span class="sxs-lookup"><span data-stu-id="ced4c-105">The **Read** element indicates whether a client can read a folder or item.</span></span> <span data-ttu-id="ced4c-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ced4c-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<Read>true or false</Read>
```

 <span data-ttu-id="ced4c-107">**boolean**</span><span class="sxs-lookup"><span data-stu-id="ced4c-107">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ced4c-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ced4c-108">Attributes and elements</span></span>

<span data-ttu-id="ced4c-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ced4c-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ced4c-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="ced4c-110">Attributes</span></span>

<span data-ttu-id="ced4c-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ced4c-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ced4c-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ced4c-112">Child elements</span></span>

<span data-ttu-id="ced4c-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ced4c-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ced4c-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ced4c-114">Parent elements</span></span>

|<span data-ttu-id="ced4c-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="ced4c-115">**Element**</span></span>|<span data-ttu-id="ced4c-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ced4c-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ced4c-117">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="ced4c-117">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="ced4c-118">Contiene los derechos del cliente en función de la configuración de permisos para el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="ced4c-118">Contains the rights of the client based on the permission settings for the item or folder.</span></span> <span data-ttu-id="ced4c-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="ced4c-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ced4c-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ced4c-120">Text value</span></span>

<span data-ttu-id="ced4c-121">Un valor de texto de **true** indica que un cliente puede leer un elemento de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="ced4c-121">A text value of **true** indicates that a client can read an item of folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ced4c-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ced4c-122">Remarks</span></span>

<span data-ttu-id="ced4c-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="ced4c-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ced4c-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ced4c-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ced4c-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ced4c-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ced4c-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ced4c-126">Schema Name</span></span>  <br/> |<span data-ttu-id="ced4c-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ced4c-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="ced4c-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ced4c-128">Validation File</span></span>  <br/> |<span data-ttu-id="ced4c-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ced4c-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ced4c-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ced4c-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="ced4c-131">False</span><span class="sxs-lookup"><span data-stu-id="ced4c-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ced4c-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="ced4c-132">See also</span></span>



- [<span data-ttu-id="ced4c-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="ced4c-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="ced4c-134">Establecimiento de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="ced4c-134">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

