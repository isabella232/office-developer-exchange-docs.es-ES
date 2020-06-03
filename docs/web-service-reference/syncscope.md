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
description: El elemento SyncScope especifica si solo los elementos o elementos y la información asociada a la carpeta se devuelven en una respuesta de sincronización.
ms.openlocfilehash: 5ede26204c823a452189222075c784f24e98d188
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463037"
---
# <a name="syncscope"></a><span data-ttu-id="96eb8-103">SyncScope</span><span class="sxs-lookup"><span data-stu-id="96eb8-103">SyncScope</span></span>

<span data-ttu-id="96eb8-104">El elemento **SyncScope** especifica si solo los elementos o elementos y la información asociada a la carpeta se devuelven en una respuesta de sincronización.</span><span class="sxs-lookup"><span data-stu-id="96eb8-104">The **SyncScope** element specifies whether just items or items and folder associated information are returned in a synchronization response.</span></span> 
  
```xml
<SyncScope>NormalItems or NormalAndAssociatedItems</SyncScope>
```

 <span data-ttu-id="96eb8-105">**SyncFolderItemsScopeType**</span><span class="sxs-lookup"><span data-stu-id="96eb8-105">**SyncFolderItemsScopeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="96eb8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="96eb8-106">Attributes and elements</span></span>

<span data-ttu-id="96eb8-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="96eb8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="96eb8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="96eb8-108">Attributes</span></span>

<span data-ttu-id="96eb8-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="96eb8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="96eb8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="96eb8-110">Child elements</span></span>

<span data-ttu-id="96eb8-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="96eb8-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="96eb8-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="96eb8-112">Parent elements</span></span>

|<span data-ttu-id="96eb8-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="96eb8-113">**Element**</span></span>|<span data-ttu-id="96eb8-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="96eb8-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="96eb8-115">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="96eb8-115">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="96eb8-116">Elemento que define una solicitud para sincronizar elementos en una carpeta de almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="96eb8-116">The element that defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> <span data-ttu-id="96eb8-117">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="96eb8-117">The following is the XPath expression to this element:</span></span>  <br/> <span data-ttu-id="96eb8-118">/SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="96eb8-118">/SyncFolderItems</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="96eb8-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="96eb8-119">Text value</span></span>

<span data-ttu-id="96eb8-120">En la siguiente tabla se enumeran los valores posibles para el elemento **SyncScope** .</span><span class="sxs-lookup"><span data-stu-id="96eb8-120">The following table lists the possible values for the **SyncScope** element.</span></span> 
  
<span data-ttu-id="96eb8-121">**Valores del elemento SyncScope**</span><span class="sxs-lookup"><span data-stu-id="96eb8-121">**SyncScope element values**</span></span>

|<span data-ttu-id="96eb8-122">**Valor**</span><span class="sxs-lookup"><span data-stu-id="96eb8-122">**Value**</span></span>|<span data-ttu-id="96eb8-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="96eb8-123">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="96eb8-124">NormalItems</span><span class="sxs-lookup"><span data-stu-id="96eb8-124">NormalItems</span></span>  <br/> |<span data-ttu-id="96eb8-125">Especifica que sólo los elementos de la carpeta se devuelven en una respuesta de sincronización.</span><span class="sxs-lookup"><span data-stu-id="96eb8-125">Specifies that only items in the folder are returned in a synchronization response.</span></span>  <br/> |
|<span data-ttu-id="96eb8-126">NormalAndAssociatedItems</span><span class="sxs-lookup"><span data-stu-id="96eb8-126">NormalAndAssociatedItems</span></span>  <br/> |<span data-ttu-id="96eb8-127">Especifica que ambos elementos de la carpeta y la información asociada a la carpeta se devuelven en una respuesta de sincronización.</span><span class="sxs-lookup"><span data-stu-id="96eb8-127">Specifies that both items in the folder and folder associated information are returned in a synchronization response.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96eb8-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="96eb8-128">Remarks</span></span>

<span data-ttu-id="96eb8-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="96eb8-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="96eb8-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="96eb8-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="96eb8-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="96eb8-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="96eb8-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="96eb8-132">Schema Name</span></span>  <br/> |<span data-ttu-id="96eb8-133">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="96eb8-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="96eb8-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="96eb8-134">Validation File</span></span>  <br/> |<span data-ttu-id="96eb8-135">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="96eb8-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="96eb8-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="96eb8-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="96eb8-137">Falso</span><span class="sxs-lookup"><span data-stu-id="96eb8-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="96eb8-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="96eb8-138">See also</span></span>



[<span data-ttu-id="96eb8-139">Operación SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="96eb8-139">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="96eb8-140">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="96eb8-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

