---
title: IsManagedFoldersRoot
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsManagedFoldersRoot
api_type:
- schema
ms.assetid: 00823fb9-bf8b-49bb-8e1b-d698c6d4063f
description: El elemento IsManagedFoldersRoot indica si la carpeta administrada es la raíz de todas las carpetas administradas.
ms.openlocfilehash: 3484a3fef56545a9a8d56af65f56f75205918ec7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836044"
---
# <a name="ismanagedfoldersroot"></a><span data-ttu-id="01a0d-103">IsManagedFoldersRoot</span><span class="sxs-lookup"><span data-stu-id="01a0d-103">IsManagedFoldersRoot</span></span>

<span data-ttu-id="01a0d-104">El elemento **IsManagedFoldersRoot** indica si la carpeta administrada es la raíz de todas las carpetas administradas.</span><span class="sxs-lookup"><span data-stu-id="01a0d-104">The **IsManagedFoldersRoot** element indicates whether the managed folder is the root for all managed folders.</span></span> 
  
```xml
<IsManagedFoldersRoot/>
```

 <span data-ttu-id="01a0d-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="01a0d-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="01a0d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="01a0d-106">Attributes and elements</span></span>

<span data-ttu-id="01a0d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="01a0d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="01a0d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="01a0d-108">Attributes</span></span>

<span data-ttu-id="01a0d-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="01a0d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="01a0d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="01a0d-110">Child elements</span></span>

<span data-ttu-id="01a0d-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="01a0d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="01a0d-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="01a0d-112">Parent elements</span></span>

|<span data-ttu-id="01a0d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="01a0d-113">**Element**</span></span>|<span data-ttu-id="01a0d-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="01a0d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="01a0d-115">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="01a0d-115">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="01a0d-116">Contiene información acerca de una carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="01a0d-116">Contains information about a managed folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="01a0d-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="01a0d-117">Text value</span></span>

<span data-ttu-id="01a0d-118">Si este elemento está presente, se requiere un valor de texto que representa un valor de tipo Boolean.</span><span class="sxs-lookup"><span data-stu-id="01a0d-118">A text value that represents a Boolean value is required if this element is present.</span></span> <span data-ttu-id="01a0d-119">Un valor de **true** indica que la carpeta es la carpeta raíz de la carpeta administrada; un valor de **false** indica que la carpeta no es la carpeta raíz de la carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="01a0d-119">A value of **true** indicates that the folder is the root folder of the managed folder; a value of **false** indicates that the folder is not the root folder of the managed folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="01a0d-120">Notas</span><span class="sxs-lookup"><span data-stu-id="01a0d-120">Remarks</span></span>

<span data-ttu-id="01a0d-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="01a0d-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="01a0d-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="01a0d-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="01a0d-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="01a0d-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="01a0d-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="01a0d-124">Schema name</span></span>  <br/> |<span data-ttu-id="01a0d-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="01a0d-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="01a0d-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="01a0d-126">Validation file</span></span>  <br/> |<span data-ttu-id="01a0d-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="01a0d-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="01a0d-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="01a0d-128">Can be empty</span></span>  <br/> |<span data-ttu-id="01a0d-129">False</span><span class="sxs-lookup"><span data-stu-id="01a0d-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="01a0d-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="01a0d-130">See also</span></span>



- [<span data-ttu-id="01a0d-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="01a0d-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

