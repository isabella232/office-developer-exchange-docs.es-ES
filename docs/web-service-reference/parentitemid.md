---
title: ParentItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ParentItemId
api_type:
- schema
ms.assetid: 72dc4391-72db-44d2-85d9-4718d59886a7
description: El elemento ParentItemId identifica el elemento primario que contiene vínculos a los datos adjuntos asociados.
ms.openlocfilehash: 9bd875ee5ead8b87996288a640e1bb14e3a5e8b8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836703"
---
# <a name="parentitemid"></a><span data-ttu-id="cd05e-103">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="cd05e-103">ParentItemId</span></span>

<span data-ttu-id="cd05e-104">El elemento **ParentItemId** identifica el elemento primario que contiene vínculos a los datos adjuntos asociados.</span><span class="sxs-lookup"><span data-stu-id="cd05e-104">The **ParentItemId** element identifies the parent item that links to an associated attachment.</span></span> 
  
- [<span data-ttu-id="cd05e-105">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="cd05e-105">CreateAttachment</span></span>](createattachment.md)
  
- [<span data-ttu-id="cd05e-106">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="cd05e-106">ParentItemId</span></span>](parentitemid.md)
  
```xml
<ParentItemId Id="" ChangeKey="" />
```

<span data-ttu-id="cd05e-107">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="cd05e-107">**ItemIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="cd05e-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cd05e-108">Attributes and elements</span></span>

<span data-ttu-id="cd05e-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cd05e-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cd05e-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="cd05e-110">Attributes</span></span>

|<span data-ttu-id="cd05e-111">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="cd05e-111">**Attribute**</span></span>|<span data-ttu-id="cd05e-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cd05e-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd05e-113">**Id**</span><span class="sxs-lookup"><span data-stu-id="cd05e-113">**Id**</span></span> <br/> |<span data-ttu-id="cd05e-114">Identifica un elemento único en el almacén de Exchange para asociar con datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="cd05e-114">Identifies a single item in the Exchange store to associate with an attachment.</span></span> <span data-ttu-id="cd05e-115">Este valor es una cadena.</span><span class="sxs-lookup"><span data-stu-id="cd05e-115">This value is a string.</span></span> <span data-ttu-id="cd05e-116">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="cd05e-116">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="cd05e-117">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="cd05e-117">**ChangeKey**</span></span> <br/> |<span data-ttu-id="cd05e-118">Identifica una versión de un elemento que se identifica con el atributo **Id** en el almacén de Exchange no especificada.</span><span class="sxs-lookup"><span data-stu-id="cd05e-118">Identifies an unspecified version of an item that is identified by the **Id** attribute in the Exchange store.</span></span> <span data-ttu-id="cd05e-119">Esto se usa para asegurarse de que un elemento actual se usa cuando se actualizan con datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="cd05e-119">This is used to make sure that a current item is used when it is updated with an attachment.</span></span> <span data-ttu-id="cd05e-120">Este valor es una cadena.</span><span class="sxs-lookup"><span data-stu-id="cd05e-120">This value is a string.</span></span> <span data-ttu-id="cd05e-121">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="cd05e-121">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cd05e-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cd05e-122">Child elements</span></span>

<span data-ttu-id="cd05e-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cd05e-123">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cd05e-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cd05e-124">Parent elements</span></span>

|<span data-ttu-id="cd05e-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="cd05e-125">**Element**</span></span>|<span data-ttu-id="cd05e-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cd05e-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cd05e-127">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="cd05e-127">CreateAttachment</span></span>](createattachment.md) <br/> |<span data-ttu-id="cd05e-128">Define una solicitud para crear un archivo adjunto a un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="cd05e-128">Defines a request to create an attachment to an item in a mailbox.</span></span>  <br/> <span data-ttu-id="cd05e-129">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="cd05e-129">The following is the XPath expression to this element:</span></span>  <br/>  `/CreateAttachment` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd05e-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cd05e-130">Remarks</span></span>

<span data-ttu-id="cd05e-131">Este elemento es necesario en la [operación CreateAttachment](createattachment-operation.md).</span><span class="sxs-lookup"><span data-stu-id="cd05e-131">This element is required in the [CreateAttachment operation](createattachment-operation.md).</span></span> <span data-ttu-id="cd05e-132">Este elemento es básicamente el mismo que el elemento [ItemId](itemid.md) .</span><span class="sxs-lookup"><span data-stu-id="cd05e-132">This element is basically the same as the [ItemId](itemid.md) element.</span></span> 
  
<span data-ttu-id="cd05e-133">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="cd05e-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cd05e-134">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cd05e-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cd05e-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cd05e-135">Namespace</span></span>  <br/> |[http://schemas.microsoft.com/exchange/services/2006/messages](http://schemas.microsoft.com/exchange/services/2006/messages) <br/> |
|<span data-ttu-id="cd05e-136">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cd05e-136">Schema Name</span></span>  <br/> |<span data-ttu-id="cd05e-137">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="cd05e-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cd05e-138">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cd05e-138">Validation File</span></span>  <br/> |<span data-ttu-id="cd05e-139">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cd05e-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cd05e-140">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cd05e-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="cd05e-141">False</span><span class="sxs-lookup"><span data-stu-id="cd05e-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cd05e-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd05e-142">See also</span></span>

- [<span data-ttu-id="cd05e-143">Operación CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="cd05e-143">CreateAttachment operation</span></span>](createattachment-operation.md)

