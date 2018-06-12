---
title: AllowExternalOof
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AllowExternalOof
api_type:
- schema
ms.assetid: e5387172-5b92-4bb1-8394-180e9c7ff771
description: El elemento AllowExternalOof contiene un valor que identifica a la que se envían los mensajes externos de fuera de oficina (OOF).
ms.openlocfilehash: 1c87a51676bf6e44b2e650a4e973d0ab89a52e31
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763432"
---
# <a name="allowexternaloof"></a><span data-ttu-id="61afb-103">AllowExternalOof</span><span class="sxs-lookup"><span data-stu-id="61afb-103">AllowExternalOof</span></span>

<span data-ttu-id="61afb-104">El elemento **AllowExternalOof** contiene un valor que identifica a la que se envían los mensajes externos de fuera de oficina (OOF).</span><span class="sxs-lookup"><span data-stu-id="61afb-104">The **AllowExternalOof** element contains a value that identifies to whom external Out of Office (OOF) messages are sent.</span></span> 
  
- [<span data-ttu-id="61afb-105">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="61afb-105">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md)
  
- [<span data-ttu-id="61afb-106">AllowExternalOof</span><span class="sxs-lookup"><span data-stu-id="61afb-106">AllowExternalOof</span></span>](allowexternaloof.md)
  
```xml
<AllowExternalOof>None or Known or All</AllowExternalOof>
```

 <span data-ttu-id="61afb-107">**ExternalAudience**</span><span class="sxs-lookup"><span data-stu-id="61afb-107">**ExternalAudience**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="61afb-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="61afb-108">Attributes and elements</span></span>

<span data-ttu-id="61afb-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="61afb-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="61afb-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="61afb-110">Attributes</span></span>

<span data-ttu-id="61afb-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="61afb-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="61afb-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="61afb-112">Child elements</span></span>

<span data-ttu-id="61afb-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="61afb-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="61afb-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="61afb-114">Parent elements</span></span>

|<span data-ttu-id="61afb-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="61afb-115">**Element**</span></span>|<span data-ttu-id="61afb-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="61afb-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="61afb-117">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="61afb-117">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md) <br/> |<span data-ttu-id="61afb-118">Contiene los resultados de la respuesta y la configuración de fuera de la oficina de un usuario.</span><span class="sxs-lookup"><span data-stu-id="61afb-118">Contains the response results and the OOF settings for a user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="61afb-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="61afb-119">Text value</span></span>

<span data-ttu-id="61afb-120">Un valor de texto es necesario para este elemento.</span><span class="sxs-lookup"><span data-stu-id="61afb-120">A text value is required for this element.</span></span> <span data-ttu-id="61afb-121">En la siguiente tabla se enumera los valores posibles para este elemento.</span><span class="sxs-lookup"><span data-stu-id="61afb-121">The following table lists the possible values for this element.</span></span>
  
|<span data-ttu-id="61afb-122">**Valor**</span><span class="sxs-lookup"><span data-stu-id="61afb-122">**Value**</span></span>|<span data-ttu-id="61afb-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="61afb-123">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="61afb-124">**None**</span><span class="sxs-lookup"><span data-stu-id="61afb-124">**None**</span></span> <br/> |<span data-ttu-id="61afb-125">Los remitentes de correo electrónico fuera de la organización del usuario de buzón de correo que envían mensajes al usuario no recibirá una respuesta de mensaje de fuera de la oficina externa.</span><span class="sxs-lookup"><span data-stu-id="61afb-125">E-mail senders outside the mailbox user's organization who send messages to the user will not receive an external OOF message response.</span></span>  <br/> |
|<span data-ttu-id="61afb-126">**Conocidos**</span><span class="sxs-lookup"><span data-stu-id="61afb-126">**Known**</span></span> <br/> |<span data-ttu-id="61afb-127">Los remitentes de correo electrónico fuera de la organización del usuario de buzón de correo que envían mensajes al usuario sólo recibirá una respuesta de mensaje de fuera de la oficina externa si el remitente está en Exchange del usuario almacenan la lista de contactos.</span><span class="sxs-lookup"><span data-stu-id="61afb-127">E-mail senders outside the mailbox user's organization who send messages to the user will only receive an external OOF message response if the sender is in the user's Exchange store contact list.</span></span>  <br/> |
|<span data-ttu-id="61afb-128">**All**</span><span class="sxs-lookup"><span data-stu-id="61afb-128">**All**</span></span> <br/> |<span data-ttu-id="61afb-129">Los remitentes de correo electrónico fuera de la organización del usuario de buzón de correo que envían mensajes al usuario recibirá una respuesta de mensaje de fuera de la oficina externa.</span><span class="sxs-lookup"><span data-stu-id="61afb-129">E-mail senders outside the mailbox user's organization who send messages to the user will receive an external OOF message response.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61afb-130">Notas</span><span class="sxs-lookup"><span data-stu-id="61afb-130">Remarks</span></span>

<span data-ttu-id="61afb-131">Este elemento comparte el mismo tipo que el elemento [ExternalAudience](externalaudience.md) .</span><span class="sxs-lookup"><span data-stu-id="61afb-131">This element shares the same type as the [ExternalAudience](externalaudience.md) element.</span></span> 
  
<span data-ttu-id="61afb-132">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="61afb-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="61afb-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="61afb-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61afb-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="61afb-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="61afb-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="61afb-135">Schema Name</span></span>  <br/> |<span data-ttu-id="61afb-136">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="61afb-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="61afb-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="61afb-137">Validation File</span></span>  <br/> |<span data-ttu-id="61afb-138">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="61afb-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="61afb-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="61afb-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="61afb-140">False</span><span class="sxs-lookup"><span data-stu-id="61afb-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="61afb-141">Ver también</span><span class="sxs-lookup"><span data-stu-id="61afb-141">See also</span></span>

- [<span data-ttu-id="61afb-142">Operación GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="61afb-142">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md) 
- [<span data-ttu-id="61afb-143">Operación SetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="61afb-143">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

