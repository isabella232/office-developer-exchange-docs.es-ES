---
title: ExchangeImpersonation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExchangeImpersonation
api_type:
- schema
ms.assetid: d8cbac49-47d0-4745-a2a7-545d33f8da93
description: El elemento ExchangeImpersonation se usa en el encabezado SOAP de una solicitud. Cuando este elemento está presente, el autor de la llamada está intentando suplantar la cuenta que está incluida dentro del elemento ExchangeImpersonation.
ms.openlocfilehash: aedeff22cda865ce1eec80dab9760d49fdc178f7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764473"
---
# <a name="exchangeimpersonation"></a><span data-ttu-id="c735f-104">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="c735f-104">ExchangeImpersonation</span></span>

<span data-ttu-id="c735f-105">El elemento **ExchangeImpersonation** se usa en el encabezado SOAP de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="c735f-105">The **ExchangeImpersonation** element is used in the SOAP header of a request.</span></span> <span data-ttu-id="c735f-106">Cuando este elemento está presente, el autor de la llamada está intentando suplantar la cuenta que está incluida dentro del elemento **ExchangeImpersonation** .</span><span class="sxs-lookup"><span data-stu-id="c735f-106">When this element is present, the caller is trying to impersonate the account that is contained within the **ExchangeImpersonation** element.</span></span> 
  
[<span data-ttu-id="c735f-107">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="c735f-107">ExchangeImpersonation</span></span>](exchangeimpersonation.md)
  
```xml
<ExchangeImpersonation>
   <ConnectingSID/>
</ExchangeImpersonation>
```

 <span data-ttu-id="c735f-108">**ExchangeImpersonationType**</span><span class="sxs-lookup"><span data-stu-id="c735f-108">**ExchangeImpersonationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c735f-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c735f-109">Attributes and elements</span></span>

<span data-ttu-id="c735f-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c735f-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c735f-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="c735f-111">Attributes</span></span>

<span data-ttu-id="c735f-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c735f-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c735f-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c735f-113">Child elements</span></span>

|<span data-ttu-id="c735f-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="c735f-114">**Element**</span></span>|<span data-ttu-id="c735f-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c735f-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c735f-116">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="c735f-116">ConnectingSID</span></span>](connectingsid.md) <br/> |<span data-ttu-id="c735f-117">Representa una cuenta para suplantar a cuando se usa el encabezado SOAP ExchangeImpersonation.</span><span class="sxs-lookup"><span data-stu-id="c735f-117">Represents an account to impersonate when you are using the ExchangeImpersonation SOAP header.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c735f-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c735f-118">Parent elements</span></span>

<span data-ttu-id="c735f-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c735f-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c735f-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c735f-120">Remarks</span></span>

<span data-ttu-id="c735f-121">La cuenta que realiza la llamada debe tener la **ms-exch-impersonation** derecha en el servidor de acceso de cliente y el **ms-exch-MayImpersonate** derecho en ya sea la base de datos de buzón de correo que contiene el buzón de correo para suplantar o el usuario o contacto de directorio activo objeto.</span><span class="sxs-lookup"><span data-stu-id="c735f-121">The calling account must have the **ms-exch-impersonation** right on the Client Access server and the **ms-exch-MayImpersonate** right on either the mailbox database that contains the mailbox to impersonate or the Active Directory User/Contact object.</span></span> 
  
<span data-ttu-id="c735f-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="c735f-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c735f-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c735f-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c735f-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c735f-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c735f-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c735f-125">Schema name</span></span>  <br/> |<span data-ttu-id="c735f-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c735f-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="c735f-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c735f-127">Validation file</span></span>  <br/> |<span data-ttu-id="c735f-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c735f-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c735f-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c735f-129">Can be empty</span></span>  <br/> |<span data-ttu-id="c735f-130">False</span><span class="sxs-lookup"><span data-stu-id="c735f-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c735f-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="c735f-131">See also</span></span>



[<span data-ttu-id="c735f-132">Autorización de servidor a servidor en EWS</span><span class="sxs-lookup"><span data-stu-id="c735f-132">Server-to-server authorization in EWS</span></span>](http://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

