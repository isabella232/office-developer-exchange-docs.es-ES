---
title: MaxItems
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4ddba6b8-0f38-42cd-96a1-0d4283f6375b
description: El elemento MaxItems especifica el número máximo de elementos que se devolverá en la solicitud.
ms.openlocfilehash: f16e9d46b59c0f562aabd5383f7f445d93414f68
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461747"
---
# <a name="maxitems"></a><span data-ttu-id="c105b-103">MaxItems</span><span class="sxs-lookup"><span data-stu-id="c105b-103">MaxItems</span></span>

<span data-ttu-id="c105b-104">El elemento **MaxItems** especifica el número máximo de elementos que se devolverá en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c105b-104">The **MaxItems** element specifies the maximum number of items to return in the request.</span></span> 
  
```XML
<MaxItems/>
```

 <span data-ttu-id="c105b-105">**int**</span><span class="sxs-lookup"><span data-stu-id="c105b-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c105b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c105b-106">Attributes and elements</span></span>

<span data-ttu-id="c105b-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c105b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c105b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c105b-108">Attributes</span></span>

<span data-ttu-id="c105b-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c105b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c105b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c105b-110">Child elements</span></span>

<span data-ttu-id="c105b-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c105b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c105b-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c105b-112">Parent elements</span></span>

[<span data-ttu-id="c105b-113">GetReminders</span><span class="sxs-lookup"><span data-stu-id="c105b-113">GetReminders</span></span>](getreminders.md)
  
## <a name="text-value"></a><span data-ttu-id="c105b-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c105b-114">Text value</span></span>

<span data-ttu-id="c105b-115">El valor de texto del elemento **MaxItems** es el número máximo de elementos que se devuelven en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c105b-115">The text value of the **MaxItems** element is the maximum number of items to return in the request.</span></span> <span data-ttu-id="c105b-116">Este número no puede ser menor que cero o mayor que 200.</span><span class="sxs-lookup"><span data-stu-id="c105b-116">This number cannot be less than zero or greater than 200.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c105b-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c105b-117">Remarks</span></span>

<span data-ttu-id="c105b-118">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c105b-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c105b-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c105b-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c105b-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c105b-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c105b-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="c105b-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c105b-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c105b-122">Schema Name</span></span>  <br/> |<span data-ttu-id="c105b-123">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="c105b-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c105b-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c105b-124">Validation File</span></span>  <br/> |<span data-ttu-id="c105b-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="c105b-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c105b-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c105b-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="c105b-127">Falso</span><span class="sxs-lookup"><span data-stu-id="c105b-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c105b-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="c105b-128">See also</span></span>



[<span data-ttu-id="c105b-129">GetReminders</span><span class="sxs-lookup"><span data-stu-id="c105b-129">GetReminders</span></span>](getreminders.md)


- [<span data-ttu-id="c105b-130">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c105b-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

