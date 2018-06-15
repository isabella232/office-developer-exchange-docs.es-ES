---
title: FindItem Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindItem
api_type:
- schema
ms.assetid: ebad6aae-16e7-44de-ae63-a95b24539729
description: Busque información sobre la EWS FindItem operación.
ms.openlocfilehash: b033ac2930981819a20f1336d40058a5f7c03b89
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764637"
---
# <a name="finditem-operation"></a><span data-ttu-id="3fa7f-103">FindItem Operation</span><span class="sxs-lookup"><span data-stu-id="3fa7f-103">FindItem operation</span></span>

<span data-ttu-id="3fa7f-104">Obtenga información acerca de la operación de EWS **FindItem** .</span><span class="sxs-lookup"><span data-stu-id="3fa7f-104">Find information about the **FindItem** EWS operation.</span></span> 
  
<span data-ttu-id="3fa7f-105">La operación **FindItem** busca los elementos que se encuentran en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-105">The **FindItem** operation searches for items that are located in a user's mailbox.</span></span> <span data-ttu-id="3fa7f-106">Esta operación proporciona muchas maneras para filtrar y formato de cómo se devuelven los resultados de búsqueda para el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-106">This operation provides many ways to filter and format how search results are returned to the caller.</span></span> 
  
## <a name="using-the-finditem-operation"></a><span data-ttu-id="3fa7f-107">Mediante la operación FindItem</span><span class="sxs-lookup"><span data-stu-id="3fa7f-107">Using the FindItem operation</span></span>

<span data-ttu-id="3fa7f-108">La solicitud de operación **FindItem** proporciona muchas formas de un buzón de correo y el formato de cómo se devuelven los datos en una respuesta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-108">The **FindItem** operation request provides many ways for you to search a mailbox and format how the data is returned in a response.</span></span> <span data-ttu-id="3fa7f-109">Puede especificar lo siguiente en una solicitud **FindItem** :</span><span class="sxs-lookup"><span data-stu-id="3fa7f-109">You can specify the following in a **FindItem** request:</span></span> 
  
- <span data-ttu-id="3fa7f-110">Si la búsqueda es un recorrido superficial o eliminado temporalmente.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-110">Whether the search is a shallow or soft-deleted traversal.</span></span> <span data-ttu-id="3fa7f-111">Es necesario especificar esto.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-111">Specifying this is required.</span></span> <span data-ttu-id="3fa7f-112">Tenga en cuenta que un recorrido eliminado temporalmente combinado con una restricción de la búsqueda, se producirá en cero los elementos devueltos, incluso si hay elementos que coincidan con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-112">Note that a soft-deleted traversal combined with a search restriction will result in zero items returned, even if there are items that match the search criteria.</span></span>
    
- <span data-ttu-id="3fa7f-113">La forma de respuesta de los elementos.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-113">The response shape of items.</span></span> <span data-ttu-id="3fa7f-114">Esto identifica las propiedades que se devuelven en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-114">This identifies the properties that are returned in the response.</span></span> <span data-ttu-id="3fa7f-115">Es necesario especificar esto.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-115">Specifying this is required.</span></span>
    
- <span data-ttu-id="3fa7f-116">Las carpetas desde la que se va a realizar la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-116">The folders from which to perform the search.</span></span> <span data-ttu-id="3fa7f-117">Es necesario especificar esto.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-117">Specifying this is required.</span></span>
    
- <span data-ttu-id="3fa7f-118">Los tipos de mecanismo y vista de paginación para devolver ver los datos en las páginas.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-118">The paging mechanism and view types for returning view data in pages.</span></span> <span data-ttu-id="3fa7f-119">Especificar esto es opcional.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-119">Specifying this is optional.</span></span>
    
- <span data-ttu-id="3fa7f-120">Opciones de agrupación y ordenación de los elementos que se devuelven.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-120">Options for grouping and sorting the items that are returned.</span></span> <span data-ttu-id="3fa7f-121">Especificar esto es opcional.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-121">Specifying this is optional.</span></span>
    
