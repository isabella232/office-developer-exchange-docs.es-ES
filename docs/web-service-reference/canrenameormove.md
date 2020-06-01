---
title: CanRenameOrMove
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CanRenameOrMove
api_type:
- schema
ms.assetid: fe0cdb04-5f2b-4f1d-9d12-7ace0883cd86
description: El elemento CanRenameOrMove indica si el cliente puede cambiar el nombre de una carpeta administrada o moverla.
ms.openlocfilehash: eb6aaeb8b0edcab5b67212c426a44daf32a0cf73
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463366"
---
# <a name="canrenameormove"></a><span data-ttu-id="b741a-103">CanRenameOrMove</span><span class="sxs-lookup"><span data-stu-id="b741a-103">CanRenameOrMove</span></span>

<span data-ttu-id="b741a-104">El elemento **CanRenameOrMove** indica si el cliente puede cambiar el nombre de una carpeta administrada o moverla.</span><span class="sxs-lookup"><span data-stu-id="b741a-104">The **CanRenameOrMove** element indicates whether a managed folder can be renamed or moved by the customer.</span></span> 
  
```xml
<CanRenameOrMove/>
```

 <span data-ttu-id="b741a-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="b741a-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b741a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b741a-106">Attributes and elements</span></span>

<span data-ttu-id="b741a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b741a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b741a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b741a-108">Attributes</span></span>

<span data-ttu-id="b741a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b741a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b741a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b741a-110">Child elements</span></span>

<span data-ttu-id="b741a-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b741a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b741a-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b741a-112">Parent elements</span></span>

|<span data-ttu-id="b741a-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b741a-113">**Element**</span></span>|<span data-ttu-id="b741a-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b741a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b741a-115">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="b741a-115">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="b741a-116">Contiene información acerca de una carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="b741a-116">Contains information about a managed folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b741a-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b741a-117">Text value</span></span>

<span data-ttu-id="b741a-118">El valor de texto representa un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="b741a-118">The text value represents a Boolean value.</span></span> <span data-ttu-id="b741a-119">Un valor de **true** indica que la carpeta se puede cambiar de nombre o mover; un valor de **false** indica que no se puede cambiar el nombre de la carpeta ni se puede mover.</span><span class="sxs-lookup"><span data-stu-id="b741a-119">A value of **true** indicates that the folder can be renamed or moved; a value of **false** indicates that the folder cannot be renamed or moved.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b741a-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b741a-120">Remarks</span></span>

<span data-ttu-id="b741a-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="b741a-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b741a-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b741a-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b741a-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="b741a-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b741a-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b741a-124">Schema name</span></span>  <br/> |<span data-ttu-id="b741a-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b741a-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="b741a-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b741a-126">Validation file</span></span>  <br/> |<span data-ttu-id="b741a-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="b741a-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b741a-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b741a-128">Can be empty</span></span>  <br/> |<span data-ttu-id="b741a-129">Falso</span><span class="sxs-lookup"><span data-stu-id="b741a-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b741a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="b741a-130">See also</span></span>



- [<span data-ttu-id="b741a-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b741a-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

