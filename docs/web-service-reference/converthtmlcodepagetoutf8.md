---
title: ConvertHtmlCodePageToUTF8
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f02c8331-0a4e-4d01-adc2-2b93ed838a42
description: El elemento ConvertHtmlCodePageToUTF8 indica si el cuerpo HTML del elemento se convierte en UTF8.
ms.openlocfilehash: aff6579835097a273101188c02a9919003b71b58
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763889"
---
# <a name="converthtmlcodepagetoutf8"></a><span data-ttu-id="3ca15-103">ConvertHtmlCodePageToUTF8</span><span class="sxs-lookup"><span data-stu-id="3ca15-103">ConvertHtmlCodePageToUTF8</span></span>

<span data-ttu-id="3ca15-104">El elemento **ConvertHtmlCodePageToUTF8** indica si el cuerpo HTML del elemento se convierte en UTF8.</span><span class="sxs-lookup"><span data-stu-id="3ca15-104">The **ConvertHtmlCodePageToUTF8** element indicates whether the item HTML body is converted to UTF8.</span></span> 
  
```XML
<ConvertHtmlCodePageToUTF8/>
```

 <span data-ttu-id="3ca15-105">**xs: Boolean**</span><span class="sxs-lookup"><span data-stu-id="3ca15-105">**xs:boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3ca15-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3ca15-106">Attributes and elements</span></span>

<span data-ttu-id="3ca15-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3ca15-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3ca15-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3ca15-108">Attributes</span></span>

<span data-ttu-id="3ca15-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3ca15-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3ca15-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3ca15-110">Child elements</span></span>

<span data-ttu-id="3ca15-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3ca15-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3ca15-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3ca15-112">Parent elements</span></span>

|<span data-ttu-id="3ca15-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3ca15-113">**Element**</span></span>|<span data-ttu-id="3ca15-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3ca15-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3ca15-115">ItemShape</span><span class="sxs-lookup"><span data-stu-id="3ca15-115">ItemShape</span></span>](itemshape.md) <br/> |<span data-ttu-id="3ca15-116">Identifica un conjunto de propiedades para devolver en una respuesta.</span><span class="sxs-lookup"><span data-stu-id="3ca15-116">Identifies a set of properties to return in a response.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3ca15-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3ca15-117">Text value</span></span>

<span data-ttu-id="3ca15-118">Un valor de texto de **true** para el elemento **ConvertHtmlCodePageToUTF8** indica que el cuerpo HTML se convierte en UTF8.</span><span class="sxs-lookup"><span data-stu-id="3ca15-118">A text value of **true** for the **ConvertHtmlCodePageToUTF8** element indicates that the HTML body is converted to UTF8.</span></span> <span data-ttu-id="3ca15-119">Un valor de texto de **false** indica que el cuerpo HTML no se convierte en UTF8.</span><span class="sxs-lookup"><span data-stu-id="3ca15-119">A text value of **false** indicates that the HTML body is not converted to UTF8.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3ca15-120">Notas</span><span class="sxs-lookup"><span data-stu-id="3ca15-120">Remarks</span></span>

<span data-ttu-id="3ca15-121">Se usa el valor predeterminado de **true** si el elemento **ConvertHtmlCodePageToUTF8** no está especificado en una solicitud.</span><span class="sxs-lookup"><span data-stu-id="3ca15-121">The default value of **true** is used if the **ConvertHtmlCodePageToUTF8** element is not specified in a request.</span></span> 
  
<span data-ttu-id="3ca15-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="3ca15-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3ca15-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3ca15-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3ca15-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3ca15-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3ca15-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3ca15-125">Schema Name</span></span>  <br/> |<span data-ttu-id="3ca15-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="3ca15-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="3ca15-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3ca15-127">Validation File</span></span>  <br/> |<span data-ttu-id="3ca15-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3ca15-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3ca15-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3ca15-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="3ca15-130">False</span><span class="sxs-lookup"><span data-stu-id="3ca15-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3ca15-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="3ca15-131">See also</span></span>



- [<span data-ttu-id="3ca15-132">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3ca15-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

