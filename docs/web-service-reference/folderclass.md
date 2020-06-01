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
description: El elemento FolderClass representa la clase de carpeta de una carpeta.
ms.openlocfilehash: ee5d382251a66ab5fbcd8054e6b5cfac82b5f994
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460060"
---
# <a name="folderclass"></a><span data-ttu-id="8443e-103">FolderClass</span><span class="sxs-lookup"><span data-stu-id="8443e-103">FolderClass</span></span>

<span data-ttu-id="8443e-104">El elemento **FolderClass** representa la clase de carpeta de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="8443e-104">The **FolderClass** element represents the folder class for a folder.</span></span> 
  
```xml
<FolderClass/>
```

 <span data-ttu-id="8443e-105">**string**</span><span class="sxs-lookup"><span data-stu-id="8443e-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8443e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8443e-106">Attributes and elements</span></span>

<span data-ttu-id="8443e-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8443e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8443e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8443e-108">Attributes</span></span>

<span data-ttu-id="8443e-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8443e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8443e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8443e-110">Child elements</span></span>

<span data-ttu-id="8443e-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8443e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8443e-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8443e-112">Parent elements</span></span>

|<span data-ttu-id="8443e-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8443e-113">**Element**</span></span>|<span data-ttu-id="8443e-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8443e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8443e-115">Folder</span><span class="sxs-lookup"><span data-stu-id="8443e-115">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="8443e-116">Representa una carpeta en un buzón.</span><span class="sxs-lookup"><span data-stu-id="8443e-116">Represents a folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="8443e-117">Hubiera</span><span class="sxs-lookup"><span data-stu-id="8443e-117">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="8443e-118">Representa una carpeta de calendario en un buzón.</span><span class="sxs-lookup"><span data-stu-id="8443e-118">Represents a calendar folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="8443e-119">Hubiera</span><span class="sxs-lookup"><span data-stu-id="8443e-119">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="8443e-120">Representa una carpeta de contactos en un buzón.</span><span class="sxs-lookup"><span data-stu-id="8443e-120">Represents a contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="8443e-121">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="8443e-121">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="8443e-122">Representa una carpeta de búsqueda en un buzón.</span><span class="sxs-lookup"><span data-stu-id="8443e-122">Represents a search folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="8443e-123">Hubiera</span><span class="sxs-lookup"><span data-stu-id="8443e-123">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="8443e-124">Representa una carpeta de tareas en un buzón.</span><span class="sxs-lookup"><span data-stu-id="8443e-124">Represents a task folder in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8443e-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="8443e-125">Text value</span></span>

<span data-ttu-id="8443e-126">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="8443e-126">A text value is required.</span></span> <span data-ttu-id="8443e-127">Las clases de carpeta normalmente comienzan con "IPF".</span><span class="sxs-lookup"><span data-stu-id="8443e-127">Folder classes typically start with "IPF."</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8443e-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8443e-128">Remarks</span></span>

<span data-ttu-id="8443e-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="8443e-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8443e-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8443e-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8443e-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="8443e-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8443e-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8443e-132">Schema Name</span></span>  <br/> |<span data-ttu-id="8443e-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="8443e-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="8443e-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8443e-134">Validation File</span></span>  <br/> |<span data-ttu-id="8443e-135">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="8443e-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8443e-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8443e-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="8443e-137">Falso</span><span class="sxs-lookup"><span data-stu-id="8443e-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8443e-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="8443e-138">See also</span></span>



- [<span data-ttu-id="8443e-139">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="8443e-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

