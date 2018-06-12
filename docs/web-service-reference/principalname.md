---
title: PrincipalName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PrincipalName
api_type:
- schema
ms.assetid: 88c142d4-0bc7-43ea-a997-d7200664d900
description: El elemento PrincipalName representa el nombre principal de usuario (UPN) de la cuenta que se usará para la suplantación de Exchange.
ms.openlocfilehash: d8557ce0435a11a5602372517db1f576028a9c97
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836882"
---
# <a name="principalname"></a><span data-ttu-id="5264e-103">PrincipalName</span><span class="sxs-lookup"><span data-stu-id="5264e-103">PrincipalName</span></span>

<span data-ttu-id="5264e-104">El elemento **PrincipalName** representa el nombre principal de usuario (UPN) de la cuenta que se usará para la suplantación de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5264e-104">The **PrincipalName** element represents the user principal name (UPN) of the account to be used for Exchange impersonation.</span></span> 
  
```xml
<PrincipalName/>
```

 <span data-ttu-id="5264e-105">**PrincipalNameType**</span><span class="sxs-lookup"><span data-stu-id="5264e-105">**PrincipalNameType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5264e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5264e-106">Attributes and elements</span></span>

<span data-ttu-id="5264e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5264e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5264e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5264e-108">Attributes</span></span>

<span data-ttu-id="5264e-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5264e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5264e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5264e-110">Child elements</span></span>

<span data-ttu-id="5264e-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5264e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5264e-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5264e-112">Parent elements</span></span>

|<span data-ttu-id="5264e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5264e-113">**Element**</span></span>|<span data-ttu-id="5264e-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5264e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5264e-115">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="5264e-115">ConnectingSID</span></span>](connectingsid.md) <br/> |<span data-ttu-id="5264e-116">Representa una cuenta para suplantar a cuando se usa el encabezado SOAP ExchangeImpersonation.</span><span class="sxs-lookup"><span data-stu-id="5264e-116">Represents an account to impersonate when you are using the ExchangeImpersonation SOAP header.</span></span>  <br/> <span data-ttu-id="5264e-117">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="5264e-117">The following is the XPath expression to this element:</span></span>  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5264e-118">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5264e-118">Text value</span></span>

<span data-ttu-id="5264e-119">El valor de texto representa el UPN de un usuario.</span><span class="sxs-lookup"><span data-stu-id="5264e-119">The text value represents the UPN of a user.</span></span> <span data-ttu-id="5264e-120">Este valor existe en el objeto de usuario en el servicio de directorio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5264e-120">This value exists on the user object in the Active Directory directory service.</span></span> <span data-ttu-id="5264e-121">Contiene el nombre de inicio de sesión de usuario y un nombre de dominio que identifica el dominio en la que la cuenta de usuario se encuentra en el siguiente formato: `someone@example.com`.</span><span class="sxs-lookup"><span data-stu-id="5264e-121">This contains the user logon name and a domain name that identifies the domain in which the user account is located, in the following format:  `someone@example.com`.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5264e-122">Notas</span><span class="sxs-lookup"><span data-stu-id="5264e-122">Remarks</span></span>

<span data-ttu-id="5264e-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="5264e-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5264e-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5264e-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5264e-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5264e-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5264e-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5264e-126">Schema Name</span></span>  <br/> |<span data-ttu-id="5264e-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5264e-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="5264e-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5264e-128">Validation File</span></span>  <br/> |<span data-ttu-id="5264e-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5264e-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5264e-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5264e-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="5264e-131">False</span><span class="sxs-lookup"><span data-stu-id="5264e-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5264e-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="5264e-132">See also</span></span>



- [<span data-ttu-id="5264e-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="5264e-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="5264e-134">Autorización de servidor a servidor en EWS</span><span class="sxs-lookup"><span data-stu-id="5264e-134">Server-to-server authorization in EWS</span></span>](http://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

