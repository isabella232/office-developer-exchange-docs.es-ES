---
title: Operación GetImItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 51186691-46d2-4d5c-b8bc-4ee2bb20fbe7
description: Busque información sobre la EWS GetImItems operación.
ms.openlocfilehash: 4335cc22b22dc5f102f2221f7fdb22a506ba026f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764875"
---
# <a name="getimitems-operation"></a><span data-ttu-id="efc13-103">Operación GetImItems</span><span class="sxs-lookup"><span data-stu-id="efc13-103">GetImItems operation</span></span>

<span data-ttu-id="efc13-104">Obtenga información acerca de la operación de EWS **GetImItems** .</span><span class="sxs-lookup"><span data-stu-id="efc13-104">Find information about the **GetImItems** EWS operation.</span></span> 
  
<span data-ttu-id="efc13-105">La operación **GetImItems** recupera información acerca de los grupos de mensajería instantánea y mensajería instantánea, póngase en contacto con los roles.</span><span class="sxs-lookup"><span data-stu-id="efc13-105">The **GetImItems** operation retrieves information about instant messaging (IM) groups and IM contact personas.</span></span> 
  
<span data-ttu-id="efc13-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="efc13-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getimitems-operation"></a><span data-ttu-id="efc13-107">Mediante la operación GetImItems</span><span class="sxs-lookup"><span data-stu-id="efc13-107">Using the GetImItems operation</span></span>

<span data-ttu-id="efc13-108">La operación **GetImItems** acepta grupo y contacto identificadores de elemento y devuelve un conjunto de información acerca de los grupos y contactos.</span><span class="sxs-lookup"><span data-stu-id="efc13-108">The **GetImItems** operation accepts group and contact item identifiers and returns a set of information about the groups and contacts.</span></span> <span data-ttu-id="efc13-109">Los conjuntos de propiedades devueltos en la respuesta se había identificado por las propiedades extendidas, varios identificadores de contacto, identificadores de grupo y extender las definiciones de propiedad como argumentos.</span><span class="sxs-lookup"><span data-stu-id="efc13-109">The property sets returned in the response are identified by extended properties, multiple contact identifiers, group identifiers, and extended property definitions as arguments.</span></span> 
  
### <a name="getimitems-operation-soap-headers"></a><span data-ttu-id="efc13-110">Encabezados SOAP de operación de GetImItems</span><span class="sxs-lookup"><span data-stu-id="efc13-110">GetImItems operation SOAP headers</span></span>

<span data-ttu-id="efc13-111">La operación de **GetImItems** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="efc13-111">The **GetImItems** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="efc13-112">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="efc13-112">**Header name**</span></span>|<span data-ttu-id="efc13-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="efc13-113">**Element**</span></span>|<span data-ttu-id="efc13-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="efc13-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="efc13-115">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="efc13-115">**Impersonation**</span></span> <br/> |[<span data-ttu-id="efc13-116">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="efc13-116">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="efc13-117">Identifica el usuario que está realizando la suplantación de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="efc13-117">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="efc13-118">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="efc13-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="efc13-119">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="efc13-119">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="efc13-120">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="efc13-120">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="efc13-121">Identifica la referencia cultural, como se define en RFC 3066, "Etiquetas para la identificación de idiomas," que se utilizará para acceder al buzón.</span><span class="sxs-lookup"><span data-stu-id="efc13-121">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="efc13-122">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="efc13-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="efc13-123">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="efc13-123">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="efc13-124">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="efc13-124">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="efc13-125">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="efc13-125">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="efc13-126">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="efc13-126">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="efc13-127">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="efc13-127">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="efc13-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="efc13-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="efc13-129">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="efc13-129">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="efc13-130">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="efc13-130">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getimitems-operation-request-example-get-detailed-information-about-im-contacts-and-groups"></a><span data-ttu-id="efc13-131">Ejemplo de solicitud de operación de GetImItems: obtener información detallada acerca de los contactos de mensajería instantánea y grupos</span><span class="sxs-lookup"><span data-stu-id="efc13-131">GetImItems operation request example: Get detailed information about IM contacts and groups</span></span>

