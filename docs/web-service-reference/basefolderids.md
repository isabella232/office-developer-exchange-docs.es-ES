---
title: BaseFolderIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BaseFolderIds
api_type:
- schema
ms.assetid: bdaa6093-f960-469a-b338-0e75aaa536c6
description: El elemento BaseFolderIds representa la colección de carpetas que se extraídos para determinar el contenido de una carpeta de búsqueda.
ms.openlocfilehash: 960e4d9c1d6eb37bf988bf163e696cbba3e1ef6f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763598"
---
# <a name="basefolderids"></a><span data-ttu-id="38e07-103">BaseFolderIds</span><span class="sxs-lookup"><span data-stu-id="38e07-103">BaseFolderIds</span></span>

<span data-ttu-id="38e07-104">El elemento **BaseFolderIds** representa la colección de carpetas que se extraídos para determinar el contenido de una carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="38e07-104">The **BaseFolderIds** element represents the collection of folders that will be mined to determine the contents of a search folder.</span></span> 
  
```xml
<BaseFolderIds>
   <FolderId/>
   <DistinguishedFolderId/>
</BaseFolderIds>
```

 <span data-ttu-id="38e07-105">**NonEmptyArrayOfBaseFolderIdsType**</span><span class="sxs-lookup"><span data-stu-id="38e07-105">**NonEmptyArrayOfBaseFolderIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="38e07-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="38e07-106">Attributes and elements</span></span>

<span data-ttu-id="38e07-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="38e07-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="38e07-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="38e07-108">Attributes</span></span>

<span data-ttu-id="38e07-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="38e07-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="38e07-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="38e07-110">Child elements</span></span>

|<span data-ttu-id="38e07-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="38e07-111">**Element**</span></span>|<span data-ttu-id="38e07-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="38e07-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="38e07-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="38e07-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="38e07-114">Contiene el identificador y cambiar la clave de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="38e07-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="38e07-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="38e07-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="38e07-116">Identifica las carpetas de MicrosoftExchange Server 2007 que se pueden hacer referencia por su nombre.</span><span class="sxs-lookup"><span data-stu-id="38e07-116">Identifies MicrosoftExchange Server 2007 folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="38e07-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="38e07-117">Parent elements</span></span>

|<span data-ttu-id="38e07-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="38e07-118">**Element**</span></span>|<span data-ttu-id="38e07-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="38e07-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="38e07-120">SearchParameters</span><span class="sxs-lookup"><span data-stu-id="38e07-120">SearchParameters</span></span>](searchparameters.md) <br/> |<span data-ttu-id="38e07-121">Representa los parámetros que definen una carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="38e07-121">Represents the parameters that define a search folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38e07-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="38e07-122">Remarks</span></span>

<span data-ttu-id="38e07-123">El elemento **BaseFolderIds** debe contener al menos un elemento [FolderId](folderid.md) o [DistinguishedFolderId](distinguishedfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="38e07-123">The **BaseFolderIds** element must contain at least one [FolderId](folderid.md) or [DistinguishedFolderId](distinguishedfolderid.md) element.</span></span> 
  
<span data-ttu-id="38e07-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="38e07-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="38e07-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="38e07-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="38e07-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="38e07-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="38e07-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="38e07-127">Schema name</span></span>  <br/> |<span data-ttu-id="38e07-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="38e07-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="38e07-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="38e07-129">Validation file</span></span>  <br/> |<span data-ttu-id="38e07-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="38e07-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="38e07-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="38e07-131">Can be empty</span></span>  <br/> |<span data-ttu-id="38e07-132">False</span><span class="sxs-lookup"><span data-stu-id="38e07-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="38e07-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="38e07-133">See also</span></span>



- [<span data-ttu-id="38e07-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="38e07-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

