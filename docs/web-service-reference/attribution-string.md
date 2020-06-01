---
title: Atribución (cadena)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 736be0bc-12c4-410e-bd17-a89f996ac432
description: El elemento de atribución especifica una cadena que se usa para identificar un atributo de un rol.
ms.openlocfilehash: 9a3243904c02c3bdeea7e4a4e7dcb240d4ad3563
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464164"
---
# <a name="attribution-string"></a><span data-ttu-id="f1c0c-103">Atribución (cadena)</span><span class="sxs-lookup"><span data-stu-id="f1c0c-103">Attribution (string)</span></span>

<span data-ttu-id="f1c0c-104">El elemento de **atribución** especifica una cadena que se usa para identificar un atributo de un rol.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-104">The **Attribution** element specifies a string used to identify an attribute of a persona.</span></span> 
  
```XML
<Attribution></Attribution>
```

 <span data-ttu-id="f1c0c-105">**XS: String**</span><span class="sxs-lookup"><span data-stu-id="f1c0c-105">**xs:string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f1c0c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f1c0c-106">Attributes and elements</span></span>

<span data-ttu-id="f1c0c-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f1c0c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f1c0c-108">Attributes</span></span>

<span data-ttu-id="f1c0c-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f1c0c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f1c0c-110">Child elements</span></span>

<span data-ttu-id="f1c0c-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f1c0c-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f1c0c-112">Parent elements</span></span>

|<span data-ttu-id="f1c0c-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f1c0c-113">**Element**</span></span>|<span data-ttu-id="f1c0c-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f1c0c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f1c0c-115">Atribuciones (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="f1c0c-115">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md) <br/> |<span data-ttu-id="f1c0c-116">Especifica una matriz de atribuciones para su elemento de **valor** asociado.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-116">Specifies an array of attributions for its associated **Value** element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f1c0c-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f1c0c-117">Text value</span></span>

<span data-ttu-id="f1c0c-118">El valor de texto del elemento de **atribución** es un valor de cadena que atribuye un valor de propiedad al contacto de origen.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-118">The text value of the **attribution** element is a string value that attributes a property value to the source contact.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f1c0c-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f1c0c-119">Remarks</span></span>

<span data-ttu-id="f1c0c-120">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f1c0c-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f1c0c-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f1c0c-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f1c0c-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="f1c0c-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f1c0c-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f1c0c-124">Schema Name</span></span>  <br/> |<span data-ttu-id="f1c0c-125">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="f1c0c-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="f1c0c-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f1c0c-126">Validation File</span></span>  <br/> |<span data-ttu-id="f1c0c-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="f1c0c-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="f1c0c-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f1c0c-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="f1c0c-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1c0c-129">See also</span></span>

- [<span data-ttu-id="f1c0c-130">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f1c0c-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