<span data-ttu-id="efc13-132">El siguiente ejemplo de una solicitud de operación **GetImItems** muestra cómo solicitar información detallada acerca de los grupos y contactos de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="efc13-132">The following example of a **GetImItems** operation request shows how to request detailed information about IM contacts and groups.</span></span> <span data-ttu-id="efc13-133">Una operación de **GetImItems** puede solicitar uno o varios contactos o detalles del grupo.</span><span class="sxs-lookup"><span data-stu-id="efc13-133">A **GetImItems** operation can request one or more contact or group details.</span></span> <span data-ttu-id="efc13-134">También puede usar las propiedades extendidas para obtener las propiedades personalizadas en grupos y contactos.</span><span class="sxs-lookup"><span data-stu-id="efc13-134">You can also use extended properties to get custom properties on groups and contacts.</span></span> <span data-ttu-id="efc13-135">Si una propiedad extendida solicitado no existe en un elemento, la respuesta omitirá la propiedad solicitada y devolver la respuesta para el conjunto de propiedades predeterminado.</span><span class="sxs-lookup"><span data-stu-id="efc13-135">If a requested extended property does not exist on an item, the response will ignore the requested property and return the response for the default property set.</span></span> <span data-ttu-id="efc13-136">En este ejemplo se muestra cómo obtener el nombre para mostrar mediante el uso de las propiedades extendidas.</span><span class="sxs-lookup"><span data-stu-id="efc13-136">This example shows you how to get the display name by using extended properties.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="efc13-137">Todos los identificadores de artículo y cambiar claves en este artículo se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="efc13-137">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> <span data-ttu-id="efc13-138">Tenga en cuenta que cambiar claves se omiten por el servicio para esta operación.</span><span class="sxs-lookup"><span data-stu-id="efc13-138">Note that change keys are ignored by the service for this operation.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
   </soap:Header>
   <soap:Body >
      <m:GetImItems>
         <m:ContactIds>
            <t:ItemId Id="AAMkADEzOTExYACABmEhpSAAA=" ChangeKey="EQAAABBmNDjF"/>
         </m:ContactIds>
         <m:GroupIds>
            <t:ItemId Id="AAMkADEzOTExYjJkBY7+0EAAA=" ChangeKey="EgAAAA=="/>
         </m:GroupIds>         
         <m:ExtendedProperties>
            <t:ExtendedProperty PropertyTag="0x3001" PropertyType="String"/>
         </m:ExtendedProperties>
      </m:GetImItems>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="efc13-139">La solicitud SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="efc13-139">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="efc13-140">GetImItems</span><span class="sxs-lookup"><span data-stu-id="efc13-140">GetImItems</span></span>](getimitems.md)
    
- [<span data-ttu-id="efc13-141">ContactIds</span><span class="sxs-lookup"><span data-stu-id="efc13-141">ContactIds</span></span>](contactids.md)
    
- [<span data-ttu-id="efc13-142">ItemId</span><span class="sxs-lookup"><span data-stu-id="efc13-142">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="efc13-143">GroupIds</span><span class="sxs-lookup"><span data-stu-id="efc13-143">GroupIds</span></span>](groupids.md)
    
- [<span data-ttu-id="efc13-144">ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)</span><span class="sxs-lookup"><span data-stu-id="efc13-144">ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)</span></span>](extendedproperties-nonemptyarrayofextendedfielduris.md)
    
- [<span data-ttu-id="efc13-145">ExtendedProperty (PathToExtendedFieldType)</span><span class="sxs-lookup"><span data-stu-id="efc13-145">ExtendedProperty (PathToExtendedFieldType)</span></span>](extendedproperty-pathtoextendedfieldtype.md)
    
## <a name="successful-getimitems-operation-response"></a><span data-ttu-id="efc13-146">Respuesta es correcta de operación GetImItems</span><span class="sxs-lookup"><span data-stu-id="efc13-146">Successful GetImItems operation response</span></span>

