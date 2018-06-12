---
title: ItemHoldPeriod
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 30369db5-4d45-40e8-bc83-3236667fc404
description: El elemento ItemHoldPeriod especifica la cantidad de tiempo para retener el contenido que coincide con la consulta de buzón de correo.
ms.openlocfilehash: 212d765aa3f0493dd4f3051de483fa08a6fa8ac7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836144"
---
# <a name="itemholdperiod"></a><span data-ttu-id="ab095-103">ItemHoldPeriod</span><span class="sxs-lookup"><span data-stu-id="ab095-103">ItemHoldPeriod</span></span>

<span data-ttu-id="ab095-104">El elemento **ItemHoldPeriod** especifica la cantidad de tiempo para retener el contenido que coincide con la consulta de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="ab095-104">The **ItemHoldPeriod** element specifies the amount of time to hold content that matches the mailbox query.</span></span> 
  
```XML
<ItemHoldPeriod/>
```

 <span data-ttu-id="ab095-105">**string**</span><span class="sxs-lookup"><span data-stu-id="ab095-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ab095-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ab095-106">Attributes and elements</span></span>

<span data-ttu-id="ab095-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ab095-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ab095-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ab095-108">Attributes</span></span>

<span data-ttu-id="ab095-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ab095-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ab095-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ab095-110">Child elements</span></span>

<span data-ttu-id="ab095-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ab095-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ab095-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ab095-112">Parent elements</span></span>

[<span data-ttu-id="ab095-113">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="ab095-113">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)
  
## <a name="text-value"></a><span data-ttu-id="ab095-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ab095-114">Text value</span></span>

<span data-ttu-id="ab095-115">El valor de texto puede ser "Ilimitado" o el valor de cadena de cualquier valor [Timespan](http://msdn.microsoft.com/en-us/library/1ecy8h51%28v=vs.110%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ab095-115">The text value can be "Unlimited" or the string value of any [Timespan](http://msdn.microsoft.com/en-us/library/1ecy8h51%28v=vs.110%29.aspx) value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ab095-116">Notas</span><span class="sxs-lookup"><span data-stu-id="ab095-116">Remarks</span></span>

<span data-ttu-id="ab095-117">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ab095-117">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="ab095-118">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ab095-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ab095-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ab095-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ab095-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ab095-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ab095-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ab095-121">Schema Name</span></span>  <br/> |<span data-ttu-id="ab095-122">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="ab095-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ab095-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ab095-123">Validation File</span></span>  <br/> |<span data-ttu-id="ab095-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ab095-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ab095-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ab095-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="ab095-126">Verdadero</span><span class="sxs-lookup"><span data-stu-id="ab095-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ab095-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="ab095-127">See also</span></span>



[<span data-ttu-id="ab095-128">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="ab095-128">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)


- [<span data-ttu-id="ab095-129">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="ab095-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

