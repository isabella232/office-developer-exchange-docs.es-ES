---
title: IsInline
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsInline
api_type:
- schema
ms.assetid: 5e7712c8-372a-4a16-be64-360c5ff3961a
description: El elemento IsInline representa si los datos adjuntos aparecen en línea dentro de un elemento.
ms.openlocfilehash: 2b3b6392fe8867ae9782dcb7211c17f4f4d9becd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464213"
---
# <a name="isinline"></a><span data-ttu-id="f089a-103">IsInline</span><span class="sxs-lookup"><span data-stu-id="f089a-103">IsInline</span></span>

<span data-ttu-id="f089a-104">El elemento **IsInline** representa si los datos adjuntos aparecen en línea dentro de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f089a-104">The **IsInline** element represents whether the attachment appears inline within an item.</span></span> 
  
```xml
<IsInline>true or false</IsInline>
```

 <span data-ttu-id="f089a-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="f089a-105">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f089a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f089a-106">Attributes and elements</span></span>

<span data-ttu-id="f089a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f089a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f089a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f089a-108">Attributes</span></span>

<span data-ttu-id="f089a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f089a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f089a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f089a-110">Child elements</span></span>

<span data-ttu-id="f089a-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f089a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f089a-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f089a-112">Parent elements</span></span>

|<span data-ttu-id="f089a-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f089a-113">**Element**</span></span>|<span data-ttu-id="f089a-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f089a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f089a-115">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="f089a-115">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="f089a-116">Representa un archivo que está adjunto a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f089a-116">Represents a file that is attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f089a-117">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="f089a-117">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="f089a-118">Representa un elemento de Exchange que está adjunto a otro elemento de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f089a-118">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f089a-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f089a-119">Text value</span></span>

<span data-ttu-id="f089a-120">Este elemento puede ser **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="f089a-120">This element can be either **true** or **false**.</span></span> <span data-ttu-id="f089a-121">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="f089a-121">The default value is **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f089a-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f089a-122">Remarks</span></span>

<span data-ttu-id="f089a-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="f089a-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f089a-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f089a-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f089a-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="f089a-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f089a-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f089a-126">Schema Name</span></span>  <br/> |<span data-ttu-id="f089a-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f089a-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="f089a-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f089a-128">Validation File</span></span>  <br/> |<span data-ttu-id="f089a-129">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="f089a-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f089a-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f089a-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="f089a-131">Falso</span><span class="sxs-lookup"><span data-stu-id="f089a-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f089a-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="f089a-132">See also</span></span>



- [<span data-ttu-id="f089a-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f089a-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

