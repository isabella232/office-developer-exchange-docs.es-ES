---
title: Eliminar
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Delete
api_type:
- schema
ms.assetid: aa45f0c1-a80d-4b6c-8a85-375b6de515f4
description: El elemento Delete indica si un cliente puede eliminar una carpeta o un elemento.
ms.openlocfilehash: 5460f9e49b126ca6b039c6f11aaa3c6eb4a40544
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457357"
---
# <a name="delete"></a><span data-ttu-id="6b095-103">Eliminar</span><span class="sxs-lookup"><span data-stu-id="6b095-103">Delete</span></span>

<span data-ttu-id="6b095-104">El elemento **Delete** indica si un cliente puede eliminar una carpeta o un elemento.</span><span class="sxs-lookup"><span data-stu-id="6b095-104">The **Delete** element indicates whether a client can delete a folder or item.</span></span> 
  
```XML
<Delete>true or false</Delete>
```

<span data-ttu-id="6b095-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="6b095-105">**boolean**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="6b095-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6b095-106">Attributes and elements</span></span>

<span data-ttu-id="6b095-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6b095-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6b095-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6b095-108">Attributes</span></span>

<span data-ttu-id="6b095-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6b095-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6b095-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6b095-110">Child elements</span></span>

<span data-ttu-id="6b095-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6b095-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6b095-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6b095-112">Parent elements</span></span>

|<span data-ttu-id="6b095-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6b095-113">**Element**</span></span>|<span data-ttu-id="6b095-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6b095-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6b095-115">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="6b095-115">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="6b095-116">Contiene los derechos del cliente en función de la configuración de los permisos del elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="6b095-116">Contains the rights of the client based on the permission settings for the item or folder.</span></span>  <br/> |
|[<span data-ttu-id="6b095-117">Actions</span><span class="sxs-lookup"><span data-stu-id="6b095-117">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="6b095-118">Representa el conjunto de acciones que se pueden realizar en un mensaje cuando se cumplen las condiciones.</span><span class="sxs-lookup"><span data-stu-id="6b095-118">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6b095-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="6b095-119">Text value</span></span>

<span data-ttu-id="6b095-120">Un valor de texto de **true** indica que un cliente puede eliminar un elemento o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="6b095-120">A text value of **true** indicates that a client can delete an item or folder.</span></span> <span data-ttu-id="6b095-121">Un valor de **false** indica que un cliente no puede eliminar un elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="6b095-121">A value of **false** indicates that a client cannot delete an item or folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6b095-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6b095-122">Remarks</span></span>

<span data-ttu-id="6b095-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="6b095-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6b095-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6b095-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6b095-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="6b095-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6b095-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6b095-126">Schema Name</span></span>  <br/> |<span data-ttu-id="6b095-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="6b095-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="6b095-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6b095-128">Validation File</span></span>  <br/> |<span data-ttu-id="6b095-129">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="6b095-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6b095-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6b095-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="6b095-131">Falso</span><span class="sxs-lookup"><span data-stu-id="6b095-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6b095-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b095-132">See also</span></span>

- [<span data-ttu-id="6b095-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6b095-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="6b095-134">Configuración de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="6b095-134">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

