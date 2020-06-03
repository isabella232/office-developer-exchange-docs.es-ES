---
title: Operación GetImItemList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e31d14e1-0c1f-4b69-98b7-157d59c13698
description: Buscar información sobre la operación de EWS de GetImItemList.
ms.openlocfilehash: aabe84054b93e7de8af6145942493a0224932e45
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456069"
---
# <a name="getimitemlist-operation"></a><span data-ttu-id="17040-103">Operación GetImItemList</span><span class="sxs-lookup"><span data-stu-id="17040-103">GetImItemList operation</span></span>

<span data-ttu-id="17040-104">Buscar información sobre la operación de EWS de **GetImItemList** .</span><span class="sxs-lookup"><span data-stu-id="17040-104">Find information about the **GetImItemList** EWS operation.</span></span> 
  
## <a name="using-the-getimitemlist-operation"></a><span data-ttu-id="17040-105">Uso de la operación GetImItemList</span><span class="sxs-lookup"><span data-stu-id="17040-105">Using the GetImItemList operation</span></span>

<span data-ttu-id="17040-106">La operación **GetImItemList** recupera la lista de grupos de mensajería instantánea (mi) y los roles de contactos de mensajería instantánea en un buzón.</span><span class="sxs-lookup"><span data-stu-id="17040-106">The **GetImItemList** operation retrieves the list of instant messaging (IM) groups and IM contact personas in a mailbox.</span></span> <span data-ttu-id="17040-107">La operación **GetImItemList** no toma ningún argumento.</span><span class="sxs-lookup"><span data-stu-id="17040-107">The **GetImItemList** operation does not take any arguments.</span></span> 
  
<span data-ttu-id="17040-108">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="17040-108">This operation was introduced in Exchange Server 2013.</span></span>
  
### <a name="getimitemlist-operation-soap-headers"></a><span data-ttu-id="17040-109">Encabezados SOAP de operación GetImItemList</span><span class="sxs-lookup"><span data-stu-id="17040-109">GetImItemList operation SOAP headers</span></span>

<span data-ttu-id="17040-110">La operación **GetImItemList** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="17040-110">The **GetImItemList** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="17040-111">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="17040-111">**Header name**</span></span>|<span data-ttu-id="17040-112">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="17040-112">**Element**</span></span>|<span data-ttu-id="17040-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="17040-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="17040-114">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="17040-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="17040-115">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="17040-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="17040-116">Identifica al usuario que está suplantando la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="17040-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="17040-117">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="17040-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="17040-118">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="17040-118">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="17040-119">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="17040-119">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="17040-120">Identifica la referencia cultural, tal y como se define en RFC 3066, "etiquetas para la identificación de idiomas", que se va a usar para obtener acceso al buzón.</span><span class="sxs-lookup"><span data-stu-id="17040-120">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="17040-121">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="17040-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="17040-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="17040-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="17040-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="17040-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="17040-124">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="17040-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="17040-125">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="17040-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="17040-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="17040-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="17040-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="17040-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="17040-128">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="17040-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="17040-129">Este encabezado se aplica a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="17040-129">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getimitemlist-operation-request-example-request-your-im-items-list"></a><span data-ttu-id="17040-130">Ejemplo de solicitud de operación GetImItemList: solicitar la lista de elementos de mi</span><span class="sxs-lookup"><span data-stu-id="17040-130">GetImItemList operation request example: Request your IM items list</span></span>

<span data-ttu-id="17040-131">El siguiente ejemplo de una solicitud de operación de **GetImItemList** muestra cómo solicitar la lista de grupos de mensajería instantánea y los roles de contactos de mensajería instantánea en un buzón.</span><span class="sxs-lookup"><span data-stu-id="17040-131">The following example of a **GetImItemList** operation request shows how to request the list of IM groups and IM contact personas in a mailbox.</span></span> <span data-ttu-id="17040-132">El elemento **GetImItemList** es la única opción de elemento en el cuerpo SOAP.</span><span class="sxs-lookup"><span data-stu-id="17040-132">The **GetImItemList** element is the only element option in the SOAP body.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
   </soap:Header>
   <soap:Body >
      <m:GetImItemList/>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="17040-133">El cuerpo SOAP de la solicitud contiene el siguiente elemento:</span><span class="sxs-lookup"><span data-stu-id="17040-133">The request SOAP body contains the following element:</span></span>
  
- [<span data-ttu-id="17040-134">GetImItemList</span><span class="sxs-lookup"><span data-stu-id="17040-134">GetImItemList</span></span>](getimitemlist.md)
    