- <span data-ttu-id="3fa7f-122">Las restricciones de búsqueda o cadenas de sintaxis de consulta avanzada (AQS) para filtrar los elementos que se devuelven.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-122">Search restrictions or Advanced Query Syntax (AQS) strings for filtering the items that are returned.</span></span> <span data-ttu-id="3fa7f-123">Para obtener más información acerca del uso de AQS para las búsquedas de índice de contenido, vea [QueryString (String)](querystring-string.md).</span><span class="sxs-lookup"><span data-stu-id="3fa7f-123">For more information about using AQS for content index searches, see [QueryString (String)](querystring-string.md).</span></span> <span data-ttu-id="3fa7f-124">Especificar esto es opcional.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-124">Specifying this is optional.</span></span>
    
- <span data-ttu-id="3fa7f-125">El criterio de ordenación para los elementos devueltos en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-125">The sort order for items returned in the response.</span></span> <span data-ttu-id="3fa7f-126">Especificar esto es opcional.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-126">Specifying this is optional.</span></span>
    
<span data-ttu-id="3fa7f-127">La operación **FindItem** devuelve sólo el primer 512 bytes de cualquier propiedad que se pueden transmitir.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-127">The **FindItem** operation returns only the first 512 bytes of any streamable property.</span></span> <span data-ttu-id="3fa7f-128">Para Unicode, devuelve los primeros 255 caracteres mediante el uso de una cadena Unicode terminada en null.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-128">For Unicode, it returns the first 255 characters by using a null-terminated Unicode string.</span></span> <span data-ttu-id="3fa7f-129">No devolver cualquiera de los formatos de cuerpo de mensaje o las listas de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-129">It does not return any of the message body formats or the recipient lists.</span></span> <span data-ttu-id="3fa7f-130">**FindItem** devolverá a un destinatario resumen.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-130">**FindItem** will return a recipient summary.</span></span> <span data-ttu-id="3fa7f-131">Puede usar la [operación GetItem](getitem-operation.md) para obtener los detalles de un elemento.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-131">You can use the [GetItem operation](getitem-operation.md) to get the details of an item.</span></span> 
  
 <span data-ttu-id="3fa7f-132">**FindItem** devuelve sólo el elemento [nombre (EmailAddressType)](name-emailaddresstype.md) y no devuelve el elemento [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) en el elemento de [buzón de correo](mailbox.md) para los siguientes campos:</span><span class="sxs-lookup"><span data-stu-id="3fa7f-132">**FindItem** returns only the [Name (EmailAddressType)](name-emailaddresstype.md) element and does not return the [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) element in the [Mailbox](mailbox.md) element for the following fields:</span></span> 
  
- <span data-ttu-id="3fa7f-133">El campo [de](from.md) los mensajes</span><span class="sxs-lookup"><span data-stu-id="3fa7f-133">The [From](from.md) field for messages</span></span> 
    
- <span data-ttu-id="3fa7f-134">El campo de [remitente](sender.md) de mensajes</span><span class="sxs-lookup"><span data-stu-id="3fa7f-134">The [Sender](sender.md) field for messages</span></span> 
    
- <span data-ttu-id="3fa7f-135">El campo [Organizador](organizer.md) para elementos de calendario</span><span class="sxs-lookup"><span data-stu-id="3fa7f-135">The [Organizer](organizer.md) field for calendar items</span></span> 
    
