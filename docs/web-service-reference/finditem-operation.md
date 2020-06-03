---
title: Operación FindItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- FindItem
api_type:
- schema
ms.assetid: ebad6aae-16e7-44de-ae63-a95b24539729
description: Busca información sobre la operación de EWS de FindItem.
localization_priority: Priority
ms.openlocfilehash: 499d1ee80ef323c883fa86eb125d8c037fb37d4e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462559"
---
# <a name="finditem-operation"></a><span data-ttu-id="a2229-103">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="a2229-103">FindItem operation</span></span>

<span data-ttu-id="a2229-104">Busca información sobre la operación de EWS de **FindItem** .</span><span class="sxs-lookup"><span data-stu-id="a2229-104">Find information about the **FindItem** EWS operation.</span></span> 
  
<span data-ttu-id="a2229-105">La operación **FindItem** busca elementos que se encuentran en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="a2229-105">The **FindItem** operation searches for items that are located in a user's mailbox.</span></span> <span data-ttu-id="a2229-106">Esta operación proporciona muchas maneras de filtrar y dar formato a cómo se devuelven los resultados de la búsqueda al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="a2229-106">This operation provides many ways to filter and format how search results are returned to the caller.</span></span> 
  
## <a name="using-the-finditem-operation"></a><span data-ttu-id="a2229-107">Uso de la operación FindItem</span><span class="sxs-lookup"><span data-stu-id="a2229-107">Using the FindItem operation</span></span>

<span data-ttu-id="a2229-108">La solicitud de operación **FindItem** proporciona muchas formas de buscar en un buzón de correo y dar formato a cómo se devuelven los datos en una respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2229-108">The **FindItem** operation request provides many ways for you to search a mailbox and format how the data is returned in a response.</span></span> <span data-ttu-id="a2229-109">Puede especificar lo siguiente en una solicitud **FindItem** :</span><span class="sxs-lookup"><span data-stu-id="a2229-109">You can specify the following in a **FindItem** request:</span></span> 
  
- <span data-ttu-id="a2229-110">Si la búsqueda es un recorrido superficial o eliminado temporalmente.</span><span class="sxs-lookup"><span data-stu-id="a2229-110">Whether the search is a shallow or soft-deleted traversal.</span></span> <span data-ttu-id="a2229-111">Es necesario especificar esto.</span><span class="sxs-lookup"><span data-stu-id="a2229-111">Specifying this is required.</span></span> <span data-ttu-id="a2229-112">Tenga en cuenta que un recorrido de eliminación temporal combinado con una restricción de búsqueda dará como resultado la devolución de elementos cero, incluso si hay elementos que coinciden con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a2229-112">Note that a soft-deleted traversal combined with a search restriction will result in zero items returned, even if there are items that match the search criteria.</span></span>
    
- <span data-ttu-id="a2229-113">Forma de respuesta de los elementos.</span><span class="sxs-lookup"><span data-stu-id="a2229-113">The response shape of items.</span></span> <span data-ttu-id="a2229-114">Identifica las propiedades que se devuelven en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2229-114">This identifies the properties that are returned in the response.</span></span> <span data-ttu-id="a2229-115">Es necesario especificar esto.</span><span class="sxs-lookup"><span data-stu-id="a2229-115">Specifying this is required.</span></span>
    
- <span data-ttu-id="a2229-116">Las carpetas desde las que se va a realizar la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a2229-116">The folders from which to perform the search.</span></span> <span data-ttu-id="a2229-117">Es necesario especificar esto.</span><span class="sxs-lookup"><span data-stu-id="a2229-117">Specifying this is required.</span></span>
    
- <span data-ttu-id="a2229-118">El mecanismo de paginación y los tipos de vista para devolver los datos de la vista en las páginas.</span><span class="sxs-lookup"><span data-stu-id="a2229-118">The paging mechanism and view types for returning view data in pages.</span></span> <span data-ttu-id="a2229-119">Especificar esto es opcional.</span><span class="sxs-lookup"><span data-stu-id="a2229-119">Specifying this is optional.</span></span>
    
