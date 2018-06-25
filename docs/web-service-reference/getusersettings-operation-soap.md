---
title: Operación GetUserSettings (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 758d965c-ef63-4de4-9120-e293abf14ff8
description: La operación GetUserSettings contiene una consulta para la configuración de acceso de cliente de los usuarios.
ms.openlocfilehash: 8bb8f766da3419ea33f89716e588a22d3924e1a4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835704"
---
# <a name="getusersettings-operation-soap"></a><span data-ttu-id="6894c-103">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6894c-103">GetUserSettings operation (SOAP)</span></span>

<span data-ttu-id="6894c-104">La operación **GetUserSettings** contiene una consulta para la configuración de acceso de cliente de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="6894c-104">The **GetUserSettings** operation contains a query for users' client access configuration.</span></span> 
  
## <a name="getusersettings-request-example"></a><span data-ttu-id="6894c-105">Ejemplo de solicitud de GetUserSettings</span><span class="sxs-lookup"><span data-stu-id="6894c-105">GetUserSettings request example</span></span>

### <a name="description"></a><span data-ttu-id="6894c-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="6894c-106">Description</span></span>

<span data-ttu-id="6894c-107">En el ejemplo de XML siguiente se muestra un cuerpo de la solicitud de detección automática que solicita un usuario nombre para mostrar, nombre distintivo (DN), identificador de implementación, el servidor de buzón de correo, nombre distintivo (DN) del buzón de correo, servidor de Active Directory, versión de servidor de acceso de cliente y Web compatibles de Exchange Esquemas de los servicios.</span><span class="sxs-lookup"><span data-stu-id="6894c-107">The following XML example shows an Autodiscover request body that requests a user's display name, distinguished name, deployment ID, mailbox server, mailbox distinguished name, Active Directory server, Client Access server version, and supported Exchange Web Services schemas.</span></span>
  
### <a name="code"></a><span data-ttu-id="6894c-108">Código</span><span class="sxs-lookup"><span data-stu-id="6894c-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover"      
               xmlns:wsa="http://www.w3.org/2005/08/addressing" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"      
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2010</a:RequestedServerVersion>
    <wsa:Action>http://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://myserver.contoso.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover">
      <a:Request>
        <a:Users>
          <a:User>
            <a:Mailbox>UserName@domain.contoso.com</a:Mailbox>
          </a:User>
        </a:Users>
        <a:RequestedSettings>
          <a:Setting>UserDisplayName</a:Setting>
          <a:Setting>UserDN</a:Setting>
          <a:Setting>UserDeploymentId</a:Setting>
          <a:Setting>InternalMailboxServer</a:Setting>
          <a:Setting>MailboxDN</a:Setting>
          <a:Setting>ActiveDirectoryServer</a:Setting>
          <a:Setting>CasVersion</a:Setting>
          <a:Setting>EwsSupportedSchemas</a:Setting>
        </a:RequestedSettings>
      </a:Request>
    </a:GetUserSettingsRequestMessage>
  </soap:Body>
</soap:Envelope>

```

### <a name="request-elements"></a><span data-ttu-id="6894c-109">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="6894c-109">Request elements</span></span>

<span data-ttu-id="6894c-110">En el cuerpo de la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="6894c-110">The following elements are used in the request body:</span></span>
  
- [<span data-ttu-id="6894c-111">GetUserSettingsRequestMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6894c-111">GetUserSettingsRequestMessage (SOAP)</span></span>](getusersettingsrequestmessage-soap.md)
    
- [<span data-ttu-id="6894c-112">Buzón de correo (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6894c-112">Mailbox (SOAP)</span></span>](mailbox-soap.md)
    
- [<span data-ttu-id="6894c-113">Solicitud (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6894c-113">Request (SOAP)</span></span>](request-soap.md)
    
- [<span data-ttu-id="6894c-114">RequestedServerVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6894c-114">RequestedServerVersion (SOAP)</span></span>](requestedserverversion-soap.md)
    
- [<span data-ttu-id="6894c-115">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6894c-115">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md)
    
- [<span data-ttu-id="6894c-116">Configuración (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6894c-116">Setting (SOAP)</span></span>](setting-soap.md)
    
- [<span data-ttu-id="6894c-117">Usuario (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6894c-117">User (SOAP)</span></span>](user-soap.md)
    
- [<span data-ttu-id="6894c-118">Usuarios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6894c-118">Users (SOAP)</span></span>](users-soap.md)
    
## <a name="getusersettings-response-example"></a><span data-ttu-id="6894c-119">Ejemplo de respuesta GetUserSettings</span><span class="sxs-lookup"><span data-stu-id="6894c-119">GetUserSettings response example</span></span>

### <a name="description"></a><span data-ttu-id="6894c-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="6894c-120">Description</span></span>

<span data-ttu-id="6894c-121">En el ejemplo siguiente se muestra una respuesta correcta de **GetUserSettings** .</span><span class="sxs-lookup"><span data-stu-id="6894c-121">The following example shows a successful **GetUserSettings** response.</span></span> 
  
### <a name="code"></a><span data-ttu-id="6894c-122">Código</span><span class="sxs-lookup"><span data-stu-id="6894c-122">Code</span></span>

```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">http://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
  </s:Header>
  <s:Body>
  <GetUserSettingsResponseMessage xmlns="http://schemas.microsoft.com/exchange/2010/Autodiscover">
      <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
        <ErrorCode>NoError</ErrorCode>
        <ErrorMessage />
        <UserResponses>
          <UserResponse>
            <ErrorCode>NoError</ErrorCode>
            <ErrorMessage>No error.</ErrorMessage>
            <RedirectTarget i:nil="true" />
            <UserSettingErrors />
            <UserSettings>
              <UserSetting i:type="StringSetting">
                <Name>UserDisplayName</Name>
                <Value>UserDisplayName</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>UserDN</Name>
                <Value>/o=First Organization/ou=Exchange Administrative Group (SDASDASDJ)/cn=Recipients/cn=UserDisplayName</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>UserDeploymentId</Name>
                <Value>a40E2742-21c6-4050-8Ed2-d41f100c22b8</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>CasVersion</Name>
                <Value>14.00.0478.000</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>EwsSupportedSchemas</Name>
                <Value>Exchange2007,  Exchange2010</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>InternalMailboxServer</Name>
                <Value>machinename.domain.contoso.com</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>ActiveDirectoryServer</Name>
                <Value>machinename.domain.contoso.com</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>MailboxDN</Name>
                <Value>/o=First Organization/ou=Exchange Administrative Group (SDASDASDJ)/cn=Configuration/cn=Servers/cn=server/cn=Contoso Pri MDB</Value>
              </UserSetting>
            </UserSettings>
          </UserResponse>
        </UserResponses>
      </Response>
    </GetUserSettingsResponseMessage>
  </s:Body>
</s:Envelope>
```

### <a name="response-elements"></a><span data-ttu-id="6894c-123">Elementos de respuesta</span><span class="sxs-lookup"><span data-stu-id="6894c-123">Response elements</span></span>

<span data-ttu-id="6894c-124">En el cuerpo de la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="6894c-124">The following elements are used in the response body:</span></span>
  
- [<span data-ttu-id="6894c-125">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6894c-125">ErrorCode (SOAP)</span></span>](errorcode-soap.md)
    
- [<span data-ttu-id="6894c-126">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6894c-126">ErrorMessage (SOAP)</span></span>](errormessage-soap.md)
    
- [<span data-ttu-id="6894c-127">GetUserSettingsResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6894c-127">GetUserSettingsResponseMessage (SOAP)</span></span>](getusersettingsresponsemessage-soap.md)
    
- [<span data-ttu-id="6894c-128">Nombre (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6894c-128">Name (SOAP)</span></span>](name-soap.md)
    
- [<span data-ttu-id="6894c-129">RedirectTarget (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6894c-129">RedirectTarget (SOAP)</span></span>](redirecttarget-soap.md)
    
- [<span data-ttu-id="6894c-130">Respuesta (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6894c-130">Response (SOAP)</span></span>](response-soap.md)
    
- [<span data-ttu-id="6894c-131">UserResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6894c-131">UserResponse (SOAP)</span></span>](userresponse-soap.md)
    
- [<span data-ttu-id="6894c-132">UserResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6894c-132">UserResponses (SOAP)</span></span>](userresponses-soap.md)
    
- [<span data-ttu-id="6894c-133">UserSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6894c-133">UserSetting (SOAP)</span></span>](usersetting-soap.md)
    
- [<span data-ttu-id="6894c-134">UserSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6894c-134">UserSettingErrors (SOAP)</span></span>](usersettingerrors-soap.md)
    
- [<span data-ttu-id="6894c-135">UserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6894c-135">UserSettings (SOAP)</span></span>](usersettings-soap.md)
    
- [<span data-ttu-id="6894c-136">Valor (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6894c-136">Value (SOAP)</span></span>](value-soap.md)
    
## <a name="see-also"></a><span data-ttu-id="6894c-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="6894c-137">See also</span></span>



[<span data-ttu-id="6894c-138">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6894c-138">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
  
[<span data-ttu-id="6894c-139">Operación GetFederationInformation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6894c-139">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)


[<span data-ttu-id="6894c-140">Elementos de Autodiscover XML SOAP para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="6894c-140">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

