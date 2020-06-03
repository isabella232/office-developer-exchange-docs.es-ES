---
title: Atribuciones (ArrayOfPersonaAttributionsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61d843c-bca5-4c88-9667-fd03d2a963a1
description: El elemento atribuciones especifica una matriz de información de atribución de uno o varios de los contactos o de los destinatarios de Active Directory agregados al rol asociado.
ms.openlocfilehash: a9883e06a8adbd5c9d3bc7e1edd28c62418df653
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460326"
---
# <a name="attributions-arrayofpersonaattributionstype"></a><span data-ttu-id="d3e02-103">Atribuciones (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="d3e02-103">Attributions (ArrayOfPersonaAttributionsType)</span></span>

<span data-ttu-id="d3e02-104">El elemento **atribuciones** especifica una matriz de información de atribución de uno o varios de los contactos o de los destinatarios de Active Directory agregados al rol asociado.</span><span class="sxs-lookup"><span data-stu-id="d3e02-104">The **Attributions** element specifies an array of attribution information for one or more of the contacts or Active Directory recipients aggregated into the associated persona.</span></span> 
  
```XML
<Attributions>
    <Attribution></Attribution>
</Attributions>
```

 <span data-ttu-id="d3e02-105">**ArrayOfPersonaAttributionsType**</span><span class="sxs-lookup"><span data-stu-id="d3e02-105">**ArrayOfPersonaAttributionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d3e02-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d3e02-106">Attributes and elements</span></span>

<span data-ttu-id="d3e02-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d3e02-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d3e02-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d3e02-108">Attributes</span></span>

<span data-ttu-id="d3e02-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d3e02-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d3e02-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d3e02-110">Child elements</span></span>

|<span data-ttu-id="d3e02-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d3e02-111">**Element**</span></span>|<span data-ttu-id="d3e02-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d3e02-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d3e02-113">Atribución (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="d3e02-113">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md) <br/> |<span data-ttu-id="d3e02-114">Especifica una instancia de una matriz de atributos para un elemento **PersonaType** .</span><span class="sxs-lookup"><span data-stu-id="d3e02-114">Specifies an instance in an array of attributes for a **PersonaType** element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d3e02-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d3e02-115">Parent elements</span></span>

|<span data-ttu-id="d3e02-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d3e02-116">**Element**</span></span>|<span data-ttu-id="d3e02-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d3e02-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d3e02-118">Rol</span><span class="sxs-lookup"><span data-stu-id="d3e02-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="d3e02-119">Especifica un conjunto de datos de rol devueltos por una solicitud **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="d3e02-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3e02-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d3e02-120">Remarks</span></span>

<span data-ttu-id="d3e02-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d3e02-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d3e02-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d3e02-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d3e02-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d3e02-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d3e02-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="d3e02-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d3e02-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d3e02-125">Schema Name</span></span>  <br/> |<span data-ttu-id="d3e02-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="d3e02-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="d3e02-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d3e02-127">Validation File</span></span>  <br/> |<span data-ttu-id="d3e02-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="d3e02-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="d3e02-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d3e02-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="d3e02-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3e02-130">See also</span></span>

- [<span data-ttu-id="d3e02-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d3e02-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

