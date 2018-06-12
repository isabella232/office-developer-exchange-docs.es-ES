---
title: Operación ConvertId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConvertId
api_type:
- schema
ms.assetid: 47d96cf6-9e2f-4fc0-9682-7258d3fbf918
description: Busque información sobre la EWS ConvertId operación.
ms.openlocfilehash: 5f1bcd8a9f0adc25b7c598ef10cc6bb139dfe02d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763884"
---
# <a name="convertid-operation"></a><span data-ttu-id="fa92b-103">Operación ConvertId</span><span class="sxs-lookup"><span data-stu-id="fa92b-103">ConvertId operation</span></span>

<span data-ttu-id="fa92b-104">Obtenga información acerca de la operación de EWS **ConvertId** .</span><span class="sxs-lookup"><span data-stu-id="fa92b-104">Find information about the **ConvertId** EWS operation.</span></span> 
  
<span data-ttu-id="fa92b-105">La operación de Exchange Web Services (EWS) **ConvertId** convierte los identificadores de elemento y carpeta entre formatos que se aceptan por Exchange Online, Exchange Online como parte de Office 365, locales y en las versiones de Exchange a partir de Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="fa92b-105">The **ConvertId** Exchange Web Services (EWS) operation converts item and folder identifiers between formats that are accepted by Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with Exchange Server 2013.</span></span> 
  
## <a name="using-the-convertid-operation"></a><span data-ttu-id="fa92b-106">Mediante la operación ConvertId</span><span class="sxs-lookup"><span data-stu-id="fa92b-106">Using the ConvertId operation</span></span>
<span data-ttu-id="fa92b-107"><a name="bk_usingConvertId"> </a></span><span class="sxs-lookup"><span data-stu-id="fa92b-107"></span></span>

<span data-ttu-id="fa92b-108">Puede convertir los siguientes identificadores mediante el uso de la operación de **ConvertId** :</span><span class="sxs-lookup"><span data-stu-id="fa92b-108">You can convert the following identifiers by using the **ConvertId** operation:</span></span> 
  
