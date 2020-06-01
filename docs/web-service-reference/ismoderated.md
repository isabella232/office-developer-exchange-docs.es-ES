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
description: El elemento IsModerated indica si el buzón de correo del destinatario está moderado.
ms.openlocfilehash: 930d5a7e09712f35d22850a93462d051a34785a1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44435488"
---
# <a name="ismoderated"></a><span data-ttu-id="43fed-103">IsModerated</span><span class="sxs-lookup"><span data-stu-id="43fed-103">IsModerated</span></span>

<span data-ttu-id="43fed-104">El elemento **IsModerated** indica si el buzón de correo del destinatario está moderado.</span><span class="sxs-lookup"><span data-stu-id="43fed-104">The **IsModerated** element indicates whether the recipient's mailbox is being moderated.</span></span> 
  
```XML
<IsModerated>true | false</IsModerated>
```

 <span data-ttu-id="43fed-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="43fed-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="43fed-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="43fed-106">Attributes and elements</span></span>

<span data-ttu-id="43fed-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="43fed-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="43fed-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="43fed-108">Attributes</span></span>

<span data-ttu-id="43fed-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="43fed-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="43fed-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="43fed-110">Child elements</span></span>

<span data-ttu-id="43fed-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="43fed-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="43fed-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="43fed-112">Parent elements</span></span>

|<span data-ttu-id="43fed-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="43fed-113">**Element**</span></span>|<span data-ttu-id="43fed-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="43fed-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="43fed-115">Sugerencias de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="43fed-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="43fed-116">Representa los valores de distintos tipos de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="43fed-116">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="43fed-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="43fed-117">Text value</span></span>

<span data-ttu-id="43fed-118">El valor de texto de este elemento es **true** si el buzón de correo del destinatario se modera.</span><span class="sxs-lookup"><span data-stu-id="43fed-118">The text value for this element is **true** if the recipient's mailbox is being moderated.</span></span> <span data-ttu-id="43fed-119">El valor es **false** si el buzón del destinatario no se modera.</span><span class="sxs-lookup"><span data-stu-id="43fed-119">The value is **false** if the recipient's mailbox is not being moderated.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="43fed-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="43fed-120">Remarks</span></span>

<span data-ttu-id="43fed-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="43fed-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="43fed-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="43fed-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="43fed-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="43fed-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="43fed-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="43fed-124">Schema Name</span></span>  <br/> |<span data-ttu-id="43fed-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="43fed-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="43fed-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="43fed-126">Validation File</span></span>  <br/> |<span data-ttu-id="43fed-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="43fed-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="43fed-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="43fed-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="43fed-129">Falso</span><span class="sxs-lookup"><span data-stu-id="43fed-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="43fed-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="43fed-130">See also</span></span>



- [<span data-ttu-id="43fed-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="43fed-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

