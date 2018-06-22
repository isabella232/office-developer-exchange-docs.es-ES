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
ms.openlocfilehash: 055012166bb125dfcf86070f2e23496bf0209b51
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764493"
---
# <a name="exportitems"></a><span data-ttu-id="0df17-103">ExportItems</span><span class="sxs-lookup"><span data-stu-id="0df17-103">ExportItems</span></span>

<span data-ttu-id="0df17-104">El elemento **ExportItems** representa una solicitud para exportar elementos de un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="0df17-104">The **ExportItems** element represents a request to export items from a mailbox.</span></span> 
  
[<span data-ttu-id="0df17-105">ExportItems</span><span class="sxs-lookup"><span data-stu-id="0df17-105">ExportItems</span></span>](exportitems.md)
  
```XML
<ExportItems>
   <ItemIds/>
</ExportItems>
```

 <span data-ttu-id="0df17-106">**ExportItemsType**</span><span class="sxs-lookup"><span data-stu-id="0df17-106">**ExportItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0df17-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0df17-107">Attributes and elements</span></span>

<span data-ttu-id="0df17-108">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0df17-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0df17-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="0df17-109">Attributes</span></span>

<span data-ttu-id="0df17-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0df17-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0df17-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0df17-111">Child elements</span></span>

|<span data-ttu-id="0df17-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="0df17-112">**Element**</span></span>|<span data-ttu-id="0df17-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0df17-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0df17-114">ItemId (NonEmptyArrayOfItemIdsType)</span><span class="sxs-lookup"><span data-stu-id="0df17-114">ItemIds (NonEmptyArrayOfItemIdsType)</span></span>](itemids-nonemptyarrayofitemidstype.md) <br/> |<span data-ttu-id="0df17-115">Contiene una matriz de identificadores de elemento que identifican los elementos que desee exportar desde un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="0df17-115">Contains an array of item identifiers that identify the items to export from a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0df17-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0df17-116">Parent elements</span></span>

<span data-ttu-id="0df17-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0df17-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="0df17-118">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0df17-118">Text value</span></span>

<span data-ttu-id="0df17-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0df17-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0df17-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0df17-120">Remarks</span></span>

<span data-ttu-id="0df17-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="0df17-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0df17-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0df17-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0df17-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0df17-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0df17-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0df17-124">Schema Name</span></span>  <br/> |<span data-ttu-id="0df17-125">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="0df17-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="0df17-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0df17-126">Validation File</span></span>  <br/> |<span data-ttu-id="0df17-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0df17-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0df17-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0df17-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="0df17-129">False</span><span class="sxs-lookup"><span data-stu-id="0df17-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0df17-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="0df17-130">See also</span></span>



[<span data-ttu-id="0df17-131">Operación ExportItems</span><span class="sxs-lookup"><span data-stu-id="0df17-131">ExportItems operation</span></span>](exportitems-operation.md)
  
[<span data-ttu-id="0df17-132">Operación UploadItems</span><span class="sxs-lookup"><span data-stu-id="0df17-132">UploadItems operation</span></span>](uploaditems-operation.md)