> [!NOTE]
> <span data-ttu-id="3fa7f-136">La operación **FindItem** puede devolver los resultados en un elemento [CalendarView](calendarview.md) .</span><span class="sxs-lookup"><span data-stu-id="3fa7f-136">The **FindItem** operation can return results in a [CalendarView](calendarview.md) element.</span></span> <span data-ttu-id="3fa7f-137">El elemento **CalendarView** devuelve los elementos de calendario único y todas las apariciones de las reuniones periódicas.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-137">The **CalendarView** element returns single calendar items and all occurrences of recurring meetings.</span></span> <span data-ttu-id="3fa7f-138">Si no se usa un elemento **CalendarView** , se devuelven los elementos de calendario único y elementos periódicos del calendario principal.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-138">If a **CalendarView** element is not used, single calendar items and recurring master calendar items are returned.</span></span> <span data-ttu-id="3fa7f-139">Si no se usa un elemento **CalendarView** , las apariciones se deben expandir desde el maestro periódico.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-139">The occurrences must be expanded from the recurring master if a **CalendarView** element is not used.</span></span> 
  
<span data-ttu-id="3fa7f-140">La operación **FindItem** puede usar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-140">The **FindItem** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
<span data-ttu-id="3fa7f-141">**La tabla 1. Encabezados SOAP de FindItem operación**</span><span class="sxs-lookup"><span data-stu-id="3fa7f-141">**Table 1. FindItem operation SOAP headers**</span></span>

