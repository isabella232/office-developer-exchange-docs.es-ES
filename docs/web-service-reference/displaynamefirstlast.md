---
title: DisplayNameFirstLast
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 013c17c9-cb37-4028-9fe6-c3f47441d0f7
description: El elemento DisplayNameFirstLast especifica el nombre para mostrar del rol asociado en el formato, el nombre de pila, el apellido.
ms.openlocfilehash: 6ba35b6a17a64d46655e51691847b9aecbf52f40
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464115"
---
# <a name="displaynamefirstlast"></a><span data-ttu-id="15f65-103">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="15f65-103">DisplayNameFirstLast</span></span>

<span data-ttu-id="15f65-104">El elemento **DisplayNameFirstLast** especifica el nombre para mostrar del rol asociado en el formato, "nombre", "apellido".</span><span class="sxs-lookup"><span data-stu-id="15f65-104">The **DisplayNameFirstLast** element specifies the display name of the associated persona in the format, "First Name", "Last Name".</span></span> 
  
```XML
<DisplayNameFirstLast>
```

 <span data-ttu-id="15f65-105">**string**</span><span class="sxs-lookup"><span data-stu-id="15f65-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="15f65-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="15f65-106">Attributes and elements</span></span>

<span data-ttu-id="15f65-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="15f65-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="15f65-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="15f65-108">Attributes</span></span>

<span data-ttu-id="15f65-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="15f65-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="15f65-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="15f65-110">Child elements</span></span>

<span data-ttu-id="15f65-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="15f65-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="15f65-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="15f65-112">Parent elements</span></span>

|<span data-ttu-id="15f65-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="15f65-113">**Element**</span></span>|<span data-ttu-id="15f65-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="15f65-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="15f65-115">Rol</span><span class="sxs-lookup"><span data-stu-id="15f65-115">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="15f65-116">Especifica un conjunto de datos de rol devueltos por una solicitud **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="15f65-116">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="15f65-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="15f65-117">Text value</span></span>

<span data-ttu-id="15f65-118">El valor de texto del elemento **DisplayNameFirstLast** es un valor de cadena que contiene el nombre para mostrar, con el nombre indicado en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="15f65-118">The text value of the **DisplayNameFirstLast** element is a string value containing the display name, with the given name first.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="15f65-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="15f65-119">Remarks</span></span>

<span data-ttu-id="15f65-120">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="15f65-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="15f65-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="15f65-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="15f65-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="15f65-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="15f65-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="15f65-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="15f65-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="15f65-124">Schema Name</span></span>  <br/> |<span data-ttu-id="15f65-125">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="15f65-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="15f65-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="15f65-126">Validation File</span></span>  <br/> |<span data-ttu-id="15f65-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="15f65-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="15f65-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="15f65-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="15f65-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="15f65-129">See also</span></span>

- [<span data-ttu-id="15f65-130">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="15f65-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

