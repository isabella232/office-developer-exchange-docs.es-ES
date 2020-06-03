---
title: ExportItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExportItems
api_type:
- schema
ms.assetid: bbbc56e4-8cc1-43ae-b70a-9a8d6bb0f399
description: El elemento ExportItems representa una solicitud para exportar elementos de un buzón de correo.
ms.openlocfilehash: 6e4996f62ea5051e6dc235ee7255057f16b3855b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457273"
---
# <a name="exportitems"></a><span data-ttu-id="d84bc-103">ExportItems</span><span class="sxs-lookup"><span data-stu-id="d84bc-103">ExportItems</span></span>

<span data-ttu-id="d84bc-104">El elemento **ExportItems** representa una solicitud para exportar elementos de un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="d84bc-104">The **ExportItems** element represents a request to export items from a mailbox.</span></span> 
  
[<span data-ttu-id="d84bc-105">ExportItems</span><span class="sxs-lookup"><span data-stu-id="d84bc-105">ExportItems</span></span>](exportitems.md)
  
```XML
<ExportItems>
   <ItemIds/>
</ExportItems>
```

 <span data-ttu-id="d84bc-106">**ExportItemsType**</span><span class="sxs-lookup"><span data-stu-id="d84bc-106">**ExportItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d84bc-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d84bc-107">Attributes and elements</span></span>

<span data-ttu-id="d84bc-108">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d84bc-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d84bc-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="d84bc-109">Attributes</span></span>

<span data-ttu-id="d84bc-110">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d84bc-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d84bc-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d84bc-111">Child elements</span></span>

|<span data-ttu-id="d84bc-112">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d84bc-112">**Element**</span></span>|<span data-ttu-id="d84bc-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d84bc-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d84bc-114">ItemIds (NonEmptyArrayOfItemIdsType)</span><span class="sxs-lookup"><span data-stu-id="d84bc-114">ItemIds (NonEmptyArrayOfItemIdsType)</span></span>](itemids-nonemptyarrayofitemidstype.md) <br/> |<span data-ttu-id="d84bc-115">Contiene una matriz de identificadores de elementos que identifican los elementos que se exportarán de un buzón.</span><span class="sxs-lookup"><span data-stu-id="d84bc-115">Contains an array of item identifiers that identify the items to export from a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d84bc-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d84bc-116">Parent elements</span></span>

<span data-ttu-id="d84bc-117">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d84bc-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="d84bc-118">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d84bc-118">Text value</span></span>

<span data-ttu-id="d84bc-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d84bc-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d84bc-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d84bc-120">Remarks</span></span>

<span data-ttu-id="d84bc-121">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="d84bc-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d84bc-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d84bc-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d84bc-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="d84bc-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d84bc-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d84bc-124">Schema Name</span></span>  <br/> |<span data-ttu-id="d84bc-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="d84bc-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="d84bc-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d84bc-126">Validation File</span></span>  <br/> |<span data-ttu-id="d84bc-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d84bc-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d84bc-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d84bc-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="d84bc-129">Falso</span><span class="sxs-lookup"><span data-stu-id="d84bc-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d84bc-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="d84bc-130">See also</span></span>



[<span data-ttu-id="d84bc-131">Operación ExportItems</span><span class="sxs-lookup"><span data-stu-id="d84bc-131">ExportItems operation</span></span>](exportitems-operation.md)
  
[<span data-ttu-id="d84bc-132">Operación UploadItems</span><span class="sxs-lookup"><span data-stu-id="d84bc-132">UploadItems operation</span></span>](uploaditems-operation.md)

