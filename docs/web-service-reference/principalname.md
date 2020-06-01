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
description: El elemento PrincipalName representa el nombre principal de usuario (UPN) de la cuenta que se va a usar para la suplantación de Exchange.
ms.openlocfilehash: 31412c1461264e28bf8d52c957a457e8d1e847ef
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44440193"
---
# <a name="principalname"></a><span data-ttu-id="efb09-103">PrincipalName</span><span class="sxs-lookup"><span data-stu-id="efb09-103">PrincipalName</span></span>

<span data-ttu-id="efb09-104">El elemento **PrincipalName** representa el nombre principal de usuario (UPN) de la cuenta que se va a usar para la suplantación de Exchange.</span><span class="sxs-lookup"><span data-stu-id="efb09-104">The **PrincipalName** element represents the user principal name (UPN) of the account to be used for Exchange impersonation.</span></span> 
  
```xml
<PrincipalName/>
```

 <span data-ttu-id="efb09-105">**PrincipalNameType**</span><span class="sxs-lookup"><span data-stu-id="efb09-105">**PrincipalNameType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="efb09-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="efb09-106">Attributes and elements</span></span>

<span data-ttu-id="efb09-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="efb09-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="efb09-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="efb09-108">Attributes</span></span>

<span data-ttu-id="efb09-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="efb09-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="efb09-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="efb09-110">Child elements</span></span>

<span data-ttu-id="efb09-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="efb09-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="efb09-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="efb09-112">Parent elements</span></span>

|<span data-ttu-id="efb09-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="efb09-113">**Element**</span></span>|<span data-ttu-id="efb09-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="efb09-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="efb09-115">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="efb09-115">ConnectingSID</span></span>](connectingsid.md) <br/> |<span data-ttu-id="efb09-116">Representa una cuenta que se va a suplantar cuando se usa el encabezado SOAP ExchangeImpersonation.</span><span class="sxs-lookup"><span data-stu-id="efb09-116">Represents an account to impersonate when you are using the ExchangeImpersonation SOAP header.</span></span>  <br/> <span data-ttu-id="efb09-117">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="efb09-117">The following is the XPath expression to this element:</span></span>  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="efb09-118">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="efb09-118">Text value</span></span>

<span data-ttu-id="efb09-119">El valor de texto representa el UPN de un usuario.</span><span class="sxs-lookup"><span data-stu-id="efb09-119">The text value represents the UPN of a user.</span></span> <span data-ttu-id="efb09-120">Este valor existe en el objeto de usuario del servicio de directorio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="efb09-120">This value exists on the user object in the Active Directory directory service.</span></span> <span data-ttu-id="efb09-121">Contiene el nombre de inicio de sesión del usuario y un nombre de dominio que identifica el dominio en el que se encuentra la cuenta de usuario, con el siguiente formato: `someone@example.com` .</span><span class="sxs-lookup"><span data-stu-id="efb09-121">This contains the user logon name and a domain name that identifies the domain in which the user account is located, in the following format:  `someone@example.com`.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="efb09-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="efb09-122">Remarks</span></span>

<span data-ttu-id="efb09-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="efb09-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="efb09-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="efb09-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="efb09-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="efb09-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="efb09-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="efb09-126">Schema Name</span></span>  <br/> |<span data-ttu-id="efb09-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="efb09-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="efb09-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="efb09-128">Validation File</span></span>  <br/> |<span data-ttu-id="efb09-129">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="efb09-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="efb09-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="efb09-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="efb09-131">Falso</span><span class="sxs-lookup"><span data-stu-id="efb09-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="efb09-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="efb09-132">See also</span></span>



- [<span data-ttu-id="efb09-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="efb09-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="efb09-134">Autorización de servidor a servidor en EWS</span><span class="sxs-lookup"><span data-stu-id="efb09-134">Server-to-server authorization in EWS</span></span>](https://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

