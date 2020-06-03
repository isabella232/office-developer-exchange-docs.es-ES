---
title: UserSid
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserSid
api_type:
- schema
ms.assetid: f8a0dcd9-8564-4e35-b307-c5d2761b48d8
description: El elemento UserSid representa el formato de lenguaje de definición de descriptores de seguridad (SDDL) del identificador de seguridad de usuario en un encabezado SOAP de contexto de seguridad serializado. No se admite la serialización de tokens.
ms.openlocfilehash: b8ee51b1998546fc4ab14bd3666192ae63c8dba8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462020"
---
# <a name="usersid"></a><span data-ttu-id="6d1b7-104">UserSid</span><span class="sxs-lookup"><span data-stu-id="6d1b7-104">UserSid</span></span>

<span data-ttu-id="6d1b7-105">El elemento **UserSid** representa el formato de lenguaje de definición de descriptores de seguridad (SDDL) del identificador de seguridad de usuario en un encabezado SOAP de contexto de seguridad serializado.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-105">The **UserSid** element represents the security descriptor definition language (SDDL) form of the user security identifier in a serialized security context SOAP header.</span></span> <span data-ttu-id="6d1b7-106">No se admite la serialización de tokens.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-106">Token serialization is not supported.</span></span> 
  
```xml
<UserSid/>
```

 <span data-ttu-id="6d1b7-107">**String**</span><span class="sxs-lookup"><span data-stu-id="6d1b7-107">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6d1b7-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6d1b7-108">Attributes and elements</span></span>

<span data-ttu-id="6d1b7-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6d1b7-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="6d1b7-110">Attributes</span></span>

<span data-ttu-id="6d1b7-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6d1b7-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6d1b7-112">Child elements</span></span>

<span data-ttu-id="6d1b7-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6d1b7-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6d1b7-114">Parent elements</span></span>

|<span data-ttu-id="6d1b7-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6d1b7-115">**Element**</span></span>|<span data-ttu-id="6d1b7-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6d1b7-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6d1b7-117">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="6d1b7-117">SerializedSecurityContext</span></span>](serializedsecuritycontext.md) <br/> |<span data-ttu-id="6d1b7-118">Se usa en el encabezado SOAP para la serialización de tokens en la autenticación de servidor a servidor.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-118">Used in the SOAP header for token serialization in server-to-server authentication.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6d1b7-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="6d1b7-119">Text value</span></span>

<span data-ttu-id="6d1b7-120">El valor de texto representa el identificador de seguridad de un usuario.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-120">The text value represents a user's security identifier.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6d1b7-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6d1b7-121">Remarks</span></span>

<span data-ttu-id="6d1b7-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6d1b7-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6d1b7-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6d1b7-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="6d1b7-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6d1b7-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6d1b7-125">Schema Name</span></span>  <br/> |<span data-ttu-id="6d1b7-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="6d1b7-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="6d1b7-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6d1b7-127">Validation File</span></span>  <br/> |<span data-ttu-id="6d1b7-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="6d1b7-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6d1b7-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6d1b7-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="6d1b7-130">Falso</span><span class="sxs-lookup"><span data-stu-id="6d1b7-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6d1b7-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d1b7-131">See also</span></span>



- [<span data-ttu-id="6d1b7-132">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6d1b7-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

