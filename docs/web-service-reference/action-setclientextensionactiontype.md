---
title: Acción (SetClientExtensionActionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c5624a87-3436-40ce-8d6b-cc01eecab64d
description: El elemento Action contiene la acción que el servidor Exchange debe realizar en una aplicación.
ms.openlocfilehash: 29579e26377edacb5fb0bb8406144eeb116b8d15
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529689"
---
# <a name="action-setclientextensionactiontype"></a><span data-ttu-id="646d8-103">Acción (SetClientExtensionActionType)</span><span class="sxs-lookup"><span data-stu-id="646d8-103">Action (SetClientExtensionActionType)</span></span>

<span data-ttu-id="646d8-104">El elemento **Action** contiene la acción que el servidor Exchange debe realizar en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="646d8-104">The **Action** element contains the action that the Exchange server should take on an app.</span></span> 
  
```XML
<Action ActionId="" ExtensionId="">
   <ClientExtension/>
</Action>
```

 <span data-ttu-id="646d8-105">**SetClientExtensionActionType**</span><span class="sxs-lookup"><span data-stu-id="646d8-105">**SetClientExtensionActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="646d8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="646d8-106">Attributes and elements</span></span>

<span data-ttu-id="646d8-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="646d8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="646d8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="646d8-108">Attributes</span></span>

|<span data-ttu-id="646d8-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="646d8-109">**Attribute**</span></span>|<span data-ttu-id="646d8-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="646d8-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="646d8-111">ActionId</span><span class="sxs-lookup"><span data-stu-id="646d8-111">ActionId</span></span>  <br/> |<span data-ttu-id="646d8-112">Especifica el identificador de la acción.</span><span class="sxs-lookup"><span data-stu-id="646d8-112">Specifies the identifier of the action.</span></span> <span data-ttu-id="646d8-113">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="646d8-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="646d8-114">ExtensionId</span><span class="sxs-lookup"><span data-stu-id="646d8-114">ExtensionId</span></span>  <br/> |<span data-ttu-id="646d8-115">Especifica el identificador de la extensión.</span><span class="sxs-lookup"><span data-stu-id="646d8-115">Specifies the identifier of the extension.</span></span> <span data-ttu-id="646d8-116">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="646d8-116">This attribute is optional.</span></span>  <br/> |
   
#### <a name="actionid"></a><span data-ttu-id="646d8-117">ActionId</span><span class="sxs-lookup"><span data-stu-id="646d8-117">ActionId</span></span>

|<span data-ttu-id="646d8-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="646d8-118">**Value**</span></span>|<span data-ttu-id="646d8-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="646d8-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="646d8-120">Configurar</span><span class="sxs-lookup"><span data-stu-id="646d8-120">Configure</span></span>  <br/> |<span data-ttu-id="646d8-121">Indica una acción de configuración.</span><span class="sxs-lookup"><span data-stu-id="646d8-121">Indicates a configuration action.</span></span>  <br/> |
|<span data-ttu-id="646d8-122">Instalar</span><span class="sxs-lookup"><span data-stu-id="646d8-122">Install</span></span>  <br/> |<span data-ttu-id="646d8-123">Indica una acción de instalación.</span><span class="sxs-lookup"><span data-stu-id="646d8-123">Indicates an installation action.</span></span>  <br/> |
|<span data-ttu-id="646d8-124">Uninstall</span><span class="sxs-lookup"><span data-stu-id="646d8-124">Uninstall</span></span>  <br/> |<span data-ttu-id="646d8-125">Indica una acción de desinstalación.</span><span class="sxs-lookup"><span data-stu-id="646d8-125">Indicates an uninstallation action.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="646d8-126">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="646d8-126">Child elements</span></span>

|<span data-ttu-id="646d8-127">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="646d8-127">**Element**</span></span>|<span data-ttu-id="646d8-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="646d8-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="646d8-129">ClientExtension</span><span class="sxs-lookup"><span data-stu-id="646d8-129">ClientExtension</span></span>](clientextension.md) <br/> |<span data-ttu-id="646d8-130">Contiene la información de usuario y configuración de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="646d8-130">Contains user and configuration information about an app.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="646d8-131">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="646d8-131">Parent elements</span></span>

|<span data-ttu-id="646d8-132">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="646d8-132">**Element**</span></span>|<span data-ttu-id="646d8-133">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="646d8-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="646d8-134">Acciones (ArrayOfSetClientExtensionActionsType)</span><span class="sxs-lookup"><span data-stu-id="646d8-134">Actions (ArrayOfSetClientExtensionActionsType)</span></span>](actions-arrayofsetclientextensionactionstype.md) <br/> |<span data-ttu-id="646d8-135">Especifica una matriz de elementos **Action** .</span><span class="sxs-lookup"><span data-stu-id="646d8-135">Specifies an array of **Action** elements.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="646d8-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="646d8-136">Remarks</span></span>

<span data-ttu-id="646d8-137">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="646d8-137">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="646d8-138">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="646d8-138">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="646d8-139">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="646d8-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="646d8-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="646d8-140">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="646d8-141">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="646d8-141">Schema Name</span></span>  <br/> |<span data-ttu-id="646d8-142">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="646d8-142">Type schema</span></span>  <br/> |
|<span data-ttu-id="646d8-143">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="646d8-143">Validation File</span></span>  <br/> |<span data-ttu-id="646d8-144">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="646d8-144">types.xsd</span></span>  <br/> |
|<span data-ttu-id="646d8-145">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="646d8-145">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="646d8-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="646d8-146">See also</span></span>

- [<span data-ttu-id="646d8-147">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="646d8-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