<span data-ttu-id="efc13-147">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de **GetImItems** para obtener un contacto de mensajería instantánea y el grupo.</span><span class="sxs-lookup"><span data-stu-id="efc13-147">The following example shows a successful response to a **GetImItems** request to get an IM contact and group.</span></span> <span data-ttu-id="efc13-148">Se solicita el nombre para mostrar de una propiedad extendida.</span><span class="sxs-lookup"><span data-stu-id="efc13-148">The display name is requested in an extended property.</span></span> <span data-ttu-id="efc13-149">Contactos de mensajería instantánea se devuelven en el formulario de un rol.</span><span class="sxs-lookup"><span data-stu-id="efc13-149">IM contacts are returned in the form of a persona.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetImItemsResponse ResponseClass="Success" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <ImItemList>
            <Groups xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <ImGroup>
                  <DisplayName>Exchange SDK Team</DisplayName>
                  <GroupType>IPM.DistList.MOC.UserGroup</GroupType>
                  <ExchangeStoreId Id="AAMkADEzQrAABY7+0EAAA=" ChangeKey="EgAAAA=="/>
                  <MemberCorrelationKey>
                     <ItemId Id="AAMkADEzOTExYjeGgGqm4QrAABmEhpSAAA=" ChangeKey="EQAAAA=="/>
                  </MemberCorrelationKey>
                  <ExtendedProperties>
                     <ExtendedProperty>
                        <ExtendedFieldURI PropertyTag="0x3001" PropertyType="String"/>
                        <Value>Exchange SDK Team</Value>
                     </ExtendedProperty>
                  </ExtendedProperties>
               </ImGroup>
            </Groups>
            <Personas xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <Persona>
                  <PersonaId Id="AAQkADEzOTBZImBzN5J/uHXc="/>
                  <PersonaType>Person</PersonaType>
                  <CreationTime>2012-11-07T00:10:35Z</CreationTime>
                  <DisplayName>Tony Smith</DisplayName>
                  <DisplayNameFirstLast>Tony Smith</DisplayNameFirstLast>
                  <DisplayNameLastFirst>Tony Smith</DisplayNameLastFirst>
                  <FileAs/>
                  <FileAsId>None</FileAsId>
                  <ImAddress>tsmith@contoso.com</ImAddress>
                  <RelevanceScore>2147483647</RelevanceScore>
                  <Attributions>
                     <Attribution>
                        <Id>0</Id>
                        <SourceId Id="AAMkADEzhQaoeGgGqm4QrAABmEhpSAAA=" ChangeKey="EQArAABmNDjF"/>
                        <DisplayName>Lync Contacts</DisplayName>
                        <IsWritable>false</IsWritable>
                        <IsQuickContact>true</IsQuickContact>
                        <IsHidden>false</IsHidden>
                     </Attribution>
                  </Attributions>
                  <DisplayNames>
                     <StringAttributedValue>
                        <Value>Tony Smith</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </DisplayNames>
                  <FileAsIds>
                     <StringAttributedValue>
                        <Value>None</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </FileAsIds>
                  <ImAddresses>
                     <StringAttributedValue>
                        <Value>tsmith@contoso.com</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </ImAddresses>
                  <ExtendedProperties>
                     <ExtendedPropertyAttributedValue>
                        <Value>
                           <ExtendedFieldURI PropertyTag="0x3001" PropertyType="String"/>
                           <Value>Tony Smith</Value>
                        </Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </ExtendedPropertyAttributedValue>
                  </ExtendedProperties>
               </Persona>
            </Personas>
         </ImItemList>
      </GetImItemsResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="efc13-150">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="efc13-150">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="efc13-151">GetImItemsResponse</span><span class="sxs-lookup"><span data-stu-id="efc13-151">GetImItemsResponse</span></span>](getimitemsresponse.md)
    
- [<span data-ttu-id="efc13-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="efc13-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="efc13-153">ImItemList</span><span class="sxs-lookup"><span data-stu-id="efc13-153">ImItemList</span></span>](imitemlist.md)
    
- [<span data-ttu-id="efc13-154">Grupos (ArrayOfImGroupType)</span><span class="sxs-lookup"><span data-stu-id="efc13-154">Groups (ArrayOfImGroupType)</span></span>](groups-arrayofimgrouptype.md)
    
- [<span data-ttu-id="efc13-155">ImGroup</span><span class="sxs-lookup"><span data-stu-id="efc13-155">ImGroup</span></span>](imgroup.md)
    
- [<span data-ttu-id="efc13-156">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="efc13-156">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="efc13-157">GroupType</span><span class="sxs-lookup"><span data-stu-id="efc13-157">GroupType</span></span>](grouptype.md)
    
- [<span data-ttu-id="efc13-158">ExchangeStoreId</span><span class="sxs-lookup"><span data-stu-id="efc13-158">ExchangeStoreId</span></span>](exchangestoreid.md)
    
- [<span data-ttu-id="efc13-159">MemberCorrelationKey</span><span class="sxs-lookup"><span data-stu-id="efc13-159">MemberCorrelationKey</span></span>](membercorrelationkey.md)
    
- [<span data-ttu-id="efc13-160">ItemId</span><span class="sxs-lookup"><span data-stu-id="efc13-160">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="efc13-161">ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)</span><span class="sxs-lookup"><span data-stu-id="efc13-161">ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)</span></span>](extendedproperties-nonemptyarrayofextendedfielduris.md)
    
- [<span data-ttu-id="efc13-162">ExtendedProperty (PathToExtendedFieldType)</span><span class="sxs-lookup"><span data-stu-id="efc13-162">ExtendedProperty (PathToExtendedFieldType)</span></span>](extendedproperty-pathtoextendedfieldtype.md)
    
- [<span data-ttu-id="efc13-163">Roles</span><span class="sxs-lookup"><span data-stu-id="efc13-163">Personas</span></span>](personas-ex15websvcsotherref.md)
    
