---
title: Referencia del servicio Web de detección automática de SOAP para Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 61c21ea9-7fea-4f56-8ada-bf80e1e6b074
description: Busque información de referencia para el servicio de detección automática de SOAP en Exchange.
ms.openlocfilehash: bfca8e8e260a6262d12542bd6834894a2375453f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468428"
---
# <a name="soap-autodiscover-web-service-reference-for-exchange"></a><span data-ttu-id="77207-103">Referencia del servicio Web de detección automática de SOAP para Exchange</span><span class="sxs-lookup"><span data-stu-id="77207-103">SOAP Autodiscover web service reference for Exchange</span></span>

<span data-ttu-id="77207-104">Busque información de referencia para el servicio de detección automática de SOAP en Exchange.</span><span class="sxs-lookup"><span data-stu-id="77207-104">Find reference information for the SOAP Autodiscover service in Exchange.</span></span>
  
<span data-ttu-id="77207-105">El servicio Detección automática proporciona la información de configuración que la aplicación usa para crear una conexión a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="77207-105">The Autodiscover service provides the configuration information that your application uses to create a connection to an Exchange server.</span></span> <span data-ttu-id="77207-106">Puede usar el servicio Detección automática de SOAP para enviar mensajes entre la aplicación cliente y el servidor Exchange para buscar la configuración que la aplicación usará para conectarse a Exchange.</span><span class="sxs-lookup"><span data-stu-id="77207-106">You can use the SOAP Autodiscover service to send messages between the client application and the Exchange server to locate the settings the application will use to connect to Exchange.</span></span> <span data-ttu-id="77207-107">A diferencia del servicio Detección automática de POX, el servicio Detección automática de SOAP permite solicitudes de detección automática por lotes para la configuración de muchos usuarios y un control más granular sobre la configuración que se devuelve en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="77207-107">Unlike the POX Autodiscover service, the SOAP Autodiscover service allows for batched Autodiscover requests for many users' settings and more granular control over which settings are returned in the response.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="77207-108">Para los clientes que tienen como destino versiones de Exchange que comienzan con Exchange Server 2010, se recomienda usar el servicio de detección automática de SOAP (en lugar del servicio Detección automática de POX).</span><span class="sxs-lookup"><span data-stu-id="77207-108">For clients that target versions of Exchange starting with Exchange Server 2010, we recommend that you use the SOAP Autodiscover service (instead of the POX Autodiscover service).</span></span> <span data-ttu-id="77207-109">Los clientes que tienen el destino de Exchange 2007 deben usar el servicio Detección automática de POX.</span><span class="sxs-lookup"><span data-stu-id="77207-109">Clients that target Exchange 2007 have to use the POX Autodiscover service.</span></span> <span data-ttu-id="77207-110">Se recomienda que los clientes que usen .NET Framework usen la API administrada de EWS porque contiene un cliente de detección automática de SOAP sólido y bien probado.</span><span class="sxs-lookup"><span data-stu-id="77207-110">We recommend that clients that use the .NET Framework use the EWS Managed API because it contains a robust and well-tested SOAP Autodiscover client.</span></span> <span data-ttu-id="77207-111">Para obtener más información sobre la API administrada de EWS, vea Introducción [a las aplicaciones cliente de la API administrada de EWS](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="77207-111">For more information about the EWS Managed API, see [Get started with EWS Managed API client applications](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx).</span></span> 
  
<span data-ttu-id="77207-112">En esta sección se proporciona información acerca de los elementos XML que se envían entre el cliente y el servidor durante la redirección de la solicitud de detección automática de SOAP y la configuración de usuario que se devuelve en una respuesta.</span><span class="sxs-lookup"><span data-stu-id="77207-112">This section provides information about the XML elements that are sent between the client and server during SOAP Autodiscover request redirections and the user settings that are returned in a response.</span></span> <span data-ttu-id="77207-113">La referencia del elemento XML contiene resúmenes de lo que representan los elementos y una descripción de las jerarquías de elementos potenciales que contienen el elemento.</span><span class="sxs-lookup"><span data-stu-id="77207-113">The XML element reference contains summaries of what the elements represent and a description of the potential element hierarchies that contain the element.</span></span> 
  
