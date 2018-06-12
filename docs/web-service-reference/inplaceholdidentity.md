---
title: InPlaceHoldIdentity
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 54f45774-00a0-4392-af1b-8c5f2208a53f
description: El elemento InPlaceHoldIdentity especifica la identidad de una suspensión que conserva los elementos del buzón de correo.
ms.openlocfilehash: 954e6ad6c3e0b7786d6bbb8230dba913a32359bc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835938"
---
# <a name="inplaceholdidentity"></a><span data-ttu-id="07698-103">InPlaceHoldIdentity</span><span class="sxs-lookup"><span data-stu-id="07698-103">InPlaceHoldIdentity</span></span>

<span data-ttu-id="07698-104">El elemento **InPlaceHoldIdentity** especifica la identidad de una suspensión que conserva los elementos del buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="07698-104">The **InPlaceHoldIdentity** element specifies the identity of a hold that preserves the mailbox items.</span></span> 
  
```XML
<InPlaceHoldIdentity></InPlaceHoldIdentity>
```

 <span data-ttu-id="07698-105">**string**</span><span class="sxs-lookup"><span data-stu-id="07698-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="07698-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="07698-106">Attributes and elements</span></span>

<span data-ttu-id="07698-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="07698-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="07698-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="07698-108">Attributes</span></span>

<span data-ttu-id="07698-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="07698-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="07698-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="07698-110">Child elements</span></span>

<span data-ttu-id="07698-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="07698-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="07698-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="07698-112">Parent elements</span></span>

<span data-ttu-id="07698-113">[SetHoldOnMailboxes](setholdonmailboxes.md) | [DiscoverySearchConfiguration](discoverysearchconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="07698-113">[SetHoldOnMailboxes](setholdonmailboxes.md) | [DiscoverySearchConfiguration](discoverysearchconfiguration.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="07698-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="07698-114">Text value</span></span>

<span data-ttu-id="07698-115">El valor de texto del elemento **InPlaceHoldIdentity** es el identificador de espera de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="07698-115">The text value of the **InPlaceHoldIdentity** element is the mailbox hold identifier.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="07698-116">Notas</span><span class="sxs-lookup"><span data-stu-id="07698-116">Remarks</span></span>

<span data-ttu-id="07698-117">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="07698-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="07698-118">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="07698-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="07698-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="07698-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="07698-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="07698-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="07698-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="07698-121">Schema name</span></span>  <br/> |<span data-ttu-id="07698-122">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="07698-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="07698-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="07698-123">Validation file</span></span>  <br/> |<span data-ttu-id="07698-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="07698-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="07698-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="07698-125">Can be empty</span></span>  <br/> |<span data-ttu-id="07698-126">False</span><span class="sxs-lookup"><span data-stu-id="07698-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="07698-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="07698-127">See also</span></span>



[<span data-ttu-id="07698-128">Operación SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="07698-128">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)


- [<span data-ttu-id="07698-129">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="07698-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

