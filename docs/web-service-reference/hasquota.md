---
title: HasQuota
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HasQuota
api_type:
- schema
ms.assetid: b6e4fef0-92a9-415f-81ae-0c5ecb7c12ad
description: El elemento HasQuota indica si la carpeta administrada tiene una cuota.
ms.openlocfilehash: 26f14ee7c9d4de267733bca11f7884d1d391b3dd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835807"
---
# <a name="hasquota"></a><span data-ttu-id="6a44e-103">HasQuota</span><span class="sxs-lookup"><span data-stu-id="6a44e-103">HasQuota</span></span>

<span data-ttu-id="6a44e-104">El elemento **HasQuota** indica si la carpeta administrada tiene una cuota.</span><span class="sxs-lookup"><span data-stu-id="6a44e-104">The **HasQuota** element indicates whether the managed folder has a quota.</span></span> 
  
```xml
<HasQuota/>
```

 <span data-ttu-id="6a44e-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="6a44e-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6a44e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6a44e-106">Attributes and elements</span></span>

<span data-ttu-id="6a44e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6a44e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6a44e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6a44e-108">Attributes</span></span>

<span data-ttu-id="6a44e-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6a44e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6a44e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6a44e-110">Child elements</span></span>

<span data-ttu-id="6a44e-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6a44e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6a44e-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6a44e-112">Parent elements</span></span>

|<span data-ttu-id="6a44e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6a44e-113">**Element**</span></span>|<span data-ttu-id="6a44e-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6a44e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6a44e-115">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="6a44e-115">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="6a44e-116">Contiene información acerca de una carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="6a44e-116">Contains information about a managed folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6a44e-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="6a44e-117">Text value</span></span>

<span data-ttu-id="6a44e-118">El valor de texto representa un valor de tipo Boolean.</span><span class="sxs-lookup"><span data-stu-id="6a44e-118">The text value represents a Boolean value.</span></span> <span data-ttu-id="6a44e-119">Un valor de **true** indica que la carpeta tiene una cuota; un valor de **false** indica que la carpeta no tiene una cuota.</span><span class="sxs-lookup"><span data-stu-id="6a44e-119">A value of **true** indicates that the folder has a quota; a value of **false** indicates that the folder does not have a quota.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6a44e-120">Notas</span><span class="sxs-lookup"><span data-stu-id="6a44e-120">Remarks</span></span>

<span data-ttu-id="6a44e-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="6a44e-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6a44e-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6a44e-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6a44e-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6a44e-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6a44e-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6a44e-124">Schema name</span></span>  <br/> |<span data-ttu-id="6a44e-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="6a44e-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="6a44e-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6a44e-126">Validation file</span></span>  <br/> |<span data-ttu-id="6a44e-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6a44e-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6a44e-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6a44e-128">Can be empty</span></span>  <br/> |<span data-ttu-id="6a44e-129">False</span><span class="sxs-lookup"><span data-stu-id="6a44e-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6a44e-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="6a44e-130">See also</span></span>



- [<span data-ttu-id="6a44e-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="6a44e-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

