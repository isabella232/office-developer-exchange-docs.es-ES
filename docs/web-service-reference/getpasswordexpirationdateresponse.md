---
title: GetPasswordExpirationDateResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3d3fff1f-ef13-46d5-bd7f-ef535eb80c72
description: El elemento GetPasswordExpirationDateResponse define la respuesta a una solicitud de operación de la operación de GetPasswordExpirationDate.
ms.openlocfilehash: 3754a53da53c12479f11c2e32cd15a08cba665fb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764946"
---
# <a name="getpasswordexpirationdateresponse"></a><span data-ttu-id="7e138-103">GetPasswordExpirationDateResponse</span><span class="sxs-lookup"><span data-stu-id="7e138-103">GetPasswordExpirationDateResponse</span></span>

<span data-ttu-id="7e138-104">El elemento **GetPasswordExpirationDateResponse** define la respuesta a una solicitud de operación de la [operación de GetPasswordExpirationDate](getpasswordexpirationdate-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="7e138-104">The **GetPasswordExpirationDateResponse** element defines the response to a [GetPasswordExpirationDate operation](getpasswordexpirationdate-operation.md) operation request.</span></span> 
  
- [<span data-ttu-id="7e138-105">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="7e138-105">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="7e138-106">GetPasswordExpirationDateResponse</span><span class="sxs-lookup"><span data-stu-id="7e138-106">GetPasswordExpirationDateResponse</span></span>](getpasswordexpirationdateresponse.md)
  
```XML
<GetPasswordExpirationDateResponse>
    <PasswordExpirationDate />
</GetPasswordExpirationDateResponse>
```

 <span data-ttu-id="7e138-107">**GetPasswordExpirationDateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="7e138-107">**GetPasswordExpirationDateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7e138-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7e138-108">Attributes and elements</span></span>

<span data-ttu-id="7e138-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7e138-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7e138-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="7e138-110">Attributes</span></span>

|<span data-ttu-id="7e138-111">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="7e138-111">**Attribute**</span></span>|<span data-ttu-id="7e138-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7e138-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7e138-113">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="7e138-113">**ResponseClass**</span></span> <br/> | <span data-ttu-id="7e138-114">Describe el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7e138-114">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="7e138-115">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="7e138-115">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="7e138-116">-Éxito</span><span class="sxs-lookup"><span data-stu-id="7e138-116">-  Success</span></span>  <br/><span data-ttu-id="7e138-117">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="7e138-117">-  Warning</span></span>  <br/><span data-ttu-id="7e138-118">-Error</span><span class="sxs-lookup"><span data-stu-id="7e138-118">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="7e138-119">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="7e138-119">ResponseClass attribute values</span></span>

|<span data-ttu-id="7e138-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7e138-120">**Value**</span></span>|<span data-ttu-id="7e138-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7e138-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7e138-122">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="7e138-122">**Success**</span></span> <br/> |<span data-ttu-id="7e138-123">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="7e138-123">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="7e138-124">**Warning**</span><span class="sxs-lookup"><span data-stu-id="7e138-124">**Warning**</span></span> <br/> | <span data-ttu-id="7e138-125">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="7e138-125">Describes a request that was not processed.</span></span> <span data-ttu-id="7e138-126">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="7e138-126">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="7e138-127">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="7e138-127">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="7e138-128">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="7e138-128">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="7e138-129">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="7e138-129">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="7e138-130">-Buzones se han movido.</span><span class="sxs-lookup"><span data-stu-id="7e138-130">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="7e138-131">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="7e138-131">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="7e138-132">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="7e138-132">-  A password is expired.</span></span>  <br/><span data-ttu-id="7e138-133">-Se superó una cuota.</span><span class="sxs-lookup"><span data-stu-id="7e138-133">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="7e138-134">**Error**</span><span class="sxs-lookup"><span data-stu-id="7e138-134">**Error**</span></span> <br/> | <span data-ttu-id="7e138-135">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="7e138-135">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="7e138-136">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="7e138-136">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="7e138-137">-No válida Atributos o elementos.</span><span class="sxs-lookup"><span data-stu-id="7e138-137">-  Invalid attributes or elements.</span></span>  <br/><span data-ttu-id="7e138-138">-Los atributos o elementos que están fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="7e138-138">-  Attributes or elements that are out of range.</span></span>  <br/><span data-ttu-id="7e138-139">-Una etiqueta desconocida.</span><span class="sxs-lookup"><span data-stu-id="7e138-139">-  An unknown tag.</span></span>  <br/><span data-ttu-id="7e138-140">-Un atributo o un elemento que no es válido en el contexto.</span><span class="sxs-lookup"><span data-stu-id="7e138-140">-  An attribute or element that is not valid in the context.</span></span>  <br/><span data-ttu-id="7e138-141">-Un intento de acceso no autorizado por cualquier cliente.</span><span class="sxs-lookup"><span data-stu-id="7e138-141">-  An unauthorized access attempt by any client.</span></span>  <br/><span data-ttu-id="7e138-142">-Un error del servidor en respuesta a una llamada de cliente válida.</span><span class="sxs-lookup"><span data-stu-id="7e138-142">-  A server-side failure in response to a valid client-side call.</span></span>  <br/><br/>  <span data-ttu-id="7e138-143">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="7e138-143">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7e138-144">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7e138-144">Child elements</span></span>

|<span data-ttu-id="7e138-145">**Nombre del elemento**</span><span class="sxs-lookup"><span data-stu-id="7e138-145">**Element name**</span></span>|<span data-ttu-id="7e138-146">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7e138-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7e138-147">PasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="7e138-147">PasswordExpirationDate</span></span>](passwordexpirationdate.md) <br/> |<span data-ttu-id="7e138-148">Proporciona la fecha de caducidad de contraseña para la cuenta de correo electrónico especificada en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7e138-148">Provides the password expiration date for the email account specified in the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7e138-149">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7e138-149">Parent elements</span></span>

|<span data-ttu-id="7e138-150">**Nombre del elemento**</span><span class="sxs-lookup"><span data-stu-id="7e138-150">**Element name**</span></span>|<span data-ttu-id="7e138-151">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7e138-151">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7e138-152">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="7e138-152">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="7e138-153">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange (EWS).</span><span class="sxs-lookup"><span data-stu-id="7e138-153">Contains the response messages for an Exchange Web Services (EWS) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7e138-154">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7e138-154">Remarks</span></span>

<span data-ttu-id="7e138-155">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="7e138-155">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="7e138-156">Este elemento se introdujo en Exchange Server 2010 Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="7e138-156">This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7e138-157">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7e138-157">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7e138-158">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7e138-158">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7e138-159">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7e138-159">Schema Name</span></span>  <br/> |<span data-ttu-id="7e138-160">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="7e138-160">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7e138-161">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7e138-161">Validation File</span></span>  <br/> |<span data-ttu-id="7e138-162">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7e138-162">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7e138-163">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7e138-163">Can be Empty</span></span>  <br/> |<span data-ttu-id="7e138-164">False</span><span class="sxs-lookup"><span data-stu-id="7e138-164">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7e138-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e138-165">See also</span></span>

- [<span data-ttu-id="7e138-166">Operación GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="7e138-166">GetPasswordExpirationDate operation</span></span>](getpasswordexpirationdate-operation.md)
- [<span data-ttu-id="7e138-167">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="7e138-167">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

