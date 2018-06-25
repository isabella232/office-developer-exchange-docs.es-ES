---
title: Acción (SetClientExtensionActionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c5624a87-3436-40ce-8d6b-cc01eecab64d
description: El elemento de acción contiene la acción que debe realizar el servidor de Exchange en una aplicación.
ms.openlocfilehash: a231cedfa6e4759dabfcbecfbe9a9b851f834247
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763389"
---
# <a name="action-setclientextensionactiontype"></a><span data-ttu-id="c2432-103">Acción (SetClientExtensionActionType)</span><span class="sxs-lookup"><span data-stu-id="c2432-103">Action (SetClientExtensionActionType)</span></span>

<span data-ttu-id="c2432-104">El elemento de **acción** contiene la acción que debe realizar el servidor de Exchange en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="c2432-104">The **Action** element contains the action that the Exchange server should take on an app.</span></span> 
  
```XML
<Action ActionId="" ExtensionId="">
   <ClientExtension/>
</Action>
```

 <span data-ttu-id="c2432-105">**SetClientExtensionActionType**</span><span class="sxs-lookup"><span data-stu-id="c2432-105">**SetClientExtensionActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c2432-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c2432-106">Attributes and elements</span></span>

<span data-ttu-id="c2432-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c2432-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c2432-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c2432-108">Attributes</span></span>

|<span data-ttu-id="c2432-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="c2432-109">**Attribute**</span></span>|<span data-ttu-id="c2432-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c2432-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c2432-111">ActionId</span><span class="sxs-lookup"><span data-stu-id="c2432-111">ActionId</span></span>  <br/> |<span data-ttu-id="c2432-112">Especifica el identificador de la acción.</span><span class="sxs-lookup"><span data-stu-id="c2432-112">Specifies the identifier of the action.</span></span> <span data-ttu-id="c2432-113">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="c2432-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="c2432-114">ExtensionId</span><span class="sxs-lookup"><span data-stu-id="c2432-114">ExtensionId</span></span>  <br/> |<span data-ttu-id="c2432-115">Especifica el identificador de la extensión.</span><span class="sxs-lookup"><span data-stu-id="c2432-115">Specifies the identifier of the extension.</span></span> <span data-ttu-id="c2432-116">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="c2432-116">This attribute is optional.</span></span>  <br/> |
   
#### <a name="actionid"></a><span data-ttu-id="c2432-117">ActionId</span><span class="sxs-lookup"><span data-stu-id="c2432-117">ActionId</span></span>

|<span data-ttu-id="c2432-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c2432-118">**Value**</span></span>|<span data-ttu-id="c2432-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c2432-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c2432-120">Configurar</span><span class="sxs-lookup"><span data-stu-id="c2432-120">Configure</span></span>  <br/> |<span data-ttu-id="c2432-121">Indica una acción de configuración.</span><span class="sxs-lookup"><span data-stu-id="c2432-121">Indicates a configuration action.</span></span>  <br/> |
|<span data-ttu-id="c2432-122">Instalar</span><span class="sxs-lookup"><span data-stu-id="c2432-122">Install</span></span>  <br/> |<span data-ttu-id="c2432-123">Indica una acción de instalación.</span><span class="sxs-lookup"><span data-stu-id="c2432-123">Indicates an installation action.</span></span>  <br/> |
|<span data-ttu-id="c2432-124">Desinstalar</span><span class="sxs-lookup"><span data-stu-id="c2432-124">Uninstall</span></span>  <br/> |<span data-ttu-id="c2432-125">Indica una acción de desinstalación.</span><span class="sxs-lookup"><span data-stu-id="c2432-125">Indicates an uninstallation action.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c2432-126">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c2432-126">Child elements</span></span>

|<span data-ttu-id="c2432-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="c2432-127">**Element**</span></span>|<span data-ttu-id="c2432-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c2432-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c2432-129">ClientExtension</span><span class="sxs-lookup"><span data-stu-id="c2432-129">ClientExtension</span></span>](clientextension.md) <br/> |<span data-ttu-id="c2432-130">Contiene información de usuario y de configuración sobre una aplicación.</span><span class="sxs-lookup"><span data-stu-id="c2432-130">Contains user and configuration information about an app.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c2432-131">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c2432-131">Parent elements</span></span>

|<span data-ttu-id="c2432-132">**Element**</span><span class="sxs-lookup"><span data-stu-id="c2432-132">**Element**</span></span>|<span data-ttu-id="c2432-133">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c2432-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c2432-134">Acciones (ArrayOfSetClientExtensionActionsType)</span><span class="sxs-lookup"><span data-stu-id="c2432-134">Actions (ArrayOfSetClientExtensionActionsType)</span></span>](actions-arrayofsetclientextensionactionstype.md) <br/> |<span data-ttu-id="c2432-135">Especifica una matriz de elementos de **acción** .</span><span class="sxs-lookup"><span data-stu-id="c2432-135">Specifies an array of **Action** elements.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2432-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c2432-136">Remarks</span></span>

<span data-ttu-id="c2432-137">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c2432-137">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c2432-138">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c2432-138">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c2432-139">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c2432-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c2432-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c2432-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c2432-141">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c2432-141">Schema Name</span></span>  <br/> |<span data-ttu-id="c2432-142">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="c2432-142">Type schema</span></span>  <br/> |
|<span data-ttu-id="c2432-143">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c2432-143">Validation File</span></span>  <br/> |<span data-ttu-id="c2432-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c2432-144">types.xsd</span></span>  <br/> |
|<span data-ttu-id="c2432-145">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c2432-145">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="c2432-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2432-146">See also</span></span>

- [<span data-ttu-id="c2432-147">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c2432-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

