---
title: Emails3
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4f4dc589-4530-4a35-b2a6-0c83cac23637
description: El elemento Emails3 especifica una matriz de valores de EmailAddressAttributedValue y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: 1d174000d59883446bb7f61af90278d197ef5ed9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764358"
---
# <a name="emails3"></a><span data-ttu-id="f91af-103">Emails3</span><span class="sxs-lookup"><span data-stu-id="f91af-103">Emails3</span></span>

<span data-ttu-id="f91af-104">El elemento **Emails3** especifica una matriz de valores de **EmailAddressAttributedValue** y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="f91af-104">The **Emails3** element specifies an array of **EmailAddressAttributedValue** values and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<Emails3>
    <EmailAddressAttributedValue></EmailAddressAttributedValue>
</Emails3>
```

 <span data-ttu-id="f91af-105">**ArrayOfEmailAddressAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="f91af-105">**ArrayOfEmailAddressAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f91af-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f91af-106">Attributes and elements</span></span>

<span data-ttu-id="f91af-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f91af-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f91af-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f91af-108">Attributes</span></span>

<span data-ttu-id="f91af-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f91af-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f91af-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f91af-110">Child elements</span></span>

|<span data-ttu-id="f91af-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f91af-111">**Element**</span></span>|<span data-ttu-id="f91af-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f91af-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f91af-113">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="f91af-113">EmailAddressAttributedValue</span></span>](emailaddressattributedvalue.md) <br/> |<span data-ttu-id="f91af-114">Especifica una instancia de una matriz de direcciones de correo electrónico y sus atribuciones asociados.</span><span class="sxs-lookup"><span data-stu-id="f91af-114">Specifies an instance of an array of email addresses and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f91af-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f91af-115">Parent elements</span></span>

|<span data-ttu-id="f91af-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="f91af-116">**Element**</span></span>|<span data-ttu-id="f91af-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f91af-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f91af-118">Rol</span><span class="sxs-lookup"><span data-stu-id="f91af-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="f91af-119">Especifica un conjunto de datos de rol devueltos por una solicitud de **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="f91af-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f91af-120">Notas</span><span class="sxs-lookup"><span data-stu-id="f91af-120">Remarks</span></span>

<span data-ttu-id="f91af-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f91af-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f91af-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f91af-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f91af-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f91af-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f91af-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f91af-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f91af-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f91af-125">Schema Name</span></span>  <br/> |<span data-ttu-id="f91af-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="f91af-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="f91af-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f91af-127">Validation File</span></span>  <br/> |<span data-ttu-id="f91af-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f91af-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="f91af-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f91af-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="f91af-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="f91af-130">See also</span></span>



- [<span data-ttu-id="f91af-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="f91af-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

