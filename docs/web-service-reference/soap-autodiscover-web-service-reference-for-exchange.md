---
title: Referencia de servicio web de detección automática de SOAP para Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 61c21ea9-7fea-4f56-8ada-bf80e1e6b074
description: Busque información de referencia para el servicio Detección automática de SOAP en Exchange.
ms.openlocfilehash: 1cb24a8667c71028f3dead78d9fa533dc9547a64
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837514"
---
# <a name="soap-autodiscover-web-service-reference-for-exchange"></a><span data-ttu-id="13c7b-103">Referencia de servicio web de detección automática de SOAP para Exchange</span><span class="sxs-lookup"><span data-stu-id="13c7b-103">SOAP Autodiscover web service reference for Exchange</span></span>

<span data-ttu-id="13c7b-104">Busque información de referencia para el servicio Detección automática de SOAP en Exchange.</span><span class="sxs-lookup"><span data-stu-id="13c7b-104">Find reference information for the SOAP Autodiscover service in Exchange.</span></span>
  
<span data-ttu-id="13c7b-105">El servicio Detección automática proporciona la información de configuración que la aplicación se usa para crear una conexión a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="13c7b-105">The Autodiscover service provides the configuration information that your application uses to create a connection to an Exchange server.</span></span> <span data-ttu-id="13c7b-106">Puede usar el servicio Detección automática de SOAP para enviar mensajes entre la aplicación cliente y el servidor de Exchange para buscar la configuración de que la aplicación usará para conectarse a Exchange.</span><span class="sxs-lookup"><span data-stu-id="13c7b-106">You can use the SOAP Autodiscover service to send messages between the client application and the Exchange server to locate the settings the application will use to connect to Exchange.</span></span> <span data-ttu-id="13c7b-107">A diferencia del servicio de detección automática de POX, permite que el servicio Detección automática de SOAP para solicitudes de detección automática por lotes para la configuración de muchos de los usuarios y un mayor control sobre qué configuración se devuelve en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="13c7b-107">Unlike the POX Autodiscover service, the SOAP Autodiscover service allows for batched Autodiscover requests for many users' settings and more granular control over which settings are returned in the response.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="13c7b-108">Para los clientes que estén destinados a las versiones de Exchange Server 2010 a partir de Exchange, se recomienda que use el servicio de detección automática de SOAP (en lugar del servicio de detección automática de POX).</span><span class="sxs-lookup"><span data-stu-id="13c7b-108">For clients that target versions of Exchange starting with Exchange Server 2010, we recommend that you use the SOAP Autodiscover service (instead of the POX Autodiscover service).</span></span> <span data-ttu-id="13c7b-109">Los clientes que estén destinados a Exchange 2007 deben usar el servicio Detección automática POX.</span><span class="sxs-lookup"><span data-stu-id="13c7b-109">Clients that target Exchange 2007 have to use the POX Autodiscover service.</span></span> <span data-ttu-id="13c7b-110">Se recomienda que los clientes que utilicen .NET Framework usan la API administrada de EWS porque contiene a un cliente de detección automática de SOAP robusto y probado.</span><span class="sxs-lookup"><span data-stu-id="13c7b-110">We recommend that clients that use the .NET Framework use the EWS Managed API because it contains a robust and well-tested SOAP Autodiscover client.</span></span> <span data-ttu-id="13c7b-111">Para obtener más información acerca de la API administrada de EWS, vea [Introducción a las aplicaciones cliente de API administrada de EWS](http://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="13c7b-111">For more information about the EWS Managed API, see [Get started with EWS Managed API client applications](http://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx).</span></span> 
  
<span data-ttu-id="13c7b-112">En esta sección se proporciona información acerca de los elementos XML que se envían entre el cliente y el servidor durante el redireccionamiento de la solicitud de detección automática de SOAP y la configuración del usuario que se devuelve en una respuesta.</span><span class="sxs-lookup"><span data-stu-id="13c7b-112">This section provides information about the XML elements that are sent between the client and server during SOAP Autodiscover request redirections and the user settings that are returned in a response.</span></span> <span data-ttu-id="13c7b-113">La referencia de elemento XML contiene resúmenes de los elementos que representan y una descripción de los posibles jerarquías de elementos que contienen el elemento.</span><span class="sxs-lookup"><span data-stu-id="13c7b-113">The XML element reference contains summaries of what the elements represent and a description of the potential element hierarchies that contain the element.</span></span> 
  
