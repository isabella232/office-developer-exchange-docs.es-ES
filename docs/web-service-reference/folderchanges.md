---
title: FolderChanges
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderChanges
api_type:
- schema
ms.assetid: d3f611ed-56a4-43f8-aa65-cbd7844b827f
description: El elemento FolderChanges representa una colección de cambios para una carpeta.
ms.openlocfilehash: 5481496100512584fd0b9745ee42d5b9516bd7fb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458386"
---
# <a name="folderchanges"></a><span data-ttu-id="99054-103">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="99054-103">FolderChanges</span></span>

<span data-ttu-id="99054-104">El elemento **FolderChanges** representa una colección de cambios para una carpeta.</span><span class="sxs-lookup"><span data-stu-id="99054-104">The **FolderChanges** element represents a collection of changes for a folder.</span></span> 
  
[<span data-ttu-id="99054-105">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="99054-105">UpdateFolder</span></span>](updatefolder.md)
  
[<span data-ttu-id="99054-106">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="99054-106">FolderChanges</span></span>](folderchanges.md)
  
```xml
<FolderChanges>
   <FolderChange/>
</FolderChanges>
```

 <span data-ttu-id="99054-107">**NonEmptyArrayOfFolderChangesType**</span><span class="sxs-lookup"><span data-stu-id="99054-107">**NonEmptyArrayOfFolderChangesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="99054-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="99054-108">Attributes and elements</span></span>

<span data-ttu-id="99054-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="99054-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="99054-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="99054-110">Attributes</span></span>

<span data-ttu-id="99054-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="99054-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="99054-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="99054-112">Child elements</span></span>

|<span data-ttu-id="99054-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="99054-113">**Element**</span></span>|<span data-ttu-id="99054-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="99054-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="99054-115">FolderChange</span><span class="sxs-lookup"><span data-stu-id="99054-115">FolderChange</span></span>](folderchange.md) <br/> |<span data-ttu-id="99054-116">Representa un único cambio que se realizará en una sola carpeta.</span><span class="sxs-lookup"><span data-stu-id="99054-116">Represents a single change to be performed on a single folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="99054-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="99054-117">Parent elements</span></span>

|<span data-ttu-id="99054-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="99054-118">**Element**</span></span>|<span data-ttu-id="99054-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="99054-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="99054-120">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="99054-120">UpdateFolder</span></span>](updatefolder.md) <br/> |<span data-ttu-id="99054-121">Representa la operación que se usa para actualizar las propiedades de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="99054-121">Represents the operation that is used to update properties for a folder.</span></span>  <br/> <span data-ttu-id="99054-122">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="99054-122">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateFolder` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99054-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="99054-123">Remarks</span></span>

<span data-ttu-id="99054-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="99054-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="99054-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="99054-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="99054-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="99054-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="99054-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="99054-127">Schema Name</span></span>  <br/> |<span data-ttu-id="99054-128">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="99054-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="99054-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="99054-129">Validation File</span></span>  <br/> |<span data-ttu-id="99054-130">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="99054-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="99054-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="99054-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="99054-132">Falso</span><span class="sxs-lookup"><span data-stu-id="99054-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="99054-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="99054-133">See also</span></span>



[<span data-ttu-id="99054-134">Operación UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="99054-134">UpdateFolder operation</span></span>](updatefolder-operation.md)

