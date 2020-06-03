---
title: Contactos (ArrayOfContactsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a2c1e833-5f8c-438d-bad7-bb5dcc29ca9e
description: El elemento Contacts especifica una matriz de contactos.
ms.openlocfilehash: eeb202f41fcf5ec7aad12a8a2b8e6dd539b3dba4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529444"
---
# <a name="contacts-arrayofcontactstype"></a><span data-ttu-id="ba65d-103">Contactos (ArrayOfContactsType)</span><span class="sxs-lookup"><span data-stu-id="ba65d-103">Contacts (ArrayOfContactsType)</span></span>

<span data-ttu-id="ba65d-104">El elemento **Contacts** especifica una matriz de contactos.</span><span class="sxs-lookup"><span data-stu-id="ba65d-104">The **Contacts** element specifies an array of contacts.</span></span> 
  
```XML
<Contacts>
    <Contact></Contact>
</Contacts>
```

 <span data-ttu-id="ba65d-105">**ArrayOfContactsType**</span><span class="sxs-lookup"><span data-stu-id="ba65d-105">**ArrayOfContactsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ba65d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ba65d-106">Attributes and elements</span></span>

<span data-ttu-id="ba65d-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ba65d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ba65d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ba65d-108">Attributes</span></span>

<span data-ttu-id="ba65d-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ba65d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ba65d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ba65d-110">Child elements</span></span>

|<span data-ttu-id="ba65d-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ba65d-111">**Element**</span></span>|<span data-ttu-id="ba65d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ba65d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba65d-113">Contacto (ContactType)</span><span class="sxs-lookup"><span data-stu-id="ba65d-113">Contact (ContactType)</span></span>](contact-contacttype.md) <br/> |<span data-ttu-id="ba65d-114">Especifica un contacto en el almacén de contactos unificados.</span><span class="sxs-lookup"><span data-stu-id="ba65d-114">Specifies a contact in the Unified Contact Store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ba65d-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ba65d-115">Parent elements</span></span>

|<span data-ttu-id="ba65d-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ba65d-116">**Element**</span></span>|<span data-ttu-id="ba65d-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ba65d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba65d-118">EntityExtractionResult</span><span class="sxs-lookup"><span data-stu-id="ba65d-118">EntityExtractionResult</span></span>](entityextractionresult.md) <br/> |<span data-ttu-id="ba65d-119">Especifica la propiedad **EntityExtractionResult** de un elemento.</span><span class="sxs-lookup"><span data-stu-id="ba65d-119">Specifies the **EntityExtractionResult** property of an item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ba65d-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ba65d-120">Remarks</span></span>

<span data-ttu-id="ba65d-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ba65d-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ba65d-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ba65d-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ba65d-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ba65d-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ba65d-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="ba65d-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ba65d-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ba65d-125">Schema Name</span></span>  <br/> |<span data-ttu-id="ba65d-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="ba65d-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="ba65d-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ba65d-127">Validation File</span></span>  <br/> |<span data-ttu-id="ba65d-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="ba65d-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="ba65d-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ba65d-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="ba65d-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba65d-130">See also</span></span>



- [<span data-ttu-id="ba65d-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ba65d-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

