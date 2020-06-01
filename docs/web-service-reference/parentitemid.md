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
description: El elemento ParentItemId identifica el elemento primario que se vincula a un dato adjunto asociado.
ms.openlocfilehash: 4f3e33da0af2438948313f0e335cd03e076d135a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465747"
---
# <a name="parentitemid"></a><span data-ttu-id="08ff1-103">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="08ff1-103">ParentItemId</span></span>

<span data-ttu-id="08ff1-104">El elemento **ParentItemId** identifica el elemento primario que se vincula a un dato adjunto asociado.</span><span class="sxs-lookup"><span data-stu-id="08ff1-104">The **ParentItemId** element identifies the parent item that links to an associated attachment.</span></span> 
  
- [<span data-ttu-id="08ff1-105">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="08ff1-105">CreateAttachment</span></span>](createattachment.md)
  
- [<span data-ttu-id="08ff1-106">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="08ff1-106">ParentItemId</span></span>](parentitemid.md)
  
```xml
<ParentItemId Id="" ChangeKey="" />
```

<span data-ttu-id="08ff1-107">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="08ff1-107">**ItemIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="08ff1-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="08ff1-108">Attributes and elements</span></span>

<span data-ttu-id="08ff1-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="08ff1-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="08ff1-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="08ff1-110">Attributes</span></span>

|<span data-ttu-id="08ff1-111">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="08ff1-111">**Attribute**</span></span>|<span data-ttu-id="08ff1-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="08ff1-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="08ff1-113">**Id**</span><span class="sxs-lookup"><span data-stu-id="08ff1-113">**Id**</span></span> <br/> |<span data-ttu-id="08ff1-114">Identifica un solo elemento del almacén de Exchange para asociarlo a datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="08ff1-114">Identifies a single item in the Exchange store to associate with an attachment.</span></span> <span data-ttu-id="08ff1-115">Este valor es una cadena.</span><span class="sxs-lookup"><span data-stu-id="08ff1-115">This value is a string.</span></span> <span data-ttu-id="08ff1-116">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="08ff1-116">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="08ff1-117">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="08ff1-117">**ChangeKey**</span></span> <br/> |<span data-ttu-id="08ff1-118">Identifica una versión no especificada de un elemento que se identifica mediante el atributo **ID** en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="08ff1-118">Identifies an unspecified version of an item that is identified by the **Id** attribute in the Exchange store.</span></span> <span data-ttu-id="08ff1-119">Se usa para asegurarse de que se usa un elemento actual cuando se actualiza con datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="08ff1-119">This is used to make sure that a current item is used when it is updated with an attachment.</span></span> <span data-ttu-id="08ff1-120">Este valor es una cadena.</span><span class="sxs-lookup"><span data-stu-id="08ff1-120">This value is a string.</span></span> <span data-ttu-id="08ff1-121">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="08ff1-121">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="08ff1-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="08ff1-122">Child elements</span></span>

<span data-ttu-id="08ff1-123">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="08ff1-123">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="08ff1-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="08ff1-124">Parent elements</span></span>

|<span data-ttu-id="08ff1-125">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="08ff1-125">**Element**</span></span>|<span data-ttu-id="08ff1-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="08ff1-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="08ff1-127">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="08ff1-127">CreateAttachment</span></span>](createattachment.md) <br/> |<span data-ttu-id="08ff1-128">Define una solicitud para crear datos adjuntos a un elemento en un buzón.</span><span class="sxs-lookup"><span data-stu-id="08ff1-128">Defines a request to create an attachment to an item in a mailbox.</span></span>  <br/> <span data-ttu-id="08ff1-129">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="08ff1-129">The following is the XPath expression to this element:</span></span>  <br/>  `/CreateAttachment` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08ff1-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="08ff1-130">Remarks</span></span>

<span data-ttu-id="08ff1-131">Este elemento es obligatorio en la [operación CreateAttachment](createattachment-operation.md).</span><span class="sxs-lookup"><span data-stu-id="08ff1-131">This element is required in the [CreateAttachment operation](createattachment-operation.md).</span></span> <span data-ttu-id="08ff1-132">Este elemento es básicamente el mismo que el elemento [Itemid](itemid.md) .</span><span class="sxs-lookup"><span data-stu-id="08ff1-132">This element is basically the same as the [ItemId](itemid.md) element.</span></span> 
  
<span data-ttu-id="08ff1-133">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="08ff1-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="08ff1-134">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="08ff1-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="08ff1-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="08ff1-135">Namespace</span></span>  <br/> |[https://schemas.microsoft.com/exchange/services/2006/messages](https://schemas.microsoft.com/exchange/services/2006/messages) <br/> |
|<span data-ttu-id="08ff1-136">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="08ff1-136">Schema Name</span></span>  <br/> |<span data-ttu-id="08ff1-137">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="08ff1-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="08ff1-138">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="08ff1-138">Validation File</span></span>  <br/> |<span data-ttu-id="08ff1-139">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="08ff1-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="08ff1-140">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="08ff1-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="08ff1-141">Falso</span><span class="sxs-lookup"><span data-stu-id="08ff1-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="08ff1-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="08ff1-142">See also</span></span>

- [<span data-ttu-id="08ff1-143">Operación CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="08ff1-143">CreateAttachment operation</span></span>](createattachment-operation.md)