<span data-ttu-id="13c7b-114">Los artículos de esta sección describen las instancias XML que se envían entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="13c7b-114">The articles in this section describe the XML instances that are sent between the client and server.</span></span> <span data-ttu-id="13c7b-115">El esquema que describe estos elementos puede encontrarse en el directorio virtual del servidor que hospeda el servicio de detección automática de SOAP.</span><span class="sxs-lookup"><span data-stu-id="13c7b-115">The schema that describes these elements can be found in the virtual directory of the server that hosts the SOAP Autodiscover service.</span></span>
  
<span data-ttu-id="13c7b-116">La operación WSDL temas de esta sección proporcionan que una visión general de qué es la operación y ejemplos de solicitud y respuesta de la operación.</span><span class="sxs-lookup"><span data-stu-id="13c7b-116">The WSDL operation topics in this section provide an overview of what the operation does and operation request and response examples.</span></span> <span data-ttu-id="13c7b-117">Puede usar la información de versión proporcionada para determinar si las características que desea utilizar están disponibles en la versión del producto que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="13c7b-117">You can use the version information provided to determine whether the features that you want to use are available in the product version that you are running.</span></span> <span data-ttu-id="13c7b-118">En los ejemplos de los temas de la operación también le ayudarán a comprender la estructura de XML que se incluye en los mensajes SOAP que se envían a y desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="13c7b-118">The examples in the operation topics also help you to understand the structure of the XML that is included in the SOAP messages that are sent to and from the server.</span></span>
  
<span data-ttu-id="13c7b-119">En esta sección también proporciona ejemplos y descripciones de los mensajes que se usan para recuperar información de configuración de detección automática mediante el servicio de detección automática de SOAP.</span><span class="sxs-lookup"><span data-stu-id="13c7b-119">This section also provides examples and descriptions of the messages that are used to retrieve Autodiscover configuration information by using the SOAP Autodiscover service.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="13c7b-120">En esta sección</span><span class="sxs-lookup"><span data-stu-id="13c7b-120">In this section</span></span>
<span data-ttu-id="13c7b-121"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="13c7b-121"></span></span>

- [<span data-ttu-id="13c7b-122">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="13c7b-122">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
    
- [<span data-ttu-id="13c7b-123">Operación GetFederationInformation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="13c7b-123">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)
    
- [<span data-ttu-id="13c7b-124">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="13c7b-124">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
    
- [<span data-ttu-id="13c7b-125">Operación GetOrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="13c7b-125">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)
    
- [<span data-ttu-id="13c7b-126">Elementos de Autodiscover XML SOAP para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="13c7b-126">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)
    
## <a name="see-also"></a><span data-ttu-id="13c7b-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="13c7b-127">See also</span></span>


- [<span data-ttu-id="13c7b-128">Referencia de servicio web de detección automática para Exchange</span><span class="sxs-lookup"><span data-stu-id="13c7b-128">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="13c7b-129">Detección automática de Exchange</span><span class="sxs-lookup"><span data-stu-id="13c7b-129">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
- [<span data-ttu-id="13c7b-130">Usar detección automática para buscar puntos de conexión</span><span class="sxs-lookup"><span data-stu-id="13c7b-130">Use Autodiscover to find connection points</span></span>](http://msdn.microsoft.com/library/03896542-549b-4c45-973c-98f9025ea26c%28Office.15%29.aspx)
- [<span data-ttu-id="13c7b-131">Obtener la configuración de usuario de Exchange mediante el uso de detección automática</span><span class="sxs-lookup"><span data-stu-id="13c7b-131">Get user settings from Exchange by using Autodiscover</span></span>](http://msdn.microsoft.com/library/6d90c305-4802-4e18-8d52-f60349feaa8d%28Office.15%29.aspx)
- [<span data-ttu-id="13c7b-132">Obtener la configuración de dominio de un servidor de Exchange</span><span class="sxs-lookup"><span data-stu-id="13c7b-132">Get domain settings from an Exchange server</span></span>](http://msdn.microsoft.com/library/2f9acb81-5135-4f72-94e8-65c235d725e6%28Office.15%29.aspx)
- [<span data-ttu-id="13c7b-133">Empezar a utilizar servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="13c7b-133">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

