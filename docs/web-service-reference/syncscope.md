---
title: SyncScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncScope
api_type:
- schema
ms.assetid: e0ca231f-0374-4844-8d4c-ada8da167920
description: El elemento SyncScope especifica si se devuelven sólo los elementos o elementos y la carpeta asociada información en una respuesta de sincronización.
ms.openlocfilehash: 847c0244a8847364e29ea584b0c0b721f00d3064
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840618"
---
# <a name="syncscope"></a><span data-ttu-id="dd26b-103">SyncScope</span><span class="sxs-lookup"><span data-stu-id="dd26b-103">SyncScope</span></span>

<span data-ttu-id="dd26b-104">El elemento **SyncScope** especifica si se devuelven sólo los elementos o elementos y la carpeta asociada información en una respuesta de sincronización.</span><span class="sxs-lookup"><span data-stu-id="dd26b-104">The **SyncScope** element specifies whether just items or items and folder associated information are returned in a synchronization response.</span></span> 
  
```xml
<SyncScope>NormalItems or NormalAndAssociatedItems</SyncScope>
```

 <span data-ttu-id="dd26b-105">**SyncFolderItemsScopeType**</span><span class="sxs-lookup"><span data-stu-id="dd26b-105">**SyncFolderItemsScopeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dd26b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="dd26b-106">Attributes and elements</span></span>

<span data-ttu-id="dd26b-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="dd26b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dd26b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="dd26b-108">Attributes</span></span>

<span data-ttu-id="dd26b-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dd26b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dd26b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dd26b-110">Child elements</span></span>

<span data-ttu-id="dd26b-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dd26b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dd26b-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="dd26b-112">Parent elements</span></span>

|<span data-ttu-id="dd26b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="dd26b-113">**Element**</span></span>|<span data-ttu-id="dd26b-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dd26b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dd26b-115">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="dd26b-115">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="dd26b-116">El elemento que define una solicitud para sincronizar los elementos en una carpeta de almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="dd26b-116">The element that defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> <span data-ttu-id="dd26b-117">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="dd26b-117">The following is the XPath expression to this element:</span></span>  <br/> <span data-ttu-id="dd26b-118">/ SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="dd26b-118">/SyncFolderItems</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="dd26b-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="dd26b-119">Text value</span></span>

<span data-ttu-id="dd26b-120">En la siguiente tabla se enumera los valores posibles para el elemento **SyncScope** .</span><span class="sxs-lookup"><span data-stu-id="dd26b-120">The following table lists the possible values for the **SyncScope** element.</span></span> 
  
<span data-ttu-id="dd26b-121">**Valores de elemento SyncScope**</span><span class="sxs-lookup"><span data-stu-id="dd26b-121">**SyncScope element values**</span></span>

|<span data-ttu-id="dd26b-122">**Valor**</span><span class="sxs-lookup"><span data-stu-id="dd26b-122">**Value**</span></span>|<span data-ttu-id="dd26b-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dd26b-123">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dd26b-124">NormalItems</span><span class="sxs-lookup"><span data-stu-id="dd26b-124">NormalItems</span></span>  <br/> |<span data-ttu-id="dd26b-125">Especifica que sólo los elementos de la carpeta se devuelven en una respuesta de sincronización.</span><span class="sxs-lookup"><span data-stu-id="dd26b-125">Specifies that only items in the folder are returned in a synchronization response.</span></span>  <br/> |
|<span data-ttu-id="dd26b-126">NormalAndAssociatedItems</span><span class="sxs-lookup"><span data-stu-id="dd26b-126">NormalAndAssociatedItems</span></span>  <br/> |<span data-ttu-id="dd26b-127">Especifica que se devuelven ambos elementos en la carpeta y la información de la carpeta asociada en una respuesta de sincronización.</span><span class="sxs-lookup"><span data-stu-id="dd26b-127">Specifies that both items in the folder and folder associated information are returned in a synchronization response.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd26b-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dd26b-128">Remarks</span></span>

<span data-ttu-id="dd26b-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="dd26b-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dd26b-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="dd26b-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dd26b-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dd26b-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="dd26b-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="dd26b-132">Schema Name</span></span>  <br/> |<span data-ttu-id="dd26b-133">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="dd26b-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="dd26b-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="dd26b-134">Validation File</span></span>  <br/> |<span data-ttu-id="dd26b-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="dd26b-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dd26b-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="dd26b-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="dd26b-137">False</span><span class="sxs-lookup"><span data-stu-id="dd26b-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dd26b-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd26b-138">See also</span></span>



[<span data-ttu-id="dd26b-139">Operación SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="dd26b-139">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="dd26b-140">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="dd26b-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

