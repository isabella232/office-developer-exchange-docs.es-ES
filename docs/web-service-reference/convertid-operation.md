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
description: Buscar información sobre la operación de EWS de ConvertId.
ms.openlocfilehash: 36bd47d3fc7c7ca7cea7b38222abb25fba6074ac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44452555"
---
# <a name="convertid-operation"></a><span data-ttu-id="3a538-103">Operación ConvertId</span><span class="sxs-lookup"><span data-stu-id="3a538-103">ConvertId operation</span></span>

<span data-ttu-id="3a538-104">Buscar información sobre la operación de EWS de **ConvertId** .</span><span class="sxs-lookup"><span data-stu-id="3a538-104">Find information about the **ConvertId** EWS operation.</span></span> 
  
<span data-ttu-id="3a538-105">La **ConvertId** de servicios web Exchange (EWS) convierte los identificadores de elementos y carpetas entre formatos aceptados por Exchange Online, Exchange online como parte de Office 365 y las versiones locales de Exchange a partir de exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3a538-105">The **ConvertId** Exchange Web Services (EWS) operation converts item and folder identifiers between formats that are accepted by Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with Exchange Server 2013.</span></span> 
  
## <a name="using-the-convertid-operation"></a><span data-ttu-id="3a538-106">Uso de la operación ConvertId</span><span class="sxs-lookup"><span data-stu-id="3a538-106">Using the ConvertId operation</span></span>
<span data-ttu-id="3a538-107"><a name="bk_usingConvertId"> </a></span><span class="sxs-lookup"><span data-stu-id="3a538-107"><a name="bk_usingConvertId"> </a></span></span>

<span data-ttu-id="3a538-108">Puede convertir los siguientes identificadores mediante la operación **ConvertId** :</span><span class="sxs-lookup"><span data-stu-id="3a538-108">You can convert the following identifiers by using the **ConvertId** operation:</span></span> 
  