## <a name="successful-getimitemlist-operation-response"></a><span data-ttu-id="17040-135">Respuesta de operación GetImItemList correcta</span><span class="sxs-lookup"><span data-stu-id="17040-135">Successful GetImItemList operation response</span></span>

<span data-ttu-id="17040-136">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **GetImItemList** .</span><span class="sxs-lookup"><span data-stu-id="17040-136">The following example shows a successful response to a **GetImItemList** operation request.</span></span> <span data-ttu-id="17040-137">La respuesta contiene cuatro grupos de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="17040-137">The response contains four IM groups.</span></span> <span data-ttu-id="17040-138">Tres de los grupos de mensajería instantánea (otros contactos, etiquetados y favoritos) son los grupos predeterminados en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="17040-138">Three of the IM groups — Other Contacts, Tagged, and Favorites — are default groups in the Exchange store.</span></span> <span data-ttu-id="17040-139">El grupo MyCustomGroup2 es un grupo personalizado creado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="17040-139">The MyCustomGroup2 group is a custom user-created group.</span></span> <span data-ttu-id="17040-140">Los demás contactos y los grupos etiquetados no tienen miembros.</span><span class="sxs-lookup"><span data-stu-id="17040-140">The Other Contacts and Tagged groups do not have members.</span></span> <span data-ttu-id="17040-141">El grupo de favoritos tiene un único miembro de contacto.</span><span class="sxs-lookup"><span data-stu-id="17040-141">The Favorites group has a single contact member.</span></span> <span data-ttu-id="17040-142">MyCustomGroup2 tiene dos contactos de miembros.</span><span class="sxs-lookup"><span data-stu-id="17040-142">The MyCustomGroup2 has two member contacts.</span></span> <span data-ttu-id="17040-143">Los identificadores de elemento se proporcionan para que se puedan realizar las siguientes solicitudes **GetItem** para obtener más información sobre los contactos de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="17040-143">The item identifiers are provided so that subsequent **GetItem** requests can be performed to get more information about the IM contacts.</span></span> 
  
