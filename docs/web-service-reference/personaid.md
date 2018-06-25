---
title: PersonaId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eec3a468-afd5-4d72-a61e-cd1964fb686c
description: El elemento PersonaId especifica el identificador de rol para el rol asociado.
ms.openlocfilehash: 77668a1b32a97eef08b3316c7d4d7c8e6494c7bb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836738"
---
# <a name="personaid"></a><span data-ttu-id="2d8e7-103">PersonaId</span><span class="sxs-lookup"><span data-stu-id="2d8e7-103">PersonaId</span></span>

<span data-ttu-id="2d8e7-104">El elemento **PersonaId** especifica el identificador de rol para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="2d8e7-104">The **PersonaId** element specifies the persona identifier for the associated persona.</span></span> 
  
```XML
<PersonaId Id="" ChangeKey=""/>
```

 <span data-ttu-id="2d8e7-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="2d8e7-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2d8e7-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2d8e7-106">Attributes and elements</span></span>

<span data-ttu-id="2d8e7-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2d8e7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2d8e7-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2d8e7-108">Attributes</span></span>

|<span data-ttu-id="2d8e7-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="2d8e7-109">**Attribute**</span></span>|<span data-ttu-id="2d8e7-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2d8e7-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2d8e7-111">Id</span><span class="sxs-lookup"><span data-stu-id="2d8e7-111">Id</span></span>  <br/> |<span data-ttu-id="2d8e7-112">El valor de texto del atributo **Id** es el identificador de la persona.</span><span class="sxs-lookup"><span data-stu-id="2d8e7-112">The text value of the **Id** attribute is the identifier of the persona.</span></span>  <br/> |
|<span data-ttu-id="2d8e7-113">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="2d8e7-113">ChangeKey</span></span>  <br/> |<span data-ttu-id="2d8e7-114">El valor de texto del atributo **ChangeKey** es la clave de cambio de la persona.</span><span class="sxs-lookup"><span data-stu-id="2d8e7-114">The text value of the **ChangeKey** attribute is the change key of the persona.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2d8e7-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2d8e7-115">Child elements</span></span>

<span data-ttu-id="2d8e7-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2d8e7-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2d8e7-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2d8e7-117">Parent elements</span></span>

<span data-ttu-id="2d8e7-118">[GetPersona](getpersona.md) | [rol](persona.md)</span><span class="sxs-lookup"><span data-stu-id="2d8e7-118">[GetPersona](getpersona.md) | [Persona](persona.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2d8e7-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2d8e7-119">Remarks</span></span>

<span data-ttu-id="2d8e7-120">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2d8e7-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2d8e7-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="2d8e7-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2d8e7-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2d8e7-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2d8e7-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2d8e7-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2d8e7-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2d8e7-124">Schema name</span></span>  <br/> |<span data-ttu-id="2d8e7-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="2d8e7-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2d8e7-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2d8e7-126">Validation file</span></span>  <br/> |<span data-ttu-id="2d8e7-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2d8e7-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2d8e7-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2d8e7-128">Can be empty</span></span>  <br/> ||
   