- <span data-ttu-id="3a538-109">El formato de identificador de EWS en la versión de lanzamiento inicial de Exchange 2007.</span><span class="sxs-lookup"><span data-stu-id="3a538-109">The identifier format for EWS in the initial release version of Exchange 2007.</span></span> <span data-ttu-id="3a538-110">Esto se representa mediante el `EwsLegacyId` valor de enumeración en la enumeración [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="3a538-110">This is represented by the  `EwsLegacyId` enumeration value in the [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) enumeration.</span></span> 
    
- <span data-ttu-id="3a538-111">El formato de identificador de EWS en Exchange 2007 SP1 o Exchange 2010.</span><span class="sxs-lookup"><span data-stu-id="3a538-111">The identifier format for EWS in Exchange 2007 SP1 or Exchange 2010.</span></span> <span data-ttu-id="3a538-112">Esto se representa mediante el `EwsId` valor de enumeración en [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="3a538-112">This is represented by the  `EwsId` enumeration value in [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).</span></span>
    
- <span data-ttu-id="3a538-113">Identificador de MAPI, como en la propiedad **PR_ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="3a538-113">The MAPI identifier, as in the **PR_ENTRYID** property.</span></span> <span data-ttu-id="3a538-114">Esto se representa mediante el `EntryId` valor de enumeración en la enumeración [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="3a538-114">This is represented by the  `EntryId` enumeration value in the [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) enumeration.</span></span> 
    
- <span data-ttu-id="3a538-115">Identificador de evento del calendario de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="3a538-115">The availability calendar event identifier.</span></span> <span data-ttu-id="3a538-116">Se trata de una representación codificada en hexadecimal de la propiedad **PR_ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="3a538-116">This is a hexadecimal-encoded representation of the **PR_ENTRYID** property.</span></span> <span data-ttu-id="3a538-117">Esto se representa mediante el `HexEntryId` valor de enumeración en [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="3a538-117">This is represented by the  `HexEntryId` enumeration value in [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).</span></span>
    
- <span data-ttu-id="3a538-118">El identificador del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3a538-118">The Exchange store identifier.</span></span> <span data-ttu-id="3a538-119">Esto se representa mediante el `StoreId` valor de enumeración en [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="3a538-119">This is represented by the  `StoreId` enumeration value in [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="3a538-120">La operación **ConvertId** no convierte los identificadores de la carpeta pública del identificador EWS al identificador del almacén.</span><span class="sxs-lookup"><span data-stu-id="3a538-120">The **ConvertId** operation does not convert public folder identifiers from the EWS identifier to the store identifier.</span></span> 
    
- <span data-ttu-id="3a538-121">Identificador de Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="3a538-121">The Outlook Web App identifier.</span></span> <span data-ttu-id="3a538-122">Esto se representa mediante el `OwaId` valor de enumeración en [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a538-122">This is represented by the  `OwaId` enumeration value in [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)</span></span>
    
    <span data-ttu-id="3a538-123">No se admite el paso de direcciones URL creadas desde este identificador a Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="3a538-123">The passing of URLs that are created from this identifier to Outlook Web App is not supported.</span></span> <span data-ttu-id="3a538-124">El identificador de Outlook Web App se aplica a Exchange 2007 y a Exchange 2010.</span><span class="sxs-lookup"><span data-stu-id="3a538-124">The Outlook Web App identifier is applicable to Exchange 2007 and Exchange 2010.</span></span> <span data-ttu-id="3a538-125">Outlook Web App para Exchange Online y versiones de Exchange a partir de Exchange Server 2013 usan identificadores EWS.</span><span class="sxs-lookup"><span data-stu-id="3a538-125">Outlook Web App for Exchange Online and versions of Exchange starting with Exchange Server 2013 uses EWS identifiers.</span></span>
    
<span data-ttu-id="3a538-126">La operación **ConvertId** no funciona según lo esperado al convertir los identificadores de carpeta pública del identificador EWS al identificador de almacén en Exchange Online y Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="3a538-126">The **ConvertId** operation does not work as expected when converting public folder identifiers from the EWS identifier to the store identifier in Exchange Online and Exchange 2013.</span></span> <span data-ttu-id="3a538-127">Puede actualizar manualmente el identificador que se devuelve como solución alternativa.</span><span class="sxs-lookup"><span data-stu-id="3a538-127">You can manually update the identifier that is returned as a workaround.</span></span> <span data-ttu-id="3a538-128">Para actualizar manualmente el identificador:</span><span class="sxs-lookup"><span data-stu-id="3a538-128">To manually update the identifier:</span></span> 
  
1. <span data-ttu-id="3a538-129">En el código de la aplicación, determine si el elemento o carpeta de destino está en una carpeta pública.</span><span class="sxs-lookup"><span data-stu-id="3a538-129">In your application code, determine whether the target item/folder is in a public folder.</span></span> 
    
2. <span data-ttu-id="3a538-130">Descodifique la cadena identificadora codificada en Base64.</span><span class="sxs-lookup"><span data-stu-id="3a538-130">Decode the Base64-encoded identifier string.</span></span>
    
3. <span data-ttu-id="3a538-131">Compruebe que el tipo byte (XXI byte) tiene un valor de 7.</span><span class="sxs-lookup"><span data-stu-id="3a538-131">Verify that the type byte (21st byte) has a value of 7.</span></span> <span data-ttu-id="3a538-132">Un valor de 7 indica que el identificador no tiene el formato correcto.</span><span class="sxs-lookup"><span data-stu-id="3a538-132">A value of 7 indicates that the identifier is in the incorrect format.</span></span>
    
4. <span data-ttu-id="3a538-133">Omitir los primeros cuatro bytes.</span><span class="sxs-lookup"><span data-stu-id="3a538-133">Skip the first four bytes.</span></span> <span data-ttu-id="3a538-134">Deben establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="3a538-134">They must be set to zero.</span></span>
    
5. <span data-ttu-id="3a538-135">Actualice los siguientes 16 bytes con el siguiente GUID: 1A447390AA6611CD9BC800AA002FC45A</span><span class="sxs-lookup"><span data-stu-id="3a538-135">Update the next 16 bytes with the following GUID: 1A447390AA6611CD9BC800AA002FC45A</span></span>
    
6. <span data-ttu-id="3a538-136">Actualice el siguiente byte (tipo byte) con un valor de 9.</span><span class="sxs-lookup"><span data-stu-id="3a538-136">Update the next byte (type byte) with a value of 9.</span></span>
    
7. <span data-ttu-id="3a538-137">Cambie el identificador a una cadena codificada en Base64.</span><span class="sxs-lookup"><span data-stu-id="3a538-137">Change the identifier to a Base64-encoded string.</span></span>
    
> [!NOTE]
> <span data-ttu-id="3a538-138">La operación **ConvertId** valida que una dirección SMTP determinada tiene un formato válido.</span><span class="sxs-lookup"><span data-stu-id="3a538-138">The **ConvertId** operation validates that a given SMTP address has a valid format.</span></span> <span data-ttu-id="3a538-139">La operación no determina si una dirección SMTP representa un buzón válido.</span><span class="sxs-lookup"><span data-stu-id="3a538-139">The operation does not determine whether an SMTP address represents a valid mailbox.</span></span> 
  
<span data-ttu-id="3a538-140">La operación **ConvertId** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="3a538-140">The **ConvertId** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
<span data-ttu-id="3a538-141">**Tabla 1. Encabezados SOAP de operación ConvertId**</span><span class="sxs-lookup"><span data-stu-id="3a538-141">**Table 1. ConvertId operation SOAP headers**</span></span>

|<span data-ttu-id="3a538-142">**Header**</span><span class="sxs-lookup"><span data-stu-id="3a538-142">**Header**</span></span>|<span data-ttu-id="3a538-143">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3a538-143">**Element**</span></span>|<span data-ttu-id="3a538-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3a538-144">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3a538-145">Suplantación</span><span class="sxs-lookup"><span data-stu-id="3a538-145">Impersonation</span></span>  <br/> |[<span data-ttu-id="3a538-146">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="3a538-146">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="3a538-147">Identifica al usuario que está suplantando la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="3a538-147">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="3a538-148">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="3a538-148">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="3a538-149">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="3a538-149">RequestVersion</span></span>  <br/> |[<span data-ttu-id="3a538-150">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="3a538-150">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="3a538-151">Identifica la versión del esquema para la solicitud de operación esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="3a538-151">Identifies the schema version for the operation request This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="3a538-152">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="3a538-152">ServerVersion</span></span>  <br/> |[<span data-ttu-id="3a538-153">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="3a538-153">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="3a538-154">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3a538-154">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="3a538-155">Esto es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="3a538-155">This is applicable to a response.</span></span>  <br/> |
   
## <a name="convertid-operation-request-example"></a><span data-ttu-id="3a538-156">Ejemplo de solicitud de operación ConvertId</span><span class="sxs-lookup"><span data-stu-id="3a538-156">ConvertId operation request example</span></span>
<span data-ttu-id="3a538-157"><a name="bk_usingConvertId"> </a></span><span class="sxs-lookup"><span data-stu-id="3a538-157"><a name="bk_usingConvertId"> </a></span></span>

<span data-ttu-id="3a538-158">El siguiente ejemplo de una solicitud **ConvertId** muestra cómo convertir un identificador EWS a un identificador de Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="3a538-158">The following example of a **ConvertId** request shows how to convert from an EWS identifier to an Outlook Web App identifier.</span></span> 
  
<span data-ttu-id="3a538-159">El elemento [RequestServerVersion](requestserverversion.md) del encabezado SOAP debe establecerse en Exchange2007_SP1 o posterior para que funcione esta operación.</span><span class="sxs-lookup"><span data-stu-id="3a538-159">The [RequestServerVersion](requestserverversion.md) element in the SOAP header must be set to Exchange2007_SP1 or later for this operation to work.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3a538-160">El identificador de elemento se ha abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="3a538-160">The item identifier has been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <ConvertId xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               DestinationFormat="OwaId">
      <SourceIds>
        <t:AlternateId Format="EwsId" Id="AAMkAGZhN2IxYTA0LWNiNzItN="
                       Mailbox="user1@example.com"/>
      </SourceIds>
    </ConvertId>
  </soap:Body>
</soap:Envelope>
```

## <a name="convertid-operation-response-example"></a><span data-ttu-id="3a538-161">Ejemplo de respuesta de operación ConvertId</span><span class="sxs-lookup"><span data-stu-id="3a538-161">ConvertId operation response example</span></span>
<span data-ttu-id="3a538-162"><a name="bk_usingConvertId"> </a></span><span class="sxs-lookup"><span data-stu-id="3a538-162"><a name="bk_usingConvertId"> </a></span></span>

<span data-ttu-id="3a538-163">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud **ConvertId** .</span><span class="sxs-lookup"><span data-stu-id="3a538-163">The following example shows a successful response to a **ConvertId** request.</span></span> <span data-ttu-id="3a538-164">Este ejemplo de respuesta contiene un identificador de Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="3a538-164">This response example contains an Outlook Web App identifier.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3a538-165">El identificador de Outlook Web App se ha abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="3a538-165">The Outlook Web App identifier has been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="1" 
                         MajorBuildNumber="191" MinorBuildNumber="0" 
                         Version="Exchange2010" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ConvertIdResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="convertid-operation-error-response-example"></a><span data-ttu-id="3a538-166">Ejemplo de respuesta de error de operación ConvertId</span><span class="sxs-lookup"><span data-stu-id="3a538-166">ConvertId operation error response example</span></span>
<span data-ttu-id="3a538-167"><a name="bk_usingConvertId"> </a></span><span class="sxs-lookup"><span data-stu-id="3a538-167"><a name="bk_usingConvertId"> </a></span></span>

<span data-ttu-id="3a538-168">En el ejemplo siguiente se muestra la respuesta a una solicitud que contiene el tipo de formato de identificador incorrecto.</span><span class="sxs-lookup"><span data-stu-id="3a538-168">The following example shows the response to a request that contains the wrong type of identifier format.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <ServerVersionInfo MajorVersion="8" MinorVersion="1" 
                       MajorBuildNumber="206" MinorBuildNumber="0"
                       Version="Exchange2010" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ConvertIdResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="version-differences"></a><span data-ttu-id="3a538-169">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="3a538-169">Version differences</span></span>
<span data-ttu-id="3a538-170"><a name="bk_ConvertIdVersionDiff"> </a></span><span class="sxs-lookup"><span data-stu-id="3a538-170"><a name="bk_ConvertIdVersionDiff"> </a></span></span>

<span data-ttu-id="3a538-171">El formato de identificador de EWS ha cambiado entre la versión de lanzamiento inicial de Exchange 2007 y Exchange 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="3a538-171">The EWS identifier format changed between the initial release version of Exchange 2007 and Exchange 2007 Service Pack 1 (SP1).</span></span> <span data-ttu-id="3a538-172">Exchange online como parte de Office 365, Exchange Online y las versiones locales de Exchange a partir de Exchange 2010 usan el mismo formato de identificador que usa Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="3a538-172">Exchange Online as part of Office 365, Exchange Online, and on-premises versions of Exchange starting with Exchange 2010 use the same identifier format that Exchange 2007 SP1 uses.</span></span>
  
<span data-ttu-id="3a538-173">La operación **ConvertId** convierte los identificadores de carpeta pública del identificador EWS al identificador de almacén en Exchange 2007 y Exchange 2010.</span><span class="sxs-lookup"><span data-stu-id="3a538-173">The **ConvertId** operation converts public folder identifiers from the EWS identifier to the store identifier in Exchange 2007 and Exchange 2010.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3a538-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a538-174">See also</span></span>
<span data-ttu-id="3a538-175"><a name="bk_ConvertIdVersionDiff"> </a></span><span class="sxs-lookup"><span data-stu-id="3a538-175"><a name="bk_ConvertIdVersionDiff"> </a></span></span>

- [<span data-ttu-id="3a538-176">Convertir identificadores</span><span class="sxs-lookup"><span data-stu-id="3a538-176">Converting Identifiers</span></span>](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)
    
- [<span data-ttu-id="3a538-177">ConvertIdType</span><span class="sxs-lookup"><span data-stu-id="3a538-177">ConvertIdType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.ConvertIdType.aspx)
    
- [<span data-ttu-id="3a538-178">ConvertId</span><span class="sxs-lookup"><span data-stu-id="3a538-178">ConvertId</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.ExchangeServiceBinding.ConvertId.aspx)
    

