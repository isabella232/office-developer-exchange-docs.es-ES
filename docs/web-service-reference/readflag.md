---
title: ReadFlag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9d91aa89-9f9f-4877-846d-aaf48bbeec7c
description: El elemento ReadFlag indica el estado de lectura para establecer en elementos de una carpeta.
ms.openlocfilehash: f3156a51fbdd3372dd28f2065499d26a50b3d497
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836954"
---
# <a name="readflag"></a><span data-ttu-id="807b8-103">ReadFlag</span><span class="sxs-lookup"><span data-stu-id="807b8-103">ReadFlag</span></span>

<span data-ttu-id="807b8-104">El elemento **ReadFlag** indica el estado de lectura para establecer en elementos de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="807b8-104">The **ReadFlag** element indicates the read state to set on items in a folder.</span></span> 
  
```XML
<ReadFlag>true | false</ReadFlag>
```

 <span data-ttu-id="807b8-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="807b8-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="807b8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="807b8-106">Attributes and elements</span></span>

<span data-ttu-id="807b8-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="807b8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="807b8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="807b8-108">Attributes</span></span>

<span data-ttu-id="807b8-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="807b8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="807b8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="807b8-110">Child elements</span></span>

<span data-ttu-id="807b8-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="807b8-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="807b8-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="807b8-112">Parent elements</span></span>

[<span data-ttu-id="807b8-113">MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="807b8-113">MarkAllItemsAsRead</span></span>](markallitemsasread.md)
  
## <a name="text-value"></a><span data-ttu-id="807b8-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="807b8-114">Text value</span></span>

<span data-ttu-id="807b8-115">Un valor de texto de **true** para el elemento **ReadFlag** indica que los elementos de la carpeta se marcarán como lectura.</span><span class="sxs-lookup"><span data-stu-id="807b8-115">A text value of **true** for the **ReadFlag** element indicates that the items in the folder will be marked as read.</span></span> <span data-ttu-id="807b8-116">Un valor de **false** indica que los elementos de la carpeta se marcarán como no leídos.</span><span class="sxs-lookup"><span data-stu-id="807b8-116">A value of **false** indicates that the items in the folder will be marked as unread.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="807b8-117">Notas</span><span class="sxs-lookup"><span data-stu-id="807b8-117">Remarks</span></span>

<span data-ttu-id="807b8-118">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="807b8-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="807b8-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="807b8-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="807b8-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="807b8-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="807b8-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="807b8-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="807b8-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="807b8-122">Schema name</span></span>  <br/> |<span data-ttu-id="807b8-123">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="807b8-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="807b8-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="807b8-124">Validation file</span></span>  <br/> |<span data-ttu-id="807b8-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="807b8-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="807b8-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="807b8-126">Can be empty</span></span>  <br/> ||
   

