---
title: ExpandDL
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExpandDL
api_type:
- schema
ms.assetid: affe84a5-ad98-4aba-83f4-8732938b763d
description: El elemento de ExpandDL define una solicitud para expandir una lista de distribución.
ms.openlocfilehash: ef93ed4684427a74a4fd2c38b4020ecb743fbaaf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764485"
---
# <a name="expanddl"></a><span data-ttu-id="ccce8-103">ExpandDL</span><span class="sxs-lookup"><span data-stu-id="ccce8-103">ExpandDL</span></span>

<span data-ttu-id="ccce8-104">El elemento de **ExpandDL** define una solicitud para expandir una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="ccce8-104">The **ExpandDL** element defines a request to expand a distribution list.</span></span> 
  
```xml
<ExpandDL>
   <Mailbox/>
</ExpandDL>
```

 <span data-ttu-id="ccce8-105">**ExpandDLType**</span><span class="sxs-lookup"><span data-stu-id="ccce8-105">**ExpandDLType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ccce8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ccce8-106">Attributes and elements</span></span>

<span data-ttu-id="ccce8-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ccce8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ccce8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ccce8-108">Attributes</span></span>

<span data-ttu-id="ccce8-109">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ccce8-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ccce8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ccce8-110">Child elements</span></span>

|<span data-ttu-id="ccce8-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ccce8-111">**Element**</span></span>|<span data-ttu-id="ccce8-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ccce8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ccce8-113">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="ccce8-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="ccce8-114">Identifica una dirección de correo electrónico completa resuelta o una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="ccce8-114">Identifies a fully resolved e-mail address or a distribution list.</span></span> <span data-ttu-id="ccce8-115">Este buzón de correo representa la lista de distribución para expandir.</span><span class="sxs-lookup"><span data-stu-id="ccce8-115">This mailbox represents the distribution list to expand.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ccce8-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ccce8-116">Parent elements</span></span>

<span data-ttu-id="ccce8-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ccce8-117">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ccce8-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ccce8-118">Remarks</span></span>

<span data-ttu-id="ccce8-119">Para obtener una lista de distribución única sólo se realizará una expansión de lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="ccce8-119">A distribution list expansion will only be performed for a single distribution list.</span></span> <span data-ttu-id="ccce8-120">Una expansión de lista de distribución no es recursiva.</span><span class="sxs-lookup"><span data-stu-id="ccce8-120">A distribution list expansion is not recursive.</span></span>
  
<span data-ttu-id="ccce8-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="ccce8-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ccce8-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ccce8-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ccce8-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ccce8-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ccce8-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ccce8-124">Schema Name</span></span>  <br/> |<span data-ttu-id="ccce8-125">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="ccce8-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="ccce8-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ccce8-126">Validation File</span></span>  <br/> |<span data-ttu-id="ccce8-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ccce8-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ccce8-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ccce8-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="ccce8-129">False</span><span class="sxs-lookup"><span data-stu-id="ccce8-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ccce8-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="ccce8-130">See also</span></span>



[<span data-ttu-id="ccce8-131">Operación de ExpandDL</span><span class="sxs-lookup"><span data-stu-id="ccce8-131">ExpandDL operation</span></span>](expanddl-operation.md)

