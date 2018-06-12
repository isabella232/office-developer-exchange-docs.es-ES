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
description: El elemento CanRenameOrMove indica si se puede cambiar el nombre de una carpeta administrada o movida por el cliente.
ms.openlocfilehash: 0303499f5cd54d4a52222e43c2c5f0b389fbcf53
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763729"
---
# <a name="canrenameormove"></a><span data-ttu-id="3eb5f-103">CanRenameOrMove</span><span class="sxs-lookup"><span data-stu-id="3eb5f-103">CanRenameOrMove</span></span>

<span data-ttu-id="3eb5f-104">El elemento **CanRenameOrMove** indica si se puede cambiar el nombre de una carpeta administrada o movida por el cliente.</span><span class="sxs-lookup"><span data-stu-id="3eb5f-104">The **CanRenameOrMove** element indicates whether a managed folder can be renamed or moved by the customer.</span></span> 
  
```xml
<CanRenameOrMove/>
```

 <span data-ttu-id="3eb5f-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="3eb5f-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3eb5f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3eb5f-106">Attributes and elements</span></span>

<span data-ttu-id="3eb5f-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3eb5f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3eb5f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3eb5f-108">Attributes</span></span>

<span data-ttu-id="3eb5f-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3eb5f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3eb5f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3eb5f-110">Child elements</span></span>

<span data-ttu-id="3eb5f-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3eb5f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3eb5f-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3eb5f-112">Parent elements</span></span>

|<span data-ttu-id="3eb5f-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3eb5f-113">**Element**</span></span>|<span data-ttu-id="3eb5f-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3eb5f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3eb5f-115">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="3eb5f-115">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="3eb5f-116">Contiene información acerca de una carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="3eb5f-116">Contains information about a managed folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3eb5f-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3eb5f-117">Text value</span></span>

<span data-ttu-id="3eb5f-118">El valor de texto representa un valor de tipo Boolean.</span><span class="sxs-lookup"><span data-stu-id="3eb5f-118">The text value represents a Boolean value.</span></span> <span data-ttu-id="3eb5f-119">Un valor de **true** indica que se puede cambiar el nombre de la carpeta o mover; un valor de **false** indica que la carpeta no se cambia o se desplaza.</span><span class="sxs-lookup"><span data-stu-id="3eb5f-119">A value of **true** indicates that the folder can be renamed or moved; a value of **false** indicates that the folder cannot be renamed or moved.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3eb5f-120">Notas</span><span class="sxs-lookup"><span data-stu-id="3eb5f-120">Remarks</span></span>

<span data-ttu-id="3eb5f-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="3eb5f-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3eb5f-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3eb5f-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3eb5f-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3eb5f-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3eb5f-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3eb5f-124">Schema name</span></span>  <br/> |<span data-ttu-id="3eb5f-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="3eb5f-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="3eb5f-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3eb5f-126">Validation file</span></span>  <br/> |<span data-ttu-id="3eb5f-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3eb5f-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3eb5f-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3eb5f-128">Can be empty</span></span>  <br/> |<span data-ttu-id="3eb5f-129">False</span><span class="sxs-lookup"><span data-stu-id="3eb5f-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3eb5f-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="3eb5f-130">See also</span></span>



- [<span data-ttu-id="3eb5f-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3eb5f-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

