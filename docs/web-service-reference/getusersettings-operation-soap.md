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
ms.openlocfilehash: e274fd4e1ca954ea25ea91a52e363c9a434b290a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466146"
---
# <a name="getusersettings-operation-soap"></a><span data-ttu-id="3b85b-103">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b85b-103">GetUserSettings operation (SOAP)</span></span>

<span data-ttu-id="3b85b-104">La operación **GetUserSettings** contiene una consulta para la configuración de acceso de cliente de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="3b85b-104">The **GetUserSettings** operation contains a query for users' client access configuration.</span></span> 
  
## <a name="getusersettings-request-example"></a><span data-ttu-id="3b85b-105">Ejemplo de solicitud GetUserSettings</span><span class="sxs-lookup"><span data-stu-id="3b85b-105">GetUserSettings request example</span></span>

### <a name="description"></a><span data-ttu-id="3b85b-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b85b-106">Description</span></span>

<span data-ttu-id="3b85b-107">El siguiente ejemplo de XML muestra un cuerpo de solicitud de detección automática que solicita el nombre para mostrar, el nombre distintivo, el identificador de implementación, el servidor de buzones, el nombre distintivo de buzón, el servidor de Active Directory, la versión del servidor de acceso de cliente y los esquemas de servicios Web de Exchange admitidos del usuario.</span><span class="sxs-lookup"><span data-stu-id="3b85b-107">The following XML example shows an Autodiscover request body that requests a user's display name, distinguished name, deployment ID, mailbox server, mailbox distinguished name, Active Directory server, Client Access server version, and supported Exchange Web Services schemas.</span></span>
  
### <a name="code"></a><span data-ttu-id="3b85b-108">Código</span><span class="sxs-lookup"><span data-stu-id="3b85b-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover"      
               xmlns:wsa="http://www.w3.org/2005/08/addressing" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"      
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2010</a:RequestedServerVersion>
    <wsa:Action>https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://myserver.contoso.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover">
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

### <a name="request-elements"></a><span data-ttu-id="3b85b-109">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="3b85b-109">Request elements</span></span>

<span data-ttu-id="3b85b-110">Los siguientes elementos se usan en el cuerpo de la solicitud:</span><span class="sxs-lookup"><span data-stu-id="3b85b-110">The following elements are used in the request body:</span></span>
  
- [<span data-ttu-id="3b85b-111">GetUserSettingsRequestMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b85b-111">GetUserSettingsRequestMessage (SOAP)</span></span>](getusersettingsrequestmessage-soap.md)
    
- [<span data-ttu-id="3b85b-112">Buzón de correo (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b85b-112">Mailbox (SOAP)</span></span>](mailbox-soap.md)
    
- [<span data-ttu-id="3b85b-113">Solicitud (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b85b-113">Request (SOAP)</span></span>](request-soap.md)
    
- [<span data-ttu-id="3b85b-114">RequestedServerVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b85b-114">RequestedServerVersion (SOAP)</span></span>](requestedserverversion-soap.md)
    
- [<span data-ttu-id="3b85b-115">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b85b-115">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md)
    
- [<span data-ttu-id="3b85b-116">Configuración (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b85b-116">Setting (SOAP)</span></span>](setting-soap.md)
    
- [<span data-ttu-id="3b85b-117">Usuario (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b85b-117">User (SOAP)</span></span>](user-soap.md)
    
- [<span data-ttu-id="3b85b-118">Usuarios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b85b-118">Users (SOAP)</span></span>](users-soap.md)
    
## <a name="getusersettings-response-example"></a><span data-ttu-id="3b85b-119">Ejemplo de respuesta GetUserSettings</span><span class="sxs-lookup"><span data-stu-id="3b85b-119">GetUserSettings response example</span></span>

### <a name="description"></a><span data-ttu-id="3b85b-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b85b-120">Description</span></span>

<span data-ttu-id="3b85b-121">En el ejemplo siguiente se muestra una respuesta **GetUserSettings** correcta.</span><span class="sxs-lookup"><span data-stu-id="3b85b-121">The following example shows a successful **GetUserSettings** response.</span></span> 
  
### <a name="code"></a><span data-ttu-id="3b85b-122">Código</span><span class="sxs-lookup"><span data-stu-id="3b85b-122">Code</span></span>

```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
  </s:Header>
  <s:Body>
  <GetUserSettingsResponseMessage xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover">
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

### <a name="response-elements"></a><span data-ttu-id="3b85b-123">Elementos de respuesta</span><span class="sxs-lookup"><span data-stu-id="3b85b-123">Response elements</span></span>

<span data-ttu-id="3b85b-124">Los siguientes elementos se usan en el cuerpo de la respuesta:</span><span class="sxs-lookup"><span data-stu-id="3b85b-124">The following elements are used in the response body:</span></span>
  
- [<span data-ttu-id="3b85b-125">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b85b-125">ErrorCode (SOAP)</span></span>](errorcode-soap.md)
    
- [<span data-ttu-id="3b85b-126">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b85b-126">ErrorMessage (SOAP)</span></span>](errormessage-soap.md)
    
- [<span data-ttu-id="3b85b-127">GetUserSettingsResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b85b-127">GetUserSettingsResponseMessage (SOAP)</span></span>](getusersettingsresponsemessage-soap.md)
    
- [<span data-ttu-id="3b85b-128">Name (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b85b-128">Name (SOAP)</span></span>](name-soap.md)
    
- [<span data-ttu-id="3b85b-129">RedirectTarget (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b85b-129">RedirectTarget (SOAP)</span></span>](redirecttarget-soap.md)
    
- [<span data-ttu-id="3b85b-130">Respuesta (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b85b-130">Response (SOAP)</span></span>](response-soap.md)
    
- [<span data-ttu-id="3b85b-131">UserResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b85b-131">UserResponse (SOAP)</span></span>](userresponse-soap.md)
    
- [<span data-ttu-id="3b85b-132">UserResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b85b-132">UserResponses (SOAP)</span></span>](userresponses-soap.md)
    
- [<span data-ttu-id="3b85b-133">UserSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b85b-133">UserSetting (SOAP)</span></span>](usersetting-soap.md)
    
- [<span data-ttu-id="3b85b-134">UserSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b85b-134">UserSettingErrors (SOAP)</span></span>](usersettingerrors-soap.md)
    
- [<span data-ttu-id="3b85b-135">UserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b85b-135">UserSettings (SOAP)</span></span>](usersettings-soap.md)
    
- [<span data-ttu-id="3b85b-136">Valor (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b85b-136">Value (SOAP)</span></span>](value-soap.md)
    
## <a name="see-also"></a><span data-ttu-id="3b85b-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b85b-137">See also</span></span>



[<span data-ttu-id="3b85b-138">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b85b-138">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
  
[<span data-ttu-id="3b85b-139">Operación GetFederationInformation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b85b-139">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)


[<span data-ttu-id="3b85b-140">Elementos XML de detección automática de SOAP para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="3b85b-140">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

