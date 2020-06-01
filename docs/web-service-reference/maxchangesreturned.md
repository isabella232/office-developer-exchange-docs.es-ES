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
ms.openlocfilehash: caf96b6e95f2e63d0e544ead26fbea18cd637861
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460088"
---
# <a name="maxchangesreturned"></a><span data-ttu-id="2e2e3-103">MaxChangesReturned</span><span class="sxs-lookup"><span data-stu-id="2e2e3-103">MaxChangesReturned</span></span>

<span data-ttu-id="2e2e3-104">El elemento **MaxChangesReturned** describe el número máximo de cambios que se pueden devolver en una respuesta de sincronización.</span><span class="sxs-lookup"><span data-stu-id="2e2e3-104">The **MaxChangesReturned** element describes the maximum number of changes that can be returned in a synchronization response.</span></span> 
  
[<span data-ttu-id="2e2e3-105">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="2e2e3-105">SyncFolderItems</span></span>](syncfolderitems.md)
  
[<span data-ttu-id="2e2e3-106">MaxChangesReturned</span><span class="sxs-lookup"><span data-stu-id="2e2e3-106">MaxChangesReturned</span></span>](maxchangesreturned.md)
  
```xml
<MaxChangesReturned/>
```

 <span data-ttu-id="2e2e3-107">**int**</span><span class="sxs-lookup"><span data-stu-id="2e2e3-107">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2e2e3-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2e2e3-108">Attributes and elements</span></span>

<span data-ttu-id="2e2e3-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2e2e3-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2e2e3-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="2e2e3-110">Attributes</span></span>

<span data-ttu-id="2e2e3-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2e2e3-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2e2e3-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2e2e3-112">Child elements</span></span>

<span data-ttu-id="2e2e3-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2e2e3-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2e2e3-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2e2e3-114">Parent elements</span></span>

|<span data-ttu-id="2e2e3-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2e2e3-115">**Element**</span></span>|<span data-ttu-id="2e2e3-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2e2e3-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e2e3-117">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="2e2e3-117">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="2e2e3-118">Define una solicitud para sincronizar elementos en una carpeta de almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2e2e3-118">Defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2e2e3-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="2e2e3-119">Text value</span></span>

<span data-ttu-id="2e2e3-120">El valor de texto representa un entero que describe el número máximo de elementos que se devuelven en una única llamada de sincronización.</span><span class="sxs-lookup"><span data-stu-id="2e2e3-120">The text value represents an integer that describes the maximum number of items that are returned in a single synchronization call.</span></span> <span data-ttu-id="2e2e3-121">El valor debe estar comprendido entre 1 y 512, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="2e2e3-121">The value must be between 1 and 512, inclusive.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2e2e3-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2e2e3-122">Remarks</span></span>

<span data-ttu-id="2e2e3-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="2e2e3-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2e2e3-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2e2e3-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2e2e3-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="2e2e3-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2e2e3-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2e2e3-126">Schema name</span></span>  <br/> |<span data-ttu-id="2e2e3-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="2e2e3-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="2e2e3-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2e2e3-128">Validation file</span></span>  <br/> |<span data-ttu-id="2e2e3-129">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="2e2e3-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2e2e3-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2e2e3-130">Can be empty</span></span>  <br/> |<span data-ttu-id="2e2e3-131">Falso</span><span class="sxs-lookup"><span data-stu-id="2e2e3-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2e2e3-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e2e3-132">See also</span></span>



[<span data-ttu-id="2e2e3-133">Operación SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="2e2e3-133">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="2e2e3-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2e2e3-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