<span data-ttu-id="17040-144">En este ejemplo se devuelven dos roles.</span><span class="sxs-lookup"><span data-stu-id="17040-144">This example returns two personas.</span></span> <span data-ttu-id="17040-145">El primer rol representa dos elementos de contacto: Anthony Martínez y Tony Smith.</span><span class="sxs-lookup"><span data-stu-id="17040-145">The first persona represents two contact items: Anthony Smith and Tony Smith.</span></span> <span data-ttu-id="17040-146">La información de contacto combinada se devuelve en el objeto de **rol** .</span><span class="sxs-lookup"><span data-stu-id="17040-146">The combined contact information is returned in the **Persona** object.</span></span> <span data-ttu-id="17040-147">El segundo rol representa un solo contacto con el nombre para mostrar de Terence Adams.</span><span class="sxs-lookup"><span data-stu-id="17040-147">The second persona represents a single contact with the display name of Terence Adams.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="17040-148">Los identificadores del almacén de Exchange, los identificadores de los elementos, los identificadores de origen, los identificadores de las carpetas y los identificadores de los roles se han reducido para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="17040-148">The Exchange store identifiers, item identifiers, source identifiers, folder identifiers, and persona identifiers have been shortened to preserve readability.</span></span> 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="349" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" />
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetImItemListResponse ResponseClass="Success" 
                             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <ImItemList>
            <Groups xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <ImGroup>
                  <DisplayName>Other Contacts</DisplayName>
                  <GroupType>IPM.DistList.MOC.OtherContacts</GroupType>
                  <ExchangeStoreId Id="AAMkAGQ1MjJjMTBkLThQoTbWAAAAAAQUAAA=" 
                                   ChangeKey="EgAAAA==" />
               </ImGroup>
               <ImGroup>
                  <DisplayName>Tagged</DisplayName>
                  <GroupType>IPM.DistList.MOC.Tagged</GroupType>
                  <ExchangeStoreId Id="AAMkAGQ1MjJAAQTAAA=" 
                                   ChangeKey="EgAAAA==" />
               </ImGroup>
               <ImGroup>
                  <DisplayName>Favorites</DisplayName>
                  <GroupType>IPM.DistList.MOC.Favorites</GroupType>
                  <ExchangeStoreId Id="AAMkAGQ1MjJjMTAAAAAQSAAA=" 
                                   ChangeKey="EgAAAA==" />
                  <MemberCorrelationKey>
                     <ItemId Id="AAMkAGQ1MjJtt/bhQoTbWAAAAAAvcAAA=" 
                             ChangeKey="EQAAAA==" />
                  </MemberCorrelationKey>
               </ImGroup>
               <ImGroup>
                  <DisplayName>MyCustomGroup2</DisplayName>
                  <GroupType>IPM.DistList.MOC.UserGroup</GroupType>
                  <ExchangeStoreId Id="AAMkAGQ1MjJjKAAA=" 
                                   ChangeKey="EgAAAA==" />
                  <MemberCorrelationKey>
                     <ItemId Id="AAMkAGQ1Matt/bhQoTbWAAAAAAvcAAA=" 
                             ChangeKey="EQAAAA==" />
                     <ItemId Id="AAMkAGQ1MjJjMTBkTbWAAAAAAveAAA=" 
                             ChangeKey="EQAAAA==" />
                  </MemberCorrelationKey>
               </ImGroup>
            </Groups>
            <Personas xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <Persona>
                  <PersonaId Id="AAQkAGQ1MjJjMTBkLTc4YkZmRkYQAQAFgxE1nBcqRGgYWWorM9/+s=" />
                  <PersonaType>Person</PersonaType>
                  <CreationTime>2012-01-12T22:14:36Z</CreationTime>
                  <DisplayName>Anthony Smith</DisplayName>
                  <DisplayNameFirstLast>Anthony Smith</DisplayNameFirstLast>
                  <DisplayNameLastFirst>Smith Anthony</DisplayNameLastFirst>
                  <FileAs>Smith, Anthony</FileAs>
                  <FileAsId>LastCommaFirst</FileAsId>
                  <GivenName>Anthony</GivenName>
                  <Surname>Smith</Surname>
                  <EmailAddress>
                     <Name>tsmith@contoso.com</Name>
                     <EmailAddress>tsmith@contoso.com</EmailAddress>
                     <RoutingType>SMTP</RoutingType>
                  </EmailAddress>
                  <EmailAddresses>
                     <EmailAddress>
                        <Name>tsmith@contoso.com</Name>
                        <EmailAddress>tsmith@contoso.com</EmailAddress>
                        <RoutingType>SMTP</RoutingType>
                     </EmailAddress>
                  </EmailAddresses>
                  <ImAddress>tsmith@contoso.com</ImAddress>
                  <RelevanceScore>2147483647</RelevanceScore>
                  <Attributions>
                     <Attribution>
                        <Id>0</Id>
                        <SourceId Id="AQMkAGQ1MjIAYzEwZC03OGNlLTQ5Bq239uFChNtYAAAIvDAAAAA==" 
                                  ChangeKey="EQAAABYAAABtF8oI7iVOQatt/bhQoTbWAAAAADB3" />
                        <DisplayName>Outlook</DisplayName>
                        <IsWritable>true</IsWritable>
                        <IsQuickContact>false</IsQuickContact>
                        <IsHidden>false</IsHidden>
                        <FolderId Id="AQMkAGQ1MjIAYzEMikE3AQBtF8oI7iVOQatt/bhQoTbWAAADEAAAAA==" 
                                  ChangeKey="AQAAAA==" />
                     </Attribution>
                     <Attribution>
                        <Id>1</Id>
                        <SourceId Id="AAMkAGQ1MjJjMTBkLTc4Y2UtNDA5Ny04/bhQoTbWAAAAAAveAAA=" 
                                  ChangeKey="EQAAABYAAABtF8oI7iVOQatt/bhQoTbWAAAAAAym" />
                        <DisplayName>Outlook</DisplayName>
                        <IsWritable>true</IsWritable>
                        <IsQuickContact>true</IsQuickContact>
                        <IsHidden>false</IsHidden>
                        <FolderId Id="AAMkAGQ1MjJjMTBkLTc4Y2UtNDA5Qatt/bhQoTbWAAAAAAvZAAA=" 
                                  ChangeKey="AQAAAA==" />
                     </Attribution>
                  </Attributions>
                  <DisplayNames>
                     <StringAttributedValue>
                        <Value>Anthony Smith</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                     <StringAttributedValue>
                        <Value>Tony Smith</Value>
                        <Attributions>
                           <Attribution>1</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </DisplayNames>
                  <FileAses>
                     <StringAttributedValue>
                        <Value>Smith, Anthony</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </FileAses>
                  <FileAsIds>
                     <StringAttributedValue>
                        <Value>LastCommaFirst</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                     <StringAttributedValue>
                        <Value>None</Value>
                        <Attributions>
                           <Attribution>1</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </FileAsIds>
                  <GivenNames>
                     <StringAttributedValue>
                        <Value>Anthony</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </GivenNames>
                  <Surnames>
                     <StringAttributedValue>
                        <Value>Smith</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </Surnames>
                  <HomePhones>
                     <PhoneNumberAttributedValue>
                        <Value>
                           <Number>4255550110</Number>
                           <Type>Home</Type>
                        </Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </PhoneNumberAttributedValue>
                  </HomePhones>
                  <MobilePhones>
                     <PhoneNumberAttributedValue>
                        <Value>
                           <Number>4255550120</Number>
                           <Type>Mobile</Type>
                        </Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </PhoneNumberAttributedValue>
                  </MobilePhones>
                  <Emails1>
                     <EmailAddressAttributedValue>
                        <Value>
                           <Name>tsmith@contoso.com</Name>
                           <EmailAddress>tsmith@contoso.com</EmailAddress>
                           <RoutingType>SMTP</RoutingType>
                        </Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                           <Attribution>1</Attribution>
                        </Attributions>
                     </EmailAddressAttributedValue>
                  </Emails1>
                  <ImAddresses>
                     <StringAttributedValue>
                        <Value>tsmith@contoso.com</Value>
                        <Attributions>
                           <Attribution>1</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </ImAddresses>
               </Persona>
               <Persona>
                  <PersonaId Id="AAQkAGQ1MjJjMTBkLkYQAQAJ3EkhEEXN5KufGbSYJanZk=" />
                  <PersonaType>Person</PersonaType>
                  <CreationTime>2012-01-05T23:06:58Z</CreationTime>
                  <DisplayName>Terence Adams</DisplayName>
                  <DisplayNameFirstLast>Terence Adams</DisplayNameFirstLast>
                  <DisplayNameLastFirst>Terence Adams</DisplayNameLastFirst>
                  <FileAsId>None</FileAsId>
                  <EmailAddress>
                     <Name>Terence Adams</Name>
                     <EmailAddress>tadams@contoso.com</EmailAddress>
                     <RoutingType>SMTP</RoutingType>
                  </EmailAddress>
                  <EmailAddresses>
                     <EmailAddress>
                        <Name>Terence Adams</Name>
                        <EmailAddress>tadams@contoso.com</EmailAddress>
                        <RoutingType>SMTP</RoutingType>
                     </EmailAddress>
                  </EmailAddresses>
                  <ImAddress>tadams@contoso.com</ImAddress>
                  <RelevanceScore>2147483647</RelevanceScore>
                  <Attributions>
                     <Attribution>
                        <Id>0</Id>
                        <SourceId Id="AAMkAGQ1MjVOQatt/bhQoTbWAAAA7iVOQatt/bhQoTbWAAAAAAvcAAA=" 
                                  ChangeKey="EQAAABYAAABtF8oI7iVOQatt/bhQoTbWAAAAAAyg" />
                        <DisplayName>Outlook</DisplayName>
                        <IsWritable>true</IsWritable>
                        <IsQuickContact>true</IsQuickContact>
                        <IsHidden>false</IsHidden>
                        <FolderId Id="AAMkAGQ1MjJjMTBkLTc4Y2rBtF8oI7iVOQatt/bhQoTbWAAAAAAvZAAA=" 
                                  ChangeKey="AQAAAA==" />
                     </Attribution>
                  </Attributions>
                  <DisplayNames>
                     <StringAttributedValue>
                        <Value>Terence Adams</Value>
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
                  <Emails1>
                     <EmailAddressAttributedValue>
                        <Value>
                           <Name>Terence Adams</Name>
                           <EmailAddress>tadams@contoso.com</EmailAddress>
                           <RoutingType>SMTP</RoutingType>
                        </Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </EmailAddressAttributedValue>
                  </Emails1>
                  <ImAddresses>
                     <StringAttributedValue>
                        <Value>tadams@contoso.com</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </ImAddresses>
               </Persona>
            </Personas>
         </ImItemList>
      </GetImItemListResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="17040-149">El cuerpo SOAP de respuesta contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="17040-149">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="17040-150">GetImItemListResponse</span><span class="sxs-lookup"><span data-stu-id="17040-150">GetImItemListResponse</span></span>](getimitemlistresponse.md)
    
