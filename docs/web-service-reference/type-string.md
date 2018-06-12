---
title: Tipo (cadena)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d5eea7a8-c40d-42a6-8e0d-67f3252496cf
description: El elemento de tipo especifica el tipo de postal dirección o número de teléfono, por ejemplo, HomeorBusiness.
ms.openlocfilehash: b2262a01b03922e36daa3b13436f1e070918b72c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840736"
---
# <a name="type-string"></a><span data-ttu-id="f5252-103">Tipo (cadena)</span><span class="sxs-lookup"><span data-stu-id="f5252-103">Type (string)</span></span>

<span data-ttu-id="f5252-104">El elemento de **tipo** especifica el tipo de dirección postal o el número de teléfono, por ejemplo, "Principal" o "Empresarial".</span><span class="sxs-lookup"><span data-stu-id="f5252-104">The **Type** element specifies the type of postal address or phone number, for example, "Home" or "Business".</span></span> 
  
```XML
<Type></Type>
```

 <span data-ttu-id="f5252-105">**string**</span><span class="sxs-lookup"><span data-stu-id="f5252-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f5252-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f5252-106">Attributes and elements</span></span>

<span data-ttu-id="f5252-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f5252-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f5252-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f5252-108">Attributes</span></span>

<span data-ttu-id="f5252-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f5252-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f5252-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f5252-110">Child elements</span></span>

<span data-ttu-id="f5252-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f5252-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f5252-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f5252-112">Parent elements</span></span>

<span data-ttu-id="f5252-113">[Teléfono](phone.md) | [PhoneNumber](phonenumber.md) | [valor (PersonaPostalAddressType)](value-personapostaladdresstype.md) | [PostalAddress (PersonaPostalAddressType)](postaladdress-personapostaladdresstype.md)</span><span class="sxs-lookup"><span data-stu-id="f5252-113">[Phone](phone.md) | [PhoneNumber](phonenumber.md) | [Value (PersonaPostalAddressType)](value-personapostaladdresstype.md) | [PostalAddress (PersonaPostalAddressType)](postaladdress-personapostaladdresstype.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="f5252-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f5252-114">Text value</span></span>

<span data-ttu-id="f5252-115">El valor de texto del **tipo de** elemento es el tipo de una dirección postal o el número de teléfono.</span><span class="sxs-lookup"><span data-stu-id="f5252-115">The text value of the **Type** element is the type of a postal address or phone number.</span></span> <span data-ttu-id="f5252-116">Por ejemplo, los valores "Principal" o "Empresarial" son los valores esperados para el **tipo de** elemento.</span><span class="sxs-lookup"><span data-stu-id="f5252-116">For example, the values "Home" or "Business" are expected values for the **Type** element.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f5252-117">Notas</span><span class="sxs-lookup"><span data-stu-id="f5252-117">Remarks</span></span>

<span data-ttu-id="f5252-118">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f5252-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f5252-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f5252-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f5252-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f5252-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f5252-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f5252-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f5252-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f5252-122">Schema name</span></span>  <br/> |<span data-ttu-id="f5252-123">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f5252-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="f5252-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f5252-124">Validation file</span></span>  <br/> |<span data-ttu-id="f5252-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f5252-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f5252-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f5252-126">Can be empty</span></span>  <br/> ||
   

