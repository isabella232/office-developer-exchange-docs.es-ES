---
title: Operación GetImItemList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e31d14e1-0c1f-4b69-98b7-157d59c13698
description: Busque información sobre la EWS GetImItemList operación.
ms.openlocfilehash: 3977b0ad31e819cd973ce261ba3152b3840003b3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764874"
---
# <a name="getimitemlist-operation"></a><span data-ttu-id="d8da7-103">Operación GetImItemList</span><span class="sxs-lookup"><span data-stu-id="d8da7-103">GetImItemList operation</span></span>

<span data-ttu-id="d8da7-104">Obtenga información acerca de la operación de EWS **GetImItemList** .</span><span class="sxs-lookup"><span data-stu-id="d8da7-104">Find information about the **GetImItemList** EWS operation.</span></span> 
  
## <a name="using-the-getimitemlist-operation"></a><span data-ttu-id="d8da7-105">Mediante la operación GetImItemList</span><span class="sxs-lookup"><span data-stu-id="d8da7-105">Using the GetImItemList operation</span></span>

<span data-ttu-id="d8da7-106">La operación **GetImItemList** recupera la lista de grupos de mensajería instantánea y mensajería instantánea, póngase en contacto con los roles en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="d8da7-106">The **GetImItemList** operation retrieves the list of instant messaging (IM) groups and IM contact personas in a mailbox.</span></span> <span data-ttu-id="d8da7-107">La operación **GetImItemList** no toma ningún argumento.</span><span class="sxs-lookup"><span data-stu-id="d8da7-107">The **GetImItemList** operation does not take any arguments.</span></span> 
  
<span data-ttu-id="d8da7-108">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d8da7-108">This operation was introduced in Exchange Server 2013.</span></span>
  
### <a name="getimitemlist-operation-soap-headers"></a><span data-ttu-id="d8da7-109">Encabezados SOAP de operación de GetImItemList</span><span class="sxs-lookup"><span data-stu-id="d8da7-109">GetImItemList operation SOAP headers</span></span>

<span data-ttu-id="d8da7-110">La operación de **GetImItemList** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="d8da7-110">The **GetImItemList** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="d8da7-111">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="d8da7-111">**Header name**</span></span>|<span data-ttu-id="d8da7-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="d8da7-112">**Element**</span></span>|<span data-ttu-id="d8da7-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d8da7-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d8da7-114">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="d8da7-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="d8da7-115">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="d8da7-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="d8da7-116">Identifica el usuario que está realizando la suplantación de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="d8da7-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="d8da7-117">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="d8da7-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d8da7-118">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="d8da7-118">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="d8da7-119">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="d8da7-119">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="d8da7-120">Identifica la referencia cultural, como se define en RFC 3066, "Etiquetas para la identificación de idiomas," que se utilizará para acceder al buzón.</span><span class="sxs-lookup"><span data-stu-id="d8da7-120">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="d8da7-121">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="d8da7-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d8da7-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="d8da7-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="d8da7-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="d8da7-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="d8da7-124">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="d8da7-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="d8da7-125">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="d8da7-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d8da7-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="d8da7-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="d8da7-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d8da7-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="d8da7-128">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d8da7-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="d8da7-129">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="d8da7-129">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getimitemlist-operation-request-example-request-your-im-items-list"></a><span data-ttu-id="d8da7-130">Ejemplo de solicitud de operación de GetImItemList: solicitud de su lista de elementos de mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="d8da7-130">GetImItemList operation request example: Request your IM items list</span></span>

<span data-ttu-id="d8da7-131">El siguiente ejemplo de una solicitud de operación **GetImItemList** muestra cómo solicitar la lista de grupos de mensajería instantánea y mensajería instantánea, póngase en contacto con los roles en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="d8da7-131">The following example of a **GetImItemList** operation request shows how to request the list of IM groups and IM contact personas in a mailbox.</span></span> <span data-ttu-id="d8da7-132">El elemento **GetImItemList** es la opción de elemento sólo en el cuerpo SOAP.</span><span class="sxs-lookup"><span data-stu-id="d8da7-132">The **GetImItemList** element is the only element option in the SOAP body.</span></span> 
  
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
      <m:GetImItemList/>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="d8da7-133">La solicitud SOAP body contiene el elemento siguiente:</span><span class="sxs-lookup"><span data-stu-id="d8da7-133">The request SOAP body contains the following element:</span></span>
  