- [<span data-ttu-id="efc13-164">PersonaId</span><span class="sxs-lookup"><span data-stu-id="efc13-164">PersonaId</span></span>](personaid.md)
    
- [<span data-ttu-id="efc13-165">PersonaType</span><span class="sxs-lookup"><span data-stu-id="efc13-165">PersonaType</span></span>](personatype.md)
    
- [<span data-ttu-id="efc13-166">CreationTime</span><span class="sxs-lookup"><span data-stu-id="efc13-166">CreationTime</span></span>](creationtime.md)
    
- [<span data-ttu-id="efc13-167">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="efc13-167">DisplayNameFirstLast</span></span>](displaynamefirstlast.md)
    
- [<span data-ttu-id="efc13-168">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="efc13-168">DisplayNameLastFirst</span></span>](displaynamelastfirst.md)
    
- [<span data-ttu-id="efc13-169">Archivar como</span><span class="sxs-lookup"><span data-stu-id="efc13-169">FileAs</span></span>](fileas.md)
    
- <span data-ttu-id="efc13-170">[FileAsId](fileasid.md) FileAsId</span><span class="sxs-lookup"><span data-stu-id="efc13-170">[FileAsId](fileasid.md) FileAsId</span></span> 
    
- [<span data-ttu-id="efc13-171">ImAddress (cadena)</span><span class="sxs-lookup"><span data-stu-id="efc13-171">ImAddress (String)</span></span>](imaddress-string.md)
    
- [<span data-ttu-id="efc13-172">RelevanceScore</span><span class="sxs-lookup"><span data-stu-id="efc13-172">RelevanceScore</span></span>](relevancescore.md)
    
- [<span data-ttu-id="efc13-173">Atribuciones (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="efc13-173">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md)
    
- [<span data-ttu-id="efc13-174">Atribución (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="efc13-174">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
    
- [<span data-ttu-id="efc13-175">Identificador (cadena)</span><span class="sxs-lookup"><span data-stu-id="efc13-175">ID (String)</span></span>](id-string.md)
    
- [<span data-ttu-id="efc13-176">SourceId</span><span class="sxs-lookup"><span data-stu-id="efc13-176">SourceId</span></span>](sourceid.md)
    
- [<span data-ttu-id="efc13-177">IsWritable</span><span class="sxs-lookup"><span data-stu-id="efc13-177">IsWritable</span></span>](iswritable.md)
    
- [<span data-ttu-id="efc13-178">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="efc13-178">IsQuickContact</span></span>](isquickcontact.md)
    
- [<span data-ttu-id="efc13-179">IsHidden</span><span class="sxs-lookup"><span data-stu-id="efc13-179">IsHidden</span></span>](ishidden.md)
    
- [<span data-ttu-id="efc13-180">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="efc13-180">StringAttributedValue</span></span>](stringattributedvalue.md)
    
- [<span data-ttu-id="efc13-181">FileAsIds</span><span class="sxs-lookup"><span data-stu-id="efc13-181">FileAsIds</span></span>](fileasids.md)
    
- [<span data-ttu-id="efc13-182">ImAddresses</span><span class="sxs-lookup"><span data-stu-id="efc13-182">ImAddresses</span></span>](imaddresses.md)
    
- [<span data-ttu-id="efc13-183">Valor (ExtendedPropertyType)</span><span class="sxs-lookup"><span data-stu-id="efc13-183">Value (ExtendedPropertyType)</span></span>](value-extendedpropertytype.md)
    
## <a name="getimitems-operation-error-response"></a><span data-ttu-id="efc13-184">Respuesta de error de la operación de GetImItems</span><span class="sxs-lookup"><span data-stu-id="efc13-184">GetImItems operation error response</span></span>

<span data-ttu-id="efc13-185">La operación **GetImItems** no validar los identificadores y no devolverá la respuesta de error esperada **ErrorInvalidImContactId** o **ErrorInvalidImGroupId** si un contacto no válido o el identificador de grupo se proporciona para el servicio.</span><span class="sxs-lookup"><span data-stu-id="efc13-185">The **GetImItems** operation does not validate identifiers and will not return the expected **ErrorInvalidImContactId** or **ErrorInvalidImGroupId** error response if an invalid contact or group identifier is provided to the service.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="efc13-186">Vea también</span><span class="sxs-lookup"><span data-stu-id="efc13-186">See also</span></span>

- [<span data-ttu-id="efc13-187">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="efc13-187">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="efc13-188">Operación GetImItemList</span><span class="sxs-lookup"><span data-stu-id="efc13-188">GetImItemList operation</span></span>](getimitemlist-operation.md)
    

