---
title: MaxChangesReturned
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MaxChangesReturned
api_type:
- schema
ms.assetid: f471db84-a666-4dfa-9993-8ca9113a0384
description: El elemento MaxChangesReturned describe el número máximo de cambios que se pueden devolver en una respuesta de sincronización.
ms.openlocfilehash: c3719b12b7e3e2f83a9454c7b68432b375d78614
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836395"
---
# <a name="maxchangesreturned"></a><span data-ttu-id="9545f-103">MaxChangesReturned</span><span class="sxs-lookup"><span data-stu-id="9545f-103">MaxChangesReturned</span></span>

<span data-ttu-id="9545f-104">El elemento **MaxChangesReturned** describe el número máximo de cambios que se pueden devolver en una respuesta de sincronización.</span><span class="sxs-lookup"><span data-stu-id="9545f-104">The **MaxChangesReturned** element describes the maximum number of changes that can be returned in a synchronization response.</span></span> 
  
[<span data-ttu-id="9545f-105">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="9545f-105">SyncFolderItems</span></span>](syncfolderitems.md)
  
[<span data-ttu-id="9545f-106">MaxChangesReturned</span><span class="sxs-lookup"><span data-stu-id="9545f-106">MaxChangesReturned</span></span>](maxchangesreturned.md)
  
```xml
<MaxChangesReturned/>
```

 <span data-ttu-id="9545f-107">**int**</span><span class="sxs-lookup"><span data-stu-id="9545f-107">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9545f-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9545f-108">Attributes and elements</span></span>

<span data-ttu-id="9545f-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9545f-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9545f-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="9545f-110">Attributes</span></span>

<span data-ttu-id="9545f-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9545f-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9545f-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9545f-112">Child elements</span></span>

<span data-ttu-id="9545f-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9545f-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9545f-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9545f-114">Parent elements</span></span>

|<span data-ttu-id="9545f-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="9545f-115">**Element**</span></span>|<span data-ttu-id="9545f-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9545f-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9545f-117">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="9545f-117">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="9545f-118">Define una solicitud para sincronizar los elementos en una carpeta de almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="9545f-118">Defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9545f-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="9545f-119">Text value</span></span>

<span data-ttu-id="9545f-120">El valor de texto representa un número entero que describe el número máximo de elementos que se devuelven en una llamada de sincronización único.</span><span class="sxs-lookup"><span data-stu-id="9545f-120">The text value represents an integer that describes the maximum number of items that are returned in a single synchronization call.</span></span> <span data-ttu-id="9545f-121">El valor debe ser entre 1 y 512, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="9545f-121">The value must be between 1 and 512, inclusive.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9545f-122">Notas</span><span class="sxs-lookup"><span data-stu-id="9545f-122">Remarks</span></span>

<span data-ttu-id="9545f-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="9545f-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9545f-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9545f-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9545f-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9545f-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9545f-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9545f-126">Schema name</span></span>  <br/> |<span data-ttu-id="9545f-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="9545f-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="9545f-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9545f-128">Validation file</span></span>  <br/> |<span data-ttu-id="9545f-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9545f-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9545f-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9545f-130">Can be empty</span></span>  <br/> |<span data-ttu-id="9545f-131">False</span><span class="sxs-lookup"><span data-stu-id="9545f-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9545f-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="9545f-132">See also</span></span>



[<span data-ttu-id="9545f-133">Operación SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="9545f-133">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="9545f-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="9545f-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

