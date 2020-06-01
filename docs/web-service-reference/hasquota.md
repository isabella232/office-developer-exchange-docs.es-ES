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
ms.openlocfilehash: 6e32aa4c69943774be928339936cca5016c58d85
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462755"
---
# <a name="hasquota"></a><span data-ttu-id="fdee3-103">HasQuota</span><span class="sxs-lookup"><span data-stu-id="fdee3-103">HasQuota</span></span>

<span data-ttu-id="fdee3-104">El elemento **HasQuota** indica si la carpeta administrada tiene una cuota.</span><span class="sxs-lookup"><span data-stu-id="fdee3-104">The **HasQuota** element indicates whether the managed folder has a quota.</span></span> 
  
```xml
<HasQuota/>
```

 <span data-ttu-id="fdee3-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="fdee3-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fdee3-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fdee3-106">Attributes and elements</span></span>

<span data-ttu-id="fdee3-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fdee3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fdee3-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="fdee3-108">Attributes</span></span>

<span data-ttu-id="fdee3-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fdee3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fdee3-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fdee3-110">Child elements</span></span>

<span data-ttu-id="fdee3-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fdee3-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fdee3-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fdee3-112">Parent elements</span></span>

|<span data-ttu-id="fdee3-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fdee3-113">**Element**</span></span>|<span data-ttu-id="fdee3-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fdee3-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fdee3-115">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="fdee3-115">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="fdee3-116">Contiene información acerca de una carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="fdee3-116">Contains information about a managed folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fdee3-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="fdee3-117">Text value</span></span>

<span data-ttu-id="fdee3-118">El valor de texto representa un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="fdee3-118">The text value represents a Boolean value.</span></span> <span data-ttu-id="fdee3-119">Un valor de **true** indica que la carpeta tiene una cuota; un valor de **false** indica que la carpeta no tiene cuota.</span><span class="sxs-lookup"><span data-stu-id="fdee3-119">A value of **true** indicates that the folder has a quota; a value of **false** indicates that the folder does not have a quota.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fdee3-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fdee3-120">Remarks</span></span>

<span data-ttu-id="fdee3-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="fdee3-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fdee3-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fdee3-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fdee3-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="fdee3-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fdee3-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fdee3-124">Schema name</span></span>  <br/> |<span data-ttu-id="fdee3-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="fdee3-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="fdee3-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fdee3-126">Validation file</span></span>  <br/> |<span data-ttu-id="fdee3-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="fdee3-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fdee3-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fdee3-128">Can be empty</span></span>  <br/> |<span data-ttu-id="fdee3-129">Falso</span><span class="sxs-lookup"><span data-stu-id="fdee3-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fdee3-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="fdee3-130">See also</span></span>



- [<span data-ttu-id="fdee3-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="fdee3-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

