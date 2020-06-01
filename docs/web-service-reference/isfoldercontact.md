---
title: IsFolderContact
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsFolderContact
api_type:
- schema
ms.assetid: 8b456255-f4ae-4ca0-845a-13c195f1c867
description: El elemento IsFolderContact indica si un usuario es un contacto de una carpeta. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: b7830a94237b721d02409e2d93b27c2c5ef015e7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455285"
---
# <a name="isfoldercontact"></a><span data-ttu-id="66837-104">IsFolderContact</span><span class="sxs-lookup"><span data-stu-id="66837-104">IsFolderContact</span></span>

<span data-ttu-id="66837-105">El elemento **IsFolderContact** indica si un usuario es un contacto de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="66837-105">The **IsFolderContact** element indicates whether a user is a contact for a folder.</span></span> <span data-ttu-id="66837-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="66837-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<IsFolderContact/>
```

 <span data-ttu-id="66837-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="66837-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="66837-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="66837-108">Attributes and elements</span></span>

<span data-ttu-id="66837-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="66837-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="66837-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="66837-110">Attributes</span></span>

<span data-ttu-id="66837-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="66837-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="66837-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="66837-112">Child elements</span></span>

<span data-ttu-id="66837-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="66837-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="66837-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="66837-114">Parent elements</span></span>

|<span data-ttu-id="66837-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="66837-115">**Element**</span></span>|<span data-ttu-id="66837-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="66837-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="66837-117">Permiso</span><span class="sxs-lookup"><span data-stu-id="66837-117">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="66837-118">Define el acceso que un usuario tiene a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="66837-118">Defines the access that a user has to a folder.</span></span> <span data-ttu-id="66837-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="66837-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="66837-120">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="66837-120">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="66837-121">Define el acceso que tiene un usuario a una carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="66837-121">Defines the access that a user has to a Calendar folder.</span></span> <span data-ttu-id="66837-122">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="66837-122">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="66837-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="66837-123">Text value</span></span>

<span data-ttu-id="66837-124">Un valor de texto de **true** indica que el usuario es un contacto para la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="66837-124">A text value of **true** indicates that the user is a contact for the specified folder.</span></span> <span data-ttu-id="66837-125">Un valor de **false** indica que el usuario no es un contacto para la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="66837-125">A value of **false** indicates that the user is not a contact for the specified folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="66837-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="66837-126">Remarks</span></span>

<span data-ttu-id="66837-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="66837-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="66837-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="66837-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="66837-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="66837-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="66837-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="66837-130">Schema Name</span></span>  <br/> |<span data-ttu-id="66837-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="66837-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="66837-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="66837-132">Validation File</span></span>  <br/> |<span data-ttu-id="66837-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="66837-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="66837-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="66837-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="66837-135">Falso</span><span class="sxs-lookup"><span data-stu-id="66837-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="66837-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="66837-136">See also</span></span>



- [<span data-ttu-id="66837-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="66837-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="66837-138">Configuración de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="66837-138">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

