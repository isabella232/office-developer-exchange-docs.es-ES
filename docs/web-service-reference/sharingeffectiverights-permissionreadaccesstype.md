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
description: El elemento SharingEffectiveRights indica los permisos que tiene el usuario para los datos de contacto que se está compartiendo.
ms.openlocfilehash: 19e67827dd2dbff6fb70423980d670da5cc257a3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837486"
---
# <a name="sharingeffectiverights-permissionreadaccesstype"></a><span data-ttu-id="d7171-103">SharingEffectiveRights (PermissionReadAccessType)</span><span class="sxs-lookup"><span data-stu-id="d7171-103">SharingEffectiveRights (PermissionReadAccessType)</span></span>

<span data-ttu-id="d7171-104">El elemento **SharingEffectiveRights** indica los permisos que tiene el usuario para los datos de contacto que se está compartiendo.</span><span class="sxs-lookup"><span data-stu-id="d7171-104">The **SharingEffectiveRights** element indicates the permissions that the user has for the contact data that is being shared.</span></span> 
  
```XML
<SharingEffectiveRights>None | FullDetails</SharingEffectiveRights >
```

 <span data-ttu-id="d7171-105">**PermissionReadAccessType**</span><span class="sxs-lookup"><span data-stu-id="d7171-105">**PermissionReadAccessType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d7171-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d7171-106">Attributes and elements</span></span>

<span data-ttu-id="d7171-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d7171-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d7171-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d7171-108">Attributes</span></span>

<span data-ttu-id="d7171-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d7171-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d7171-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d7171-110">Child elements</span></span>

<span data-ttu-id="d7171-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d7171-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d7171-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d7171-112">Parent elements</span></span>

|<span data-ttu-id="d7171-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d7171-113">**Element**</span></span>|<span data-ttu-id="d7171-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d7171-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d7171-115">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="d7171-115">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="d7171-116">Representa una carpeta de contactos que se encuentra en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="d7171-116">Represents a Contacts folder that is contained in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d7171-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d7171-117">Text value</span></span>

<span data-ttu-id="d7171-118">En la siguiente tabla se enumera los valores posibles para el elemento **SharingEffectiveRights** .</span><span class="sxs-lookup"><span data-stu-id="d7171-118">The following table lists the possible values for the **SharingEffectiveRights** element.</span></span> 
  
<span data-ttu-id="d7171-119">**Valores de texto de elemento SharingEffectiveRights**</span><span class="sxs-lookup"><span data-stu-id="d7171-119">**SharingEffectiveRights element text values**</span></span>

|<span data-ttu-id="d7171-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d7171-120">**Value**</span></span>|<span data-ttu-id="d7171-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d7171-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d7171-122">None</span><span class="sxs-lookup"><span data-stu-id="d7171-122">None</span></span>  <br/> |<span data-ttu-id="d7171-123">Indica que el usuario no tiene permiso para leer elementos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="d7171-123">Indicates that the user does not have permission to read items in the folder.</span></span>  <br/> |
|<span data-ttu-id="d7171-124">FullDetails</span><span class="sxs-lookup"><span data-stu-id="d7171-124">FullDetails</span></span>  <br/> |<span data-ttu-id="d7171-125">Indica que el usuario tiene permiso para leer todos los elementos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="d7171-125">Indicates that the user has permission to read all items in the folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7171-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d7171-126">Remarks</span></span>

<span data-ttu-id="d7171-127">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d7171-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d7171-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d7171-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d7171-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d7171-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d7171-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d7171-130">Schema Name</span></span>  <br/> |<span data-ttu-id="d7171-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d7171-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="d7171-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d7171-132">Validation File</span></span>  <br/> |<span data-ttu-id="d7171-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d7171-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d7171-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d7171-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="d7171-135">False</span><span class="sxs-lookup"><span data-stu-id="d7171-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d7171-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7171-136">See also</span></span>



- [<span data-ttu-id="d7171-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d7171-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