- [<span data-ttu-id="d8da7-134">GetImItemList</span><span class="sxs-lookup"><span data-stu-id="d8da7-134">GetImItemList</span></span>](getimitemlist.md)
    
## <a name="successful-getimitemlist-operation-response"></a><span data-ttu-id="d8da7-135">Respuesta es correcta de operación GetImItemList</span><span class="sxs-lookup"><span data-stu-id="d8da7-135">Successful GetImItemList operation response</span></span>

<span data-ttu-id="d8da7-136">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **GetImItemList** .</span><span class="sxs-lookup"><span data-stu-id="d8da7-136">The following example shows a successful response to a **GetImItemList** operation request.</span></span> <span data-ttu-id="d8da7-137">La respuesta contiene cuatro grupos de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="d8da7-137">The response contains four IM groups.</span></span> <span data-ttu-id="d8da7-138">Tres de los grupos de mensajería instantánea: otros contactos, etiquetados y favoritos — son grupos de forma predeterminada en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d8da7-138">Three of the IM groups — Other Contacts, Tagged, and Favorites — are default groups in the Exchange store.</span></span> <span data-ttu-id="d8da7-139">El grupo de MyCustomGroup2 es un grupo personalizado creado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="d8da7-139">The MyCustomGroup2 group is a custom user-created group.</span></span> <span data-ttu-id="d8da7-140">Los grupos de otros contactos y etiquetados no tienen miembros.</span><span class="sxs-lookup"><span data-stu-id="d8da7-140">The Other Contacts and Tagged groups do not have members.</span></span> <span data-ttu-id="d8da7-141">El grupo de favoritos tiene un solo miembro de contacto.</span><span class="sxs-lookup"><span data-stu-id="d8da7-141">The Favorites group has a single contact member.</span></span> <span data-ttu-id="d8da7-142">El MyCustomGroup2 tiene dos contactos de miembro.</span><span class="sxs-lookup"><span data-stu-id="d8da7-142">The MyCustomGroup2 has two member contacts.</span></span> <span data-ttu-id="d8da7-143">Los identificadores de elemento se proporcionan para que se pueden realizar las solicitudes posteriores **GetItem** para obtener más información acerca de los contactos de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="d8da7-143">The item identifiers are provided so that subsequent **GetItem** requests can be performed to get more information about the IM contacts.</span></span> 
  
<span data-ttu-id="d8da7-144">En este ejemplo se devuelven dos roles.</span><span class="sxs-lookup"><span data-stu-id="d8da7-144">This example returns two personas.</span></span> <span data-ttu-id="d8da7-145">El primer rol representa dos elementos de contacto: Anthony Smith y Tony Smith.</span><span class="sxs-lookup"><span data-stu-id="d8da7-145">The first persona represents two contact items: Anthony Smith and Tony Smith.</span></span> <span data-ttu-id="d8da7-146">Se devuelve la información de contacto combinada en el objeto de **rol** .</span><span class="sxs-lookup"><span data-stu-id="d8da7-146">The combined contact information is returned in the **Persona** object.</span></span> <span data-ttu-id="d8da7-147">El segundo rol representa un solo contacto con el nombre para mostrar de Terence Adams.</span><span class="sxs-lookup"><span data-stu-id="d8da7-147">The second persona represents a single contact with the display name of Terence Adams.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d8da7-148">Los identificadores del almacén de Exchange, los identificadores de elemento, identificadores de origen, identificadores de carpeta e identificadores de rol se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="d8da7-148">The Exchange store identifiers, item identifiers, source identifiers, folder identifiers, and persona identifiers have been shortened to preserve readability.</span></span> 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="349" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" />
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetImItemListResponse ResponseClass="Success" 
                             xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <ImItemList>
            <Groups xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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
            <Personas xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="d8da7-149">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="d8da7-149">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d8da7-150">GetImItemListResponse</span><span class="sxs-lookup"><span data-stu-id="d8da7-150">GetImItemListResponse</span></span>](getimitemlistresponse.md)
    
- [<span data-ttu-id="d8da7-151">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d8da7-151">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d8da7-152">ImItemList</span><span class="sxs-lookup"><span data-stu-id="d8da7-152">ImItemList</span></span>](imitemlist.md)
    
- [<span data-ttu-id="d8da7-153">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="d8da7-153">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="d8da7-154">GroupType</span><span class="sxs-lookup"><span data-stu-id="d8da7-154">GroupType</span></span>](grouptype.md)
    
