---
title: SID
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SID
api_type:
- schema
ms.assetid: 2f33b29b-163b-4106-a74d-6fb76ec38951
description: El elemento SID representa el formato de lenguaje de definición de descriptores de seguridad (SDDL) del identificador de seguridad (SID) de la cuenta que se va a usar para la suplantación o el acceso delegado.
ms.openlocfilehash: 0e3f740e9a056f7c0042049d97757b5f2d3c441d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468050"
---
# <a name="sid"></a><span data-ttu-id="1a9ba-103">SID</span><span class="sxs-lookup"><span data-stu-id="1a9ba-103">SID</span></span>

<span data-ttu-id="1a9ba-104">El elemento **SID** representa el formato de lenguaje de definición de descriptores de seguridad (SDDL) del identificador de seguridad (SID) de la cuenta que se va a usar para la suplantación o el acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="1a9ba-104">The **SID** element represents the security descriptor definition language (SDDL) form of the security identifier (SID) for the account to use for impersonation or delegate access.</span></span> 
  
```xml
<SID/>
```

 <span data-ttu-id="1a9ba-105">**SIDType**</span><span class="sxs-lookup"><span data-stu-id="1a9ba-105">**SIDType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1a9ba-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1a9ba-106">Attributes and elements</span></span>

<span data-ttu-id="1a9ba-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1a9ba-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1a9ba-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1a9ba-108">Attributes</span></span>

<span data-ttu-id="1a9ba-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1a9ba-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1a9ba-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1a9ba-110">Child elements</span></span>

<span data-ttu-id="1a9ba-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1a9ba-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1a9ba-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1a9ba-112">Parent elements</span></span>

|<span data-ttu-id="1a9ba-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1a9ba-113">**Element**</span></span>|<span data-ttu-id="1a9ba-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1a9ba-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1a9ba-115">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="1a9ba-115">ConnectingSID</span></span>](connectingsid.md) <br/> |<span data-ttu-id="1a9ba-116">Representa una cuenta que se va a suplantar al usar el encabezado SOAP ExchangeImpersonation.</span><span class="sxs-lookup"><span data-stu-id="1a9ba-116">Represents an account to impersonate when using the ExchangeImpersonation SOAP header.</span></span>  <br/> <span data-ttu-id="1a9ba-117">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="1a9ba-117">The following is the XPath expression to this element:</span></span>  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[<span data-ttu-id="1a9ba-118">UserId</span><span class="sxs-lookup"><span data-stu-id="1a9ba-118">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="1a9ba-119">Identifica un usuario delegado o un usuario con permisos de acceso a la carpeta.</span><span class="sxs-lookup"><span data-stu-id="1a9ba-119">Identifies a delegate user or a user with folder access permissions.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1a9ba-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="1a9ba-120">Text value</span></span>

<span data-ttu-id="1a9ba-121">El valor de texto es una representación de cadena de un SID.</span><span class="sxs-lookup"><span data-stu-id="1a9ba-121">The text value is a string representation of a SID.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1a9ba-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1a9ba-122">Remarks</span></span>

<span data-ttu-id="1a9ba-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con el rol de servidor acceso de clientes instalado.</span><span class="sxs-lookup"><span data-stu-id="1a9ba-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1a9ba-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1a9ba-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1a9ba-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="1a9ba-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1a9ba-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1a9ba-126">Schema Name</span></span>  <br/> |<span data-ttu-id="1a9ba-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="1a9ba-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="1a9ba-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1a9ba-128">Validation File</span></span>  <br/> |<span data-ttu-id="1a9ba-129">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="1a9ba-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1a9ba-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1a9ba-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="1a9ba-131">Falso</span><span class="sxs-lookup"><span data-stu-id="1a9ba-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1a9ba-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a9ba-132">See also</span></span>



- [<span data-ttu-id="1a9ba-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1a9ba-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

