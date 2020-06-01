---
title: Inaddresses (ArrayOfStringAttributedValuesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b95d0a8b-15a6-4711-b014-55698dbd679c
description: El elemento imaddresses especifica una matriz de direcciones de mensajes instantáneos y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: 6714af5d88e50047f48da2f10dbb33d2e2feb724
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460445"
---
# <a name="imaddresses-arrayofstringattributedvaluestype"></a><span data-ttu-id="60b1a-103">Inaddresses (ArrayOfStringAttributedValuesType)</span><span class="sxs-lookup"><span data-stu-id="60b1a-103">ImAddresses (ArrayOfStringAttributedValuesType)</span></span>

<span data-ttu-id="60b1a-104">El elemento **Imaddresses** especifica una matriz de direcciones de mensajes instantáneos y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="60b1a-104">The **ImAddresses** element specifies an array of instant message addresses and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<ImAddresses>
    <StringAttributedValue/>
</ImAddresses>
```

 <span data-ttu-id="60b1a-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="60b1a-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="60b1a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="60b1a-106">Attributes and elements</span></span>

<span data-ttu-id="60b1a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="60b1a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="60b1a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="60b1a-108">Attributes</span></span>

<span data-ttu-id="60b1a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="60b1a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="60b1a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="60b1a-110">Child elements</span></span>

|<span data-ttu-id="60b1a-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="60b1a-111">**Element**</span></span>|<span data-ttu-id="60b1a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="60b1a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="60b1a-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="60b1a-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="60b1a-114">Especifica una instancia de una matriz de atributos asociada a un elemento de rol.</span><span class="sxs-lookup"><span data-stu-id="60b1a-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="60b1a-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="60b1a-115">Parent elements</span></span>

|<span data-ttu-id="60b1a-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="60b1a-116">**Element**</span></span>|<span data-ttu-id="60b1a-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="60b1a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="60b1a-118">Rol</span><span class="sxs-lookup"><span data-stu-id="60b1a-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="60b1a-119">Especifica un conjunto de datos de rol devueltos por una solicitud **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="60b1a-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="60b1a-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="60b1a-120">Remarks</span></span>

<span data-ttu-id="60b1a-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="60b1a-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="60b1a-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="60b1a-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="60b1a-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="60b1a-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="60b1a-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="60b1a-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="60b1a-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="60b1a-125">Schema Name</span></span>  <br/> |<span data-ttu-id="60b1a-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="60b1a-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="60b1a-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="60b1a-127">Validation File</span></span>  <br/> |<span data-ttu-id="60b1a-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="60b1a-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="60b1a-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="60b1a-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="60b1a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="60b1a-130">See also</span></span>



- [<span data-ttu-id="60b1a-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="60b1a-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

