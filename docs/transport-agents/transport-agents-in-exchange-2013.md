---
title: Los agentes de transporte en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 36d63aa6-1b72-4670-b5c3-da685f3017cb
description: Obtenga información acerca de los agentes de transporte en Exchange 2013.
ms.openlocfilehash: 1a28ae79e2a7e338ddd6cb1f6961dd14a980b56e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763377"
---
# <a name="transport-agents-in-exchange"></a><span data-ttu-id="4d353-103">Los agentes de transporte en Exchange</span><span class="sxs-lookup"><span data-stu-id="4d353-103">Transport agents in Exchange</span></span>
  
<span data-ttu-id="4d353-104">Exchange 2013 proporciona una biblioteca de clases que admiten la extensión del comportamiento de transporte de Exchange y habilitar la lectura, escritura y la conversión de tipos de contenido.</span><span class="sxs-lookup"><span data-stu-id="4d353-104">Exchange 2013 provides a library of classes that support the extension of the Exchange transport behavior and enable the reading, writing, and converting of content types.</span></span> <span data-ttu-id="4d353-105">Puede usar estas clases para crear aplicaciones de transporte de Exchange que leerán, escribir y procesan los mensajes en la canalización de transporte.</span><span class="sxs-lookup"><span data-stu-id="4d353-105">You can use these classes to create Exchange transport applications that read, write, and process messages in the transport pipeline.</span></span>
  
## <a name="what-you-need-to-know-about-transport-agents"></a><span data-ttu-id="4d353-106">Lo que necesita saber acerca de los agentes de transporte</span><span class="sxs-lookup"><span data-stu-id="4d353-106">What you need to know about transport agents</span></span>

|<span data-ttu-id="4d353-107">Si se pregunta acerca de...</span><span class="sxs-lookup"><span data-stu-id="4d353-107">If you're wondering about…</span></span>|<span data-ttu-id="4d353-108">Lea esto</span><span class="sxs-lookup"><span data-stu-id="4d353-108">Read this</span></span>|
|:-----|:-----|
|<span data-ttu-id="4d353-109">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="4d353-109">Availability</span></span>  <br/> |<span data-ttu-id="4d353-110">Los agentes de transporte están disponibles en las versiones de Exchange a partir de Exchange 2007.</span><span class="sxs-lookup"><span data-stu-id="4d353-110">Transport agents are available in versions of Exchange starting with Exchange 2007.</span></span> <span data-ttu-id="4d353-111">Los agentes de transporte no se admiten en Office 365 o Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="4d353-111">Transport agents are not supported in Office 365 or Exchange Online.</span></span>  <br/> |
|<span data-ttu-id="4d353-112">Uso remoto</span><span class="sxs-lookup"><span data-stu-id="4d353-112">Remote usage</span></span>  <br/> |<span data-ttu-id="4d353-113">Los agentes de transporte se ejecutan en el servidor de Exchange y no admiten el uso remoto.</span><span class="sxs-lookup"><span data-stu-id="4d353-113">Transport agents run on the Exchange server and do not support remote usage.</span></span>  <br/> |
|<span data-ttu-id="4d353-114">Los idiomas admitidos</span><span class="sxs-lookup"><span data-stu-id="4d353-114">Languages supported</span></span>  <br/> |<span data-ttu-id="4d353-115">Puede usar cualquier lenguaje de .NET Framework para trabajar con los agentes de transporte.</span><span class="sxs-lookup"><span data-stu-id="4d353-115">You can use any .NET Framework language to work with transport agents.</span></span>  <br/> |
|<span data-ttu-id="4d353-116">Las pruebas y las herramientas de depuración disponibles</span><span class="sxs-lookup"><span data-stu-id="4d353-116">Available test and debug tools</span></span>  <br/> |<span data-ttu-id="4d353-117">Usar versiones de Visual Studio desde Visual Studio 2012 para depurar a los agentes de transporte.</span><span class="sxs-lookup"><span data-stu-id="4d353-117">Use versions of Visual Studio starting with Visual Studio 2012 to debug transport agents.</span></span>  <br/> |
|<span data-ttu-id="4d353-118">Métodos de implementación</span><span class="sxs-lookup"><span data-stu-id="4d353-118">Deployment methods</span></span>  <br/> |<span data-ttu-id="4d353-119">Puede instalar aplicaciones de agente de transporte mediante un script de [Shell de administración de Exchange](../management/exchange-management-shell.md) .</span><span class="sxs-lookup"><span data-stu-id="4d353-119">You can install transport agent applications by using an [Exchange Management Shell](../management/exchange-management-shell.md) script.</span></span>  <br/> |
   
## <a name="in-this-section"></a><span data-ttu-id="4d353-120">En esta sección</span><span class="sxs-lookup"><span data-stu-id="4d353-120">In this section</span></span>

- [<span data-ttu-id="4d353-121">Agente de transporte nuevos y actualizados API en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="4d353-121">New and updated transport agent APIs in Exchange 2013</span></span>](new-and-updated-transport-agent-apis-in-exchange-2013.md)
    
- [<span data-ttu-id="4d353-122">Ejemplos de código de agente para Exchange 2013 de transporte</span><span class="sxs-lookup"><span data-stu-id="4d353-122">Transport agent code samples for Exchange 2013</span></span>](transport-agent-code-samples-for-exchange-2013.md)
    
- [<span data-ttu-id="4d353-123">Conceptos de agente en Exchange 2013 de transporte</span><span class="sxs-lookup"><span data-stu-id="4d353-123">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)
    
- [<span data-ttu-id="4d353-124">Leer y modificar los mensajes en la canalización de transporte de Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="4d353-124">Reading and modifying messages in the Exchange 2013 transport pipeline</span></span>](reading-and-modifying-messages-in-the-exchange-2013-transport-pipeline.md)
    
- [<span data-ttu-id="4d353-125">Creación de los agentes de transporte de Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="4d353-125">Creating transport agents for Exchange 2013</span></span>](creating-transport-agents-for-exchange-2013.md)
    
- [<span data-ttu-id="4d353-126">Referencia de agente de transporte de Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="4d353-126">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)
    
## <a name="see-also"></a><span data-ttu-id="4d353-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d353-127">See also</span></span>

- [<span data-ttu-id="4d353-128">Desarrollo de Exchange y Exchange Online</span><span class="sxs-lookup"><span data-stu-id="4d353-128">Exchange Online and Exchange development</span></span>](../exchange-server-development.md)    
- [<span data-ttu-id="4d353-129">Explore la API administrada de EWS, EWS y servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="4d353-129">Explore the EWS Managed API, EWS, and web services in Exchange</span></span>](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)   
- [<span data-ttu-id="4d353-130">Copia de seguridad y restauración para Exchange</span><span class="sxs-lookup"><span data-stu-id="4d353-130">Backup and restore for Exchange</span></span>](../backup-restore/backup-and-restore-for-exchange-2013.md) 
    

