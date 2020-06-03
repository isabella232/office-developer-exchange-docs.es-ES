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
ms.openlocfilehash: 0d67d7eaf6ffbeeb790249190a98f252dbdb9c87
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458288"
---
# <a name="getinboxrulesresponse"></a><span data-ttu-id="bcdb5-103">GetInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="bcdb5-103">GetInboxRulesResponse</span></span>

<span data-ttu-id="bcdb5-104">El elemento **GetInboxRulesResponse** define una respuesta a una solicitud de [operación GetInboxRules](getinboxrules-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="bcdb5-104">The **GetInboxRulesResponse** element defines a response to a [GetInboxRules operation](getinboxrules-operation.md) request.</span></span> 
  
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

 <span data-ttu-id="bcdb5-105">**GetInboxRulesResponseType**</span><span class="sxs-lookup"><span data-stu-id="bcdb5-105">**GetInboxRulesResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bcdb5-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="bcdb5-106">Attributes and elements</span></span>

<span data-ttu-id="bcdb5-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bcdb5-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="bcdb5-108">Attributes</span></span>

|<span data-ttu-id="bcdb5-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="bcdb5-109">**Attribute**</span></span>|<span data-ttu-id="bcdb5-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bcdb5-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bcdb5-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="bcdb5-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="bcdb5-112">Describe el estado de una respuesta de [operación de GetInboxRules](getinboxrules-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="bcdb5-112">Describes the status of a [GetInboxRules operation](getinboxrules-operation.md) response.</span></span> <br/><br/><span data-ttu-id="bcdb5-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="bcdb5-113">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="bcdb5-114">-Correcto</span><span class="sxs-lookup"><span data-stu-id="bcdb5-114">-  Success</span></span>  <br/><span data-ttu-id="bcdb5-115">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="bcdb5-115">-  Warning</span></span>  <br/><span data-ttu-id="bcdb5-116">-Error</span><span class="sxs-lookup"><span data-stu-id="bcdb5-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="bcdb5-117">Atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="bcdb5-117">ResponseClass Attribute</span></span>

|<span data-ttu-id="bcdb5-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="bcdb5-118">**Value**</span></span>|<span data-ttu-id="bcdb5-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bcdb5-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bcdb5-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="bcdb5-120">**Success**</span></span> <br/> |<span data-ttu-id="bcdb5-121">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="bcdb5-122">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="bcdb5-122">**Warning**</span></span> <br/> | <span data-ttu-id="bcdb5-123">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-123">Describes a request that was not processed.</span></span> <span data-ttu-id="bcdb5-124">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="bcdb5-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="bcdb5-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="bcdb5-126">-El almacén de Exchange está sin conexión durante el lote.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="bcdb5-127">-Los servicios de dominio de Active Directory (AD DS) están sin conexión.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="bcdb5-128">-Se mueven los buzones.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="bcdb5-129">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="bcdb5-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="bcdb5-131">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="bcdb5-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="bcdb5-132">**Error**</span></span> <br/> | <span data-ttu-id="bcdb5-133">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="bcdb5-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="bcdb5-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="bcdb5-135">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="bcdb5-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="bcdb5-136">-Atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="bcdb5-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="bcdb5-137">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="bcdb5-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="bcdb5-138">-Un atributo o elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="bcdb5-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="bcdb5-139">-Un intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="bcdb5-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="bcdb5-140">-Un error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="bcdb5-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="bcdb5-141">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="bcdb5-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bcdb5-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bcdb5-142">Child elements</span></span>

|<span data-ttu-id="bcdb5-143">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bcdb5-143">**Element**</span></span>|<span data-ttu-id="bcdb5-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bcdb5-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bcdb5-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="bcdb5-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="bcdb5-146">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-146">Provides text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="bcdb5-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="bcdb5-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="bcdb5-148">Proporciona información de estado sobre la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-148">Provides status information about the request.</span></span>  <br/> |
|[<span data-ttu-id="bcdb5-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="bcdb5-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="bcdb5-150">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="bcdb5-151">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="bcdb5-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="bcdb5-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="bcdb5-153">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="bcdb5-154">OutlookRuleBlobExists</span><span class="sxs-lookup"><span data-stu-id="bcdb5-154">OutlookRuleBlobExists</span></span>](outlookruleblobexists.md) <br/> |<span data-ttu-id="bcdb5-155">Indica si existe un BLOB de reglas de Microsoft Outlook en el buzón de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-155">Indicates whether a Microsoft Outlook rule blob exists in the user's mailbox.</span></span>  <br/> |
|[<span data-ttu-id="bcdb5-156">InboxRules</span><span class="sxs-lookup"><span data-stu-id="bcdb5-156">InboxRules</span></span>](inboxrules.md) <br/> |<span data-ttu-id="bcdb5-157">Representa una matriz de las reglas en el buzón de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-157">Represents an array of the rules in the user's mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bcdb5-158">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bcdb5-158">Parent elements</span></span>

<span data-ttu-id="bcdb5-159">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-159">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="bcdb5-160">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="bcdb5-160">Text value</span></span>

<span data-ttu-id="bcdb5-161">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-161">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bcdb5-162">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bcdb5-162">Remarks</span></span>

<span data-ttu-id="bcdb5-163">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-163">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bcdb5-164">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="bcdb5-164">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bcdb5-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="bcdb5-165">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bcdb5-166">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="bcdb5-166">Schema name</span></span>  <br/> |<span data-ttu-id="bcdb5-167">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="bcdb5-167">Messages schema</span></span>  <br/> |
|<span data-ttu-id="bcdb5-168">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="bcdb5-168">Validation file</span></span>  <br/> |<span data-ttu-id="bcdb5-169">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="bcdb5-169">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bcdb5-170">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="bcdb5-170">Can be empty</span></span>  <br/> |<span data-ttu-id="bcdb5-171">Falso</span><span class="sxs-lookup"><span data-stu-id="bcdb5-171">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bcdb5-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="bcdb5-172">See also</span></span>

- [<span data-ttu-id="bcdb5-173">GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="bcdb5-173">GetInboxRules</span></span>](getinboxrules.md)
- [<span data-ttu-id="bcdb5-174">Operación de GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="bcdb5-174">GetInboxRules operation</span></span>](getinboxrules-operation.md)

