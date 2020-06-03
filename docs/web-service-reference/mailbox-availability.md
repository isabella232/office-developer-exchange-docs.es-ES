---
title: Buzón de correo (disponibilidad)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Mailbox
api_type:
- schema
ms.assetid: affd192e-8914-473f-9098-d9bdf898de2c
description: El elemento Mailbox representa al usuario del buzón de correo para una solicitud SetUserOofSettings o GetUserOofSettings.
ms.openlocfilehash: 1bda6e8b90551b86b4e1c2711ac25693a65e5410
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458078"
---
# <a name="mailbox-availability"></a><span data-ttu-id="392e8-103">Buzón de correo (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="392e8-103">Mailbox (Availability)</span></span>

<span data-ttu-id="392e8-104">El elemento **Mailbox** representa al usuario del buzón de correo para una solicitud SetUserOofSettings o GetUserOofSettings.</span><span class="sxs-lookup"><span data-stu-id="392e8-104">The **Mailbox** element represents the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span> 
  
```xml
<Mailbox>
   <Name>...</Name>
   <Address>...</Address>
   <RoutingType>...</RoutingType>
</Mailbox>
```

<span data-ttu-id="392e8-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="392e8-105">**EmailAddressType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="392e8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="392e8-106">Attributes and elements</span></span>

<span data-ttu-id="392e8-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="392e8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="392e8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="392e8-108">Attributes</span></span>

<span data-ttu-id="392e8-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="392e8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="392e8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="392e8-110">Child elements</span></span>

|<span data-ttu-id="392e8-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="392e8-111">**Element**</span></span>|<span data-ttu-id="392e8-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="392e8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="392e8-113">Nombre (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="392e8-113">Name (EmailAddress)</span></span>](name-emailaddress.md) <br/> |<span data-ttu-id="392e8-114">Representa el nombre para mostrar del usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="392e8-114">Represents the display name of the mailbox user.</span></span> <span data-ttu-id="392e8-115">Este elemento es opcional en SetUserOofSettingsRequest.</span><span class="sxs-lookup"><span data-stu-id="392e8-115">This element is optional in the SetUserOofSettingsRequest.</span></span> <span data-ttu-id="392e8-116">GetUserOofSettingsRequest devolverá este elemento.</span><span class="sxs-lookup"><span data-stu-id="392e8-116">The GetUserOofSettingsRequest will return this element.</span></span>  <br/> |
|[<span data-ttu-id="392e8-117">Address (cadena)</span><span class="sxs-lookup"><span data-stu-id="392e8-117">Address (string)</span></span>](address-string.md) <br/> |<span data-ttu-id="392e8-118">Representa la dirección de correo electrónico del usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="392e8-118">Represents the e-mail address of the mailbox user.</span></span> <span data-ttu-id="392e8-119">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="392e8-119">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="392e8-120">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="392e8-120">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="392e8-121">Representa el protocolo de enrutamiento para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="392e8-121">Represents the routing protocol for the message.</span></span> <span data-ttu-id="392e8-122">Este elemento es opcional en SetUserOofSettingsRequest.</span><span class="sxs-lookup"><span data-stu-id="392e8-122">This element is optional in the SetUserOofSettingsRequest.</span></span> <span data-ttu-id="392e8-123">GetUserOofSettingsRequest devolverá este elemento.</span><span class="sxs-lookup"><span data-stu-id="392e8-123">The GetUserOofSettingsRequest will return this element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="392e8-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="392e8-124">Parent elements</span></span>

|<span data-ttu-id="392e8-125">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="392e8-125">**Element**</span></span>|<span data-ttu-id="392e8-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="392e8-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="392e8-127">GetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="392e8-127">GetUserOofSettingsRequest</span></span>](getuseroofsettingsrequest.md) <br/> |<span data-ttu-id="392e8-128">Se usa para obtener los mensajes y la configuración de fuera de la oficina (OOF) del usuario de un buzón.</span><span class="sxs-lookup"><span data-stu-id="392e8-128">Used to get a mailbox user's Out of Office (OOF) settings and messages.</span></span>  <br/> <span data-ttu-id="392e8-129">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="392e8-129">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserOofSettingsRequest` <br/> |
|[<span data-ttu-id="392e8-130">SetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="392e8-130">SetUserOofSettingsRequest</span></span>](setuseroofsettingsrequest.md) <br/> |<span data-ttu-id="392e8-131">Se usa para establecer los mensajes y la configuración OOF de un usuario de buzón.</span><span class="sxs-lookup"><span data-stu-id="392e8-131">Used to set a mailbox user's OOF settings and messages.</span></span>  <br/> <span data-ttu-id="392e8-132">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="392e8-132">The following is the XPath expression to this element:</span></span>  <br/>  `/SetUserOofSettingsRequest` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="392e8-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="392e8-133">Remarks</span></span>

<span data-ttu-id="392e8-134">La dirección de correo electrónico se usa para identificar la carpeta de calendario que contiene la configuración de OOF.</span><span class="sxs-lookup"><span data-stu-id="392e8-134">The e-mail address is used to identify the calendar folder that contains the OOF settings.</span></span> 
  
<span data-ttu-id="392e8-135">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="392e8-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="392e8-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="392e8-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="392e8-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="392e8-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="392e8-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="392e8-138">Schema Name</span></span>  <br/> |<span data-ttu-id="392e8-139">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="392e8-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="392e8-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="392e8-140">Validation File</span></span>  <br/> |<span data-ttu-id="392e8-141">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="392e8-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="392e8-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="392e8-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="392e8-143">Falso</span><span class="sxs-lookup"><span data-stu-id="392e8-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="392e8-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="392e8-144">See also</span></span>

- [<span data-ttu-id="392e8-145">Operación GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="392e8-145">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
- [<span data-ttu-id="392e8-146">Operación SetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="392e8-146">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

