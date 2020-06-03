---
title: GetPasswordExpirationDateResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3d3fff1f-ef13-46d5-bd7f-ef535eb80c72
description: El elemento GetPasswordExpirationDateResponse define la respuesta a una solicitud de operación de operación de GetPasswordExpirationDate.
ms.openlocfilehash: c925b2b37879ba0f8f25b2dd73737ed2f3202555
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530207"
---
# <a name="getpasswordexpirationdateresponse"></a><span data-ttu-id="acb8a-103">GetPasswordExpirationDateResponse</span><span class="sxs-lookup"><span data-stu-id="acb8a-103">GetPasswordExpirationDateResponse</span></span>

<span data-ttu-id="acb8a-104">El elemento **GetPasswordExpirationDateResponse** define la respuesta a una solicitud de operación de [operación de GetPasswordExpirationDate](getpasswordexpirationdate-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="acb8a-104">The **GetPasswordExpirationDateResponse** element defines the response to a [GetPasswordExpirationDate operation](getpasswordexpirationdate-operation.md) operation request.</span></span> 
  
- [<span data-ttu-id="acb8a-105">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="acb8a-105">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="acb8a-106">GetPasswordExpirationDateResponse</span><span class="sxs-lookup"><span data-stu-id="acb8a-106">GetPasswordExpirationDateResponse</span></span>](getpasswordexpirationdateresponse.md)
  
```XML
<GetPasswordExpirationDateResponse>
    <PasswordExpirationDate />
</GetPasswordExpirationDateResponse>
```

 <span data-ttu-id="acb8a-107">**GetPasswordExpirationDateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="acb8a-107">**GetPasswordExpirationDateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="acb8a-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="acb8a-108">Attributes and elements</span></span>

<span data-ttu-id="acb8a-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="acb8a-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="acb8a-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="acb8a-110">Attributes</span></span>

|<span data-ttu-id="acb8a-111">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="acb8a-111">**Attribute**</span></span>|<span data-ttu-id="acb8a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="acb8a-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="acb8a-113">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="acb8a-113">**ResponseClass**</span></span> <br/> | <span data-ttu-id="acb8a-114">Describe el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="acb8a-114">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="acb8a-115">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="acb8a-115">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="acb8a-116">-Correcto</span><span class="sxs-lookup"><span data-stu-id="acb8a-116">-  Success</span></span>  <br/><span data-ttu-id="acb8a-117">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="acb8a-117">-  Warning</span></span>  <br/><span data-ttu-id="acb8a-118">-Error</span><span class="sxs-lookup"><span data-stu-id="acb8a-118">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="acb8a-119">Valores del atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="acb8a-119">ResponseClass attribute values</span></span>

|<span data-ttu-id="acb8a-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="acb8a-120">**Value**</span></span>|<span data-ttu-id="acb8a-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="acb8a-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="acb8a-122">**Success**</span><span class="sxs-lookup"><span data-stu-id="acb8a-122">**Success**</span></span> <br/> |<span data-ttu-id="acb8a-123">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="acb8a-123">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="acb8a-124">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="acb8a-124">**Warning**</span></span> <br/> | <span data-ttu-id="acb8a-125">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="acb8a-125">Describes a request that was not processed.</span></span> <span data-ttu-id="acb8a-126">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="acb8a-126">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="acb8a-127">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="acb8a-127">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="acb8a-128">-El almacén de Exchange está sin conexión durante el lote.</span><span class="sxs-lookup"><span data-stu-id="acb8a-128">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="acb8a-129">-Los servicios de dominio de Active Directory (AD DS) están sin conexión.</span><span class="sxs-lookup"><span data-stu-id="acb8a-129">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="acb8a-130">-Se movieron los buzones.</span><span class="sxs-lookup"><span data-stu-id="acb8a-130">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="acb8a-131">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="acb8a-131">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="acb8a-132">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="acb8a-132">-  A password is expired.</span></span>  <br/><span data-ttu-id="acb8a-133">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="acb8a-133">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="acb8a-134">**Error**</span><span class="sxs-lookup"><span data-stu-id="acb8a-134">**Error**</span></span> <br/> | <span data-ttu-id="acb8a-135">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="acb8a-135">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="acb8a-136">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="acb8a-136">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="acb8a-137">-Atributos o elementos no válidos.</span><span class="sxs-lookup"><span data-stu-id="acb8a-137">-  Invalid attributes or elements.</span></span>  <br/><span data-ttu-id="acb8a-138">-Atributos o elementos que están fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="acb8a-138">-  Attributes or elements that are out of range.</span></span>  <br/><span data-ttu-id="acb8a-139">-Una etiqueta desconocida.</span><span class="sxs-lookup"><span data-stu-id="acb8a-139">-  An unknown tag.</span></span>  <br/><span data-ttu-id="acb8a-140">: Un atributo o elemento que no es válido en el contexto.</span><span class="sxs-lookup"><span data-stu-id="acb8a-140">-  An attribute or element that is not valid in the context.</span></span>  <br/><span data-ttu-id="acb8a-141">-Un intento de acceso no autorizado por parte de cualquier cliente.</span><span class="sxs-lookup"><span data-stu-id="acb8a-141">-  An unauthorized access attempt by any client.</span></span>  <br/><span data-ttu-id="acb8a-142">-Un error del servidor en respuesta a una llamada válida del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="acb8a-142">-  A server-side failure in response to a valid client-side call.</span></span>  <br/><br/>  <span data-ttu-id="acb8a-143">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="acb8a-143">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="acb8a-144">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="acb8a-144">Child elements</span></span>

|<span data-ttu-id="acb8a-145">**Nombre del elemento**</span><span class="sxs-lookup"><span data-stu-id="acb8a-145">**Element name**</span></span>|<span data-ttu-id="acb8a-146">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="acb8a-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="acb8a-147">PasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="acb8a-147">PasswordExpirationDate</span></span>](passwordexpirationdate.md) <br/> |<span data-ttu-id="acb8a-148">Proporciona la fecha de expiración de la contraseña de la cuenta de correo electrónico especificada en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="acb8a-148">Provides the password expiration date for the email account specified in the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="acb8a-149">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="acb8a-149">Parent elements</span></span>

|<span data-ttu-id="acb8a-150">**Nombre del elemento**</span><span class="sxs-lookup"><span data-stu-id="acb8a-150">**Element name**</span></span>|<span data-ttu-id="acb8a-151">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="acb8a-151">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="acb8a-152">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="acb8a-152">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="acb8a-153">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange (EWS).</span><span class="sxs-lookup"><span data-stu-id="acb8a-153">Contains the response messages for an Exchange Web Services (EWS) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="acb8a-154">Comentarios</span><span class="sxs-lookup"><span data-stu-id="acb8a-154">Remarks</span></span>

<span data-ttu-id="acb8a-155">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="acb8a-155">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="acb8a-156">Este elemento se introdujo en Exchange Server 2010 Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="acb8a-156">This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="acb8a-157">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="acb8a-157">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="acb8a-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="acb8a-158">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="acb8a-159">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="acb8a-159">Schema Name</span></span>  <br/> |<span data-ttu-id="acb8a-160">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="acb8a-160">Messages schema</span></span>  <br/> |
|<span data-ttu-id="acb8a-161">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="acb8a-161">Validation File</span></span>  <br/> |<span data-ttu-id="acb8a-162">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="acb8a-162">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="acb8a-163">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="acb8a-163">Can be Empty</span></span>  <br/> |<span data-ttu-id="acb8a-164">Falso</span><span class="sxs-lookup"><span data-stu-id="acb8a-164">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="acb8a-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="acb8a-165">See also</span></span>

- [<span data-ttu-id="acb8a-166">Operación GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="acb8a-166">GetPasswordExpirationDate operation</span></span>](getpasswordexpirationdate-operation.md)
- [<span data-ttu-id="acb8a-167">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="acb8a-167">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