- [<span data-ttu-id="17040-151">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="17040-151">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="17040-152">ImItemList</span><span class="sxs-lookup"><span data-stu-id="17040-152">ImItemList</span></span>](imitemlist.md)
    
- [<span data-ttu-id="17040-153">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="17040-153">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="17040-154">GroupType</span><span class="sxs-lookup"><span data-stu-id="17040-154">GroupType</span></span>](grouptype.md)
    
- [<span data-ttu-id="17040-155">ExchangeStoreId</span><span class="sxs-lookup"><span data-stu-id="17040-155">ExchangeStoreId</span></span>](exchangestoreid.md)
    
- [<span data-ttu-id="17040-156">MemberCorrelationKey</span><span class="sxs-lookup"><span data-stu-id="17040-156">MemberCorrelationKey</span></span>](membercorrelationkey.md)
    
- [<span data-ttu-id="17040-157">ItemId</span><span class="sxs-lookup"><span data-stu-id="17040-157">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="17040-158">Roles</span><span class="sxs-lookup"><span data-stu-id="17040-158">Personas</span></span>](personas-ex15websvcsotherref.md)
    
- [<span data-ttu-id="17040-159">PersonaId</span><span class="sxs-lookup"><span data-stu-id="17040-159">PersonaId</span></span>](personaid.md)
    
