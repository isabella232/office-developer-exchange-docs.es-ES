---
title: Operación AddEntityFeedback
manager: luken
ms.date: 4/18/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 00e40197-5794-4268-b937-bd65aa044890
description: La operación AddEntityFeedback devuelve información de error correspondiente a problemas del lado servidor.
ms.openlocfilehash: a1027a0a1ee06cf3e83833b1d84c13d77b07c0b9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458442"
---
# <a name="addentityfeedback-operation"></a>Operación AddEntityFeedback

La operación **AddEntityFeedback** devuelve información de error correspondiente a problemas del lado servidor. 
  
Esta operación depende del tipo de evento que se está registrando. Uno de los eventos más importantes es **EntityAdded**, que corresponde a una entidad seleccionada. Esta operación es un lote, por lo que se puede usar para registrar lotes de entradas en una sola solicitud. 
  
## <a name="findpeople-request-examples"></a>Ejemplos de solicitudes de FindPeople

La operación **AddEntityFeedback** proporciona un medio para que los clientes registren detalles de interacción con entidades devueltas por el servicio. Esto puede usarse como una señal para mejorar la relevancia en segundo plano para cada cliente. Por ejemplo, los clientes pueden usar esta operación para enviar comentarios sobre entidades de personas devueltas desde **FindPeople**.
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
                             xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                             xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:AddEntityFeedback>
            <m:EntityFeedbackEntries>
                  <t:EntityFeedbackEntry>
                        <t:ClientEventTimeUTC> 2015-07-05T22:16:18+00:00</t:ClientEventTimeUTC>
                        <t:ClientEventTimeLocal> 2015-07-05T22:16:18+00:00</t:ClientEventTimeLocal>
                        <t:ClientSessionId>00000000-0000-0000-0000-000000000012</t:ClientSessionId>
                        <t:ClientVersion>15.01.0101.01</t:ClientVersion>
                        <t:ClientId>Web</t:ClientId>
                        <t:TransactionId>123456789</t:TransactionId>
                        <t:EventType>EntityAdded</t:EventType>
                        <t:TargetEntityList>["a","b","c"]</t:TargetEntityList>
                        <t:SourceOfEntityAdded></t:SourceOfEntityAdded>
                        <t:JSONPropertyBag></t:JSONPropertyBag>
                  </t:EntityFeedbackEntry>
                  <t:EntityFeedbackEntry>
                  …
                  </t:EntityFeedbackEntry>
            </m:EntityFeedbackEntries>
      </m:AddEntityFeedback>
   </soap:Body>
</soap:Envelope>

```

### <a name="the-request-soap-body-contents"></a>El contenido del cuerpo SOAP de la solicitud

La solicitud SOAP contiene un elemento único **EntityFeedbackEntries**. Esto, a su vez, contiene una matriz de objetos **EntityFeedbackEntry** . Cada entrada de la matriz puede contener los siguientes elementos. 
  
|**Parámetros de solicitud**|**Obligatorio**|**Descripción**|**Tipo**|
|:-----|:-----|:-----|:-----|
|**ClientEventTimeUtc** <br/> |Sí  <br/> |La hora UTC en que se produjo el evento en el lado cliente.  <br/> |DateTime  <br/> |
|**ClientEventTimeLocal** <br/> |Sí  <br/> |La hora local en la que se produjo el evento en el lado cliente.  <br/> |DateTime  <br/> |
|**ClientId** <br/> |Sí  <br/> |Tipo de cliente (por ejemplo, Outlook, OWA, etc.).  <br/> |Enumeración ClientIDType  <br/> |
|**ClientSessionId** <br/> |Sí  <br/> |GUID que identifica el identificador de sesión. Se genera en el cliente.  <br/> |GUID  <br/> |
|**ClientVersion** <br/> |Sí  <br/> |Versión del cliente (por ejemplo, 15.01.0101.000).  <br/> |Cadena  <br/> |
|**EntityAddSource** <br/> |No  <br/> |Origen para EntityAded (por ejemplo, EntityRelevanceAPI, Types, pegados).  <br/> |Enumeración EntityAddSource  <br/> |
|**EntrySequenceNumber** <br/> |Sí  <br/> |Entero incremental por sesión de cliente. Se usa para detectar la pérdida de datos.  <br/> |Int  <br/> |
|**EventType** <br/> |Sí  <br/> |Tipo de evento (por ejemplo, entidad agregada, entidad eliminada).  <br/> |Cadena  <br/> |
|**JSONPropertyBag** <br/> |No  <br/> |Propiedades adicionales asociadas con el evento (objeto binario JSON de pares clave-valor).  <br/> |BLOB de JSON  <br/> |
|**TargetEntityList** <br/> |No  <br/> |Lista de entidades asociadas al evento.  <br/> |Cadena JSON  <br/> |
|**TransactionId** <br/> |No  <br/> |IDENTIFICADOR (GUID) que correlaciona el identificador en los registros de consulta.  <br/> |Cadena  <br/> |
   
### <a name="successful-addentityfeedback-operation-response"></a>Respuesta de operación AddEntityFeedback correcta

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" 
                                MinorVersion="1" 
                                MajorBuildNumber="228" 
                                MinorBuildNumber="0" 
                                Version="V2_49" 
                                xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                                xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                                xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <AddEntityFeedbackResponse ResponseClass="Success" 
                                                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                                              xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                                                              xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <ErrorCount>0</ErrorCount>
            <ErrorDetails />
        </AddEntityFeedbackResponse>
    </s:Body>
</s:Envelope> 

```

