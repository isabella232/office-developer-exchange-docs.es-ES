---
title: GetRooms
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetRooms
api_type:
- schema
ms.assetid: 82a737c7-da41-4777-8ad8-89851a0b602b
description: El elemento GetRooms es el elemento raíz de una solicitud para obtener una lista de salas dentro de una lista de salas determinada.
ms.openlocfilehash: 77fde5980a03d4c0509344933b0901cb21ab7197
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458596"
---
# <a name="getrooms"></a><span data-ttu-id="2e099-103">GetRooms</span><span class="sxs-lookup"><span data-stu-id="2e099-103">GetRooms</span></span>

<span data-ttu-id="2e099-104">El elemento **GetRooms** es el elemento raíz de una solicitud para obtener una lista de salas dentro de una lista de salas determinada.</span><span class="sxs-lookup"><span data-stu-id="2e099-104">The **GetRooms** element is the root element in a request to get a list of rooms within a particular room list.</span></span> 
  
```XML
<GetRooms>
   <RoomList/>
</GetRooms>
```

 <span data-ttu-id="2e099-105">**GetRoomsType**</span><span class="sxs-lookup"><span data-stu-id="2e099-105">**GetRoomsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2e099-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2e099-106">Attributes and elements</span></span>

<span data-ttu-id="2e099-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2e099-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2e099-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2e099-108">Attributes</span></span>

<span data-ttu-id="2e099-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2e099-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2e099-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2e099-110">Child elements</span></span>

|<span data-ttu-id="2e099-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2e099-111">**Element**</span></span>|<span data-ttu-id="2e099-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2e099-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e099-113">RoomList</span><span class="sxs-lookup"><span data-stu-id="2e099-113">RoomList</span></span>](roomlist.md) <br/> |<span data-ttu-id="2e099-114">Representa una dirección de correo electrónico que identifica una lista de salas de reuniones</span><span class="sxs-lookup"><span data-stu-id="2e099-114">Represents an e-mail address that identifies a list of meeting rooms</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2e099-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2e099-115">Parent elements</span></span>

<span data-ttu-id="2e099-116">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2e099-116">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="2e099-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="2e099-117">Text value</span></span>

<span data-ttu-id="2e099-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2e099-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2e099-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2e099-119">Remarks</span></span>

<span data-ttu-id="2e099-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="2e099-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2e099-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2e099-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2e099-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="2e099-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2e099-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2e099-123">Schema Name</span></span>  <br/> |<span data-ttu-id="2e099-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="2e099-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2e099-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2e099-125">Validation File</span></span>  <br/> |<span data-ttu-id="2e099-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="2e099-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2e099-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2e099-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="2e099-128">Falso</span><span class="sxs-lookup"><span data-stu-id="2e099-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2e099-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e099-129">See also</span></span>



- [<span data-ttu-id="2e099-130">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2e099-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

