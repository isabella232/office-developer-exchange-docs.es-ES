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
description: El elemento ExchangeImpersonation se usa en el encabezado SOAP de una solicitud. Cuando este elemento está presente, el autor de la llamada está intentando suplantar la cuenta contenida en el elemento ExchangeImpersonation.
ms.openlocfilehash: 188219d95453dc45378c6ca65ab93c2de7db4eac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463352"
---
# <a name="exchangeimpersonation"></a><span data-ttu-id="ada41-104">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="ada41-104">ExchangeImpersonation</span></span>

<span data-ttu-id="ada41-105">El elemento **ExchangeImpersonation** se usa en el encabezado SOAP de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="ada41-105">The **ExchangeImpersonation** element is used in the SOAP header of a request.</span></span> <span data-ttu-id="ada41-106">Cuando este elemento está presente, el autor de la llamada está intentando suplantar la cuenta contenida en el elemento **ExchangeImpersonation** .</span><span class="sxs-lookup"><span data-stu-id="ada41-106">When this element is present, the caller is trying to impersonate the account that is contained within the **ExchangeImpersonation** element.</span></span> 
  
[<span data-ttu-id="ada41-107">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="ada41-107">ExchangeImpersonation</span></span>](exchangeimpersonation.md)
  
```xml
<ExchangeImpersonation>
   <ConnectingSID/>
</ExchangeImpersonation>
```

 <span data-ttu-id="ada41-108">**ExchangeImpersonationType**</span><span class="sxs-lookup"><span data-stu-id="ada41-108">**ExchangeImpersonationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ada41-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ada41-109">Attributes and elements</span></span>

<span data-ttu-id="ada41-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ada41-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ada41-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="ada41-111">Attributes</span></span>

<span data-ttu-id="ada41-112">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ada41-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ada41-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ada41-113">Child elements</span></span>

|<span data-ttu-id="ada41-114">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ada41-114">**Element**</span></span>|<span data-ttu-id="ada41-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ada41-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ada41-116">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="ada41-116">ConnectingSID</span></span>](connectingsid.md) <br/> |<span data-ttu-id="ada41-117">Representa una cuenta que se va a suplantar cuando se usa el encabezado SOAP ExchangeImpersonation.</span><span class="sxs-lookup"><span data-stu-id="ada41-117">Represents an account to impersonate when you are using the ExchangeImpersonation SOAP header.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ada41-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ada41-118">Parent elements</span></span>

<span data-ttu-id="ada41-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ada41-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ada41-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ada41-120">Remarks</span></span>

<span data-ttu-id="ada41-121">La cuenta de llamada debe tener el derecho **MS-Exch-Impersonation** en el servidor de acceso de cliente y el derecho **MS-Exch-MayImpersonate** en la base de datos de buzones de correo que contiene el buzón de correo para la suplantación o el objeto de contacto o de usuario de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ada41-121">The calling account must have the **ms-exch-impersonation** right on the Client Access server and the **ms-exch-MayImpersonate** right on either the mailbox database that contains the mailbox to impersonate or the Active Directory User/Contact object.</span></span> 
  
<span data-ttu-id="ada41-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="ada41-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ada41-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ada41-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ada41-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="ada41-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ada41-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ada41-125">Schema name</span></span>  <br/> |<span data-ttu-id="ada41-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ada41-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="ada41-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ada41-127">Validation file</span></span>  <br/> |<span data-ttu-id="ada41-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="ada41-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ada41-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ada41-129">Can be empty</span></span>  <br/> |<span data-ttu-id="ada41-130">Falso</span><span class="sxs-lookup"><span data-stu-id="ada41-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ada41-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="ada41-131">See also</span></span>



[<span data-ttu-id="ada41-132">Autorización de servidor a servidor en EWS</span><span class="sxs-lookup"><span data-stu-id="ada41-132">Server-to-server authorization in EWS</span></span>](https://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