- [<span data-ttu-id="17040-160">PersonaType</span><span class="sxs-lookup"><span data-stu-id="17040-160">PersonaType</span></span>](personatype.md)
    
- [<span data-ttu-id="17040-161">CreationTime</span><span class="sxs-lookup"><span data-stu-id="17040-161">CreationTime</span></span>](creationtime.md)
    
- [<span data-ttu-id="17040-162">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="17040-162">DisplayNameFirstLast</span></span>](displaynamefirstlast.md)
    
- [<span data-ttu-id="17040-163">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="17040-163">DisplayNameLastFirst</span></span>](displaynamelastfirst.md)
    
- [<span data-ttu-id="17040-164">FileAs</span><span class="sxs-lookup"><span data-stu-id="17040-164">FileAs</span></span>](fileas.md)
    
- [<span data-ttu-id="17040-165">FileAsId</span><span class="sxs-lookup"><span data-stu-id="17040-165">FileAsId</span></span>](fileasid.md)
    
- [<span data-ttu-id="17040-166">GivenName</span><span class="sxs-lookup"><span data-stu-id="17040-166">GivenName</span></span>](givenname.md)
    
- [<span data-ttu-id="17040-167">Apellido</span><span class="sxs-lookup"><span data-stu-id="17040-167">Surname</span></span>](surname.md)
    