### <a name="the-response-soap-body-contains-the-following-elements"></a>El cuerpo SOAP de respuesta contiene los siguientes elementos

#### <a name="errors"></a>Errores 
  
La API puede registrar un lote de entradas de comentarios, se registra todo lo que podemos. Este campo representa el número de entradas de error que no se registraron.
    
#### <a name="errordetails"></a>ErrorDetails
  
Detalles relativos a los errores anteriores separa por `;` .
    
### <a name="currently-supported-values"></a>Valores actualmente admitidos

|**Enumeración ClientIdType**|
|:-----|
|Desktop  <br/> |
|Exchange  <br/> |
|IMAP4  <br/> |
|2015  <br/> |
|MacMail  <br/> |
|MacOutlook  <br/> |
|Mobile  <br/> |
|Otros  <br/> |
|Outlook  <br/> |
|OutlookService  <br/> |
|POP3  <br/> |
|Tablet  <br/> |
|Web  <br/> |
   
|**Enumeración EntityAddSource**|
|:-----|
|Directory  <br/> |
|EntityRelevanceApi  <br/> |
|EntityRelevanceApiCache  <br/> |
|ExplicitTyping  <br/> |
|LocalCache  <br/> |
|LocalCacheAndEntityRelevanceAPI  <br/> |
|Ninguno  <br/> |
|Otros  <br/> |
|Paste  <br/> |
   
### <a name="addentityfeedback-operation-error-response"></a>Respuesta de error de operación de AddEntityFeedback

Para los códigos de error que son genéricos para EWS, vea [ResponseCode](responsecode.md).
  
### <a name="example-of-addentityfeedback-in-conjunction-with-findpeople"></a>Ejemplo de AddEntityFeedback en combinación con FindPeople

#### <a name="findpeople-request"></a>Solicitud FindPeople
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
<soap:Body >
    <m:FindPeople>
      <m:IndexedPageItemView BasePoint="Beginning" MaxEntriesReturned="100" Offset="0"/>
      <m:QueryString>user1</m:QueryString>
      <m:SearchPeopleSuggestionIndex>true</m:SearchPeopleSuggestionIndex>
    </m:FindPeople>
  </soap:Body>
</soap:Envelope>    
    
```

#### <a name="findpeople-response"></a>Respuesta FindPeople

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" MinorVersion="1" MajorBuildNumber="302" MinorBuildNumber="0" Version="V2_68" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <FindPeopleResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <People>
                <Persona xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
                    <PersonaId Id="AAUQAFjZ4UxX8SZCqSPFsmh0cSo=" />
                    <PersonaType>Person</PersonaType>
                    <CreationTime>2015-10-02T23:25:42</CreationTime>
                    <DisplayName>user2</DisplayName>
…
                  </Persona>
            </People>
            <TotalNumberOfPeopleInView>0</TotalNumberOfPeopleInView>
            <FirstMatchingRowIndex>0</FirstMatchingRowIndex>
            <FirstLoadedRowIndex>0</FirstLoadedRowIndex>
            <TransactionId>b56ad16e-5d5a-4574-90f8-b8dd57382be6</TransactionId>
        </FindPeopleResponse>
    </s:Body>
</s:Envelope>

```

#### <a name="addentityfeedback-request"></a>Solicitud AddEntityFeedback

```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:AddEntityFeedback>
<m:EntityFeedbackEntries>
<t:EntityFeedbackEntry>
         <t:ClientEventTimeUtc>2015-07-05T22:16:18+00:00</t:ClientEventTimeUtc>
         <t:ClientEventTimeLocal>2015-07-05T22:16:18+00:00</t:ClientEventTimeLocal>
         <t:ClientSessionId>00000000-0000-0000-0000-000000000012</t:ClientSessionId>
         <t:ClientVersion>15.01.0101.01</t:ClientVersion>
         <t:ClientId>Web</t:ClientId>
         <t:TransactionId>b56ad16e-5d5a-4574-90f8-b8dd57382be6</t:TransactionId>
         <t:EventType>EntityAdded</t:EventType>
         <t:TargetEntityList>["user1@ms7.com"]</t:TargetEntityList>
         <t:SourceOfEntityAdded>EntityRelevanceApi</t:SourceOfEntityAdded>
         <t:JSONPropertyBag></t:JSONPropertyBag>
</t:EntityFeedbackEntry>
</m:EntityFeedbackEntries>
      </m:AddEntityFeedback>
   </soap:Body>
</soap:Envelope>

```

> [!NOTE]
> Mediante FindPeople Response ID Transaction como el identificador de transacción de solicitud AddEntityFeedback. 
  
#### <a name="addentityfeedback-response"></a>Respuesta AddEntityFeedback

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" MinorVersion="1" MajorBuildNumber="302" MinorBuildNumber="0" Version="V2_68" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <AddEntityFeedbackResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <ErrorCount>0</ErrorCount>
            <ErrorDetails />
        </AddEntityFeedbackResponse>
    </s:Body>
</s:Envelope>

```


