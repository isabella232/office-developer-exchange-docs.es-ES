---
title: Omitir
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Ignore
api_type:
- schema
ms.assetid: 7789eec5-ceec-43f2-84d5-d0d15b734076
description: El elemento omitir identifica los elementos se debe omitir durante la sincronización.
ms.openlocfilehash: 0ecff9bfeb1257552b7e52c0115e9e814edecd4b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835858"
---
# <a name="ignore"></a><span data-ttu-id="d7d48-103">Omitir</span><span class="sxs-lookup"><span data-stu-id="d7d48-103">Ignore</span></span>

<span data-ttu-id="d7d48-104">El elemento **Omitir** identifica los elementos se debe omitir durante la sincronización.</span><span class="sxs-lookup"><span data-stu-id="d7d48-104">The **Ignore** element identifies items to skip during synchronization.</span></span> 
  
[<span data-ttu-id="d7d48-105">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="d7d48-105">SyncFolderItems</span></span>](syncfolderitems.md)
  
[<span data-ttu-id="d7d48-106">Ignorar</span><span class="sxs-lookup"><span data-stu-id="d7d48-106">Ignore</span></span>](ignore.md)
  
```xml
<Ignore>
   <ItemId/>
</Ignore>
```

 <span data-ttu-id="d7d48-107">**ArrayOfBaseItemIdsType**</span><span class="sxs-lookup"><span data-stu-id="d7d48-107">**ArrayOfBaseItemIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d7d48-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d7d48-108">Attributes and elements</span></span>

<span data-ttu-id="d7d48-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d7d48-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d7d48-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="d7d48-110">Attributes</span></span>

<span data-ttu-id="d7d48-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d7d48-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d7d48-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d7d48-112">Child elements</span></span>

|<span data-ttu-id="d7d48-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d7d48-113">**Element**</span></span>|<span data-ttu-id="d7d48-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d7d48-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d7d48-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="d7d48-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="d7d48-116">Contiene el único identificador y cambiar la clave de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d7d48-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d7d48-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d7d48-117">Parent elements</span></span>

|<span data-ttu-id="d7d48-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="d7d48-118">**Element**</span></span>|<span data-ttu-id="d7d48-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d7d48-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d7d48-120">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="d7d48-120">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="d7d48-121">Define una solicitud para sincronizar los elementos en una carpeta de almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d7d48-121">Defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7d48-122">Notas</span><span class="sxs-lookup"><span data-stu-id="d7d48-122">Remarks</span></span>

<span data-ttu-id="d7d48-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="d7d48-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d7d48-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d7d48-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d7d48-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d7d48-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d7d48-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d7d48-126">Schema name</span></span>  <br/> |<span data-ttu-id="d7d48-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="d7d48-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d7d48-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d7d48-128">Validation file</span></span>  <br/> |<span data-ttu-id="d7d48-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d7d48-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d7d48-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d7d48-130">Can be empty</span></span>  <br/> |<span data-ttu-id="d7d48-131">False</span><span class="sxs-lookup"><span data-stu-id="d7d48-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d7d48-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="d7d48-132">See also</span></span>



[<span data-ttu-id="d7d48-133">Operación SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="d7d48-133">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="d7d48-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d7d48-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
