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
description: El elemento AllowExternalOof contiene un valor que identifica a quién se envían los mensajes fuera de la oficina (OOF) externos.
ms.openlocfilehash: e4934bc4bc86e1f9f764279a13ecaeca073d9e5d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464815"
---
# <a name="allowexternaloof"></a><span data-ttu-id="603f9-103">AllowExternalOof</span><span class="sxs-lookup"><span data-stu-id="603f9-103">AllowExternalOof</span></span>

<span data-ttu-id="603f9-104">El elemento **AllowExternalOof** contiene un valor que identifica a quién se envían los mensajes fuera de la oficina (OOF) externos.</span><span class="sxs-lookup"><span data-stu-id="603f9-104">The **AllowExternalOof** element contains a value that identifies to whom external Out of Office (OOF) messages are sent.</span></span> 
  
- [<span data-ttu-id="603f9-105">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="603f9-105">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md)
  
- [<span data-ttu-id="603f9-106">AllowExternalOof</span><span class="sxs-lookup"><span data-stu-id="603f9-106">AllowExternalOof</span></span>](allowexternaloof.md)
  
```xml
<AllowExternalOof>None or Known or All</AllowExternalOof>
```

 <span data-ttu-id="603f9-107">**ExternalAudience**</span><span class="sxs-lookup"><span data-stu-id="603f9-107">**ExternalAudience**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="603f9-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="603f9-108">Attributes and elements</span></span>

<span data-ttu-id="603f9-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="603f9-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="603f9-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="603f9-110">Attributes</span></span>

<span data-ttu-id="603f9-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="603f9-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="603f9-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="603f9-112">Child elements</span></span>

<span data-ttu-id="603f9-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="603f9-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="603f9-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="603f9-114">Parent elements</span></span>

|<span data-ttu-id="603f9-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="603f9-115">**Element**</span></span>|<span data-ttu-id="603f9-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="603f9-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="603f9-117">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="603f9-117">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md) <br/> |<span data-ttu-id="603f9-118">Contiene los resultados de la respuesta y la configuración de OOF para un usuario.</span><span class="sxs-lookup"><span data-stu-id="603f9-118">Contains the response results and the OOF settings for a user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="603f9-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="603f9-119">Text value</span></span>

<span data-ttu-id="603f9-120">Se requiere un valor de texto para este elemento.</span><span class="sxs-lookup"><span data-stu-id="603f9-120">A text value is required for this element.</span></span> <span data-ttu-id="603f9-121">En la siguiente tabla se enumeran los valores posibles para este elemento.</span><span class="sxs-lookup"><span data-stu-id="603f9-121">The following table lists the possible values for this element.</span></span>
  
|<span data-ttu-id="603f9-122">**Valor**</span><span class="sxs-lookup"><span data-stu-id="603f9-122">**Value**</span></span>|<span data-ttu-id="603f9-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="603f9-123">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="603f9-124">**Ninguno**</span><span class="sxs-lookup"><span data-stu-id="603f9-124">**None**</span></span> <br/> |<span data-ttu-id="603f9-125">Los remitentes de correo electrónico que se encuentran fuera de la organización del usuario del buzón que envían mensajes al usuario no recibirán una respuesta de mensaje OOF externa.</span><span class="sxs-lookup"><span data-stu-id="603f9-125">E-mail senders outside the mailbox user's organization who send messages to the user will not receive an external OOF message response.</span></span>  <br/> |
|<span data-ttu-id="603f9-126">**Válida**</span><span class="sxs-lookup"><span data-stu-id="603f9-126">**Known**</span></span> <br/> |<span data-ttu-id="603f9-127">Los remitentes de correo electrónico que se encuentran fuera de la organización del usuario del buzón de correo que envían mensajes al usuario solo recibirán una respuesta de mensaje de OOF externa si el remitente está en la lista de contactos del almacén de Exchange del usuario.</span><span class="sxs-lookup"><span data-stu-id="603f9-127">E-mail senders outside the mailbox user's organization who send messages to the user will only receive an external OOF message response if the sender is in the user's Exchange store contact list.</span></span>  <br/> |
|<span data-ttu-id="603f9-128">**All**</span><span class="sxs-lookup"><span data-stu-id="603f9-128">**All**</span></span> <br/> |<span data-ttu-id="603f9-129">Los remitentes de correo electrónico que se encuentran fuera de la organización del usuario del buzón de correo que envían mensajes al usuario recibirán una respuesta de mensaje OOF externa.</span><span class="sxs-lookup"><span data-stu-id="603f9-129">E-mail senders outside the mailbox user's organization who send messages to the user will receive an external OOF message response.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="603f9-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="603f9-130">Remarks</span></span>

<span data-ttu-id="603f9-131">Este elemento comparte el mismo tipo que el elemento [ExternalAudience](externalaudience.md) .</span><span class="sxs-lookup"><span data-stu-id="603f9-131">This element shares the same type as the [ExternalAudience](externalaudience.md) element.</span></span> 
  
<span data-ttu-id="603f9-132">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="603f9-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="603f9-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="603f9-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="603f9-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="603f9-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="603f9-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="603f9-135">Schema Name</span></span>  <br/> |<span data-ttu-id="603f9-136">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="603f9-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="603f9-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="603f9-137">Validation File</span></span>  <br/> |<span data-ttu-id="603f9-138">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="603f9-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="603f9-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="603f9-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="603f9-140">Falso</span><span class="sxs-lookup"><span data-stu-id="603f9-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="603f9-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="603f9-141">See also</span></span>

- [<span data-ttu-id="603f9-142">Operación GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="603f9-142">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md) 
- [<span data-ttu-id="603f9-143">Operación SetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="603f9-143">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

