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
description: El elemento de SID representa el formulario de idioma (SDDL) de definición de descriptor de seguridad del identificador de seguridad (SID) para que la cuenta a utilizar para la suplantación o delegación de acceso.
ms.openlocfilehash: efcea42c12ec1d26ea31fdb8de337c37a2338a96
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837492"
---
# <a name="sid"></a><span data-ttu-id="37b92-103">SID</span><span class="sxs-lookup"><span data-stu-id="37b92-103">SID</span></span>

<span data-ttu-id="37b92-104">El elemento de **SID** representa el formulario de idioma (SDDL) de definición de descriptor de seguridad del identificador de seguridad (SID) para que la cuenta a utilizar para la suplantación o delegación de acceso.</span><span class="sxs-lookup"><span data-stu-id="37b92-104">The **SID** element represents the security descriptor definition language (SDDL) form of the security identifier (SID) for the account to use for impersonation or delegate access.</span></span> 
  
```xml
<SID/>
```

 <span data-ttu-id="37b92-105">**SIDType**</span><span class="sxs-lookup"><span data-stu-id="37b92-105">**SIDType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="37b92-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="37b92-106">Attributes and elements</span></span>

<span data-ttu-id="37b92-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="37b92-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="37b92-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="37b92-108">Attributes</span></span>

<span data-ttu-id="37b92-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="37b92-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="37b92-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="37b92-110">Child elements</span></span>

<span data-ttu-id="37b92-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="37b92-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="37b92-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="37b92-112">Parent elements</span></span>

|<span data-ttu-id="37b92-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="37b92-113">**Element**</span></span>|<span data-ttu-id="37b92-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="37b92-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="37b92-115">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="37b92-115">ConnectingSID</span></span>](connectingsid.md) <br/> |<span data-ttu-id="37b92-116">Representa una cuenta para suplantar a cuando se usa el encabezado SOAP ExchangeImpersonation.</span><span class="sxs-lookup"><span data-stu-id="37b92-116">Represents an account to impersonate when using the ExchangeImpersonation SOAP header.</span></span>  <br/> <span data-ttu-id="37b92-117">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="37b92-117">The following is the XPath expression to this element:</span></span>  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[<span data-ttu-id="37b92-118">UserId</span><span class="sxs-lookup"><span data-stu-id="37b92-118">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="37b92-119">Identifica un usuario delegado o un usuario con permisos de acceso de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="37b92-119">Identifies a delegate user or a user with folder access permissions.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="37b92-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="37b92-120">Text value</span></span>

<span data-ttu-id="37b92-121">El valor de texto es una representación de cadena de un SID.</span><span class="sxs-lookup"><span data-stu-id="37b92-121">The text value is a string representation of a SID.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="37b92-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="37b92-122">Remarks</span></span>

<span data-ttu-id="37b92-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con la función de servidor de acceso de cliente instalada.</span><span class="sxs-lookup"><span data-stu-id="37b92-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="37b92-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="37b92-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="37b92-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="37b92-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="37b92-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="37b92-126">Schema Name</span></span>  <br/> |<span data-ttu-id="37b92-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="37b92-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="37b92-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="37b92-128">Validation File</span></span>  <br/> |<span data-ttu-id="37b92-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="37b92-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="37b92-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="37b92-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="37b92-131">False</span><span class="sxs-lookup"><span data-stu-id="37b92-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="37b92-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="37b92-132">See also</span></span>



- [<span data-ttu-id="37b92-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="37b92-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

