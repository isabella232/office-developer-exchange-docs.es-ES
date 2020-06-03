---
title: Atribución (PersonaAttributionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dc59e17e-baea-4617-8ca1-4382a89de0d7
description: El elemento de atribución especifica una instancia en una matriz de atributos para un elemento PersonaType.
ms.openlocfilehash: 05b0d41c116f2ed7b8dbb3ac44108bb879256b5c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464178"
---
# <a name="attribution-personaattributiontype"></a><span data-ttu-id="d7e3e-103">Atribución (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="d7e3e-103">Attribution (PersonaAttributionType)</span></span>

<span data-ttu-id="d7e3e-104">El elemento de **atribución** especifica una instancia en una matriz de atributos para un elemento **PersonaType** .</span><span class="sxs-lookup"><span data-stu-id="d7e3e-104">The **Attribution** element specifies an instance in an array of attributes for a **PersonaType** element.</span></span> 
  
```XML
<Attribution>
    <Id></Id>
    <SourceId></SourceId>
    <DisplayName></DisplayName>
    <IsWritable></IsWritable>
    <IsQuickContact></IsQuickContact>
    <IsHidden></IsHidden>
    <FolderId></FolderId>
</Attribution>
```

 <span data-ttu-id="d7e3e-105">**PersonaAttributionType**</span><span class="sxs-lookup"><span data-stu-id="d7e3e-105">**PersonaAttributionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d7e3e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d7e3e-106">Attributes and elements</span></span>

<span data-ttu-id="d7e3e-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d7e3e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d7e3e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d7e3e-108">Attributes</span></span>

<span data-ttu-id="d7e3e-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d7e3e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d7e3e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d7e3e-110">Child elements</span></span>

|<span data-ttu-id="d7e3e-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d7e3e-111">**Element**</span></span>|<span data-ttu-id="d7e3e-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d7e3e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d7e3e-113">ID (cadena)</span><span class="sxs-lookup"><span data-stu-id="d7e3e-113">ID (String)</span></span>](id-string.md) <br/> |<span data-ttu-id="d7e3e-114">Especifica una cadena que identifica de forma única una aplicación o una atribución en un rol.</span><span class="sxs-lookup"><span data-stu-id="d7e3e-114">Specifies a string that uniquely identifies an app or an attribution in a persona.</span></span>  <br/> |
|[<span data-ttu-id="d7e3e-115">SourceId</span><span class="sxs-lookup"><span data-stu-id="d7e3e-115">SourceId</span></span>](sourceid.md) <br/> |<span data-ttu-id="d7e3e-116">Especifica el identificador del destinatario de contacto o de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d7e3e-116">Specifies the identifier of the contact or Active Directory recipient.</span></span>  <br/> |
|[<span data-ttu-id="d7e3e-117">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="d7e3e-117">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="d7e3e-118">Define el nombre para mostrar de una carpeta, un contacto, una lista de distribución, un usuario delegado o una regla.</span><span class="sxs-lookup"><span data-stu-id="d7e3e-118">Defines the display name of a folder, contact, distribution list, delegate user, or rule.</span></span>  <br/> |
|[<span data-ttu-id="d7e3e-119">IsWritable</span><span class="sxs-lookup"><span data-stu-id="d7e3e-119">IsWritable</span></span>](iswritable.md) <br/> |<span data-ttu-id="d7e3e-120">Especifica si se puede escribir en el contacto subyacente o en el destinatario de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d7e3e-120">Specifies whether the underlying contact or Active Directory recipient can be written to.</span></span>  <br/> |
|[<span data-ttu-id="d7e3e-121">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="d7e3e-121">IsQuickContact</span></span>](isquickcontact.md) <br/> |<span data-ttu-id="d7e3e-122">Especifica un valor booleano que indica si el contacto subyacente o el destinatario de Active Directory es un contacto rápido.</span><span class="sxs-lookup"><span data-stu-id="d7e3e-122">Specifies a Boolean value that indicates whether the underlying contact or Active Directory recipient is a quick contact.</span></span>  <br/> |
|[<span data-ttu-id="d7e3e-123">IsHidden</span><span class="sxs-lookup"><span data-stu-id="d7e3e-123">IsHidden</span></span>](ishidden.md) <br/> |<span data-ttu-id="d7e3e-124">Contiene un valor booleano que indica si el contacto subyacente o el destinatario de Active Directory se deben ocultar o mostrar como parte del rol.</span><span class="sxs-lookup"><span data-stu-id="d7e3e-124">Contains a Boolean value that indicates whether the underlying contact or Active Directory recipient should be hidden or displayed as part of the persona.</span></span>  <br/> |
|[<span data-ttu-id="d7e3e-125">FolderId</span><span class="sxs-lookup"><span data-stu-id="d7e3e-125">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="d7e3e-126">Contiene el identificador y la clave de cambio de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="d7e3e-126">Contains the identifier and change key of a folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d7e3e-127">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d7e3e-127">Parent elements</span></span>

|<span data-ttu-id="d7e3e-128">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d7e3e-128">**Element**</span></span>|<span data-ttu-id="d7e3e-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d7e3e-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d7e3e-130">Atribuciones (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="d7e3e-130">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md) <br/> |<span data-ttu-id="d7e3e-131">Especifica una matriz de información de atribución de uno o varios de los contactos o de los destinatarios de Active Directory (AD) agregados al rol asociado.</span><span class="sxs-lookup"><span data-stu-id="d7e3e-131">Specifies an array of attribution information for one or more of the contacts or active directory (AD) recipients aggregated into the associated persona.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7e3e-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d7e3e-132">Remarks</span></span>

<span data-ttu-id="d7e3e-133">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d7e3e-133">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d7e3e-134">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d7e3e-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d7e3e-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d7e3e-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d7e3e-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="d7e3e-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d7e3e-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d7e3e-137">Schema Name</span></span>  <br/> |<span data-ttu-id="d7e3e-138">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="d7e3e-138">Type schema</span></span>  <br/> |
|<span data-ttu-id="d7e3e-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d7e3e-139">Validation File</span></span>  <br/> |<span data-ttu-id="d7e3e-140">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="d7e3e-140">types.xsd</span></span>  <br/> |
|<span data-ttu-id="d7e3e-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d7e3e-141">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="d7e3e-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7e3e-142">See also</span></span>

- [<span data-ttu-id="d7e3e-143">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d7e3e-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

