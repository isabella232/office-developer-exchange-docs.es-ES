---
title: Atribuciones (ArrayOfPersonaAttributionsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61d843c-bca5-4c88-9667-fd03d2a963a1
description: El elemento de atribuciones especifica una matriz de información de atribución para uno o varios de los contactos o los destinatarios de Active Directory agregados a la persona asociada.
ms.openlocfilehash: 52fecb4e4381d5e9dbbaf7134fa18068ba15f6ec
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763580"
---
# <a name="attributions-arrayofpersonaattributionstype"></a><span data-ttu-id="f3e5a-103">Atribuciones (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="f3e5a-103">Attributions (ArrayOfPersonaAttributionsType)</span></span>

<span data-ttu-id="f3e5a-104">El elemento de **atribuciones** especifica una matriz de información de atribución para uno o varios de los contactos o los destinatarios de Active Directory agregados a la persona asociada.</span><span class="sxs-lookup"><span data-stu-id="f3e5a-104">The **Attributions** element specifies an array of attribution information for one or more of the contacts or Active Directory recipients aggregated into the associated persona.</span></span> 
  
```XML
<Attributions>
    <Attribution></Attribution>
</Attributions>
```

 <span data-ttu-id="f3e5a-105">**ArrayOfPersonaAttributionsType**</span><span class="sxs-lookup"><span data-stu-id="f3e5a-105">**ArrayOfPersonaAttributionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f3e5a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f3e5a-106">Attributes and elements</span></span>

<span data-ttu-id="f3e5a-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f3e5a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f3e5a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f3e5a-108">Attributes</span></span>

<span data-ttu-id="f3e5a-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f3e5a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f3e5a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f3e5a-110">Child elements</span></span>

|<span data-ttu-id="f3e5a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f3e5a-111">**Element**</span></span>|<span data-ttu-id="f3e5a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f3e5a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f3e5a-113">Atribución (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="f3e5a-113">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md) <br/> |<span data-ttu-id="f3e5a-114">Especifica una instancia de una matriz de atributos para un elemento **PersonaType** .</span><span class="sxs-lookup"><span data-stu-id="f3e5a-114">Specifies an instance in an array of attributes for a **PersonaType** element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f3e5a-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f3e5a-115">Parent elements</span></span>

|<span data-ttu-id="f3e5a-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="f3e5a-116">**Element**</span></span>|<span data-ttu-id="f3e5a-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f3e5a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f3e5a-118">Rol</span><span class="sxs-lookup"><span data-stu-id="f3e5a-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="f3e5a-119">Especifica un conjunto de datos de rol devueltos por una solicitud de **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="f3e5a-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3e5a-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f3e5a-120">Remarks</span></span>

<span data-ttu-id="f3e5a-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f3e5a-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f3e5a-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f3e5a-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f3e5a-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f3e5a-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f3e5a-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f3e5a-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f3e5a-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f3e5a-125">Schema Name</span></span>  <br/> |<span data-ttu-id="f3e5a-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="f3e5a-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="f3e5a-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f3e5a-127">Validation File</span></span>  <br/> |<span data-ttu-id="f3e5a-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f3e5a-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="f3e5a-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f3e5a-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="f3e5a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3e5a-130">See also</span></span>

- [<span data-ttu-id="f3e5a-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="f3e5a-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