- <span data-ttu-id="fa92b-109">El formato de identificador para EWS en la versión inicial de Exchange 2007.</span><span class="sxs-lookup"><span data-stu-id="fa92b-109">The identifier format for EWS in the initial release version of Exchange 2007.</span></span> <span data-ttu-id="fa92b-110">Esto está representado por el `EwsLegacyId` valor de la enumeración en la enumeración [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="fa92b-110">This is represented by the  `EwsLegacyId` enumeration value in the [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) enumeration.</span></span> 
    
- <span data-ttu-id="fa92b-111">El formato de identificador para EWS en Exchange 2007 SP1 o Exchange 2010.</span><span class="sxs-lookup"><span data-stu-id="fa92b-111">The identifier format for EWS in Exchange 2007 SP1 or Exchange 2010.</span></span> <span data-ttu-id="fa92b-112">Esto está representado por el `EwsId` valor de la enumeración en [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="fa92b-112">This is represented by the  `EwsId` enumeration value in [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).</span></span>
    
- <span data-ttu-id="fa92b-113">El identificador MAPI, como se muestra en la propiedad de **entrada del objeto** .</span><span class="sxs-lookup"><span data-stu-id="fa92b-113">The MAPI identifier, as in the **PR_ENTRYID** property.</span></span> <span data-ttu-id="fa92b-114">Esto está representado por el `EntryId` valor de la enumeración en la enumeración [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="fa92b-114">This is represented by the  `EntryId` enumeration value in the [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) enumeration.</span></span> 
    
- <span data-ttu-id="fa92b-115">El identificador de evento del calendario de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="fa92b-115">The availability calendar event identifier.</span></span> <span data-ttu-id="fa92b-116">Ésta es una representación codificada en hexadecimal de la propiedad de **entrada del objeto** .</span><span class="sxs-lookup"><span data-stu-id="fa92b-116">This is a hexadecimal-encoded representation of the **PR_ENTRYID** property.</span></span> <span data-ttu-id="fa92b-117">Esto está representado por el `HexEntryId` valor de la enumeración en [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="fa92b-117">This is represented by the  `HexEntryId` enumeration value in [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).</span></span>
    
- <span data-ttu-id="fa92b-118">El identificador de almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="fa92b-118">The Exchange store identifier.</span></span> <span data-ttu-id="fa92b-119">Esto está representado por el `StoreId` valor de la enumeración en [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="fa92b-119">This is represented by the  `StoreId` enumeration value in [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="fa92b-120">La operación **ConvertId** no convierte el identificador de almacén de identificadores de carpetas públicas desde el identificador de EWS.</span><span class="sxs-lookup"><span data-stu-id="fa92b-120">The **ConvertId** operation does not convert public folder identifiers from the EWS identifier to the store identifier.</span></span> 
    
- <span data-ttu-id="fa92b-121">El identificador de Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="fa92b-121">The Outlook Web App identifier.</span></span> <span data-ttu-id="fa92b-122">Esto está representado por el `OwaId` valor de la enumeración en [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fa92b-122">This is represented by the  `OwaId` enumeration value in [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)</span></span>
    
    <span data-ttu-id="fa92b-123">No se admite el paso de las direcciones URL que se crean desde este identificador a Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="fa92b-123">The passing of URLs that are created from this identifier to Outlook Web App is not supported.</span></span> <span data-ttu-id="fa92b-124">El identificador de Outlook Web App es aplicable a Exchange 2007 y Exchange 2010.</span><span class="sxs-lookup"><span data-stu-id="fa92b-124">The Outlook Web App identifier is applicable to Exchange 2007 and Exchange 2010.</span></span> <span data-ttu-id="fa92b-125">Outlook Web App para Exchange Online y versiones de Exchange a partir de Exchange Server 2013 usa identificadores EWS.</span><span class="sxs-lookup"><span data-stu-id="fa92b-125">Outlook Web App for Exchange Online and versions of Exchange starting with Exchange Server 2013 uses EWS identifiers.</span></span>
    
<span data-ttu-id="fa92b-126">La operación **ConvertId** no funciona según lo esperado cuando se convierte los identificadores de carpetas públicas desde el identificador de EWS al identificador del almacén de Exchange Online y Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="fa92b-126">The **ConvertId** operation does not work as expected when converting public folder identifiers from the EWS identifier to the store identifier in Exchange Online and Exchange 2013.</span></span> <span data-ttu-id="fa92b-127">Puede actualizar manualmente el identificador que se devuelve como una solución alternativa.</span><span class="sxs-lookup"><span data-stu-id="fa92b-127">You can manually update the identifier that is returned as a workaround.</span></span> <span data-ttu-id="fa92b-128">Para actualizar manualmente el identificador:</span><span class="sxs-lookup"><span data-stu-id="fa92b-128">To manually update the identifier:</span></span> 
  
1. <span data-ttu-id="fa92b-129">En el código de la aplicación, determine si el elemento o la carpeta de destino está en una carpeta pública.</span><span class="sxs-lookup"><span data-stu-id="fa92b-129">In your application code, determine whether the target item/folder is in a public folder.</span></span> 
    
2. <span data-ttu-id="fa92b-130">Descodificar la cadena de identificador con codificación Base64.</span><span class="sxs-lookup"><span data-stu-id="fa92b-130">Decode the Base64-encoded identifier string.</span></span>
    
3. <span data-ttu-id="fa92b-131">Compruebe que el tipo byte (byte 21) tiene un valor de 7.</span><span class="sxs-lookup"><span data-stu-id="fa92b-131">Verify that the type byte (21st byte) has a value of 7.</span></span> <span data-ttu-id="fa92b-132">Un valor de 7 indica que el identificador está en el formato incorrecto.</span><span class="sxs-lookup"><span data-stu-id="fa92b-132">A value of 7 indicates that the identifier is in the incorrect format.</span></span>
    
4. <span data-ttu-id="fa92b-133">Omitir los primeros cuatro bytes.</span><span class="sxs-lookup"><span data-stu-id="fa92b-133">Skip the first four bytes.</span></span> <span data-ttu-id="fa92b-134">Debe establecer en cero.</span><span class="sxs-lookup"><span data-stu-id="fa92b-134">They must be set to zero.</span></span>
    
5. <span data-ttu-id="fa92b-135">Actualizar los siguientes 16 bytes con el siguiente GUID: 1A447390AA6611CD9BC800AA002FC45A</span><span class="sxs-lookup"><span data-stu-id="fa92b-135">Update the next 16 bytes with the following GUID: 1A447390AA6611CD9BC800AA002FC45A</span></span>
    
6. <span data-ttu-id="fa92b-136">Actualizar el siguiente byte (de tipo byte) con un valor de 9.</span><span class="sxs-lookup"><span data-stu-id="fa92b-136">Update the next byte (type byte) with a value of 9.</span></span>
    
7. <span data-ttu-id="fa92b-137">Cambie el identificador a una cadena con codificación Base64.</span><span class="sxs-lookup"><span data-stu-id="fa92b-137">Change the identifier to a Base64-encoded string.</span></span>
    
> [!NOTE]
> <span data-ttu-id="fa92b-138">La operación de **ConvertId** valida que una dirección SMTP concreta tiene un formato válido.</span><span class="sxs-lookup"><span data-stu-id="fa92b-138">The **ConvertId** operation validates that a given SMTP address has a valid format.</span></span> <span data-ttu-id="fa92b-139">La operación no determina si una dirección SMTP representa un buzón válido.</span><span class="sxs-lookup"><span data-stu-id="fa92b-139">The operation does not determine whether an SMTP address represents a valid mailbox.</span></span> 
  
<span data-ttu-id="fa92b-140">La operación de **ConvertId** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="fa92b-140">The **ConvertId** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
<span data-ttu-id="fa92b-141">**La tabla 1. Encabezados SOAP de operación de ConvertId**</span><span class="sxs-lookup"><span data-stu-id="fa92b-141">**Table 1. ConvertId operation SOAP headers**</span></span>

|<span data-ttu-id="fa92b-142">**Header**</span><span class="sxs-lookup"><span data-stu-id="fa92b-142">**Header**</span></span>|<span data-ttu-id="fa92b-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="fa92b-143">**Element**</span></span>|<span data-ttu-id="fa92b-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fa92b-144">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fa92b-145">Suplantación</span><span class="sxs-lookup"><span data-stu-id="fa92b-145">Impersonation</span></span>  <br/> |[<span data-ttu-id="fa92b-146">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="fa92b-146">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="fa92b-147">Identifica el usuario que está realizando la suplantación de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="fa92b-147">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="fa92b-148">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="fa92b-148">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="fa92b-149">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="fa92b-149">RequestVersion</span></span>  <br/> |[<span data-ttu-id="fa92b-150">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="fa92b-150">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="fa92b-151">Identifica la versión del esquema para la solicitud de la operación es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="fa92b-151">Identifies the schema version for the operation request This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="fa92b-152">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="fa92b-152">ServerVersion</span></span>  <br/> |[<span data-ttu-id="fa92b-153">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="fa92b-153">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="fa92b-154">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fa92b-154">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="fa92b-155">Esto es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="fa92b-155">This is applicable to a response.</span></span>  <br/> |
   
## <a name="convertid-operation-request-example"></a><span data-ttu-id="fa92b-156">Ejemplo de solicitud de operación de ConvertId</span><span class="sxs-lookup"><span data-stu-id="fa92b-156">ConvertId operation request example</span></span>
<span data-ttu-id="fa92b-157"><a name="bk_usingConvertId"> </a></span><span class="sxs-lookup"><span data-stu-id="fa92b-157"></span></span>

<span data-ttu-id="fa92b-158">El siguiente ejemplo de una solicitud de **ConvertId** muestra cómo convertir un identificador EWS de a un identificador de Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="fa92b-158">The following example of a **ConvertId** request shows how to convert from an EWS identifier to an Outlook Web App identifier.</span></span> 
  
<span data-ttu-id="fa92b-159">El elemento [RequestServerVersion](requestserverversion.md) en el encabezado SOAP debe establecerse en Exchange2007_SP1 o posterior para realizar esta operación para que funcione.</span><span class="sxs-lookup"><span data-stu-id="fa92b-159">The [RequestServerVersion](requestserverversion.md) element in the SOAP header must be set to Exchange2007_SP1 or later for this operation to work.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="fa92b-160">El identificador del elemento se ha acortado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="fa92b-160">The item identifier has been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <ConvertId xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               DestinationFormat="OwaId">
      <SourceIds>
        <t:AlternateId Format="EwsId" Id="AAMkAGZhN2IxYTA0LWNiNzItN="
                       Mailbox="user1@example.com"/>
      </SourceIds>
    </ConvertId>
  </soap:Body>
</soap:Envelope>
```

## <a name="convertid-operation-response-example"></a><span data-ttu-id="fa92b-161">Ejemplo de respuesta la operación ConvertId</span><span class="sxs-lookup"><span data-stu-id="fa92b-161">ConvertId operation response example</span></span>
<span data-ttu-id="fa92b-162"><a name="bk_usingConvertId"> </a></span><span class="sxs-lookup"><span data-stu-id="fa92b-162"></span></span>

<span data-ttu-id="fa92b-163">En el ejemplo siguiente se muestra una respuesta a una solicitud **ConvertId** correcta.</span><span class="sxs-lookup"><span data-stu-id="fa92b-163">The following example shows a successful response to a **ConvertId** request.</span></span> <span data-ttu-id="fa92b-164">En este ejemplo de respuesta contiene un identificador de Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="fa92b-164">This response example contains an Outlook Web App identifier.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="fa92b-165">Se ha reducido el identificador de Outlook Web App para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="fa92b-165">The Outlook Web App identifier has been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="1" 
                         MajorBuildNumber="191" MinorBuildNumber="0" 
                         Version="Exchange2010" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ConvertIdResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessages>
        <ConvertIdResponseMessage ResponseClass="Success">
          <ResponseCode>NoError</ResponseCode>
          <AlternateId xsi:type="t:AlternateIdType" Format="OwaId" Id="RgAAAAAS2%2" 
                         Mailbox="user@example.com" />
        </ConvertIdResponseMessage>
      </ResponseMessages>
    </ConvertIdResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="convertid-operation-error-response-example"></a><span data-ttu-id="fa92b-166">Ejemplo de respuesta de error de operación de ConvertId</span><span class="sxs-lookup"><span data-stu-id="fa92b-166">ConvertId operation error response example</span></span>
<span data-ttu-id="fa92b-167"><a name="bk_usingConvertId"> </a></span><span class="sxs-lookup"><span data-stu-id="fa92b-167"></span></span>

<span data-ttu-id="fa92b-168">En el ejemplo siguiente se muestra la respuesta a una solicitud que contiene el tipo de formato de identificador incorrecto.</span><span class="sxs-lookup"><span data-stu-id="fa92b-168">The following example shows the response to a request that contains the wrong type of identifier format.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <ServerVersionInfo MajorVersion="8" MinorVersion="1" 
                       MajorBuildNumber="206" MinorBuildNumber="0"
                       Version="Exchange2010" 
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ConvertIdResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessages>
        <ConvertIdResponseMessage ResponseClass="Error">
          <MessageText>Id is malformed.</MessageText>
          <ResponseCode>ErrorInvalidIdMalformed</ResponseCode>
          <DescriptiveLinkKey>0</DescriptiveLinkKey>
        </ConvertIdResponseMessage>
      </ResponseMessages>
    </ConvertIdResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="version-differences"></a><span data-ttu-id="fa92b-169">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="fa92b-169">Version differences</span></span>
<span data-ttu-id="fa92b-170"><a name="bk_ConvertIdVersionDiff"> </a></span><span class="sxs-lookup"><span data-stu-id="fa92b-170"></span></span>

<span data-ttu-id="fa92b-171">El formato de identificador de EWS han cambiado entre la versión de lanzamiento inicial de Exchange 2007 y Exchange 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="fa92b-171">The EWS identifier format changed between the initial release version of Exchange 2007 and Exchange 2007 Service Pack 1 (SP1).</span></span> <span data-ttu-id="fa92b-172">Exchange Online como parte de Office 365, Exchange Online y versiones locales de Exchange a partir de Exchange 2010 usan el mismo formato de identificador que usa Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="fa92b-172">Exchange Online as part of Office 365, Exchange Online, and on-premises versions of Exchange starting with Exchange 2010 use the same identifier format that Exchange 2007 SP1 uses.</span></span>
  
<span data-ttu-id="fa92b-173">La operación **ConvertId** convierte los identificadores de carpetas públicas desde el identificador de EWS al identificador del almacén de Exchange 2007 y Exchange 2010.</span><span class="sxs-lookup"><span data-stu-id="fa92b-173">The **ConvertId** operation converts public folder identifiers from the EWS identifier to the store identifier in Exchange 2007 and Exchange 2010.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fa92b-174">Ver también</span><span class="sxs-lookup"><span data-stu-id="fa92b-174">See also</span></span>
<span data-ttu-id="fa92b-175"><a name="bk_ConvertIdVersionDiff"> </a></span><span class="sxs-lookup"><span data-stu-id="fa92b-175"></span></span>

- [<span data-ttu-id="fa92b-176">Convertir identificadores</span><span class="sxs-lookup"><span data-stu-id="fa92b-176">Converting Identifiers</span></span>](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)
    
- [<span data-ttu-id="fa92b-177">ConvertIdType</span><span class="sxs-lookup"><span data-stu-id="fa92b-177">ConvertIdType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.ConvertIdType.aspx)
    
- [<span data-ttu-id="fa92b-178">ConvertId</span><span class="sxs-lookup"><span data-stu-id="fa92b-178">ConvertId</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.ExchangeServiceBinding.ConvertId.aspx)
    

