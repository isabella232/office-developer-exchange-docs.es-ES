---
title: SharingEffectiveRights (PermissionReadAccessType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SharingEffectiveRights
api_type:
- schema
ms.assetid: 808bb4a1-aa2d-48c5-94b3-551b52c348bd
description: El elemento SharingEffectiveRights indica los permisos que tiene el usuario para los datos de contacto que se están compartiendo.
ms.openlocfilehash: 64b1e6d831068e9699e9cd47693e74919e0416a5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526665"
---
# <a name="sharingeffectiverights-permissionreadaccesstype"></a><span data-ttu-id="fc103-103">SharingEffectiveRights (PermissionReadAccessType)</span><span class="sxs-lookup"><span data-stu-id="fc103-103">SharingEffectiveRights (PermissionReadAccessType)</span></span>

<span data-ttu-id="fc103-104">El elemento **SharingEffectiveRights** indica los permisos que tiene el usuario para los datos de contacto que se están compartiendo.</span><span class="sxs-lookup"><span data-stu-id="fc103-104">The **SharingEffectiveRights** element indicates the permissions that the user has for the contact data that is being shared.</span></span> 
  
```XML
<SharingEffectiveRights>None | FullDetails</SharingEffectiveRights >
```

 <span data-ttu-id="fc103-105">**PermissionReadAccessType**</span><span class="sxs-lookup"><span data-stu-id="fc103-105">**PermissionReadAccessType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fc103-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fc103-106">Attributes and elements</span></span>

<span data-ttu-id="fc103-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fc103-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fc103-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="fc103-108">Attributes</span></span>

<span data-ttu-id="fc103-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fc103-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fc103-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fc103-110">Child elements</span></span>

<span data-ttu-id="fc103-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fc103-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fc103-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fc103-112">Parent elements</span></span>

|<span data-ttu-id="fc103-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fc103-113">**Element**</span></span>|<span data-ttu-id="fc103-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fc103-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fc103-115">Hubiera</span><span class="sxs-lookup"><span data-stu-id="fc103-115">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="fc103-116">Representa una carpeta de contactos contenida en un buzón.</span><span class="sxs-lookup"><span data-stu-id="fc103-116">Represents a Contacts folder that is contained in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fc103-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="fc103-117">Text value</span></span>

<span data-ttu-id="fc103-118">En la siguiente tabla se enumeran los valores posibles para el elemento **SharingEffectiveRights** .</span><span class="sxs-lookup"><span data-stu-id="fc103-118">The following table lists the possible values for the **SharingEffectiveRights** element.</span></span> 
  
<span data-ttu-id="fc103-119">**Valores de texto del elemento SharingEffectiveRights**</span><span class="sxs-lookup"><span data-stu-id="fc103-119">**SharingEffectiveRights element text values**</span></span>

|<span data-ttu-id="fc103-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="fc103-120">**Value**</span></span>|<span data-ttu-id="fc103-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fc103-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fc103-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="fc103-122">None</span></span>  <br/> |<span data-ttu-id="fc103-123">Indica que el usuario no tiene permiso para leer los elementos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="fc103-123">Indicates that the user does not have permission to read items in the folder.</span></span>  <br/> |
|<span data-ttu-id="fc103-124">FullDetails</span><span class="sxs-lookup"><span data-stu-id="fc103-124">FullDetails</span></span>  <br/> |<span data-ttu-id="fc103-125">Indica que el usuario tiene permiso para leer todos los elementos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="fc103-125">Indicates that the user has permission to read all items in the folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc103-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fc103-126">Remarks</span></span>

<span data-ttu-id="fc103-127">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="fc103-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fc103-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fc103-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fc103-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="fc103-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fc103-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fc103-130">Schema Name</span></span>  <br/> |<span data-ttu-id="fc103-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="fc103-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="fc103-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fc103-132">Validation File</span></span>  <br/> |<span data-ttu-id="fc103-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="fc103-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fc103-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fc103-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="fc103-135">Falso</span><span class="sxs-lookup"><span data-stu-id="fc103-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fc103-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc103-136">See also</span></span>



- [<span data-ttu-id="fc103-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="fc103-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

