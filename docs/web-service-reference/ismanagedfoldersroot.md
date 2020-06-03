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
ms.openlocfilehash: 4373dba9dce92de8e175948d889f0806e100fa6c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466027"
---
# <a name="ismanagedfoldersroot"></a><span data-ttu-id="43457-103">IsManagedFoldersRoot</span><span class="sxs-lookup"><span data-stu-id="43457-103">IsManagedFoldersRoot</span></span>

<span data-ttu-id="43457-104">El elemento **IsManagedFoldersRoot** indica si la carpeta administrada es la raíz de todas las carpetas administradas.</span><span class="sxs-lookup"><span data-stu-id="43457-104">The **IsManagedFoldersRoot** element indicates whether the managed folder is the root for all managed folders.</span></span> 
  
```xml
<IsManagedFoldersRoot/>
```

 <span data-ttu-id="43457-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="43457-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="43457-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="43457-106">Attributes and elements</span></span>

<span data-ttu-id="43457-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="43457-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="43457-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="43457-108">Attributes</span></span>

<span data-ttu-id="43457-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="43457-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="43457-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="43457-110">Child elements</span></span>

<span data-ttu-id="43457-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="43457-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="43457-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="43457-112">Parent elements</span></span>

|<span data-ttu-id="43457-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="43457-113">**Element**</span></span>|<span data-ttu-id="43457-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="43457-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="43457-115">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="43457-115">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="43457-116">Contiene información acerca de una carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="43457-116">Contains information about a managed folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="43457-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="43457-117">Text value</span></span>

<span data-ttu-id="43457-118">Es necesario un valor de texto que representa un valor booleano si este elemento está presente.</span><span class="sxs-lookup"><span data-stu-id="43457-118">A text value that represents a Boolean value is required if this element is present.</span></span> <span data-ttu-id="43457-119">Un valor de **true** indica que la carpeta es la carpeta raíz de la carpeta administrada; un valor de **false** indica que la carpeta no es la carpeta raíz de la carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="43457-119">A value of **true** indicates that the folder is the root folder of the managed folder; a value of **false** indicates that the folder is not the root folder of the managed folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="43457-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="43457-120">Remarks</span></span>

<span data-ttu-id="43457-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="43457-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="43457-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="43457-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="43457-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="43457-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="43457-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="43457-124">Schema name</span></span>  <br/> |<span data-ttu-id="43457-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="43457-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="43457-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="43457-126">Validation file</span></span>  <br/> |<span data-ttu-id="43457-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="43457-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="43457-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="43457-128">Can be empty</span></span>  <br/> |<span data-ttu-id="43457-129">Falso</span><span class="sxs-lookup"><span data-stu-id="43457-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="43457-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="43457-130">See also</span></span>



- [<span data-ttu-id="43457-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="43457-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

