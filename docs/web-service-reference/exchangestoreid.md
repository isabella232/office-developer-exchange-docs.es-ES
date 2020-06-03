---
title: ExchangeStoreId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5acceb42-a757-4c74-ab1c-b1abf7bf1e0a
description: El elemento ExchangeStoreId especifica el identificador del grupo de mensajería instantánea (mi).
ms.openlocfilehash: c1b1e1830987449eeb7ea186d00743ea9cc75a77
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456993"
---
# <a name="exchangestoreid"></a><span data-ttu-id="f02cf-103">ExchangeStoreId</span><span class="sxs-lookup"><span data-stu-id="f02cf-103">ExchangeStoreId</span></span>

<span data-ttu-id="f02cf-104">El elemento **ExchangeStoreId** especifica el identificador del grupo de mensajería instantánea (mi).</span><span class="sxs-lookup"><span data-stu-id="f02cf-104">The **ExchangeStoreId** element specifies the instant messaging (IM) group identifier.</span></span> 
  
```XML
<ExchangeStoreId Id="" ChangeKey=""/>
```

 <span data-ttu-id="f02cf-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="f02cf-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f02cf-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f02cf-106">Attributes and elements</span></span>

<span data-ttu-id="f02cf-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f02cf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f02cf-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f02cf-108">Attributes</span></span>

|<span data-ttu-id="f02cf-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="f02cf-109">**Attribute**</span></span>|<span data-ttu-id="f02cf-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f02cf-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f02cf-111">Id</span><span class="sxs-lookup"><span data-stu-id="f02cf-111">Id</span></span>  <br/> |<span data-ttu-id="f02cf-112">El valor de texto del atributo **ID** es el identificador del grupo.</span><span class="sxs-lookup"><span data-stu-id="f02cf-112">The text value of the **Id** attribute is the identifier of the group.</span></span>  <br/> |
|<span data-ttu-id="f02cf-113">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="f02cf-113">ChangeKey</span></span>  <br/> |<span data-ttu-id="f02cf-114">El valor de texto del atributo **changekey** es la clave de cambio del grupo.</span><span class="sxs-lookup"><span data-stu-id="f02cf-114">The text value of the **ChangeKey** attribute is the change key of the group.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f02cf-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f02cf-115">Child elements</span></span>

<span data-ttu-id="f02cf-116">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f02cf-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f02cf-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f02cf-117">Parent elements</span></span>

|<span data-ttu-id="f02cf-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f02cf-118">**Element**</span></span>|<span data-ttu-id="f02cf-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f02cf-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f02cf-120">Desagrupo</span><span class="sxs-lookup"><span data-stu-id="f02cf-120">ImGroup</span></span>](imgroup.md) <br/> |<span data-ttu-id="f02cf-121">Representa un grupo de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="f02cf-121">Represents an instant messaging group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f02cf-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f02cf-122">Remarks</span></span>

<span data-ttu-id="f02cf-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f02cf-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f02cf-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f02cf-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f02cf-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f02cf-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f02cf-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="f02cf-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f02cf-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f02cf-127">Schema Name</span></span>  <br/> |<span data-ttu-id="f02cf-128">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="f02cf-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="f02cf-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f02cf-129">Validation File</span></span>  <br/> |<span data-ttu-id="f02cf-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="f02cf-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="f02cf-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f02cf-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="f02cf-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="f02cf-132">See also</span></span>



- [<span data-ttu-id="f02cf-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f02cf-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

