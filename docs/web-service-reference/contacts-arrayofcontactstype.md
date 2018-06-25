---
title: Contactos (ArrayOfContactsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a2c1e833-5f8c-438d-bad7-bb5dcc29ca9e
description: El elemento de contactos especifica una matriz de los contactos.
ms.openlocfilehash: 01aab90d28c5d9706a45a2e42be1e60221394e80
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763792"
---
# <a name="contacts-arrayofcontactstype"></a><span data-ttu-id="25358-103">Contactos (ArrayOfContactsType)</span><span class="sxs-lookup"><span data-stu-id="25358-103">Contacts (ArrayOfContactsType)</span></span>

<span data-ttu-id="25358-104">El elemento de **contactos** especifica una matriz de los contactos.</span><span class="sxs-lookup"><span data-stu-id="25358-104">The **Contacts** element specifies an array of contacts.</span></span> 
  
```XML
<Contacts>
    <Contact></Contact>
</Contacts>
```

 <span data-ttu-id="25358-105">**ArrayOfContactsType**</span><span class="sxs-lookup"><span data-stu-id="25358-105">**ArrayOfContactsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="25358-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="25358-106">Attributes and elements</span></span>

<span data-ttu-id="25358-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="25358-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="25358-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="25358-108">Attributes</span></span>

<span data-ttu-id="25358-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="25358-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="25358-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="25358-110">Child elements</span></span>

|<span data-ttu-id="25358-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="25358-111">**Element**</span></span>|<span data-ttu-id="25358-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="25358-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="25358-113">Contacto (ContactType)</span><span class="sxs-lookup"><span data-stu-id="25358-113">Contact (ContactType)</span></span>](contact-contacttype.md) <br/> |<span data-ttu-id="25358-114">Especifica un contacto en el almacén de contactos unificados.</span><span class="sxs-lookup"><span data-stu-id="25358-114">Specifies a contact in the Unified Contact Store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="25358-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="25358-115">Parent elements</span></span>

|<span data-ttu-id="25358-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="25358-116">**Element**</span></span>|<span data-ttu-id="25358-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="25358-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="25358-118">EntityExtractionResult</span><span class="sxs-lookup"><span data-stu-id="25358-118">EntityExtractionResult</span></span>](entityextractionresult.md) <br/> |<span data-ttu-id="25358-119">Especifica la propiedad **EntityExtractionResult** de un elemento.</span><span class="sxs-lookup"><span data-stu-id="25358-119">Specifies the **EntityExtractionResult** property of an item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25358-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="25358-120">Remarks</span></span>

<span data-ttu-id="25358-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="25358-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="25358-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="25358-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="25358-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="25358-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="25358-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="25358-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="25358-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="25358-125">Schema Name</span></span>  <br/> |<span data-ttu-id="25358-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="25358-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="25358-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="25358-127">Validation File</span></span>  <br/> |<span data-ttu-id="25358-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="25358-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="25358-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="25358-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="25358-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="25358-130">See also</span></span>



- [<span data-ttu-id="25358-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="25358-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

