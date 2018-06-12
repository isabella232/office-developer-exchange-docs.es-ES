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
description: El elemento UserSid representa el formulario de idioma (SDDL) de definición de descriptor de seguridad del identificador de seguridad de usuario en un encabezado SOAP de contexto de seguridad serializado. No se admite la serialización de token.
ms.openlocfilehash: 3c72f68638f99a4ee5081517027f0834ebf65b49
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840932"
---
# <a name="usersid"></a><span data-ttu-id="aa4c2-104">UserSid</span><span class="sxs-lookup"><span data-stu-id="aa4c2-104">UserSid</span></span>

<span data-ttu-id="aa4c2-105">El elemento **UserSid** representa el formulario de idioma (SDDL) de definición de descriptor de seguridad del identificador de seguridad de usuario en un encabezado SOAP de contexto de seguridad serializado.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-105">The **UserSid** element represents the security descriptor definition language (SDDL) form of the user security identifier in a serialized security context SOAP header.</span></span> <span data-ttu-id="aa4c2-106">No se admite la serialización de token.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-106">Token serialization is not supported.</span></span> 
  
```xml
<UserSid/>
```

 <span data-ttu-id="aa4c2-107">**String**</span><span class="sxs-lookup"><span data-stu-id="aa4c2-107">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aa4c2-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="aa4c2-108">Attributes and elements</span></span>

<span data-ttu-id="aa4c2-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aa4c2-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="aa4c2-110">Attributes</span></span>

<span data-ttu-id="aa4c2-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aa4c2-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="aa4c2-112">Child elements</span></span>

<span data-ttu-id="aa4c2-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="aa4c2-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="aa4c2-114">Parent elements</span></span>

|<span data-ttu-id="aa4c2-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="aa4c2-115">**Element**</span></span>|<span data-ttu-id="aa4c2-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aa4c2-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aa4c2-117">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="aa4c2-117">SerializedSecurityContext</span></span>](serializedsecuritycontext.md) <br/> |<span data-ttu-id="aa4c2-118">Se usa en el encabezado SOAP para la serialización de token de autenticación de servidor a servidor.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-118">Used in the SOAP header for token serialization in server-to-server authentication.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="aa4c2-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="aa4c2-119">Text value</span></span>

<span data-ttu-id="aa4c2-120">El valor de texto representa el identificador de seguridad de un usuario.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-120">The text value represents a user's security identifier.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aa4c2-121">Notas</span><span class="sxs-lookup"><span data-stu-id="aa4c2-121">Remarks</span></span>

<span data-ttu-id="aa4c2-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aa4c2-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="aa4c2-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aa4c2-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="aa4c2-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="aa4c2-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="aa4c2-125">Schema Name</span></span>  <br/> |<span data-ttu-id="aa4c2-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="aa4c2-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="aa4c2-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="aa4c2-127">Validation File</span></span>  <br/> |<span data-ttu-id="aa4c2-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="aa4c2-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="aa4c2-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="aa4c2-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="aa4c2-130">False</span><span class="sxs-lookup"><span data-stu-id="aa4c2-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aa4c2-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="aa4c2-131">See also</span></span>



- [<span data-ttu-id="aa4c2-132">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="aa4c2-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

