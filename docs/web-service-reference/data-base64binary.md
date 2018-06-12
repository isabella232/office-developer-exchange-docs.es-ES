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
description: El elemento de datos contiene los datos de un solo elemento exportado o un elemento que se va a cargar en un buzón de correo.
ms.openlocfilehash: 9560273e31a64edb2254489961733dfe7360ad01
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764018"
---
# <a name="data-base64binary"></a><span data-ttu-id="853d7-103">Datos (base64Binary)</span><span class="sxs-lookup"><span data-stu-id="853d7-103">Data (base64Binary)</span></span>

<span data-ttu-id="853d7-104">El elemento de **datos** contiene los datos de un solo elemento exportado o un elemento que se va a cargar en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="853d7-104">The **Data** element contains the data of a single exported item or an item to upload into a mailbox.</span></span> 
  
```XML
<Data/>
```

<span data-ttu-id="853d7-105">**base64Binary**</span><span class="sxs-lookup"><span data-stu-id="853d7-105">**xs:base64Binary**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="853d7-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="853d7-106">Attributes and elements</span></span>

<span data-ttu-id="853d7-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="853d7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="853d7-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="853d7-108">Attributes</span></span>

<span data-ttu-id="853d7-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="853d7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="853d7-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="853d7-110">Child elements</span></span>

<span data-ttu-id="853d7-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="853d7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="853d7-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="853d7-112">Parent elements</span></span>

|<span data-ttu-id="853d7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="853d7-113">**Element**</span></span>|<span data-ttu-id="853d7-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="853d7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="853d7-115">ExportItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="853d7-115">ExportItemsResponseMessage</span></span>](exportitemsresponsemessage.md) <br/> |<span data-ttu-id="853d7-116">Contiene el estado y los resultados de una solicitud para exportar un elemento de un solo buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="853d7-116">Contains the status and results of a request to export a single mailbox item.</span></span>  <br/> |
|[<span data-ttu-id="853d7-117">Elemento (UploadItemType)</span><span class="sxs-lookup"><span data-stu-id="853d7-117">Item (UploadItemType)</span></span>](item-uploaditemtype.md) <br/> |<span data-ttu-id="853d7-118">Representa un solo elemento va a cargar en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="853d7-118">Represents a single item to upload into a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="853d7-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="853d7-119">Text value</span></span>

<span data-ttu-id="853d7-120">El elemento de **datos** contiene los nombres de propiedad y valores de un elemento exportado o un elemento que se cargará en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="853d7-120">The **Data** element contains the property names and values for an exported item or an item that will be uploaded into a mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="853d7-121">Notas</span><span class="sxs-lookup"><span data-stu-id="853d7-121">Remarks</span></span>

<span data-ttu-id="853d7-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="853d7-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="853d7-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="853d7-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="853d7-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="853d7-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="853d7-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="853d7-125">Schema Name</span></span>  <br/> |<span data-ttu-id="853d7-126">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="853d7-126">Message schema</span></span>  <br/> |
|<span data-ttu-id="853d7-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="853d7-127">Validation File</span></span>  <br/> |<span data-ttu-id="853d7-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="853d7-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="853d7-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="853d7-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="853d7-130">False</span><span class="sxs-lookup"><span data-stu-id="853d7-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="853d7-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="853d7-131">See also</span></span>

- [<span data-ttu-id="853d7-132">Operación ExportItems</span><span class="sxs-lookup"><span data-stu-id="853d7-132">ExportItems operation</span></span>](exportitems-operation.md)
- [<span data-ttu-id="853d7-133">Operación UploadItems</span><span class="sxs-lookup"><span data-stu-id="853d7-133">UploadItems operation</span></span>](uploaditems-operation.md)

