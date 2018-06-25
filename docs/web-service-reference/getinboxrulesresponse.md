---
title: GetInboxRulesResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetInboxRulesResponse
api_type:
- schema
ms.assetid: 6d6c1950-c328-489a-94bf-a250fdbd5cd9
description: El elemento GetInboxRulesResponse define una respuesta a una solicitud de operación GetInboxRules.
ms.openlocfilehash: d84064ab777fe13ded7727381842ddd1ee9d047d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764889"
---
# <a name="getinboxrulesresponse"></a><span data-ttu-id="23c59-103">GetInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="23c59-103">GetInboxRulesResponse</span></span>

<span data-ttu-id="23c59-104">El elemento **GetInboxRulesResponse** define una respuesta a una solicitud de [operación GetInboxRules](getinboxrules-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="23c59-104">The **GetInboxRulesResponse** element defines a response to a [GetInboxRules operation](getinboxrules-operation.md) request.</span></span> 
  
```XML
<GetInboxRulesResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <OutlookRuleBlobExists/>
   <InboxRules/>
</GetInboxRulesResponse>
```

 <span data-ttu-id="23c59-105">**GetInboxRulesResponseType**</span><span class="sxs-lookup"><span data-stu-id="23c59-105">**GetInboxRulesResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="23c59-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="23c59-106">Attributes and elements</span></span>

<span data-ttu-id="23c59-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="23c59-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="23c59-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="23c59-108">Attributes</span></span>

|<span data-ttu-id="23c59-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="23c59-109">**Attribute**</span></span>|<span data-ttu-id="23c59-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="23c59-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="23c59-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="23c59-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="23c59-112">Describe el estado de una respuesta de [la operación GetInboxRules](getinboxrules-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="23c59-112">Describes the status of a [GetInboxRules operation](getinboxrules-operation.md) response.</span></span> <br/><br/><span data-ttu-id="23c59-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="23c59-113">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="23c59-114">-Éxito</span><span class="sxs-lookup"><span data-stu-id="23c59-114">-  Success</span></span>  <br/><span data-ttu-id="23c59-115">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="23c59-115">-  Warning</span></span>  <br/><span data-ttu-id="23c59-116">-Error</span><span class="sxs-lookup"><span data-stu-id="23c59-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="23c59-117">Atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="23c59-117">ResponseClass Attribute</span></span>

|<span data-ttu-id="23c59-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="23c59-118">**Value**</span></span>|<span data-ttu-id="23c59-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="23c59-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="23c59-120">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="23c59-120">**Success**</span></span> <br/> |<span data-ttu-id="23c59-121">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="23c59-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="23c59-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="23c59-122">**Warning**</span></span> <br/> | <span data-ttu-id="23c59-123">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="23c59-123">Describes a request that was not processed.</span></span> <span data-ttu-id="23c59-124">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="23c59-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="23c59-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="23c59-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="23c59-126">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="23c59-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="23c59-127">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="23c59-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="23c59-128">-Se mueven los buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="23c59-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="23c59-129">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="23c59-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="23c59-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="23c59-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="23c59-131">-Se ha excedido una cuota.</span><span class="sxs-lookup"><span data-stu-id="23c59-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="23c59-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="23c59-132">**Error**</span></span> <br/> | <span data-ttu-id="23c59-133">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="23c59-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="23c59-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="23c59-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="23c59-135">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="23c59-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="23c59-136">-Los atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="23c59-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="23c59-137">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="23c59-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="23c59-138">-Un atributo o un elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="23c59-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="23c59-139">-Un intento de acceso no autorizado por cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="23c59-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="23c59-140">-Un error del lado del servidor en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="23c59-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="23c59-141">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="23c59-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="23c59-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="23c59-142">Child elements</span></span>

|<span data-ttu-id="23c59-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="23c59-143">**Element**</span></span>|<span data-ttu-id="23c59-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="23c59-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="23c59-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="23c59-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="23c59-146">Proporciona la descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="23c59-146">Provides text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="23c59-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="23c59-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="23c59-148">Proporciona información de estado acerca de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="23c59-148">Provides status information about the request.</span></span>  <br/> |
|[<span data-ttu-id="23c59-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="23c59-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="23c59-150">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="23c59-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="23c59-151">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="23c59-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="23c59-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="23c59-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="23c59-153">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="23c59-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="23c59-154">OutlookRuleBlobExists</span><span class="sxs-lookup"><span data-stu-id="23c59-154">OutlookRuleBlobExists</span></span>](outlookruleblobexists.md) <br/> |<span data-ttu-id="23c59-155">Indica si existe un blob de regla de Microsoft Outlook en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="23c59-155">Indicates whether a Microsoft Outlook rule blob exists in the user's mailbox.</span></span>  <br/> |
|[<span data-ttu-id="23c59-156">InboxRules</span><span class="sxs-lookup"><span data-stu-id="23c59-156">InboxRules</span></span>](inboxrules.md) <br/> |<span data-ttu-id="23c59-157">Representa una matriz de las reglas en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="23c59-157">Represents an array of the rules in the user's mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="23c59-158">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="23c59-158">Parent elements</span></span>

<span data-ttu-id="23c59-159">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="23c59-159">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="23c59-160">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="23c59-160">Text value</span></span>

<span data-ttu-id="23c59-161">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="23c59-161">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="23c59-162">Comentarios</span><span class="sxs-lookup"><span data-stu-id="23c59-162">Remarks</span></span>

<span data-ttu-id="23c59-163">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="23c59-163">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="23c59-164">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="23c59-164">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="23c59-165">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="23c59-165">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="23c59-166">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="23c59-166">Schema name</span></span>  <br/> |<span data-ttu-id="23c59-167">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="23c59-167">Messages schema</span></span>  <br/> |
|<span data-ttu-id="23c59-168">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="23c59-168">Validation file</span></span>  <br/> |<span data-ttu-id="23c59-169">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="23c59-169">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="23c59-170">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="23c59-170">Can be empty</span></span>  <br/> |<span data-ttu-id="23c59-171">False</span><span class="sxs-lookup"><span data-stu-id="23c59-171">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="23c59-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="23c59-172">See also</span></span>

- [<span data-ttu-id="23c59-173">GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="23c59-173">GetInboxRules</span></span>](getinboxrules.md)
- [<span data-ttu-id="23c59-174">Operación de GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="23c59-174">GetInboxRules operation</span></span>](getinboxrules-operation.md)

