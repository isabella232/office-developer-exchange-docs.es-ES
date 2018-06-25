---
title: FolderClass
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderClass
api_type:
- schema
ms.assetid: 0041d135-2869-4612-89a5-d1aa86aa1093
description: El elemento FolderClass representa la clase de carpeta para una carpeta.
ms.openlocfilehash: 87be00563d0375abebf32159ff38d62d03112b95
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764674"
---
# <a name="folderclass"></a><span data-ttu-id="657c1-103">FolderClass</span><span class="sxs-lookup"><span data-stu-id="657c1-103">FolderClass</span></span>

<span data-ttu-id="657c1-104">El elemento **FolderClass** representa la clase de carpeta para una carpeta.</span><span class="sxs-lookup"><span data-stu-id="657c1-104">The **FolderClass** element represents the folder class for a folder.</span></span> 
  
```xml
<FolderClass/>
```

 <span data-ttu-id="657c1-105">**string**</span><span class="sxs-lookup"><span data-stu-id="657c1-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="657c1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="657c1-106">Attributes and elements</span></span>

<span data-ttu-id="657c1-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="657c1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="657c1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="657c1-108">Attributes</span></span>

<span data-ttu-id="657c1-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="657c1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="657c1-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="657c1-110">Child elements</span></span>

<span data-ttu-id="657c1-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="657c1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="657c1-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="657c1-112">Parent elements</span></span>

|<span data-ttu-id="657c1-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="657c1-113">**Element**</span></span>|<span data-ttu-id="657c1-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="657c1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="657c1-115">Folder</span><span class="sxs-lookup"><span data-stu-id="657c1-115">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="657c1-116">Representa una carpeta en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="657c1-116">Represents a folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="657c1-117">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="657c1-117">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="657c1-118">Representa una carpeta del calendario en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="657c1-118">Represents a calendar folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="657c1-119">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="657c1-119">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="657c1-120">Representa una carpeta de contactos en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="657c1-120">Represents a contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="657c1-121">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="657c1-121">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="657c1-122">Representa una carpeta de búsqueda en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="657c1-122">Represents a search folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="657c1-123">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="657c1-123">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="657c1-124">Representa una carpeta de tareas en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="657c1-124">Represents a task folder in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="657c1-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="657c1-125">Text value</span></span>

<span data-ttu-id="657c1-126">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="657c1-126">A text value is required.</span></span> <span data-ttu-id="657c1-127">Las clases de carpeta suelen comenzar con "IPF".</span><span class="sxs-lookup"><span data-stu-id="657c1-127">Folder classes typically start with "IPF."</span></span>
  
## <a name="remarks"></a><span data-ttu-id="657c1-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="657c1-128">Remarks</span></span>

<span data-ttu-id="657c1-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="657c1-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="657c1-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="657c1-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="657c1-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="657c1-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="657c1-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="657c1-132">Schema Name</span></span>  <br/> |<span data-ttu-id="657c1-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="657c1-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="657c1-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="657c1-134">Validation File</span></span>  <br/> |<span data-ttu-id="657c1-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="657c1-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="657c1-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="657c1-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="657c1-137">False</span><span class="sxs-lookup"><span data-stu-id="657c1-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="657c1-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="657c1-138">See also</span></span>



- [<span data-ttu-id="657c1-139">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="657c1-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

