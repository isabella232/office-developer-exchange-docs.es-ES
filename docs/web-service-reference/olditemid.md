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
ms.openlocfilehash: 9fab14478ffbb2dd8ad013d59520af943584f2eb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467469"
---
# <a name="olditemid"></a><span data-ttu-id="c53d0-103">OldItemId</span><span class="sxs-lookup"><span data-stu-id="c53d0-103">OldItemId</span></span>

<span data-ttu-id="c53d0-104">El elemento **OldItemId** contiene el identificador único del elemento que se ha copiado o movido.</span><span class="sxs-lookup"><span data-stu-id="c53d0-104">The **OldItemId** element contains the unique identifier of the item that was copied or moved.</span></span> 
  
```xml
<OldItemId Id="" ChangeKey=""/>
```

 <span data-ttu-id="c53d0-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="c53d0-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c53d0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c53d0-106">Attributes and elements</span></span>

<span data-ttu-id="c53d0-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c53d0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c53d0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c53d0-108">Attributes</span></span>

|<span data-ttu-id="c53d0-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c53d0-109">**Attribute**</span></span>|<span data-ttu-id="c53d0-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c53d0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c53d0-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="c53d0-111">**Id**</span></span> <br/> |<span data-ttu-id="c53d0-112">Contiene una cadena que identifica un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c53d0-112">Contains a string that identifies an item in the Exchange store.</span></span> <span data-ttu-id="c53d0-113">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c53d0-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="c53d0-114">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="c53d0-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="c53d0-115">Contiene una cadena que identifica una versión de un elemento identificado por el atributo id.</span><span class="sxs-lookup"><span data-stu-id="c53d0-115">Contains a string that identifies a version of an item that is identified by the Id attribute.</span></span> <span data-ttu-id="c53d0-116">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="c53d0-116">This attribute is optional.</span></span> <span data-ttu-id="c53d0-117">Use este atributo para asegurarse de que se usa la versión correcta de un elemento.</span><span class="sxs-lookup"><span data-stu-id="c53d0-117">Use this attribute to make sure that the correct version of an item is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c53d0-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c53d0-118">Child elements</span></span>

<span data-ttu-id="c53d0-119">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c53d0-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c53d0-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c53d0-120">Parent elements</span></span>

|<span data-ttu-id="c53d0-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c53d0-121">**Element**</span></span>|<span data-ttu-id="c53d0-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c53d0-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c53d0-123">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="c53d0-123">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="c53d0-124">Representa un evento en el que se copia un elemento o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="c53d0-124">Represents an event in which an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="c53d0-125">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="c53d0-125">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="c53d0-126">Representa un evento en el que se mueve un elemento o una carpeta de una carpeta principal a otra carpeta principal.</span><span class="sxs-lookup"><span data-stu-id="c53d0-126">Represents an event in which an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c53d0-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c53d0-127">Remarks</span></span>

<span data-ttu-id="c53d0-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="c53d0-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c53d0-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c53d0-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c53d0-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="c53d0-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c53d0-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c53d0-131">Schema Name</span></span>  <br/> |<span data-ttu-id="c53d0-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c53d0-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="c53d0-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c53d0-133">Validation File</span></span>  <br/> |<span data-ttu-id="c53d0-134">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c53d0-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c53d0-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c53d0-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="c53d0-136">Falso</span><span class="sxs-lookup"><span data-stu-id="c53d0-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c53d0-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="c53d0-137">See also</span></span>



[<span data-ttu-id="c53d0-138">Operación subscribe</span><span class="sxs-lookup"><span data-stu-id="c53d0-138">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="c53d0-139">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="c53d0-139">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="c53d0-140">Operación unsubscribe</span><span class="sxs-lookup"><span data-stu-id="c53d0-140">Unsubscribe operation</span></span>](unsubscribe-operation.md)


- [<span data-ttu-id="c53d0-141">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c53d0-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