<span data-ttu-id="77207-114">En los artículos de esta sección se describen las instancias de XML que se envían entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="77207-114">The articles in this section describe the XML instances that are sent between the client and server.</span></span> <span data-ttu-id="77207-115">El esquema que describe estos elementos se puede encontrar en el directorio virtual del servidor que hospeda el servicio Detección automática de SOAP.</span><span class="sxs-lookup"><span data-stu-id="77207-115">The schema that describes these elements can be found in the virtual directory of the server that hosts the SOAP Autodiscover service.</span></span>
  
<span data-ttu-id="77207-116">En los temas de funcionamiento de WSDL de esta sección se proporciona información general sobre lo que hace la operación y los ejemplos de solicitud y respuesta de la operación.</span><span class="sxs-lookup"><span data-stu-id="77207-116">The WSDL operation topics in this section provide an overview of what the operation does and operation request and response examples.</span></span> <span data-ttu-id="77207-117">Puede usar la información de versión proporcionada para determinar si las características que desea usar están disponibles en la versión del producto que está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="77207-117">You can use the version information provided to determine whether the features that you want to use are available in the product version that you are running.</span></span> <span data-ttu-id="77207-118">Los ejemplos de los temas de operación también ayudan a comprender la estructura del XML que se incluye en los mensajes SOAP que se envían a y desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="77207-118">The examples in the operation topics also help you to understand the structure of the XML that is included in the SOAP messages that are sent to and from the server.</span></span>
  
<span data-ttu-id="77207-119">En esta sección también se proporcionan ejemplos y descripciones de los mensajes que se usan para recuperar información de configuración de detección automática mediante el servicio Detección automática de SOAP.</span><span class="sxs-lookup"><span data-stu-id="77207-119">This section also provides examples and descriptions of the messages that are used to retrieve Autodiscover configuration information by using the SOAP Autodiscover service.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="77207-120">En esta sección</span><span class="sxs-lookup"><span data-stu-id="77207-120">In this section</span></span>
<span data-ttu-id="77207-121"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="77207-121"><a name="bk_InThisSection"> </a></span></span>

- [<span data-ttu-id="77207-122">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="77207-122">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
    
- [<span data-ttu-id="77207-123">Operación GetFederationInformation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="77207-123">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)
    
- [<span data-ttu-id="77207-124">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="77207-124">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
    
- [<span data-ttu-id="77207-125">Operación GetOrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="77207-125">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)
    
- [<span data-ttu-id="77207-126">Elementos XML de detección automática de SOAP para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="77207-126">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)
    
## <a name="see-also"></a><span data-ttu-id="77207-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="77207-127">See also</span></span>


- [<span data-ttu-id="77207-128">Referencia del servicio web de Detección automática para Exchange</span><span class="sxs-lookup"><span data-stu-id="77207-128">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="77207-129">Detección automática en Exchange</span><span class="sxs-lookup"><span data-stu-id="77207-129">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
- [<span data-ttu-id="77207-130">Usar autodetección para buscar puntos de conexión</span><span class="sxs-lookup"><span data-stu-id="77207-130">Use Autodiscover to find connection points</span></span>](https://msdn.microsoft.com/library/03896542-549b-4c45-973c-98f9025ea26c%28Office.15%29.aspx)
- [<span data-ttu-id="77207-131">Obtener la configuración de usuario de Exchange mediante el uso de detección automática</span><span class="sxs-lookup"><span data-stu-id="77207-131">Get user settings from Exchange by using Autodiscover</span></span>](https://msdn.microsoft.com/library/6d90c305-4802-4e18-8d52-f60349feaa8d%28Office.15%29.aspx)
- [<span data-ttu-id="77207-132">Obtener la configuración de dominio de un servidor de Exchange</span><span class="sxs-lookup"><span data-stu-id="77207-132">Get domain settings from an Exchange server</span></span>](https://msdn.microsoft.com/library/2f9acb81-5135-4f72-94e8-65c235d725e6%28Office.15%29.aspx)
- [<span data-ttu-id="77207-133">Empezar a usar los servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="77207-133">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