- [<span data-ttu-id="d8da7-155">ExchangeStoreId</span><span class="sxs-lookup"><span data-stu-id="d8da7-155">ExchangeStoreId</span></span>](exchangestoreid.md)
    
- [<span data-ttu-id="d8da7-156">MemberCorrelationKey</span><span class="sxs-lookup"><span data-stu-id="d8da7-156">MemberCorrelationKey</span></span>](membercorrelationkey.md)
    
- [<span data-ttu-id="d8da7-157">ItemId</span><span class="sxs-lookup"><span data-stu-id="d8da7-157">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="d8da7-158">Roles</span><span class="sxs-lookup"><span data-stu-id="d8da7-158">Personas</span></span>](personas-ex15websvcsotherref.md)
    
- [<span data-ttu-id="d8da7-159">PersonaId</span><span class="sxs-lookup"><span data-stu-id="d8da7-159">PersonaId</span></span>](personaid.md)
    
- [<span data-ttu-id="d8da7-160">PersonaType</span><span class="sxs-lookup"><span data-stu-id="d8da7-160">PersonaType</span></span>](personatype.md)
    
- [<span data-ttu-id="d8da7-161">CreationTime</span><span class="sxs-lookup"><span data-stu-id="d8da7-161">CreationTime</span></span>](creationtime.md)
    
- [<span data-ttu-id="d8da7-162">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="d8da7-162">DisplayNameFirstLast</span></span>](displaynamefirstlast.md)
    
- [<span data-ttu-id="d8da7-163">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="d8da7-163">DisplayNameLastFirst</span></span>](displaynamelastfirst.md)
    
- [<span data-ttu-id="d8da7-164">Archivar como</span><span class="sxs-lookup"><span data-stu-id="d8da7-164">FileAs</span></span>](fileas.md)
    
- [<span data-ttu-id="d8da7-165">FileAsId</span><span class="sxs-lookup"><span data-stu-id="d8da7-165">FileAsId</span></span>](fileasid.md)
    
- [<span data-ttu-id="d8da7-166">GivenName</span><span class="sxs-lookup"><span data-stu-id="d8da7-166">GivenName</span></span>](givenname.md)
    
- [<span data-ttu-id="d8da7-167">Apellido</span><span class="sxs-lookup"><span data-stu-id="d8da7-167">Surname</span></span>](surname.md)
    
