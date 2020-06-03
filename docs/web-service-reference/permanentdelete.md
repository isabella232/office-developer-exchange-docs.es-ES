---
title: PermanentDelete
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PermanentDelete
api_type:
- schema
ms.assetid: 1a0e0f46-1472-4eb7-bb54-f193a2603587
description: El elemento PermanentDelete indica si los mensajes se eliminan permanentemente y no se guardan en la carpeta elementos eliminados.
ms.openlocfilehash: da7680eefca9ad359948af38eac49d18e9055988
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467770"
---
# <a name="permanentdelete"></a><span data-ttu-id="1168f-103">PermanentDelete</span><span class="sxs-lookup"><span data-stu-id="1168f-103">PermanentDelete</span></span>

<span data-ttu-id="1168f-104">El elemento **PermanentDelete** indica si los mensajes se eliminan permanentemente y no se guardan en la carpeta elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="1168f-104">The **PermanentDelete** element indicates whether messages are to be permanently deleted and not saved to the Deleted Items folder.</span></span> 
  
```XML
<PermanentDelete>true | false</PermanentDelete>
```

 <span data-ttu-id="1168f-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="1168f-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1168f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1168f-106">Attributes and elements</span></span>

<span data-ttu-id="1168f-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1168f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1168f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1168f-108">Attributes</span></span>

<span data-ttu-id="1168f-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1168f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1168f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1168f-110">Child elements</span></span>

<span data-ttu-id="1168f-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1168f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1168f-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1168f-112">Parent elements</span></span>

|<span data-ttu-id="1168f-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1168f-113">**Element**</span></span>|<span data-ttu-id="1168f-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1168f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1168f-115">Actions</span><span class="sxs-lookup"><span data-stu-id="1168f-115">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="1168f-116">Representa el conjunto de acciones que se pueden realizar en un mensaje cuando se cumplen las condiciones.</span><span class="sxs-lookup"><span data-stu-id="1168f-116">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1168f-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="1168f-117">Text value</span></span>

<span data-ttu-id="1168f-118">Un valor de texto de **true** indica que el mensaje debe marcarse para que se elimine de forma permanente.</span><span class="sxs-lookup"><span data-stu-id="1168f-118">A text value of **true** indicates that the message must be marked to be permanently deleted.</span></span> <span data-ttu-id="1168f-119">Un valor de **false** indica que el mensaje no debe marcarse para que se elimine de forma permanente.</span><span class="sxs-lookup"><span data-stu-id="1168f-119">A value of **false** indicates that the message must not be marked to be permanently deleted.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1168f-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1168f-120">Remarks</span></span>

<span data-ttu-id="1168f-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="1168f-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1168f-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1168f-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1168f-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="1168f-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1168f-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1168f-124">Schema Name</span></span>  <br/> |<span data-ttu-id="1168f-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="1168f-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1168f-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1168f-126">Validation File</span></span>  <br/> |<span data-ttu-id="1168f-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="1168f-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1168f-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1168f-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="1168f-129">Verdadero</span><span class="sxs-lookup"><span data-stu-id="1168f-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1168f-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="1168f-130">See also</span></span>



- [<span data-ttu-id="1168f-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1168f-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

