---
title: ForwardAllowed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bc32e0f4-61e9-4c9f-9a03-90a07eb51c53
description: El elemento ForwardAllowed especifica si los mensajes de correo electrónico de reenvío están habilitados.
ms.openlocfilehash: 3c722809bf68239c7d776108cb60d98afbed6e93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461936"
---
# <a name="forwardallowed"></a><span data-ttu-id="3ca4b-103">ForwardAllowed</span><span class="sxs-lookup"><span data-stu-id="3ca4b-103">ForwardAllowed</span></span>

<span data-ttu-id="3ca4b-104">El elemento **ForwardAllowed** especifica si los mensajes de correo electrónico de reenvío están habilitados.</span><span class="sxs-lookup"><span data-stu-id="3ca4b-104">The **ForwardAllowed** element specifies whether forwarding emails is enabled.</span></span> 
  
```XML
<ForwardAllowed>true | false</ForwardAllowed>
```

 <span data-ttu-id="3ca4b-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="3ca4b-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3ca4b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3ca4b-106">Attributes and elements</span></span>

<span data-ttu-id="3ca4b-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3ca4b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3ca4b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3ca4b-108">Attributes</span></span>

<span data-ttu-id="3ca4b-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3ca4b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3ca4b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3ca4b-110">Child elements</span></span>

<span data-ttu-id="3ca4b-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3ca4b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3ca4b-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3ca4b-112">Parent elements</span></span>

|<span data-ttu-id="3ca4b-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3ca4b-113">**Element**</span></span>|<span data-ttu-id="3ca4b-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3ca4b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3ca4b-115">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="3ca4b-115">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md) <br/> |<span data-ttu-id="3ca4b-116">Especifica información sobre la licencia de administración de derechos.</span><span class="sxs-lookup"><span data-stu-id="3ca4b-116">Specifies information about the rights management license.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3ca4b-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3ca4b-117">Text value</span></span>

<span data-ttu-id="3ca4b-118">Un valor de texto de **true** para el elemento **ForwardAllowed** indica que se permite el reenvío de correos electrónicos.</span><span class="sxs-lookup"><span data-stu-id="3ca4b-118">A text value of **true** for the **ForwardAllowed** element indicates that forwarding emails is allowed.</span></span> <span data-ttu-id="3ca4b-119">Un valor de **false** indica que no se permite el reenvío.</span><span class="sxs-lookup"><span data-stu-id="3ca4b-119">A value of **false** indicates that forwarding is not allowed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3ca4b-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3ca4b-120">Remarks</span></span>

<span data-ttu-id="3ca4b-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3ca4b-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3ca4b-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3ca4b-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3ca4b-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3ca4b-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3ca4b-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="3ca4b-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3ca4b-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3ca4b-125">Schema Name</span></span>  <br/> |<span data-ttu-id="3ca4b-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="3ca4b-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="3ca4b-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3ca4b-127">Validation File</span></span>  <br/> |<span data-ttu-id="3ca4b-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="3ca4b-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="3ca4b-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3ca4b-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="3ca4b-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ca4b-130">See also</span></span>



- [<span data-ttu-id="3ca4b-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="3ca4b-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