- [<span data-ttu-id="17040-168">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="17040-168">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="17040-169">Nombre (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="17040-169">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="17040-170">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="17040-170">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="17040-171">EmailAddresses (ArrayOfEmailAddressesType)</span><span class="sxs-lookup"><span data-stu-id="17040-171">EmailAddresses (ArrayOfEmailAddressesType)</span></span>](emailaddresses-arrayofemailaddressestype.md)
    
- [<span data-ttu-id="17040-172">IMAddress (cadena)</span><span class="sxs-lookup"><span data-stu-id="17040-172">ImAddress (String)</span></span>](imaddress-string.md)
    
- [<span data-ttu-id="17040-173">RelevanceScore</span><span class="sxs-lookup"><span data-stu-id="17040-173">RelevanceScore</span></span>](relevancescore.md)
    
- [<span data-ttu-id="17040-174">Atribuciones (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="17040-174">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md)
    
- [<span data-ttu-id="17040-175">Atribución (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="17040-175">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
    
- [<span data-ttu-id="17040-176">ID (cadena)</span><span class="sxs-lookup"><span data-stu-id="17040-176">ID (String)</span></span>](id-string.md)
    
- [<span data-ttu-id="17040-177">SourceId</span><span class="sxs-lookup"><span data-stu-id="17040-177">SourceId</span></span>](sourceid.md)
    
- [<span data-ttu-id="17040-178">IsWritable</span><span class="sxs-lookup"><span data-stu-id="17040-178">IsWritable</span></span>](iswritable.md)
    
- [<span data-ttu-id="17040-179">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="17040-179">IsQuickContact</span></span>](isquickcontact.md)
    
- [<span data-ttu-id="17040-180">IsHidden</span><span class="sxs-lookup"><span data-stu-id="17040-180">IsHidden</span></span>](ishidden.md)
    
- [<span data-ttu-id="17040-181">FolderId</span><span class="sxs-lookup"><span data-stu-id="17040-181">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="17040-182">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="17040-182">StringAttributedValue</span></span>](stringattributedvalue.md)
    
- [<span data-ttu-id="17040-183">FileAses</span><span class="sxs-lookup"><span data-stu-id="17040-183">FileAses</span></span>](fileases.md)
    
- [<span data-ttu-id="17040-184">FileAsIds</span><span class="sxs-lookup"><span data-stu-id="17040-184">FileAsIds</span></span>](fileasids.md)
    
- [<span data-ttu-id="17040-185">GivenNames</span><span class="sxs-lookup"><span data-stu-id="17040-185">GivenNames</span></span>](givennames.md)
    
- [<span data-ttu-id="17040-186">Apellidos</span><span class="sxs-lookup"><span data-stu-id="17040-186">Surnames</span></span>](surnames.md)
    
- [<span data-ttu-id="17040-187">HomePhones</span><span class="sxs-lookup"><span data-stu-id="17040-187">HomePhones</span></span>](homephones.md)
    
- [<span data-ttu-id="17040-188">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="17040-188">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md)
    
- [<span data-ttu-id="17040-189">MobilePhones</span><span class="sxs-lookup"><span data-stu-id="17040-189">MobilePhones</span></span>](mobilephones.md)
    
- [<span data-ttu-id="17040-190">Emails1</span><span class="sxs-lookup"><span data-stu-id="17040-190">Emails1</span></span>](emails1.md)
    
- [<span data-ttu-id="17040-191">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="17040-191">EmailAddressAttributedValue</span></span>](emailaddressattributedvalue.md)
    
- [<span data-ttu-id="17040-192">Indirecciones</span><span class="sxs-lookup"><span data-stu-id="17040-192">ImAddresses</span></span>](imaddresses.md)
    
- [<span data-ttu-id="17040-193">Valor (ExtendedPropertyType)</span><span class="sxs-lookup"><span data-stu-id="17040-193">Value (ExtendedPropertyType)</span></span>](value-extendedpropertytype.md)
    
## <a name="getimitemlist-operation-error-response"></a><span data-ttu-id="17040-194">Respuesta de error de operación de GetImItemList</span><span class="sxs-lookup"><span data-stu-id="17040-194">GetImItemList operation error response</span></span>

<span data-ttu-id="17040-195">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **GetImItemList** .</span><span class="sxs-lookup"><span data-stu-id="17040-195">The following example shows an error response to a **GetImItemList** operation request.</span></span> <span data-ttu-id="17040-196">Se trata de una respuesta a una solicitud que contiene una versión de servidor solicitada incorrecta en el encabezado SOAP.</span><span class="sxs-lookup"><span data-stu-id="17040-196">This is a response to a request that contains an incorrect requested server version in the SOAP header.</span></span> <span data-ttu-id="17040-197">Esta respuesta de error es un error de SOAP y no se representa en el esquema EWS.</span><span class="sxs-lookup"><span data-stu-id="17040-197">This error response is a SOAP fault and is not represented in the EWS schema.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Body>
      <s:Fault>
         <faultcode xmlns:a="https://schemas.microsoft.com/exchange/services/2006/types">a:ErrorIncorrectSchemaVersion</faultcode>
         <faultstring xml:lang="en-US">The request is valid but does not specify the correct server version in the RequestServerVersion SOAP header.  Ensure that the RequestServerVersion SOAP header is set with the correct RequestServerVersionValue.</faultstring>
         <detail>
            <e:ResponseCode xmlns:e="https://schemas.microsoft.com/exchange/services/2006/errors">ErrorIncorrectSchemaVersion</e:ResponseCode>
            <e:Message xmlns:e="https://schemas.microsoft.com/exchange/services/2006/errors">The request is valid but does not specify the correct server version in the RequestServerVersion SOAP header.  Ensure that the RequestServerVersion SOAP header is set with the correct RequestServerVersionValue.</e:Message>
         </detail>
      </s:Fault>
   </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="17040-198">Vea también</span><span class="sxs-lookup"><span data-stu-id="17040-198">See also</span></span>

- [<span data-ttu-id="17040-199">Operación AddImGroup</span><span class="sxs-lookup"><span data-stu-id="17040-199">AddImGroup operation</span></span>](addimgroup-operation.md)
    
- [<span data-ttu-id="17040-200">Personas y contactos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="17040-200">People and contacts in EWS in Exchange</span></span>](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [<span data-ttu-id="17040-201">Operación GetImItems</span><span class="sxs-lookup"><span data-stu-id="17040-201">GetImItems operation</span></span>](getimitems-operation.md)
    

