---
title: EmailAddressEntity
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20049467-c01a-4c7d-8ada-ca1801cc95ed
description: El elemento EmailAddressEntity especifica una sola entidad de dirección de correo electrónico.
ms.openlocfilehash: b76b08f93e60c8492906f3cc94e60f5725c8a9dc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526224"
---
# <a name="emailaddressentity"></a><span data-ttu-id="a1887-103">EmailAddressEntity</span><span class="sxs-lookup"><span data-stu-id="a1887-103">EmailAddressEntity</span></span>

<span data-ttu-id="a1887-104">El elemento **EmailAddressEntity** especifica una sola entidad de dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="a1887-104">The **EmailAddressEntity** element specifies a single email address entity.</span></span> 
  
```XML
<EmailAddressEntity>
    <EmailAddress></EmailAddress>
</EmailAddressEntity>
```

 <span data-ttu-id="a1887-105">**EmailAddressEntityType**</span><span class="sxs-lookup"><span data-stu-id="a1887-105">**EmailAddressEntityType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a1887-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a1887-106">Attributes and elements</span></span>

<span data-ttu-id="a1887-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a1887-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a1887-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a1887-108">Attributes</span></span>

<span data-ttu-id="a1887-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a1887-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a1887-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a1887-110">Child elements</span></span>

|<span data-ttu-id="a1887-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a1887-111">**Element**</span></span>|<span data-ttu-id="a1887-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a1887-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a1887-113">EmailAddress (cadena)</span><span class="sxs-lookup"><span data-stu-id="a1887-113">EmailAddress (string)</span></span>](emailaddress-string.md) <br/> |<span data-ttu-id="a1887-114">Especifica una sola dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="a1887-114">Specifies a single email address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a1887-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a1887-115">Parent elements</span></span>

|<span data-ttu-id="a1887-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a1887-116">**Element**</span></span>|<span data-ttu-id="a1887-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a1887-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a1887-118">EmailAddresses (ArrayOfEmailAddressEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="a1887-118">EmailAddresses (ArrayOfEmailAddressEntitiesType)</span></span>](emailaddresses-arrayofemailaddressentitiestype.md) <br/> |<span data-ttu-id="a1887-119">Especifica una matriz de entidades de direcciones de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="a1887-119">Specifies an array of email address entities.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1887-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a1887-120">Remarks</span></span>

<span data-ttu-id="a1887-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a1887-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a1887-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a1887-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a1887-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a1887-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a1887-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="a1887-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a1887-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a1887-125">Schema Name</span></span>  <br/> |<span data-ttu-id="a1887-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="a1887-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="a1887-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a1887-127">Validation File</span></span>  <br/> |<span data-ttu-id="a1887-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="a1887-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="a1887-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a1887-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="a1887-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1887-130">See also</span></span>



- [<span data-ttu-id="a1887-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a1887-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

