---
title: Datos (base64Binary)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Data
api_type:
- schema
ms.assetid: 26d8c2d0-bed2-4aed-b381-20e2ace6892f
description: El elemento Data contiene los datos de un elemento exportado único o un elemento que se va a cargar en un buzón.
ms.openlocfilehash: 43ee16ca7caf634756ca00a88715d9834adad92b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526973"
---
# <a name="data-base64binary"></a><span data-ttu-id="f40bd-103">Datos (base64Binary)</span><span class="sxs-lookup"><span data-stu-id="f40bd-103">Data (base64Binary)</span></span>

<span data-ttu-id="f40bd-104">El elemento **Data** contiene los datos de un elemento exportado único o un elemento que se va a cargar en un buzón.</span><span class="sxs-lookup"><span data-stu-id="f40bd-104">The **Data** element contains the data of a single exported item or an item to upload into a mailbox.</span></span> 
  
```XML
<Data/>
```

<span data-ttu-id="f40bd-105">**XS: base64Binary**</span><span class="sxs-lookup"><span data-stu-id="f40bd-105">**xs:base64Binary**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f40bd-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f40bd-106">Attributes and elements</span></span>

<span data-ttu-id="f40bd-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f40bd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f40bd-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f40bd-108">Attributes</span></span>

<span data-ttu-id="f40bd-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f40bd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f40bd-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f40bd-110">Child elements</span></span>

<span data-ttu-id="f40bd-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f40bd-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f40bd-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f40bd-112">Parent elements</span></span>

|<span data-ttu-id="f40bd-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f40bd-113">**Element**</span></span>|<span data-ttu-id="f40bd-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f40bd-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f40bd-115">ExportItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f40bd-115">ExportItemsResponseMessage</span></span>](exportitemsresponsemessage.md) <br/> |<span data-ttu-id="f40bd-116">Contiene el estado y los resultados de una solicitud para exportar un solo elemento de buzón.</span><span class="sxs-lookup"><span data-stu-id="f40bd-116">Contains the status and results of a request to export a single mailbox item.</span></span>  <br/> |
|[<span data-ttu-id="f40bd-117">Item (UploadItemType)</span><span class="sxs-lookup"><span data-stu-id="f40bd-117">Item (UploadItemType)</span></span>](item-uploaditemtype.md) <br/> |<span data-ttu-id="f40bd-118">Representa un solo elemento que se va a cargar en un buzón.</span><span class="sxs-lookup"><span data-stu-id="f40bd-118">Represents a single item to upload into a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f40bd-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f40bd-119">Text value</span></span>

<span data-ttu-id="f40bd-120">El elemento **Data** contiene los nombres y los valores de las propiedades de un elemento exportado o un elemento que se cargará en un buzón.</span><span class="sxs-lookup"><span data-stu-id="f40bd-120">The **Data** element contains the property names and values for an exported item or an item that will be uploaded into a mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f40bd-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f40bd-121">Remarks</span></span>

<span data-ttu-id="f40bd-122">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f40bd-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f40bd-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f40bd-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f40bd-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="f40bd-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f40bd-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f40bd-125">Schema Name</span></span>  <br/> |<span data-ttu-id="f40bd-126">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="f40bd-126">Message schema</span></span>  <br/> |
|<span data-ttu-id="f40bd-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f40bd-127">Validation File</span></span>  <br/> |<span data-ttu-id="f40bd-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="f40bd-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f40bd-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f40bd-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="f40bd-130">Falso</span><span class="sxs-lookup"><span data-stu-id="f40bd-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f40bd-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="f40bd-131">See also</span></span>

- [<span data-ttu-id="f40bd-132">Operación ExportItems</span><span class="sxs-lookup"><span data-stu-id="f40bd-132">ExportItems operation</span></span>](exportitems-operation.md)
- [<span data-ttu-id="f40bd-133">Operación UploadItems</span><span class="sxs-lookup"><span data-stu-id="f40bd-133">UploadItems operation</span></span>](uploaditems-operation.md)

