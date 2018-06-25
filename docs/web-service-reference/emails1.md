---
title: Emails1
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cc02bd86-c618-446a-92f0-749423cbc4ee
description: El elemento Emails1 especifica una matriz de valores de EmailAddressAttributedValue y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: f1a1223244c91731b1a5a1beb9daed6d680d3bc4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764354"
---
# <a name="emails1"></a><span data-ttu-id="62fe5-103">Emails1</span><span class="sxs-lookup"><span data-stu-id="62fe5-103">Emails1</span></span>

<span data-ttu-id="62fe5-104">El elemento **Emails1** especifica una matriz de valores de **EmailAddressAttributedValue** y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="62fe5-104">The **Emails1** element specifies an array of **EmailAddressAttributedValue** values and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<Emails1>
    <EmailAddressAttributedValue></EmailAddressAttributedValue>
</Emails1>
```

 <span data-ttu-id="62fe5-105">**ArrayOfEmailAddressAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="62fe5-105">**ArrayOfEmailAddressAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="62fe5-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="62fe5-106">Attributes and elements</span></span>

<span data-ttu-id="62fe5-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="62fe5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="62fe5-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="62fe5-108">Attributes</span></span>

<span data-ttu-id="62fe5-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="62fe5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="62fe5-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="62fe5-110">Child elements</span></span>

|<span data-ttu-id="62fe5-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="62fe5-111">**Element**</span></span>|<span data-ttu-id="62fe5-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="62fe5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="62fe5-113">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="62fe5-113">EmailAddressAttributedValue</span></span>](emailaddressattributedvalue.md) <br/> |<span data-ttu-id="62fe5-114">Especifica una instancia de una matriz de direcciones de correo electrónico y sus atribuciones asociados.</span><span class="sxs-lookup"><span data-stu-id="62fe5-114">Specifies an instance of an array of email addresses and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="62fe5-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="62fe5-115">Parent elements</span></span>

|<span data-ttu-id="62fe5-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="62fe5-116">**Element**</span></span>|<span data-ttu-id="62fe5-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="62fe5-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="62fe5-118">Rol</span><span class="sxs-lookup"><span data-stu-id="62fe5-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="62fe5-119">Especifica un conjunto de datos de rol devueltos por una solicitud de **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="62fe5-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62fe5-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="62fe5-120">Remarks</span></span>

<span data-ttu-id="62fe5-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="62fe5-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="62fe5-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="62fe5-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="62fe5-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="62fe5-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="62fe5-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="62fe5-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="62fe5-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="62fe5-125">Schema Name</span></span>  <br/> |<span data-ttu-id="62fe5-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="62fe5-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="62fe5-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="62fe5-127">Validation File</span></span>  <br/> |<span data-ttu-id="62fe5-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="62fe5-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="62fe5-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="62fe5-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="62fe5-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="62fe5-130">See also</span></span>



- [<span data-ttu-id="62fe5-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="62fe5-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

