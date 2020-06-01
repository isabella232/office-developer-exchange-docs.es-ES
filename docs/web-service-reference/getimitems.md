---
title: GetImItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 455e5709-6c06-49fd-bfb2-403fc912287c
description: El elemento de solicitud GetImItems define una solicitud para obtener información sobre los grupos de mensajería instantánea especificados y los roles de contacto de mensajería instantánea.
ms.openlocfilehash: e3973cbbf800ffe91472b9c733c4d4a927b91c9f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456454"
---
# <a name="getimitems"></a><span data-ttu-id="897df-103">GetImItems</span><span class="sxs-lookup"><span data-stu-id="897df-103">GetImItems</span></span>

<span data-ttu-id="897df-104">El elemento de solicitud **GetImItems** define una solicitud para obtener información sobre los grupos de mensajería instantánea especificados y los roles de contacto de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="897df-104">The **GetImItems** request element defines a request to get information about the specified instant messaging groups and instant messaging contact personas.</span></span> 
  
```XML
<GetImItems>
   <ContactIds/>
   <GroupIds/>
   <ExtendedProperties/>
</GetImItems>
```

 <span data-ttu-id="897df-105">**GetImItemsType**</span><span class="sxs-lookup"><span data-stu-id="897df-105">**GetImItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="897df-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="897df-106">Attributes and elements</span></span>

<span data-ttu-id="897df-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="897df-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="897df-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="897df-108">Attributes</span></span>

<span data-ttu-id="897df-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="897df-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="897df-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="897df-110">Child elements</span></span>

<span data-ttu-id="897df-111">[ContactIds](contactids.md)  |  [GroupIds](groupids.md)  |  [ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)](extendedproperties-nonemptyarrayofextendedfielduris.md)</span><span class="sxs-lookup"><span data-stu-id="897df-111">[ContactIds](contactids.md) | [GroupIds](groupids.md) | [ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)](extendedproperties-nonemptyarrayofextendedfielduris.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="897df-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="897df-112">Parent elements</span></span>

<span data-ttu-id="897df-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="897df-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="897df-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="897df-114">Remarks</span></span>

<span data-ttu-id="897df-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="897df-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="897df-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="897df-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="897df-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="897df-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="897df-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="897df-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="897df-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="897df-119">Schema name</span></span>  <br/> |<span data-ttu-id="897df-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="897df-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="897df-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="897df-121">Validation file</span></span>  <br/> |<span data-ttu-id="897df-122">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="897df-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="897df-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="897df-123">Can be empty</span></span>  <br/> ||
   

