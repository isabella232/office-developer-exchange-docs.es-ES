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
description: El elemento CanDelete indica si se puede eliminar una carpeta administrada por un cliente.
ms.openlocfilehash: b70b28bd6b3c9452f5d7f249f453218d555754da
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763723"
---
# <a name="candelete"></a><span data-ttu-id="a57d6-103">CanDelete</span><span class="sxs-lookup"><span data-stu-id="a57d6-103">CanDelete</span></span>

<span data-ttu-id="a57d6-104">El elemento **CanDelete** indica si se puede eliminar una carpeta administrada por un cliente.</span><span class="sxs-lookup"><span data-stu-id="a57d6-104">The **CanDelete** element indicates whether a managed folder can be deleted by a customer.</span></span> 
  
```xml
<CanDelete/>
```

 <span data-ttu-id="a57d6-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a57d6-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a57d6-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a57d6-106">Attributes and elements</span></span>

<span data-ttu-id="a57d6-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a57d6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a57d6-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a57d6-108">Attributes</span></span>

<span data-ttu-id="a57d6-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a57d6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a57d6-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a57d6-110">Child elements</span></span>

<span data-ttu-id="a57d6-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a57d6-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a57d6-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a57d6-112">Parent elements</span></span>

|<span data-ttu-id="a57d6-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a57d6-113">**Element**</span></span>|<span data-ttu-id="a57d6-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a57d6-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a57d6-115">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="a57d6-115">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="a57d6-116">Contiene información acerca de una carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="a57d6-116">Contains information about a managed folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a57d6-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a57d6-117">Text value</span></span>

<span data-ttu-id="a57d6-118">Si este elemento está presente, se requiere un valor de texto que representa un valor de tipo Boolean.</span><span class="sxs-lookup"><span data-stu-id="a57d6-118">A text value that represents a Boolean value is required if this element is present.</span></span> <span data-ttu-id="a57d6-119">Un valor de **true** indica que se puede eliminar la carpeta; un valor de **false** significa que no se puede eliminar la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a57d6-119">A value of **true** indicates that the folder can be deleted; a value of **false** means that the folder cannot be deleted.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a57d6-120">Notas</span><span class="sxs-lookup"><span data-stu-id="a57d6-120">Remarks</span></span>

<span data-ttu-id="a57d6-121">Para eliminar una carpeta administrada, use la [operación DeleteFolder](deletefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="a57d6-121">To delete a managed folder, use the [DeleteFolder operation](deletefolder-operation.md).</span></span>
  
<span data-ttu-id="a57d6-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="a57d6-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a57d6-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a57d6-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a57d6-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a57d6-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a57d6-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a57d6-125">Schema name</span></span>  <br/> |<span data-ttu-id="a57d6-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a57d6-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="a57d6-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a57d6-127">Validation file</span></span>  <br/> |<span data-ttu-id="a57d6-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a57d6-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a57d6-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a57d6-129">Can be empty</span></span>  <br/> |<span data-ttu-id="a57d6-130">False</span><span class="sxs-lookup"><span data-stu-id="a57d6-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a57d6-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="a57d6-131">See also</span></span>



[<span data-ttu-id="a57d6-132">Operación CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="a57d6-132">CreateManagedFolder operation</span></span>](createmanagedfolder-operation.md)


- [<span data-ttu-id="a57d6-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="a57d6-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="a57d6-134">Eliminación de carpetas</span><span class="sxs-lookup"><span data-stu-id="a57d6-134">Deleting Folders</span></span>](http://msdn.microsoft.com/library/1958add5-5071-4239-adb2-40f7a7d74aee%28Office.15%29.aspx)

