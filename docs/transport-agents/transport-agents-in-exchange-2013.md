---
title: Agentes de transporte en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 36d63aa6-1b72-4670-b5c3-da685f3017cb
description: Obtenga información acerca de los agentes de transporte en Exchange 2013.
ms.openlocfilehash: 62fb259672c47242a57b939deb4887e1e5519e2a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461761"
---
# <a name="transport-agents-in-exchange"></a><span data-ttu-id="3c941-103">Agentes de transporte en Exchange</span><span class="sxs-lookup"><span data-stu-id="3c941-103">Transport agents in Exchange</span></span>
  
<span data-ttu-id="3c941-104">Exchange 2013 proporciona una biblioteca de clases que admiten la extensión del comportamiento de transporte de Exchange y habilitan la lectura, escritura y conversión de tipos de contenido.</span><span class="sxs-lookup"><span data-stu-id="3c941-104">Exchange 2013 provides a library of classes that support the extension of the Exchange transport behavior and enable the reading, writing, and converting of content types.</span></span> <span data-ttu-id="3c941-105">Puede usar estas clases para crear aplicaciones de transporte de Exchange que lean, escriban y procesen mensajes en la canalización de transporte.</span><span class="sxs-lookup"><span data-stu-id="3c941-105">You can use these classes to create Exchange transport applications that read, write, and process messages in the transport pipeline.</span></span>
  
## <a name="what-you-need-to-know-about-transport-agents"></a><span data-ttu-id="3c941-106">Lo que debe saber sobre los agentes de transporte</span><span class="sxs-lookup"><span data-stu-id="3c941-106">What you need to know about transport agents</span></span>

|<span data-ttu-id="3c941-107">Si está preguntando por...</span><span class="sxs-lookup"><span data-stu-id="3c941-107">If you're wondering about…</span></span>|<span data-ttu-id="3c941-108">Lea esto</span><span class="sxs-lookup"><span data-stu-id="3c941-108">Read this</span></span>|
|:-----|:-----|
|<span data-ttu-id="3c941-109">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="3c941-109">Availability</span></span>  <br/> |<span data-ttu-id="3c941-110">Los agentes de transporte están disponibles en las versiones de Exchange a partir de Exchange 2007.</span><span class="sxs-lookup"><span data-stu-id="3c941-110">Transport agents are available in versions of Exchange starting with Exchange 2007.</span></span> <span data-ttu-id="3c941-111">Los agentes de transporte no son compatibles con Office 365 o Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="3c941-111">Transport agents are not supported in Office 365 or Exchange Online.</span></span>  <br/> |
|<span data-ttu-id="3c941-112">Uso remoto</span><span class="sxs-lookup"><span data-stu-id="3c941-112">Remote usage</span></span>  <br/> |<span data-ttu-id="3c941-113">Los agentes de transporte se ejecutan en el servidor de Exchange y no admiten el uso remoto.</span><span class="sxs-lookup"><span data-stu-id="3c941-113">Transport agents run on the Exchange server and do not support remote usage.</span></span>  <br/> |
|<span data-ttu-id="3c941-114">Los idiomas admitidos</span><span class="sxs-lookup"><span data-stu-id="3c941-114">Languages supported</span></span>  <br/> |<span data-ttu-id="3c941-115">Puede usar cualquier lenguaje de .NET Framework para trabajar con agentes de transporte.</span><span class="sxs-lookup"><span data-stu-id="3c941-115">You can use any .NET Framework language to work with transport agents.</span></span>  <br/> |
|<span data-ttu-id="3c941-116">Las pruebas y las herramientas de depuración disponibles</span><span class="sxs-lookup"><span data-stu-id="3c941-116">Available test and debug tools</span></span>  <br/> |<span data-ttu-id="3c941-117">Use versiones de Visual Studio que empiecen con Visual Studio 2012 para depurar agentes de transporte.</span><span class="sxs-lookup"><span data-stu-id="3c941-117">Use versions of Visual Studio starting with Visual Studio 2012 to debug transport agents.</span></span>  <br/> |
|<span data-ttu-id="3c941-118">Métodos de implementación</span><span class="sxs-lookup"><span data-stu-id="3c941-118">Deployment methods</span></span>  <br/> |<span data-ttu-id="3c941-119">Puede instalar aplicaciones de agente de transporte mediante un script de [Shell de administración de Exchange](../management/exchange-management-shell.md) .</span><span class="sxs-lookup"><span data-stu-id="3c941-119">You can install transport agent applications by using an [Exchange Management Shell](../management/exchange-management-shell.md) script.</span></span>  <br/> |
   
## <a name="in-this-section"></a><span data-ttu-id="3c941-120">En esta sección</span><span class="sxs-lookup"><span data-stu-id="3c941-120">In this section</span></span>

- [<span data-ttu-id="3c941-121">API de agente de transporte nuevas y actualizadas en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="3c941-121">New and updated transport agent APIs in Exchange 2013</span></span>](new-and-updated-transport-agent-apis-in-exchange-2013.md)
    
- [<span data-ttu-id="3c941-122">Ejemplos de código de agente de transporte para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="3c941-122">Transport agent code samples for Exchange 2013</span></span>](transport-agent-code-samples-for-exchange-2013.md)
    
- [<span data-ttu-id="3c941-123">Conceptos del agente de transporte en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="3c941-123">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)
    
- [<span data-ttu-id="3c941-124">Leer y modificar mensajes en la canalización de transporte de Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="3c941-124">Reading and modifying messages in the Exchange 2013 transport pipeline</span></span>](reading-and-modifying-messages-in-the-exchange-2013-transport-pipeline.md)
    
- [<span data-ttu-id="3c941-125">Crear agentes de transporte para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="3c941-125">Creating transport agents for Exchange 2013</span></span>](creating-transport-agents-for-exchange-2013.md)
    
- [<span data-ttu-id="3c941-126">Referencia del agente de transporte para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="3c941-126">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)
    
## <a name="see-also"></a><span data-ttu-id="3c941-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c941-127">See also</span></span>

- [<span data-ttu-id="3c941-128">Desarrollo de Exchange y Exchange Online</span><span class="sxs-lookup"><span data-stu-id="3c941-128">Exchange Online and Exchange development</span></span>](../exchange-server-development.md)    
- [<span data-ttu-id="3c941-129">Explorar la API administrada de EWS, EWS y servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="3c941-129">Explore the EWS Managed API, EWS, and web services in Exchange</span></span>](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)   
- [<span data-ttu-id="3c941-130">Copia de seguridad y restauración para Exchange</span><span class="sxs-lookup"><span data-stu-id="3c941-130">Backup and restore for Exchange</span></span>](../backup-restore/backup-and-restore-for-exchange-2013.md) 
    

