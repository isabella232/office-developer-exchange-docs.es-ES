---
title: ReadFlagChange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReadFlagChange
api_type:
- schema
ms.assetid: 527bfe90-63d0-4b2f-97f7-7875b3a516b2
description: El elemento ReadFlagChange se devuelve en SyncFolderItems respuestas a la operación cuando se leyó un elemento. Esta propiedad es de sólo lectura.
ms.openlocfilehash: 28ef0267e8308ba58057bec01ab2672a19ee94a1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836953"
---
# <a name="readflagchange"></a><span data-ttu-id="58c3b-104">ReadFlagChange</span><span class="sxs-lookup"><span data-stu-id="58c3b-104">ReadFlagChange</span></span>

<span data-ttu-id="58c3b-105">El elemento **ReadFlagChange** se devuelve en las respuestas de [operación SyncFolderItems](syncfolderitems-operation.md) cuando se leyó un elemento.</span><span class="sxs-lookup"><span data-stu-id="58c3b-105">The **ReadFlagChange** element is returned in [SyncFolderItems operation](syncfolderitems-operation.md) responses when an item has been read.</span></span> <span data-ttu-id="58c3b-106">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="58c3b-106">This property is read-only.</span></span> 
  
```xml
<ReadFlagChange>
   <ItemId/>
   <IsRead/>
</ReadFlagChange>
```

 <span data-ttu-id="58c3b-107">**SyncFolderItemsReadFlagType**</span><span class="sxs-lookup"><span data-stu-id="58c3b-107">**SyncFolderItemsReadFlagType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="58c3b-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="58c3b-108">Attributes and elements</span></span>

<span data-ttu-id="58c3b-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="58c3b-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="58c3b-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="58c3b-110">Attributes</span></span>

<span data-ttu-id="58c3b-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="58c3b-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="58c3b-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="58c3b-112">Child elements</span></span>

|<span data-ttu-id="58c3b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="58c3b-113">**Element**</span></span>|<span data-ttu-id="58c3b-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="58c3b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="58c3b-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="58c3b-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="58c3b-116">Identifica el elemento para el que se ha cambiado la marca de lectura.</span><span class="sxs-lookup"><span data-stu-id="58c3b-116">Identifies the item for which the read-flag has been changed.</span></span>  <br/> |
|[<span data-ttu-id="58c3b-117">Estáleído</span><span class="sxs-lookup"><span data-stu-id="58c3b-117">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="58c3b-118">Indica si la marca de lectura se ha establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="58c3b-118">Indicates whether the read-flag has been set to **true**.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="58c3b-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="58c3b-119">Parent elements</span></span>

|<span data-ttu-id="58c3b-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="58c3b-120">**Element**</span></span>|<span data-ttu-id="58c3b-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="58c3b-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="58c3b-122">Cambios (elementos)</span><span class="sxs-lookup"><span data-stu-id="58c3b-122">Changes (Items)</span></span>](changes-items.md) <br/> |<span data-ttu-id="58c3b-123">Contiene una matriz de secuencia de tipos de cambios que representan los tipos de las diferencias entre los elementos en el cliente y los elementos en el servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="58c3b-123">Contains a sequence array of change types that represent the types of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58c3b-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="58c3b-124">Remarks</span></span>

<span data-ttu-id="58c3b-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="58c3b-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="58c3b-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="58c3b-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="58c3b-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="58c3b-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="58c3b-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="58c3b-128">Schema Name</span></span>  <br/> |<span data-ttu-id="58c3b-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="58c3b-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="58c3b-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="58c3b-130">Validation File</span></span>  <br/> |<span data-ttu-id="58c3b-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="58c3b-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="58c3b-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="58c3b-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="58c3b-133">False</span><span class="sxs-lookup"><span data-stu-id="58c3b-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="58c3b-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="58c3b-134">See also</span></span>



- [<span data-ttu-id="58c3b-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="58c3b-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

