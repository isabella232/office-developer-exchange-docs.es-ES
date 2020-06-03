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
description: El elemento CreateHierarchy indica si un cliente puede crear una tabla de jerarquías. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 3fb0c34a8a148cc8336c70d643a21ecb6fef30b5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457525"
---
# <a name="createhierarchy"></a><span data-ttu-id="006be-104">CreateHierarchy</span><span class="sxs-lookup"><span data-stu-id="006be-104">CreateHierarchy</span></span>

<span data-ttu-id="006be-105">El elemento **CreateHierarchy** indica si un cliente puede crear una tabla de jerarquías.</span><span class="sxs-lookup"><span data-stu-id="006be-105">The **CreateHierarchy** element indicates whether a client can create a hierarchy table.</span></span> <span data-ttu-id="006be-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="006be-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<CreateHierarchy>true or false</CreateHierarchy>
```

 <span data-ttu-id="006be-107">**boolean**</span><span class="sxs-lookup"><span data-stu-id="006be-107">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="006be-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="006be-108">Attributes and elements</span></span>

<span data-ttu-id="006be-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="006be-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="006be-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="006be-110">Attributes</span></span>

<span data-ttu-id="006be-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="006be-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="006be-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="006be-112">Child elements</span></span>

<span data-ttu-id="006be-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="006be-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="006be-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="006be-114">Parent elements</span></span>

|<span data-ttu-id="006be-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="006be-115">**Element**</span></span>|<span data-ttu-id="006be-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="006be-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="006be-117">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="006be-117">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="006be-118">Contiene los derechos del cliente en función de la configuración de los permisos del elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="006be-118">Contains the rights of the client based on the permission settings for the item or folder.</span></span> <span data-ttu-id="006be-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="006be-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="006be-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="006be-120">Text value</span></span>

<span data-ttu-id="006be-121">Un valor de texto de **true** indica que un cliente puede crear una tabla de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="006be-121">A text value of **true** indicates that a client can create a hierarchy table.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="006be-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="006be-122">Remarks</span></span>

<span data-ttu-id="006be-123">Esta propiedad solo se usa en objetos Folder.</span><span class="sxs-lookup"><span data-stu-id="006be-123">This property is only used on folder objects.</span></span>
  
<span data-ttu-id="006be-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="006be-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="006be-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="006be-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="006be-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="006be-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="006be-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="006be-127">Schema Name</span></span>  <br/> |<span data-ttu-id="006be-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="006be-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="006be-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="006be-129">Validation File</span></span>  <br/> |<span data-ttu-id="006be-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="006be-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="006be-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="006be-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="006be-132">Falso</span><span class="sxs-lookup"><span data-stu-id="006be-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="006be-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="006be-133">See also</span></span>



- [<span data-ttu-id="006be-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="006be-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="006be-135">Configuración de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="006be-135">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

