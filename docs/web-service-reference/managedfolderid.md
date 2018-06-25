---
title: ManagedFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ManagedFolderId
api_type:
- schema
ms.assetid: 3efb7abb-0e91-4d8a-9fa2-3dec8bd17c30
description: El elemento ManagedFolderId contiene el identificador de la carpeta de la carpeta administrada.
ms.openlocfilehash: acdb69f82678633baff12c46494c39015c36d233
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836340"
---
# <a name="managedfolderid"></a><span data-ttu-id="27749-103">ManagedFolderId</span><span class="sxs-lookup"><span data-stu-id="27749-103">ManagedFolderId</span></span>

<span data-ttu-id="27749-104">El elemento **ManagedFolderId** contiene el identificador de la carpeta de la carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="27749-104">The **ManagedFolderId** element contains the folder ID of the managed folder.</span></span> 
  
```xml
<ManagedFolderId/>
```

 <span data-ttu-id="27749-105">**string**</span><span class="sxs-lookup"><span data-stu-id="27749-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="27749-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="27749-106">Attributes and elements</span></span>

<span data-ttu-id="27749-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="27749-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="27749-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="27749-108">Attributes</span></span>

<span data-ttu-id="27749-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="27749-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="27749-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="27749-110">Child elements</span></span>

<span data-ttu-id="27749-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="27749-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="27749-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="27749-112">Parent elements</span></span>

|<span data-ttu-id="27749-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="27749-113">**Element**</span></span>|<span data-ttu-id="27749-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="27749-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="27749-115">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="27749-115">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="27749-116">Contiene información acerca de una carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="27749-116">Contains information about a managed folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="27749-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="27749-117">Text value</span></span>

<span data-ttu-id="27749-118">Un valor de texto es necesario para este elemento.</span><span class="sxs-lookup"><span data-stu-id="27749-118">A text value is required for this element.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="27749-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="27749-119">Remarks</span></span>

<span data-ttu-id="27749-120">El valor de identificador de **ManagedFolderId** es el equivalente de la propiedad **Guid** que se recupera mediante la `Get-ManagedFolder` comando de Microsoft Windows Powershell.</span><span class="sxs-lookup"><span data-stu-id="27749-120">The **ManagedFolderId** identifier value is the equivalent of the **Guid** property that is retrieved by the  `Get-ManagedFolder` Microsoft Windows Powershell command.</span></span> <span data-ttu-id="27749-121">También es el valor del atributo **GUID de objeto** para la carpeta administrada en el servicio de directorio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="27749-121">It is also the value of the **objectGUID** attribute for the managed folder in the Active Directory directory service.</span></span> 
  
<span data-ttu-id="27749-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="27749-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="27749-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="27749-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="27749-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="27749-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="27749-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="27749-125">Schema name</span></span>  <br/> |<span data-ttu-id="27749-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="27749-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="27749-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="27749-127">Validation file</span></span>  <br/> |<span data-ttu-id="27749-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="27749-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="27749-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="27749-129">Can be empty</span></span>  <br/> |<span data-ttu-id="27749-130">False</span><span class="sxs-lookup"><span data-stu-id="27749-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="27749-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="27749-131">See also</span></span>



[<span data-ttu-id="27749-132">Operación CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="27749-132">CreateManagedFolder operation</span></span>](createmanagedfolder-operation.md)


- [<span data-ttu-id="27749-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="27749-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="27749-134">Eliminación de carpetas</span><span class="sxs-lookup"><span data-stu-id="27749-134">Deleting Folders</span></span>](http://msdn.microsoft.com/library/1958add5-5071-4239-adb2-40f7a7d74aee%28Office.15%29.aspx)
  
[<span data-ttu-id="27749-135">Adición de las carpetas administradas</span><span class="sxs-lookup"><span data-stu-id="27749-135">Adding Managed Folders</span></span>](http://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