- [<span data-ttu-id="d8da7-168">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="d8da7-168">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="d8da7-169">Nombre (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="d8da7-169">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="d8da7-170">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="d8da7-170">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="d8da7-171">EmailAddresses (ArrayOfEmailAddressesType)</span><span class="sxs-lookup"><span data-stu-id="d8da7-171">EmailAddresses (ArrayOfEmailAddressesType)</span></span>](emailaddresses-arrayofemailaddressestype.md)
    
- [<span data-ttu-id="d8da7-172">ImAddress (cadena)</span><span class="sxs-lookup"><span data-stu-id="d8da7-172">ImAddress (String)</span></span>](imaddress-string.md)
    
- [<span data-ttu-id="d8da7-173">RelevanceScore</span><span class="sxs-lookup"><span data-stu-id="d8da7-173">RelevanceScore</span></span>](relevancescore.md)
    
- [<span data-ttu-id="d8da7-174">Atribuciones (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="d8da7-174">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md)
    
- [<span data-ttu-id="d8da7-175">Atribución (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="d8da7-175">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
    
- [<span data-ttu-id="d8da7-176">Identificador (cadena)</span><span class="sxs-lookup"><span data-stu-id="d8da7-176">ID (String)</span></span>](id-string.md)
    
- [<span data-ttu-id="d8da7-177">SourceId</span><span class="sxs-lookup"><span data-stu-id="d8da7-177">SourceId</span></span>](sourceid.md)
    
- [<span data-ttu-id="d8da7-178">IsWritable</span><span class="sxs-lookup"><span data-stu-id="d8da7-178">IsWritable</span></span>](iswritable.md)
    
- [<span data-ttu-id="d8da7-179">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="d8da7-179">IsQuickContact</span></span>](isquickcontact.md)
    
- [<span data-ttu-id="d8da7-180">IsHidden</span><span class="sxs-lookup"><span data-stu-id="d8da7-180">IsHidden</span></span>](ishidden.md)
    
- [<span data-ttu-id="d8da7-181">FolderId</span><span class="sxs-lookup"><span data-stu-id="d8da7-181">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="d8da7-182">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="d8da7-182">StringAttributedValue</span></span>](stringattributedvalue.md)
    
- [<span data-ttu-id="d8da7-183">FileAses</span><span class="sxs-lookup"><span data-stu-id="d8da7-183">FileAses</span></span>](fileases.md)
    
- [<span data-ttu-id="d8da7-184">FileAsIds</span><span class="sxs-lookup"><span data-stu-id="d8da7-184">FileAsIds</span></span>](fileasids.md)
    
- [<span data-ttu-id="d8da7-185">GivenNames</span><span class="sxs-lookup"><span data-stu-id="d8da7-185">GivenNames</span></span>](givennames.md)
    
- [<span data-ttu-id="d8da7-186">Apellidos</span><span class="sxs-lookup"><span data-stu-id="d8da7-186">Surnames</span></span>](surnames.md)
    
- [<span data-ttu-id="d8da7-187">HomePhones</span><span class="sxs-lookup"><span data-stu-id="d8da7-187">HomePhones</span></span>](homephones.md)
    
- [<span data-ttu-id="d8da7-188">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="d8da7-188">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md)
    
- [<span data-ttu-id="d8da7-189">MobilePhones</span><span class="sxs-lookup"><span data-stu-id="d8da7-189">MobilePhones</span></span>](mobilephones.md)
    
- [<span data-ttu-id="d8da7-190">Emails1</span><span class="sxs-lookup"><span data-stu-id="d8da7-190">Emails1</span></span>](emails1.md)
    
- [<span data-ttu-id="d8da7-191">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="d8da7-191">EmailAddressAttributedValue</span></span>](emailaddressattributedvalue.md)
    
- [<span data-ttu-id="d8da7-192">ImAddresses</span><span class="sxs-lookup"><span data-stu-id="d8da7-192">ImAddresses</span></span>](imaddresses.md)
    
- [<span data-ttu-id="d8da7-193">Valor (ExtendedPropertyType)</span><span class="sxs-lookup"><span data-stu-id="d8da7-193">Value (ExtendedPropertyType)</span></span>](value-extendedpropertytype.md)
    
## <a name="getimitemlist-operation-error-response"></a><span data-ttu-id="d8da7-194">Respuesta de error de la operación de GetImItemList</span><span class="sxs-lookup"><span data-stu-id="d8da7-194">GetImItemList operation error response</span></span>

<span data-ttu-id="d8da7-195">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **GetImItemList** .</span><span class="sxs-lookup"><span data-stu-id="d8da7-195">The following example shows an error response to a **GetImItemList** operation request.</span></span> <span data-ttu-id="d8da7-196">Esta es una respuesta a una solicitud que contiene una versión incorrecta del servidor solicitado en el encabezado SOAP.</span><span class="sxs-lookup"><span data-stu-id="d8da7-196">This is a response to a request that contains an incorrect requested server version in the SOAP header.</span></span> <span data-ttu-id="d8da7-197">Este error es un error de SOAP y respuesta no está representada en el esquema EWS.</span><span class="sxs-lookup"><span data-stu-id="d8da7-197">This error response is a SOAP fault and is not represented in the EWS schema.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Body>
      <s:Fault>
         <faultcode xmlns:a="http://schemas.microsoft.com/exchange/services/2006/types">a:ErrorIncorrectSchemaVersion</faultcode>
         <faultstring xml:lang="en-US">The request is valid but does not specify the correct server version in the RequestServerVersion SOAP header.  Ensure that the RequestServerVersion SOAP header is set with the correct RequestServerVersionValue.</faultstring>
         <detail>
            <e:ResponseCode xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">ErrorIncorrectSchemaVersion</e:ResponseCode>
            <e:Message xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">The request is valid but does not specify the correct server version in the RequestServerVersion SOAP header.  Ensure that the RequestServerVersion SOAP header is set with the correct RequestServerVersionValue.</e:Message>
         </detail>
      </s:Fault>
   </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="d8da7-198">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8da7-198">See also</span></span>

- [<span data-ttu-id="d8da7-199">Operación AddImGroup</span><span class="sxs-lookup"><span data-stu-id="d8da7-199">AddImGroup operation</span></span>](addimgroup-operation.md)
    
- [<span data-ttu-id="d8da7-200">Las personas y los contactos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d8da7-200">People and contacts in EWS in Exchange</span></span>](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [<span data-ttu-id="d8da7-201">Operación GetImItems</span><span class="sxs-lookup"><span data-stu-id="d8da7-201">GetImItems operation</span></span>](getimitems-operation.md)
    