- <span data-ttu-id="a2229-120">Opciones para agrupar y ordenar los elementos que se devuelven.</span><span class="sxs-lookup"><span data-stu-id="a2229-120">Options for grouping and sorting the items that are returned.</span></span> <span data-ttu-id="a2229-121">Especificar esto es opcional.</span><span class="sxs-lookup"><span data-stu-id="a2229-121">Specifying this is optional.</span></span>
    
- <span data-ttu-id="a2229-122">Restricciones de búsqueda o cadenas de sintaxis de consulta avanzada (AQS) para filtrar los elementos que se devuelven.</span><span class="sxs-lookup"><span data-stu-id="a2229-122">Search restrictions or Advanced Query Syntax (AQS) strings for filtering the items that are returned.</span></span> <span data-ttu-id="a2229-123">Para obtener más información sobre el uso de AQS para búsquedas de índice de contenido, consulte [QueryString (cadena)](querystring-string.md).</span><span class="sxs-lookup"><span data-stu-id="a2229-123">For more information about using AQS for content index searches, see [QueryString (String)](querystring-string.md).</span></span> <span data-ttu-id="a2229-124">Especificar esto es opcional.</span><span class="sxs-lookup"><span data-stu-id="a2229-124">Specifying this is optional.</span></span>
    
- <span data-ttu-id="a2229-125">Criterio de ordenación de los elementos devueltos en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2229-125">The sort order for items returned in the response.</span></span> <span data-ttu-id="a2229-126">Especificar esto es opcional.</span><span class="sxs-lookup"><span data-stu-id="a2229-126">Specifying this is optional.</span></span>
    
<span data-ttu-id="a2229-127">La operación **FindItem** devuelve sólo los primeros 512 bytes de cualquier propiedad streamable.</span><span class="sxs-lookup"><span data-stu-id="a2229-127">The **FindItem** operation returns only the first 512 bytes of any streamable property.</span></span> <span data-ttu-id="a2229-128">Para Unicode, devuelve los primeros 255 caracteres mediante una cadena Unicode terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="a2229-128">For Unicode, it returns the first 255 characters by using a null-terminated Unicode string.</span></span> <span data-ttu-id="a2229-129">No devuelve ninguno de los formatos del cuerpo del mensaje o las listas de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="a2229-129">It does not return any of the message body formats or the recipient lists.</span></span> <span data-ttu-id="a2229-130">**FindItem** devolverá un resumen de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="a2229-130">**FindItem** will return a recipient summary.</span></span> <span data-ttu-id="a2229-131">Puede usar la [operación GetItem](getitem-operation.md) para obtener los detalles de un elemento.</span><span class="sxs-lookup"><span data-stu-id="a2229-131">You can use the [GetItem operation](getitem-operation.md) to get the details of an item.</span></span> 
  
 <span data-ttu-id="a2229-132">**FindItem** solo devuelve el elemento [Name (EmailAddressType)](name-emailaddresstype.md) y no devuelve el elemento [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) en el elemento [Mailbox](mailbox.md) para los siguientes campos:</span><span class="sxs-lookup"><span data-stu-id="a2229-132">**FindItem** returns only the [Name (EmailAddressType)](name-emailaddresstype.md) element and does not return the [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) element in the [Mailbox](mailbox.md) element for the following fields:</span></span> 
  
- <span data-ttu-id="a2229-133">El campo [de](from.md) para los mensajes</span><span class="sxs-lookup"><span data-stu-id="a2229-133">The [From](from.md) field for messages</span></span> 
    
- <span data-ttu-id="a2229-134">El campo [Sender](sender.md) para los mensajes</span><span class="sxs-lookup"><span data-stu-id="a2229-134">The [Sender](sender.md) field for messages</span></span> 
    
- <span data-ttu-id="a2229-135">El campo [Organizer](organizer.md) para los elementos de calendario</span><span class="sxs-lookup"><span data-stu-id="a2229-135">The [Organizer](organizer.md) field for calendar items</span></span> 
    