|<span data-ttu-id="3fa7f-142">**Header**</span><span class="sxs-lookup"><span data-stu-id="3fa7f-142">**Header**</span></span>|<span data-ttu-id="3fa7f-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="3fa7f-143">**Element**</span></span>|<span data-ttu-id="3fa7f-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3fa7f-144">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3fa7f-145">**DateTimePrecision**</span><span class="sxs-lookup"><span data-stu-id="3fa7f-145">**DateTimePrecision**</span></span> <br/> |[<span data-ttu-id="3fa7f-146">DateTimePrecision</span><span class="sxs-lookup"><span data-stu-id="3fa7f-146">DateTimePrecision</span></span>](datetimeprecision.md) <br/> |<span data-ttu-id="3fa7f-147">Especifica la resolución de los valores de fecha y hora en las respuestas desde el servidor, en segundos o en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-147">Specifies the resolution of data/time values in responses from the server, either in seconds or in milliseconds.</span></span> <span data-ttu-id="3fa7f-148">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-148">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="3fa7f-149">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="3fa7f-149">**Impersonation**</span></span> <br/> |[<span data-ttu-id="3fa7f-150">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="3fa7f-150">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="3fa7f-151">Identifica el usuario que está realizando la suplantación de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-151">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="3fa7f-152">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-152">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="3fa7f-153">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="3fa7f-153">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="3fa7f-154">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="3fa7f-154">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="3fa7f-155">Identifica la referencia cultural de RFC3066 va a usar para tener acceso al buzón.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-155">Identifies the RFC3066 culture to be used to access the mailbox.</span></span> <span data-ttu-id="3fa7f-156">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-156">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="3fa7f-157">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="3fa7f-157">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="3fa7f-158">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="3fa7f-158">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="3fa7f-159">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-159">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="3fa7f-160">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-160">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="3fa7f-161">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="3fa7f-161">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="3fa7f-162">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="3fa7f-162">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="3fa7f-163">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-163">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="3fa7f-164">Esto es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-164">This is applicable to a response.</span></span>  <br/> |
|<span data-ttu-id="3fa7f-165">**TimeZoneContext**</span><span class="sxs-lookup"><span data-stu-id="3fa7f-165">**TimeZoneContext**</span></span> <br/> |[<span data-ttu-id="3fa7f-166">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="3fa7f-166">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="3fa7f-167">Identifica la zona horaria que se usará para todas las respuestas desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-167">Identifies the time zone to be used for all responses from the server.</span></span> <span data-ttu-id="3fa7f-168">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-168">This is applicable to a request.</span></span>  <br/> |
   
## <a name="finditem-operation-request-example"></a><span data-ttu-id="3fa7f-169">Ejemplo de solicitud de operación FindItem</span><span class="sxs-lookup"><span data-stu-id="3fa7f-169">FindItem operation request example</span></span>

<span data-ttu-id="3fa7f-170">El siguiente ejemplo de una solicitud de **FindItem** muestra cómo obtener el identificador del elemento que se define en la enumeración **IdOnly** del elemento [BaseShape](baseshape.md) para los elementos que se encuentran en la carpeta Elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-170">The following example of a **FindItem** request shows how to obtain the item identifier that is defined by the **IdOnly** enumeration of the [BaseShape](baseshape.md) element for items that are found in the Deleted Items folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
              Traversal="Shallow">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
      </ItemShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="deleteditems"/>
      </ParentFolderIds>
    </FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="3fa7f-171">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="3fa7f-171">The following elements are used in the request:</span></span> 
  
- [<span data-ttu-id="3fa7f-172">FindItem</span><span class="sxs-lookup"><span data-stu-id="3fa7f-172">FindItem</span></span>](finditem.md)
    
- [<span data-ttu-id="3fa7f-173">ItemShape</span><span class="sxs-lookup"><span data-stu-id="3fa7f-173">ItemShape</span></span>](itemshape.md)
    
- [<span data-ttu-id="3fa7f-174">BaseShape</span><span class="sxs-lookup"><span data-stu-id="3fa7f-174">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="3fa7f-175">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="3fa7f-175">ParentFolderIds</span></span>](parentfolderids.md)
    
- [<span data-ttu-id="3fa7f-176">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="3fa7f-176">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
<span data-ttu-id="3fa7f-177">Para ver más opciones para un mensaje de solicitud **FindItem** , explore la jerarquía de esquema.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-177">For more options for a **FindItem** request message, explore the schema hierarchy.</span></span> <span data-ttu-id="3fa7f-178">Comenzar en el elemento de [FindItem](finditem.md) .</span><span class="sxs-lookup"><span data-stu-id="3fa7f-178">Start at the [FindItem](finditem.md) element.</span></span> 
  
## <a name="successful-finditem-operation-response"></a><span data-ttu-id="3fa7f-179">Respuesta es correcta de operación FindItem</span><span class="sxs-lookup"><span data-stu-id="3fa7f-179">Successful FindItem operation response</span></span>

<span data-ttu-id="3fa7f-180">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud de **FindItem** .</span><span class="sxs-lookup"><span data-stu-id="3fa7f-180">The following example shows a successful response to the **FindItem** request.</span></span> 
  
<span data-ttu-id="3fa7f-181">Elementos del [mensaje](message-ex15websvcsotherref.md) representan los mensajes de correo electrónico y todos los otros elementos que no están fuertemente tipados por el esquema de EWS.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-181">[Message](message-ex15websvcsotherref.md) elements represent email messages and all other items that are not strongly typed by the EWS schema.</span></span> <span data-ttu-id="3fa7f-182">Elementos como IPM. Uso compartido y IPM.InfoPath se devuelven como elementos del [mensaje](message-ex15websvcsotherref.md) .</span><span class="sxs-lookup"><span data-stu-id="3fa7f-182">Items such as IPM.Sharing and IPM.InfoPath are returned as [Message](message-ex15websvcsotherref.md) elements.</span></span> <span data-ttu-id="3fa7f-183">Exchange no devuelve [el elemento de base](item.md) de las respuestas.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-183">Exchange does not return the base [Item](item.md) element in responses.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder TotalItemsInView="10" IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AS4AUn=" ChangeKey="fsVU4==" />
              </t:Message>
              <t:Message>
                <t:ItemId Id="AS4AUM=" ChangeKey="fsVUA==" />
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </FindItemResponse>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="3fa7f-184">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="3fa7f-184">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="3fa7f-185">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="3fa7f-185">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="3fa7f-186">FindItemResponse</span><span class="sxs-lookup"><span data-stu-id="3fa7f-186">FindItemResponse</span></span>](finditemresponse.md)
    
- [<span data-ttu-id="3fa7f-187">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="3fa7f-187">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="3fa7f-188">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="3fa7f-188">FindItemResponseMessage</span></span>](finditemresponsemessage.md)
    
- [<span data-ttu-id="3fa7f-189">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="3fa7f-189">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="3fa7f-190">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="3fa7f-190">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md)
    
- [<span data-ttu-id="3fa7f-191">Items</span><span class="sxs-lookup"><span data-stu-id="3fa7f-191">Items</span></span>](items.md)
    
- [<span data-ttu-id="3fa7f-192">Message</span><span class="sxs-lookup"><span data-stu-id="3fa7f-192">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="3fa7f-193">ItemId</span><span class="sxs-lookup"><span data-stu-id="3fa7f-193">ItemId</span></span>](itemid.md)
    
<span data-ttu-id="3fa7f-194">Para ver más opciones para un mensaje de respuesta **FindItem** , explore la jerarquía de esquema.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-194">For more options for a **FindItem** response message, explore the schema hierarchy.</span></span> <span data-ttu-id="3fa7f-195">Comenzar en el elemento de [FindItemResponse](finditemresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="3fa7f-195">Start at the [FindItemResponse](finditemresponse.md) element.</span></span> 
  
## <a name="finditem-operation-error-response"></a><span data-ttu-id="3fa7f-196">Respuesta de error de la operación FindItem</span><span class="sxs-lookup"><span data-stu-id="3fa7f-196">FindItem operation error response</span></span>

<span data-ttu-id="3fa7f-197">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de **FindItem** .</span><span class="sxs-lookup"><span data-stu-id="3fa7f-197">The following example shows an error response to a **FindItem** request.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Error">
          <m:MessageText>Id is malformed.</m:MessageText>
          <m:ResponseCode>ErrorInvalidIdMalformed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </FindItemResponse>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="3fa7f-198">En la respuesta de error, se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="3fa7f-198">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="3fa7f-199">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="3fa7f-199">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="3fa7f-200">FindItemResponse</span><span class="sxs-lookup"><span data-stu-id="3fa7f-200">FindItemResponse</span></span>](finditemresponse.md)
    
- [<span data-ttu-id="3fa7f-201">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="3fa7f-201">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="3fa7f-202">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="3fa7f-202">FindItemResponseMessage</span></span>](finditemresponsemessage.md)
    
- [<span data-ttu-id="3fa7f-203">MessageText</span><span class="sxs-lookup"><span data-stu-id="3fa7f-203">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="3fa7f-204">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="3fa7f-204">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="3fa7f-205">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="3fa7f-205">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="3fa7f-206">Para ver más opciones para un mensaje de respuesta de error **FindItem** , explore la jerarquía de esquema.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-206">For more options for a **FindItem** error response message, explore the schema hierarchy.</span></span> <span data-ttu-id="3fa7f-207">Comenzar en el elemento de [FindItemResponse](finditemresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="3fa7f-207">Start at the [FindItemResponse](finditemresponse.md) element.</span></span> 
  
## <a name="version-differences"></a><span data-ttu-id="3fa7f-208">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="3fa7f-208">Version differences</span></span>

<span data-ttu-id="3fa7f-209">Las versiones de Exchange con la versión principal 15 iniciales y finales con generación 15.0.898.11 devuelto un valor de ErrorInvalidOperation en el elemento [ResponseCode](responsecode.md) cuando la operación **FindItem** se usa para buscar en varias carpetas de un buzón de archivo.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-209">Versions of Exchange starting with major version 15 and ending with build 15.0.898.11 return an ErrorInvalidOperation value in the [ResponseCode](responsecode.md) element when the **FindItem** operation is used to search multiple folders in an archive mailbox.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3fa7f-210">Ver también</span><span class="sxs-lookup"><span data-stu-id="3fa7f-210">See also</span></span>

- [<span data-ttu-id="3fa7f-211">Buscar elementos</span><span class="sxs-lookup"><span data-stu-id="3fa7f-211">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)
    
- [<span data-ttu-id="3fa7f-212">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3fa7f-212">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
    
- <span data-ttu-id="3fa7f-213">**FindItemType**</span><span class="sxs-lookup"><span data-stu-id="3fa7f-213">**FindItemType**</span></span>
    
