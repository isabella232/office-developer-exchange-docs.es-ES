---
title: ItemHoldPeriod
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 30369db5-4d45-40e8-bc83-3236667fc404
description: El elemento ItemHoldPeriod especifica la cantidad de tiempo que se conservará el contenido que coincida con la consulta de buzón de correo.
ms.openlocfilehash: 185666b72cc96dd88605b7baa6433d070e7ebc91
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44452289"
---
# <a name="itemholdperiod"></a><span data-ttu-id="4ca17-103">ItemHoldPeriod</span><span class="sxs-lookup"><span data-stu-id="4ca17-103">ItemHoldPeriod</span></span>

<span data-ttu-id="4ca17-104">El elemento **ItemHoldPeriod** especifica la cantidad de tiempo que se conservará el contenido que coincida con la consulta de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="4ca17-104">The **ItemHoldPeriod** element specifies the amount of time to hold content that matches the mailbox query.</span></span> 
  
```XML
<ItemHoldPeriod/>
```

 <span data-ttu-id="4ca17-105">**string**</span><span class="sxs-lookup"><span data-stu-id="4ca17-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4ca17-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4ca17-106">Attributes and elements</span></span>

<span data-ttu-id="4ca17-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4ca17-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4ca17-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4ca17-108">Attributes</span></span>

<span data-ttu-id="4ca17-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="4ca17-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4ca17-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4ca17-110">Child elements</span></span>

<span data-ttu-id="4ca17-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="4ca17-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4ca17-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4ca17-112">Parent elements</span></span>

[<span data-ttu-id="4ca17-113">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="4ca17-113">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)
  
## <a name="text-value"></a><span data-ttu-id="4ca17-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="4ca17-114">Text value</span></span>

<span data-ttu-id="4ca17-115">El valor de texto puede ser "Unlimited" o el valor de cadena de cualquier valor [TimeSpan](https://msdn.microsoft.com/library/1ecy8h51%28v=vs.110%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4ca17-115">The text value can be "Unlimited" or the string value of any [Timespan](https://msdn.microsoft.com/library/1ecy8h51%28v=vs.110%29.aspx) value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4ca17-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4ca17-116">Remarks</span></span>

<span data-ttu-id="4ca17-117">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="4ca17-117">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="4ca17-118">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="4ca17-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4ca17-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4ca17-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ca17-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="4ca17-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4ca17-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4ca17-121">Schema Name</span></span>  <br/> |<span data-ttu-id="4ca17-122">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="4ca17-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4ca17-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4ca17-123">Validation File</span></span>  <br/> |<span data-ttu-id="4ca17-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="4ca17-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4ca17-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4ca17-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="4ca17-126">Verdadero</span><span class="sxs-lookup"><span data-stu-id="4ca17-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4ca17-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ca17-127">See also</span></span>



[<span data-ttu-id="4ca17-128">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="4ca17-128">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)


- [<span data-ttu-id="4ca17-129">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="4ca17-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

