---
title: Emails3
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4f4dc589-4530-4a35-b2a6-0c83cac23637
description: El elemento Emails3 especifica una matriz de valores de EmailAddressAttributedValue y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: 0505b0ea248a3ab2de7ec18a344fa57651f84cca
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460725"
---
# <a name="emails3"></a><span data-ttu-id="4ead8-103">Emails3</span><span class="sxs-lookup"><span data-stu-id="4ead8-103">Emails3</span></span>

<span data-ttu-id="4ead8-104">El elemento **Emails3** especifica una matriz de valores de **EmailAddressAttributedValue** y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="4ead8-104">The **Emails3** element specifies an array of **EmailAddressAttributedValue** values and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<Emails3>
    <EmailAddressAttributedValue></EmailAddressAttributedValue>
</Emails3>
```

 <span data-ttu-id="4ead8-105">**ArrayOfEmailAddressAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="4ead8-105">**ArrayOfEmailAddressAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4ead8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4ead8-106">Attributes and elements</span></span>

<span data-ttu-id="4ead8-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4ead8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4ead8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4ead8-108">Attributes</span></span>

<span data-ttu-id="4ead8-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="4ead8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4ead8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4ead8-110">Child elements</span></span>

|<span data-ttu-id="4ead8-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4ead8-111">**Element**</span></span>|<span data-ttu-id="4ead8-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4ead8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4ead8-113">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="4ead8-113">EmailAddressAttributedValue</span></span>](emailaddressattributedvalue.md) <br/> |<span data-ttu-id="4ead8-114">Especifica una instancia de una matriz de direcciones de correo electrónico y sus atribuciones asociadas.</span><span class="sxs-lookup"><span data-stu-id="4ead8-114">Specifies an instance of an array of email addresses and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4ead8-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4ead8-115">Parent elements</span></span>

|<span data-ttu-id="4ead8-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4ead8-116">**Element**</span></span>|<span data-ttu-id="4ead8-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4ead8-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4ead8-118">Rol</span><span class="sxs-lookup"><span data-stu-id="4ead8-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="4ead8-119">Especifica un conjunto de datos de rol devueltos por una solicitud **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="4ead8-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ead8-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4ead8-120">Remarks</span></span>

<span data-ttu-id="4ead8-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4ead8-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="4ead8-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="4ead8-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4ead8-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4ead8-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ead8-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="4ead8-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4ead8-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4ead8-125">Schema Name</span></span>  <br/> |<span data-ttu-id="4ead8-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="4ead8-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="4ead8-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4ead8-127">Validation File</span></span>  <br/> |<span data-ttu-id="4ead8-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="4ead8-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="4ead8-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4ead8-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="4ead8-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ead8-130">See also</span></span>



- [<span data-ttu-id="4ead8-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="4ead8-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

