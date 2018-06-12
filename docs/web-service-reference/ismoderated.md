---
title: IsModerated
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsModerated
api_type:
- schema
ms.assetid: a7562256-feb9-41a1-857e-b5d41cbed680
description: El elemento IsModerated indica si se va a modera el buzón del destinatario.
ms.openlocfilehash: 8db234f9706bb8187978a76f745323749d7a640a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836055"
---
# <a name="ismoderated"></a><span data-ttu-id="07991-103">IsModerated</span><span class="sxs-lookup"><span data-stu-id="07991-103">IsModerated</span></span>

<span data-ttu-id="07991-104">El elemento **IsModerated** indica si se va a modera el buzón del destinatario.</span><span class="sxs-lookup"><span data-stu-id="07991-104">The **IsModerated** element indicates whether the recipient's mailbox is being moderated.</span></span> 
  
```XML
<IsModerated>true | false</IsModerated>
```

 <span data-ttu-id="07991-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="07991-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="07991-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="07991-106">Attributes and elements</span></span>

<span data-ttu-id="07991-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="07991-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="07991-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="07991-108">Attributes</span></span>

<span data-ttu-id="07991-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="07991-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="07991-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="07991-110">Child elements</span></span>

<span data-ttu-id="07991-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="07991-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="07991-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="07991-112">Parent elements</span></span>

|<span data-ttu-id="07991-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="07991-113">**Element**</span></span>|<span data-ttu-id="07991-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="07991-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="07991-115">Sugerencias de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="07991-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="07991-116">Representa los valores de distintos tipos de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="07991-116">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="07991-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="07991-117">Text value</span></span>

<span data-ttu-id="07991-118">El valor de texto para este elemento es **true** si se va a modera el buzón del destinatario.</span><span class="sxs-lookup"><span data-stu-id="07991-118">The text value for this element is **true** if the recipient's mailbox is being moderated.</span></span> <span data-ttu-id="07991-119">El valor es **false** si no se está moderado el buzón del destinatario.</span><span class="sxs-lookup"><span data-stu-id="07991-119">The value is **false** if the recipient's mailbox is not being moderated.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="07991-120">Notas</span><span class="sxs-lookup"><span data-stu-id="07991-120">Remarks</span></span>

<span data-ttu-id="07991-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="07991-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="07991-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="07991-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="07991-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="07991-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="07991-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="07991-124">Schema Name</span></span>  <br/> |<span data-ttu-id="07991-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="07991-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="07991-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="07991-126">Validation File</span></span>  <br/> |<span data-ttu-id="07991-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="07991-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="07991-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="07991-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="07991-129">False</span><span class="sxs-lookup"><span data-stu-id="07991-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="07991-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="07991-130">See also</span></span>



- [<span data-ttu-id="07991-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="07991-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