> [!NOTE]
> <span data-ttu-id="a2229-136">La operación **FindItem** puede devolver resultados en un elemento [CalendarView](calendarview.md) .</span><span class="sxs-lookup"><span data-stu-id="a2229-136">The **FindItem** operation can return results in a [CalendarView](calendarview.md) element.</span></span> <span data-ttu-id="a2229-137">El elemento **CalendarView** devuelve elementos de calendario únicos y todas las repeticiones de reuniones periódicas.</span><span class="sxs-lookup"><span data-stu-id="a2229-137">The **CalendarView** element returns single calendar items and all occurrences of recurring meetings.</span></span> <span data-ttu-id="a2229-138">Si no se usa un elemento **CalendarView** , se devuelven los elementos de calendario únicos y los elementos de calendario principal periódicos.</span><span class="sxs-lookup"><span data-stu-id="a2229-138">If a **CalendarView** element is not used, single calendar items and recurring master calendar items are returned.</span></span> <span data-ttu-id="a2229-139">Las repeticiones deben expandirse desde el maestro periódico si no se usa un elemento **CalendarView** .</span><span class="sxs-lookup"><span data-stu-id="a2229-139">The occurrences must be expanded from the recurring master if a **CalendarView** element is not used.</span></span> 
  
<span data-ttu-id="a2229-140">La operación **FindItem** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="a2229-140">The **FindItem** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
<span data-ttu-id="a2229-141">**Tabla 1. Encabezados SOAP de la operación FindItem**</span><span class="sxs-lookup"><span data-stu-id="a2229-141">**Table 1. FindItem operation SOAP headers**</span></span>

