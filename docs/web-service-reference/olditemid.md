---
title: OldItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OldItemId
api_type:
- schema
ms.assetid: fb57deee-9cc3-4730-9805-ff34f39e3ab7
description: El elemento OldItemId contiene el identificador único del elemento que se ha copiado o movido.
ms.openlocfilehash: ced7fc6891e0d1fde42a8cb9cad4f4e55493b5d1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836648"
---
# <a name="olditemid"></a><span data-ttu-id="cc5b1-103">OldItemId</span><span class="sxs-lookup"><span data-stu-id="cc5b1-103">OldItemId</span></span>

<span data-ttu-id="cc5b1-104">El elemento **OldItemId** contiene el identificador único del elemento que se ha copiado o movido.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-104">The **OldItemId** element contains the unique identifier of the item that was copied or moved.</span></span> 
  
```xml
<OldItemId Id="" ChangeKey=""/>
```

 <span data-ttu-id="cc5b1-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="cc5b1-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cc5b1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cc5b1-106">Attributes and elements</span></span>

<span data-ttu-id="cc5b1-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cc5b1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="cc5b1-108">Attributes</span></span>

|<span data-ttu-id="cc5b1-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="cc5b1-109">**Attribute**</span></span>|<span data-ttu-id="cc5b1-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cc5b1-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cc5b1-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="cc5b1-111">**Id**</span></span> <br/> |<span data-ttu-id="cc5b1-112">Contiene una cadena que identifica un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-112">Contains a string that identifies an item in the Exchange store.</span></span> <span data-ttu-id="cc5b1-113">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="cc5b1-114">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="cc5b1-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="cc5b1-115">Contiene una cadena que identifica una versión de un elemento que se identifica con el atributo Id.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-115">Contains a string that identifies a version of an item that is identified by the Id attribute.</span></span> <span data-ttu-id="cc5b1-116">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-116">This attribute is optional.</span></span> <span data-ttu-id="cc5b1-117">Use este atributo para asegurarse de que se usa la versión correcta de un elemento.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-117">Use this attribute to make sure that the correct version of an item is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cc5b1-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cc5b1-118">Child elements</span></span>

<span data-ttu-id="cc5b1-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cc5b1-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cc5b1-120">Parent elements</span></span>

|<span data-ttu-id="cc5b1-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="cc5b1-121">**Element**</span></span>|<span data-ttu-id="cc5b1-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cc5b1-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cc5b1-123">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="cc5b1-123">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="cc5b1-124">Representa un evento en el que se copia un elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-124">Represents an event in which an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="cc5b1-125">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="cc5b1-125">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="cc5b1-126">Representa un evento en el que una carpeta o elemento se mueve de una carpeta principal a otra carpeta primaria.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-126">Represents an event in which an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc5b1-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cc5b1-127">Remarks</span></span>

<span data-ttu-id="cc5b1-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cc5b1-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cc5b1-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cc5b1-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cc5b1-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cc5b1-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cc5b1-131">Schema Name</span></span>  <br/> |<span data-ttu-id="cc5b1-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="cc5b1-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="cc5b1-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cc5b1-133">Validation File</span></span>  <br/> |<span data-ttu-id="cc5b1-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cc5b1-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cc5b1-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cc5b1-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="cc5b1-136">False</span><span class="sxs-lookup"><span data-stu-id="cc5b1-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cc5b1-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc5b1-137">See also</span></span>



[<span data-ttu-id="cc5b1-138">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="cc5b1-138">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="cc5b1-139">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="cc5b1-139">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="cc5b1-140">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="cc5b1-140">Unsubscribe operation</span></span>](unsubscribe-operation.md)


- [<span data-ttu-id="cc5b1-141">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="cc5b1-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

