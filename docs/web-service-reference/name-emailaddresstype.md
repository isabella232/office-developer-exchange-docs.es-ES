---
title: Nombre (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Name
api_type:
- schema
ms.assetid: 98c58c53-9acc-4e89-9fcf-03f1b05abee1
description: El elemento Name representa el nombre de un usuario de buzón de correo.
ms.openlocfilehash: b140fd46608a04f9aaba17f917cc4171c056dcf2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836504"
---
# <a name="name-emailaddresstype"></a><span data-ttu-id="08f95-103">Nombre (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="08f95-103">Name (EmailAddressType)</span></span>

<span data-ttu-id="08f95-104">El elemento **Name** representa el nombre de un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="08f95-104">The **Name** element represents the name of a mailbox user.</span></span> 
  
```xml
<Name/>
```

<span data-ttu-id="08f95-105">**string**</span><span class="sxs-lookup"><span data-stu-id="08f95-105">**string**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="08f95-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="08f95-106">Attributes and elements</span></span>

<span data-ttu-id="08f95-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="08f95-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="08f95-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="08f95-108">Attributes</span></span>

<span data-ttu-id="08f95-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="08f95-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="08f95-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="08f95-110">Child elements</span></span>

<span data-ttu-id="08f95-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="08f95-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="08f95-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="08f95-112">Parent elements</span></span>

|<span data-ttu-id="08f95-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="08f95-113">**Element**</span></span>|<span data-ttu-id="08f95-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="08f95-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="08f95-115">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="08f95-115">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="08f95-116">Identifica una dirección de correo electrónico completa resuelta.</span><span class="sxs-lookup"><span data-stu-id="08f95-116">Identifies a fully resolved e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="08f95-117">RoomList</span><span class="sxs-lookup"><span data-stu-id="08f95-117">RoomList</span></span>](roomlist.md) <br/> |<span data-ttu-id="08f95-118">Identifica una lista de las salas de reuniones.</span><span class="sxs-lookup"><span data-stu-id="08f95-118">Identifies a list of meeting rooms.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="08f95-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="08f95-119">Text value</span></span>

<span data-ttu-id="08f95-120">Si se usa este elemento, es necesario un valor de texto que representa una cadena.</span><span class="sxs-lookup"><span data-stu-id="08f95-120">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="08f95-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="08f95-121">Remarks</span></span>

<span data-ttu-id="08f95-122">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="08f95-122">This element is optional.</span></span> <span data-ttu-id="08f95-123">El elemento **Name** existe en los tipos de **AttachmentType**, **EmailAddressType**y **EmailAddress** .</span><span class="sxs-lookup"><span data-stu-id="08f95-123">The **Name** element exists in the **AttachmentType**, **EmailAddressType**, and **EmailAddress** types.</span></span> <span data-ttu-id="08f95-124">El elemento **nombre** en el tipo de **EmailAddress** se describe en el tema de elemento [nombre (EmailAddress)](name-emailaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="08f95-124">The **Name** element in the **EmailAddress** type is described in the [Name (EmailAddress)](name-emailaddress.md) element topic.</span></span> 
  
<span data-ttu-id="08f95-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="08f95-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="08f95-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="08f95-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="08f95-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="08f95-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="08f95-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="08f95-128">Schema Name</span></span>  <br/> |<span data-ttu-id="08f95-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="08f95-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="08f95-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="08f95-130">Validation File</span></span>  <br/> |<span data-ttu-id="08f95-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="08f95-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="08f95-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="08f95-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="08f95-133">False</span><span class="sxs-lookup"><span data-stu-id="08f95-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="08f95-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="08f95-134">See also</span></span>

- [<span data-ttu-id="08f95-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="08f95-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

