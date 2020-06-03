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
description: El elemento ExpandDL define una solicitud para expandir una lista de distribución.
ms.openlocfilehash: 52b1ea1b51ce185c7a266e3002a4484e4b813bc0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456937"
---
# <a name="expanddl"></a><span data-ttu-id="891ad-103">ExpandDL</span><span class="sxs-lookup"><span data-stu-id="891ad-103">ExpandDL</span></span>

<span data-ttu-id="891ad-104">El elemento **ExpandDL** define una solicitud para expandir una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="891ad-104">The **ExpandDL** element defines a request to expand a distribution list.</span></span> 
  
```xml
<ExpandDL>
   <Mailbox/>
</ExpandDL>
```

 <span data-ttu-id="891ad-105">**ExpandDLType**</span><span class="sxs-lookup"><span data-stu-id="891ad-105">**ExpandDLType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="891ad-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="891ad-106">Attributes and elements</span></span>

<span data-ttu-id="891ad-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="891ad-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="891ad-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="891ad-108">Attributes</span></span>

<span data-ttu-id="891ad-109">Ninguno</span><span class="sxs-lookup"><span data-stu-id="891ad-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="891ad-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="891ad-110">Child elements</span></span>

|<span data-ttu-id="891ad-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="891ad-111">**Element**</span></span>|<span data-ttu-id="891ad-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="891ad-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="891ad-113">Buzón</span><span class="sxs-lookup"><span data-stu-id="891ad-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="891ad-114">Identifica una dirección de correo electrónico completamente resuelta o una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="891ad-114">Identifies a fully resolved e-mail address or a distribution list.</span></span> <span data-ttu-id="891ad-115">Este buzón representa la lista de distribución que se va a expandir.</span><span class="sxs-lookup"><span data-stu-id="891ad-115">This mailbox represents the distribution list to expand.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="891ad-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="891ad-116">Parent elements</span></span>

<span data-ttu-id="891ad-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="891ad-117">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="891ad-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="891ad-118">Remarks</span></span>

<span data-ttu-id="891ad-119">Solo se realizará una expansión de la lista de distribución para una única lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="891ad-119">A distribution list expansion will only be performed for a single distribution list.</span></span> <span data-ttu-id="891ad-120">Una expansión de lista de distribución no es recurrente.</span><span class="sxs-lookup"><span data-stu-id="891ad-120">A distribution list expansion is not recursive.</span></span>
  
<span data-ttu-id="891ad-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="891ad-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="891ad-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="891ad-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="891ad-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="891ad-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="891ad-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="891ad-124">Schema Name</span></span>  <br/> |<span data-ttu-id="891ad-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="891ad-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="891ad-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="891ad-126">Validation File</span></span>  <br/> |<span data-ttu-id="891ad-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="891ad-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="891ad-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="891ad-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="891ad-129">Falso</span><span class="sxs-lookup"><span data-stu-id="891ad-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="891ad-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="891ad-130">See also</span></span>



[<span data-ttu-id="891ad-131">Operación ExpandDL</span><span class="sxs-lookup"><span data-stu-id="891ad-131">ExpandDL operation</span></span>](expanddl-operation.md)

