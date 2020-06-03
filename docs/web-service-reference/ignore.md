---
title: Ignore
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
description: El elemento ignore identifica los elementos que se deben omitir durante la sincronización.
ms.openlocfilehash: b65d11d8c7655279dac0e7d3cbd13f8a9317540c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458575"
---
# <a name="ignore"></a><span data-ttu-id="7009c-103">Ignore</span><span class="sxs-lookup"><span data-stu-id="7009c-103">Ignore</span></span>

<span data-ttu-id="7009c-104">El elemento **Ignore** identifica los elementos que se deben omitir durante la sincronización.</span><span class="sxs-lookup"><span data-stu-id="7009c-104">The **Ignore** element identifies items to skip during synchronization.</span></span> 
  
[<span data-ttu-id="7009c-105">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="7009c-105">SyncFolderItems</span></span>](syncfolderitems.md)
  
[<span data-ttu-id="7009c-106">Ignore</span><span class="sxs-lookup"><span data-stu-id="7009c-106">Ignore</span></span>](ignore.md)
  
```xml
<Ignore>
   <ItemId/>
</Ignore>
```

 <span data-ttu-id="7009c-107">**ArrayOfBaseItemIdsType**</span><span class="sxs-lookup"><span data-stu-id="7009c-107">**ArrayOfBaseItemIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7009c-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7009c-108">Attributes and elements</span></span>

<span data-ttu-id="7009c-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7009c-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7009c-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="7009c-110">Attributes</span></span>

<span data-ttu-id="7009c-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7009c-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7009c-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7009c-112">Child elements</span></span>

|<span data-ttu-id="7009c-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7009c-113">**Element**</span></span>|<span data-ttu-id="7009c-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7009c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7009c-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="7009c-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="7009c-116">Contiene el identificador único y la clave de cambio de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="7009c-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7009c-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7009c-117">Parent elements</span></span>

|<span data-ttu-id="7009c-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7009c-118">**Element**</span></span>|<span data-ttu-id="7009c-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7009c-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7009c-120">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="7009c-120">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="7009c-121">Define una solicitud para sincronizar elementos en una carpeta de almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="7009c-121">Defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7009c-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7009c-122">Remarks</span></span>

<span data-ttu-id="7009c-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="7009c-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7009c-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7009c-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7009c-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="7009c-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7009c-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7009c-126">Schema name</span></span>  <br/> |<span data-ttu-id="7009c-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="7009c-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7009c-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7009c-128">Validation file</span></span>  <br/> |<span data-ttu-id="7009c-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="7009c-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7009c-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7009c-130">Can be empty</span></span>  <br/> |<span data-ttu-id="7009c-131">Falso</span><span class="sxs-lookup"><span data-stu-id="7009c-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7009c-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="7009c-132">See also</span></span>



[<span data-ttu-id="7009c-133">Operación SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="7009c-133">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="7009c-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="7009c-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

