---
title: Atribución (PersonaAttributionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dc59e17e-baea-4617-8ca1-4382a89de0d7
description: El elemento de atribución especifica una instancia de una matriz de atributos para un elemento PersonaType.
ms.openlocfilehash: 0e800c92c75bf0c475d4bffd33d6ab49f9ad9a9a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763581"
---
# <a name="attribution-personaattributiontype"></a><span data-ttu-id="61c5a-103">Atribución (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="61c5a-103">Attribution (PersonaAttributionType)</span></span>

<span data-ttu-id="61c5a-104">El elemento de **atribución** especifica una instancia de una matriz de atributos para un elemento **PersonaType** .</span><span class="sxs-lookup"><span data-stu-id="61c5a-104">The **Attribution** element specifies an instance in an array of attributes for a **PersonaType** element.</span></span> 
  
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

 <span data-ttu-id="61c5a-105">**PersonaAttributionType**</span><span class="sxs-lookup"><span data-stu-id="61c5a-105">**PersonaAttributionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="61c5a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="61c5a-106">Attributes and elements</span></span>

<span data-ttu-id="61c5a-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="61c5a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="61c5a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="61c5a-108">Attributes</span></span>

<span data-ttu-id="61c5a-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="61c5a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="61c5a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="61c5a-110">Child elements</span></span>

|<span data-ttu-id="61c5a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="61c5a-111">**Element**</span></span>|<span data-ttu-id="61c5a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="61c5a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="61c5a-113">Identificador (cadena)</span><span class="sxs-lookup"><span data-stu-id="61c5a-113">ID (String)</span></span>](id-string.md) <br/> |<span data-ttu-id="61c5a-114">Especifica una cadena que identifica de forma exclusiva una aplicación o una atribución en un rol.</span><span class="sxs-lookup"><span data-stu-id="61c5a-114">Specifies a string that uniquely identifies an app or an attribution in a persona.</span></span>  <br/> |
|[<span data-ttu-id="61c5a-115">SourceId</span><span class="sxs-lookup"><span data-stu-id="61c5a-115">SourceId</span></span>](sourceid.md) <br/> |<span data-ttu-id="61c5a-116">Especifica el identificador del contacto o destinatario de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="61c5a-116">Specifies the identifier of the contact or Active Directory recipient.</span></span>  <br/> |
|[<span data-ttu-id="61c5a-117">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="61c5a-117">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="61c5a-118">Define el nombre para mostrar de una carpeta, contacto, lista de distribución, usuario delegado o regla.</span><span class="sxs-lookup"><span data-stu-id="61c5a-118">Defines the display name of a folder, contact, distribution list, delegate user, or rule.</span></span>  <br/> |
|[<span data-ttu-id="61c5a-119">IsWritable</span><span class="sxs-lookup"><span data-stu-id="61c5a-119">IsWritable</span></span>](iswritable.md) <br/> |<span data-ttu-id="61c5a-120">Especifica si se puede escribir en el contacto subyacente o el destinatario de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="61c5a-120">Specifies whether the underlying contact or Active Directory recipient can be written to.</span></span>  <br/> |
|[<span data-ttu-id="61c5a-121">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="61c5a-121">IsQuickContact</span></span>](isquickcontact.md) <br/> |<span data-ttu-id="61c5a-122">Especifica un valor booleano que indica si el contacto subyacente o el destinatario de Active Directory es un contacto rápido.</span><span class="sxs-lookup"><span data-stu-id="61c5a-122">Specifies a Boolean value that indicates whether the underlying contact or Active Directory recipient is a quick contact.</span></span>  <br/> |
|[<span data-ttu-id="61c5a-123">IsHidden</span><span class="sxs-lookup"><span data-stu-id="61c5a-123">IsHidden</span></span>](ishidden.md) <br/> |<span data-ttu-id="61c5a-124">Contiene un valor booleano que indica si el contacto subyacente o el destinatario de Active Directory debe ser oculto o que se muestra como parte del rol.</span><span class="sxs-lookup"><span data-stu-id="61c5a-124">Contains a Boolean value that indicates whether the underlying contact or Active Directory recipient should be hidden or displayed as part of the persona.</span></span>  <br/> |
|[<span data-ttu-id="61c5a-125">FolderId</span><span class="sxs-lookup"><span data-stu-id="61c5a-125">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="61c5a-126">Contiene el identificador y cambiar la clave de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="61c5a-126">Contains the identifier and change key of a folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="61c5a-127">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="61c5a-127">Parent elements</span></span>

|<span data-ttu-id="61c5a-128">**Element**</span><span class="sxs-lookup"><span data-stu-id="61c5a-128">**Element**</span></span>|<span data-ttu-id="61c5a-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="61c5a-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="61c5a-130">Atribuciones (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="61c5a-130">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md) <br/> |<span data-ttu-id="61c5a-131">Especifica una matriz de información de atribución para uno o varios de los contactos o los destinatarios de active directory (AD) agregados a la persona asociada.</span><span class="sxs-lookup"><span data-stu-id="61c5a-131">Specifies an array of attribution information for one or more of the contacts or active directory (AD) recipients aggregated into the associated persona.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61c5a-132">Notas</span><span class="sxs-lookup"><span data-stu-id="61c5a-132">Remarks</span></span>

<span data-ttu-id="61c5a-133">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="61c5a-133">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="61c5a-134">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="61c5a-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="61c5a-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="61c5a-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61c5a-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="61c5a-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="61c5a-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="61c5a-137">Schema Name</span></span>  <br/> |<span data-ttu-id="61c5a-138">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="61c5a-138">Type schema</span></span>  <br/> |
|<span data-ttu-id="61c5a-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="61c5a-139">Validation File</span></span>  <br/> |<span data-ttu-id="61c5a-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="61c5a-140">types.xsd</span></span>  <br/> |
|<span data-ttu-id="61c5a-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="61c5a-141">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="61c5a-142">Ver también</span><span class="sxs-lookup"><span data-stu-id="61c5a-142">See also</span></span>

- [<span data-ttu-id="61c5a-143">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="61c5a-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

