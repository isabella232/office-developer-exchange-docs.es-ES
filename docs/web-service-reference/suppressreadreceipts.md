---
title: SuppressReadReceipts
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f0805560-7a2f-455b-94d2-ec4f1e3652c3
description: El elemento SuppressReadReceipts indica si se deben suprimir las confirmaciones de lectura.
ms.openlocfilehash: aa604d4907582bd73727ba664958a589a222f9cb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455936"
---
# <a name="suppressreadreceipts"></a><span data-ttu-id="c8f1d-103">SuppressReadReceipts</span><span class="sxs-lookup"><span data-stu-id="c8f1d-103">SuppressReadReceipts</span></span>

<span data-ttu-id="c8f1d-104">El elemento **SuppressReadReceipts** indica si se deben suprimir las confirmaciones de lectura.</span><span class="sxs-lookup"><span data-stu-id="c8f1d-104">The **SuppressReadReceipts** element indicates whether read receipts should be suppressed.</span></span> 
  
```XML
<SuppressReadReceipts>true | false</SuppressReadReceipts>
```

 <span data-ttu-id="c8f1d-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c8f1d-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c8f1d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c8f1d-106">Attributes and elements</span></span>

<span data-ttu-id="c8f1d-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c8f1d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c8f1d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c8f1d-108">Attributes</span></span>

<span data-ttu-id="c8f1d-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c8f1d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c8f1d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c8f1d-110">Child elements</span></span>

<span data-ttu-id="c8f1d-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c8f1d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c8f1d-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c8f1d-112">Parent elements</span></span>

<span data-ttu-id="c8f1d-113">[ConversationAction](conversationaction.md)  |  [MarkAllItemsAsRead](markallitemsasread.md)</span><span class="sxs-lookup"><span data-stu-id="c8f1d-113">[ConversationAction](conversationaction.md) | [MarkAllItemsAsRead](markallitemsasread.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="c8f1d-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c8f1d-114">Text value</span></span>

<span data-ttu-id="c8f1d-115">Un valor de texto de **true** para el elemento **SuppressReadReciepts** indica que se eliminan las confirmaciones de lectura.</span><span class="sxs-lookup"><span data-stu-id="c8f1d-115">A text value of **true** for the **SuppressReadReciepts** element indicates that read receipts are suppressed.</span></span> <span data-ttu-id="c8f1d-116">Un valor de **false** indica que las confirmaciones de lectura se enviarán al remitente.</span><span class="sxs-lookup"><span data-stu-id="c8f1d-116">A value of **false** indicates that read receipts will be sent to the sender.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c8f1d-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c8f1d-117">Remarks</span></span>

<span data-ttu-id="c8f1d-118">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c8f1d-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c8f1d-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c8f1d-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c8f1d-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c8f1d-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c8f1d-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="c8f1d-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c8f1d-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c8f1d-122">Schema name</span></span>  <br/> |<span data-ttu-id="c8f1d-123">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="c8f1d-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c8f1d-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c8f1d-124">Validation file</span></span>  <br/> |<span data-ttu-id="c8f1d-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="c8f1d-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c8f1d-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c8f1d-126">Can be empty</span></span>  <br/> ||
   

