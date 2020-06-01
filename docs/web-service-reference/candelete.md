---
title: CanDelete
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CanDelete
api_type:
- schema
ms.assetid: 55e17121-aad0-4f90-889f-2c3512e9579c
description: El elemento CanDelete indica si un cliente puede eliminar una carpeta administrada.
ms.openlocfilehash: 5fe16c276bdb0c5b3b73ca63099559d3e869db3e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461593"
---
# <a name="candelete"></a><span data-ttu-id="459ed-103">CanDelete</span><span class="sxs-lookup"><span data-stu-id="459ed-103">CanDelete</span></span>

<span data-ttu-id="459ed-104">El elemento **CanDelete** indica si un cliente puede eliminar una carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="459ed-104">The **CanDelete** element indicates whether a managed folder can be deleted by a customer.</span></span> 
  
```xml
<CanDelete/>
```

 <span data-ttu-id="459ed-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="459ed-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="459ed-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="459ed-106">Attributes and elements</span></span>

<span data-ttu-id="459ed-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="459ed-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="459ed-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="459ed-108">Attributes</span></span>

<span data-ttu-id="459ed-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="459ed-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="459ed-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="459ed-110">Child elements</span></span>

<span data-ttu-id="459ed-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="459ed-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="459ed-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="459ed-112">Parent elements</span></span>

|<span data-ttu-id="459ed-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="459ed-113">**Element**</span></span>|<span data-ttu-id="459ed-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="459ed-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="459ed-115">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="459ed-115">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="459ed-116">Contiene información acerca de una carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="459ed-116">Contains information about a managed folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="459ed-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="459ed-117">Text value</span></span>

<span data-ttu-id="459ed-118">Es necesario un valor de texto que representa un valor booleano si este elemento está presente.</span><span class="sxs-lookup"><span data-stu-id="459ed-118">A text value that represents a Boolean value is required if this element is present.</span></span> <span data-ttu-id="459ed-119">Un valor de **true** indica que la carpeta se puede eliminar; un valor de **false** significa que no se puede eliminar la carpeta.</span><span class="sxs-lookup"><span data-stu-id="459ed-119">A value of **true** indicates that the folder can be deleted; a value of **false** means that the folder cannot be deleted.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="459ed-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="459ed-120">Remarks</span></span>

<span data-ttu-id="459ed-121">Para eliminar una carpeta administrada, use la [operación DeleteFolder](deletefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="459ed-121">To delete a managed folder, use the [DeleteFolder operation](deletefolder-operation.md).</span></span>
  
<span data-ttu-id="459ed-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="459ed-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="459ed-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="459ed-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="459ed-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="459ed-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="459ed-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="459ed-125">Schema name</span></span>  <br/> |<span data-ttu-id="459ed-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="459ed-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="459ed-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="459ed-127">Validation file</span></span>  <br/> |<span data-ttu-id="459ed-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="459ed-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="459ed-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="459ed-129">Can be empty</span></span>  <br/> |<span data-ttu-id="459ed-130">Falso</span><span class="sxs-lookup"><span data-stu-id="459ed-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="459ed-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="459ed-131">See also</span></span>



[<span data-ttu-id="459ed-132">Operación CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="459ed-132">CreateManagedFolder operation</span></span>](createmanagedfolder-operation.md)


- [<span data-ttu-id="459ed-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="459ed-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="459ed-134">Eliminar carpetas</span><span class="sxs-lookup"><span data-stu-id="459ed-134">Deleting Folders</span></span>](https://msdn.microsoft.com/library/1958add5-5071-4239-adb2-40f7a7d74aee%28Office.15%29.aspx)