|<span data-ttu-id="a2229-142">**Header**</span><span class="sxs-lookup"><span data-stu-id="a2229-142">**Header**</span></span>|<span data-ttu-id="a2229-143">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a2229-143">**Element**</span></span>|<span data-ttu-id="a2229-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a2229-144">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a2229-145">**DateTimePrecision**</span><span class="sxs-lookup"><span data-stu-id="a2229-145">**DateTimePrecision**</span></span> <br/> |[<span data-ttu-id="a2229-146">DateTimePrecision</span><span class="sxs-lookup"><span data-stu-id="a2229-146">DateTimePrecision</span></span>](datetimeprecision.md) <br/> |<span data-ttu-id="a2229-147">Especifica la resolución de los valores de datos/tiempo en respuestas del servidor, en segundos o en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="a2229-147">Specifies the resolution of data/time values in responses from the server, either in seconds or in milliseconds.</span></span> <span data-ttu-id="a2229-148">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="a2229-148">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="a2229-149">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="a2229-149">**Impersonation**</span></span> <br/> |[<span data-ttu-id="a2229-150">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="a2229-150">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="a2229-151">Identifica al usuario que está suplantando la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="a2229-151">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="a2229-152">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="a2229-152">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="a2229-153">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="a2229-153">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="a2229-154">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="a2229-154">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="a2229-155">Identifica la referencia cultural RFC3066 que se va a usar para obtener acceso al buzón.</span><span class="sxs-lookup"><span data-stu-id="a2229-155">Identifies the RFC3066 culture to be used to access the mailbox.</span></span> <span data-ttu-id="a2229-156">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="a2229-156">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="a2229-157">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="a2229-157">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="a2229-158">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="a2229-158">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="a2229-159">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="a2229-159">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="a2229-160">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="a2229-160">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="a2229-161">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="a2229-161">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="a2229-162">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="a2229-162">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="a2229-163">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a2229-163">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="a2229-164">Esto es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2229-164">This is applicable to a response.</span></span>  <br/> |
|<span data-ttu-id="a2229-165">**TimeZoneContext**</span><span class="sxs-lookup"><span data-stu-id="a2229-165">**TimeZoneContext**</span></span> <br/> |[<span data-ttu-id="a2229-166">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="a2229-166">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="a2229-167">Identifica la zona horaria que se va a usar para todas las respuestas del servidor.</span><span class="sxs-lookup"><span data-stu-id="a2229-167">Identifies the time zone to be used for all responses from the server.</span></span> <span data-ttu-id="a2229-168">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="a2229-168">This is applicable to a request.</span></span>  <br/> |
   
## <a name="finditem-operation-request-example"></a><span data-ttu-id="a2229-169">Ejemplo de solicitud de operación de FindItem</span><span class="sxs-lookup"><span data-stu-id="a2229-169">FindItem operation request example</span></span>

<span data-ttu-id="a2229-170">El siguiente ejemplo de una solicitud **FindItem** muestra cómo obtener el identificador de elemento definido por la enumeración **IdOnly** del elemento [BaseShape](baseshape.md) para los elementos que se encuentran en la carpeta elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="a2229-170">The following example of a **FindItem** request shows how to obtain the item identifier that is defined by the **IdOnly** enumeration of the [BaseShape](baseshape.md) element for items that are found in the Deleted Items folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
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

<span data-ttu-id="a2229-171">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="a2229-171">The following elements are used in the request:</span></span> 
  
- [<span data-ttu-id="a2229-172">FindItem</span><span class="sxs-lookup"><span data-stu-id="a2229-172">FindItem</span></span>](finditem.md)
    
- [<span data-ttu-id="a2229-173">ItemShape</span><span class="sxs-lookup"><span data-stu-id="a2229-173">ItemShape</span></span>](itemshape.md)
    
- [<span data-ttu-id="a2229-174">BaseShape</span><span class="sxs-lookup"><span data-stu-id="a2229-174">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="a2229-175">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="a2229-175">ParentFolderIds</span></span>](parentfolderids.md)
    
- [<span data-ttu-id="a2229-176">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="a2229-176">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
<span data-ttu-id="a2229-177">Para obtener más opciones para un mensaje de solicitud **FindItem** , explore la jerarquía del esquema.</span><span class="sxs-lookup"><span data-stu-id="a2229-177">For more options for a **FindItem** request message, explore the schema hierarchy.</span></span> <span data-ttu-id="a2229-178">Comienza en el elemento [FindItem](finditem.md) .</span><span class="sxs-lookup"><span data-stu-id="a2229-178">Start at the [FindItem](finditem.md) element.</span></span> 
  
## <a name="successful-finditem-operation-response"></a><span data-ttu-id="a2229-179">Respuesta correcta a la operación FindItem</span><span class="sxs-lookup"><span data-stu-id="a2229-179">Successful FindItem operation response</span></span>

<span data-ttu-id="a2229-180">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud **FindItem** .</span><span class="sxs-lookup"><span data-stu-id="a2229-180">The following example shows a successful response to the **FindItem** request.</span></span> 
  
<span data-ttu-id="a2229-181">Los elementos de [mensaje](message-ex15websvcsotherref.md) representan mensajes de correo electrónico y todos los demás elementos que no tienen establecimiento inflexible de tipos en el esquema EWS.</span><span class="sxs-lookup"><span data-stu-id="a2229-181">[Message](message-ex15websvcsotherref.md) elements represent email messages and all other items that are not strongly typed by the EWS schema.</span></span> <span data-ttu-id="a2229-182">Elementos como IPM. Uso compartido e IPM. InfoPath se devuelven como elementos del [mensaje](message-ex15websvcsotherref.md) .</span><span class="sxs-lookup"><span data-stu-id="a2229-182">Items such as IPM.Sharing and IPM.InfoPath are returned as [Message](message-ex15websvcsotherref.md) elements.</span></span> <span data-ttu-id="a2229-183">Exchange no devuelve el elemento de [elemento](item.md) base en las respuestas.</span><span class="sxs-lookup"><span data-stu-id="a2229-183">Exchange does not return the base [Item](item.md) element in responses.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="a2229-184">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="a2229-184">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="a2229-185">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="a2229-185">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="a2229-186">FindItemResponse</span><span class="sxs-lookup"><span data-stu-id="a2229-186">FindItemResponse</span></span>](finditemresponse.md)
    
- [<span data-ttu-id="a2229-187">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a2229-187">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="a2229-188">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a2229-188">FindItemResponseMessage</span></span>](finditemresponsemessage.md)
    
- [<span data-ttu-id="a2229-189">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a2229-189">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="a2229-190">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="a2229-190">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md)
    
- [<span data-ttu-id="a2229-191">Items</span><span class="sxs-lookup"><span data-stu-id="a2229-191">Items</span></span>](items.md)
    
- [<span data-ttu-id="a2229-192">Message</span><span class="sxs-lookup"><span data-stu-id="a2229-192">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="a2229-193">ItemId</span><span class="sxs-lookup"><span data-stu-id="a2229-193">ItemId</span></span>](itemid.md)
    
<span data-ttu-id="a2229-194">Para obtener más opciones para un mensaje de respuesta **FindItem** , explore la jerarquía del esquema.</span><span class="sxs-lookup"><span data-stu-id="a2229-194">For more options for a **FindItem** response message, explore the schema hierarchy.</span></span> <span data-ttu-id="a2229-195">Empiece en el elemento [FindItemResponse](finditemresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="a2229-195">Start at the [FindItemResponse](finditemresponse.md) element.</span></span> 
  
## <a name="finditem-operation-error-response"></a><span data-ttu-id="a2229-196">Respuesta de error de la operación FindItem</span><span class="sxs-lookup"><span data-stu-id="a2229-196">FindItem operation error response</span></span>

<span data-ttu-id="a2229-197">En el ejemplo siguiente se muestra una respuesta de error a una solicitud **FindItem** .</span><span class="sxs-lookup"><span data-stu-id="a2229-197">The following example shows an error response to a **FindItem** request.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="a2229-198">Los siguientes elementos se usan en la respuesta de error:</span><span class="sxs-lookup"><span data-stu-id="a2229-198">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="a2229-199">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="a2229-199">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="a2229-200">FindItemResponse</span><span class="sxs-lookup"><span data-stu-id="a2229-200">FindItemResponse</span></span>](finditemresponse.md)
    
- [<span data-ttu-id="a2229-201">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a2229-201">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="a2229-202">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a2229-202">FindItemResponseMessage</span></span>](finditemresponsemessage.md)
    
- [<span data-ttu-id="a2229-203">MessageText</span><span class="sxs-lookup"><span data-stu-id="a2229-203">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="a2229-204">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a2229-204">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="a2229-205">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="a2229-205">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="a2229-206">Para obtener más opciones para un mensaje de respuesta de error de **FindItem** , explore la jerarquía del esquema.</span><span class="sxs-lookup"><span data-stu-id="a2229-206">For more options for a **FindItem** error response message, explore the schema hierarchy.</span></span> <span data-ttu-id="a2229-207">Empiece en el elemento [FindItemResponse](finditemresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="a2229-207">Start at the [FindItemResponse](finditemresponse.md) element.</span></span> 
  
## <a name="version-differences"></a><span data-ttu-id="a2229-208">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="a2229-208">Version differences</span></span>

<span data-ttu-id="a2229-209">Las versiones de Exchange que comienzan con la versión principal 15 y terminan con la compilación 15.0.898.11 devuelven un valor de ErrorInvalidOperation en el elemento [ResponseCode](responsecode.md) cuando se usa la operación **FindItem** para buscar en varias carpetas de un buzón de archivo.</span><span class="sxs-lookup"><span data-stu-id="a2229-209">Versions of Exchange starting with major version 15 and ending with build 15.0.898.11 return an ErrorInvalidOperation value in the [ResponseCode](responsecode.md) element when the **FindItem** operation is used to search multiple folders in an archive mailbox.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a2229-210">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2229-210">See also</span></span>

- [<span data-ttu-id="a2229-211">Buscar elementos</span><span class="sxs-lookup"><span data-stu-id="a2229-211">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)
    
- [<span data-ttu-id="a2229-212">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a2229-212">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
    
- <span data-ttu-id="a2229-213">**FindItemType**</span><span class="sxs-lookup"><span data-stu-id="a2229-213">**FindItemType**</span></span>
    

