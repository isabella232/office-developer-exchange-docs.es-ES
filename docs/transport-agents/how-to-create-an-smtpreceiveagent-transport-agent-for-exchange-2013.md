---
title: Crear un agente de transporte de SmtpReceiveAgent para Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cdc7c462-74a7-49d6-95b2-155d783840e9
description: Descubra cómo crear un agente de transporte de SmtpReceiveAgent personalizado para usarlo con Exchange 2013.
ms.openlocfilehash: 5ba021d02849ffc7e125029f0fd18ebf14c3f8da
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459142"
---
# <a name="create-an-smtpreceiveagent-transport-agent-for-exchange-2013"></a><span data-ttu-id="339ea-103">Crear un agente de transporte de SmtpReceiveAgent para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="339ea-103">Create an SmtpReceiveAgent transport agent for Exchange 2013</span></span>

<span data-ttu-id="339ea-104">Descubra cómo crear un agente de transporte de SmtpReceiveAgent personalizado para usarlo con Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="339ea-104">Find out how to create a custom SmtpReceiveAgent transport agent to use with Exchange 2013.</span></span>
  
<span data-ttu-id="339ea-105">**Se aplica a:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="339ea-105">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="339ea-106">Fragmentos de código y aplicaciones de ejemplo relacionados:</span><span class="sxs-lookup"><span data-stu-id="339ea-106">Related code snippets and sample apps:</span></span>

- [<span data-ttu-id="339ea-107">Exchange 2013: crear un agente de transporte de conversión de cuerpo</span><span class="sxs-lookup"><span data-stu-id="339ea-107">Exchange 2013: Build a body conversion transport agent</span></span>](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0)
  
<span data-ttu-id="339ea-108">Las clases [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) y [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) permiten ampliar el comportamiento del servicio de transporte front-end en un servidor de acceso de cliente o el servicio de transporte en un servidor de buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="339ea-108">The [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) and [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) classes enable you to extend the behavior of the Front End Transport service on a Client Access Server or the Transport service on a Mailbox server.</span></span> <span data-ttu-id="339ea-109">Puede usar estas clases para implementar agentes de transporte diseñados para responder a los mensajes a medida que entran en la organización.</span><span class="sxs-lookup"><span data-stu-id="339ea-109">You can use these classes to implement transport agents that are designed to respond to messages as they come into your organization.</span></span> 
  
<span data-ttu-id="339ea-110">Las clases [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) y [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) incluyen los eventos que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="339ea-110">The [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) and [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) classes include the events listed in the following table.</span></span> 
  
<span data-ttu-id="339ea-111">**Tabla 1. Eventos de la clase SmtpReceiveAgent**</span><span class="sxs-lookup"><span data-stu-id="339ea-111">**Table 1. SmtpReceiveAgent class events**</span></span>

|<span data-ttu-id="339ea-112">**Event**</span><span class="sxs-lookup"><span data-stu-id="339ea-112">**Event**</span></span>|<span data-ttu-id="339ea-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="339ea-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="339ea-114">OnAuthCommand</span><span class="sxs-lookup"><span data-stu-id="339ea-114">OnAuthCommand</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnAuthCommand.aspx) <br/> |<span data-ttu-id="339ea-115">Se usa cuando el agente requiere información que se proporciona únicamente en el comando **auth** de SMTP, como un agente que acepta o rechaza los intentos de entregar un mensaje en función del tipo de método de autenticación usado.</span><span class="sxs-lookup"><span data-stu-id="339ea-115">Use when your agent requires information that is provided only in the SMTP **AUTH** command, such as an agent that accepts or rejects attempts to deliver a message based on the type of authentication method used.</span></span>  <br/> |
|[<span data-ttu-id="339ea-116">OnConnect</span><span class="sxs-lookup"><span data-stu-id="339ea-116">OnConnect</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnConnect.aspx) <br/> |<span data-ttu-id="339ea-117">Se usa cuando el agente requiere información que se proporciona únicamente cuando se abre una conexión a través de SMTP para el servicio de transporte front-end, como un agente que realiza una acción basada en la dirección o el dominio del servidor SMTP remoto.</span><span class="sxs-lookup"><span data-stu-id="339ea-117">Use when your agent requires information that is provided only when a connection is opened via SMTP to the Front End Transport service, such as an agent that performs an action based on the address or domain of the remote SMTP server.</span></span>  <br/> |
|[<span data-ttu-id="339ea-118">OnDataCommand</span><span class="sxs-lookup"><span data-stu-id="339ea-118">OnDataCommand</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDataCommand.aspx) <br/> |<span data-ttu-id="339ea-119">Use este evento cuando su agente requiera la información que se proporciona en el comando de **datos** SMTP.</span><span class="sxs-lookup"><span data-stu-id="339ea-119">Use this event when your agent requires information that is provided in the SMTP **DATA** command.</span></span>  <br/> |
|[<span data-ttu-id="339ea-120">OnDisconnect</span><span class="sxs-lookup"><span data-stu-id="339ea-120">OnDisconnect</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDisconnect.aspx) <br/> |<span data-ttu-id="339ea-121">Se usa cuando el agente requiere información que está disponible en el momento de la desconexión, como la fecha y la hora actuales, a fin de realizar cálculos de tiempo.</span><span class="sxs-lookup"><span data-stu-id="339ea-121">Use when your agent requires information that is available at the time of disconnection, such as the current date and time, in order to perform time calculations.</span></span>  <br/> |
|[<span data-ttu-id="339ea-122">OnEhloCommand</span><span class="sxs-lookup"><span data-stu-id="339ea-122">OnEhloCommand</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEhloCommand.aspx) <br/> |<span data-ttu-id="339ea-123">Se usa cuando el agente requiere información que se proporciona en el comando SMTP **EHLO** ; por ejemplo, si el agente acepta o rechaza mensajes en función de la identidad proporcionada en el comando **EHLO** .</span><span class="sxs-lookup"><span data-stu-id="339ea-123">Use when your agent requires information that is provided in the SMTP **EHLO** command; for example, if your agent accepts or rejects messages based on the identity provided in the **EHLO** command.</span></span>  <br/> |
|[<span data-ttu-id="339ea-124">OnEndOfAuthentication</span><span class="sxs-lookup"><span data-stu-id="339ea-124">OnEndOfAuthentication</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfAuthentication.aspx) <br/> |<span data-ttu-id="339ea-125">Se usa cuando el agente requiere información que está disponible después de que el servidor remoto complete el proceso de autenticación; por ejemplo, para un agente que realiza una acción en un mensaje en función de la información de autenticación proporcionada por el servidor SMTP remoto o el cliente.</span><span class="sxs-lookup"><span data-stu-id="339ea-125">Use when your agent requires information that is available after the remote server completes the authentication process; for example, for an agent that performs an action on a message based on the authentication information provided by the remote SMTP server or client.</span></span>  <br/> |
|[<span data-ttu-id="339ea-126">OnEndOfData</span><span class="sxs-lookup"><span data-stu-id="339ea-126">OnEndOfData</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) <br/> |<span data-ttu-id="339ea-127">Se usa cuando el agente debe realizar una acción basándose en los datos que están disponibles en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="339ea-127">Use when your agent must perform an action based on data that is available in the message.</span></span> <span data-ttu-id="339ea-128">Este evento no se desencadenará en el servicio de transporte de front-end.</span><span class="sxs-lookup"><span data-stu-id="339ea-128">This event will not fire on the Front End Transport service.</span></span> <span data-ttu-id="339ea-129">Si el agente de transporte tiene que usar este evento, deberá instalarlo en un servidor de buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="339ea-129">If your transport agent has to use this event, you have to install it on a Mailbox server.</span></span>  <br/> |
|[<span data-ttu-id="339ea-130">OnEndOfHeaders</span><span class="sxs-lookup"><span data-stu-id="339ea-130">OnEndOfHeaders</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) <br/> |<span data-ttu-id="339ea-131">Se usa cuando el agente debe realizar una acción basándose en la información que está disponible en los encabezados del mensaje enviado.</span><span class="sxs-lookup"><span data-stu-id="339ea-131">Use when your agent must perform an action based on information that is available in the headers of the submitted message.</span></span>  <br/> |
   
## <a name="creating-a-custom-smtpreceiveagent-transport-agent"></a><span data-ttu-id="339ea-132">Creación de un agente de transporte de SmtpReceiveAgent personalizado</span><span class="sxs-lookup"><span data-stu-id="339ea-132">Creating a custom SmtpReceiveAgent transport agent</span></span>

<span data-ttu-id="339ea-133">El siguiente procedimiento describe cómo crear un agente de transporte de SmtpReceiveAgent personalizado.</span><span class="sxs-lookup"><span data-stu-id="339ea-133">The following procedure describes how to create a custom SmtpReceiveAgent transport agent.</span></span> 
  
### <a name="to-create-the-transport-agent"></a><span data-ttu-id="339ea-134">Para crear el agente de transporte</span><span class="sxs-lookup"><span data-stu-id="339ea-134">To create the transport agent</span></span>

1. <span data-ttu-id="339ea-135">Agregue referencias a los espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="339ea-135">Add references to the namespaces.</span></span>
    
   ```cs
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Smtp;
      using Microsoft.Exchange.Data.Transport.Email;
      using Microsoft.Exchange.Data.TextConverters;
  
   ```

   <span data-ttu-id="339ea-136">Puede encontrar estos espacios de nombres en su servidor Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="339ea-136">You can find these namespaces on your Exchange 2013 server.</span></span> <span data-ttu-id="339ea-137">Al agregar una referencia a estos espacios de nombres, tendrá acceso a los miembros de [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) , así como a otras clases usadas en la muestra de [Exchange 2013: Build a Body Conversion Transport Agent](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0) .</span><span class="sxs-lookup"><span data-stu-id="339ea-137">When you add a reference to these namespaces, you will have access to the [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) members as well as other classes used in the [Exchange 2013: Build a body conversion transport agent](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0) sample.</span></span> 
    
2. <span data-ttu-id="339ea-138">Implemente la clase derivada para la clase [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) .</span><span class="sxs-lookup"><span data-stu-id="339ea-138">Implement the derived class for the [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) class.</span></span> 
    
   ```cs
      public class BodyConversionFactory : SmtpReceiveAgentFactory
      {
          /// <summary>
          /// Create a new BodyConversion
          /// </summary>
          /// <param name="server">Exchange server</param>
          /// <returns>A new BodyConversion</returns>
          public override SmtpReceiveAgent CreateAgent(SmtpServer server)
          {
              return new BodyConversion();
          }
      }
  
   ```

   <span data-ttu-id="339ea-139">Este código creará una instancia de la clase derivada y reemplazará el método **CreateAgent** para crear una instancia del nuevo agente personalizado.</span><span class="sxs-lookup"><span data-stu-id="339ea-139">This code will instantiate the derived class and override the **CreateAgent** method to create an instance of your new custom agent.</span></span> 
    
3. <span data-ttu-id="339ea-140">Definir el agente.</span><span class="sxs-lookup"><span data-stu-id="339ea-140">Define your agent.</span></span>
    
   ```cs
     public class BodyConversion : SmtpReceiveAgent
      {
          // Your custom code goes here
          /// <summary>
          /// The constructor registers an end of data event handler.
          /// </summary>
          public BodyConversion()
          {
              Debug.WriteLine("[BodyConversion] Agent constructor");
              this.OnEndOfData += new EndOfDataEventHandler(this.OnEndOfDataHandler);
          }
      }
  
   ```

   <span data-ttu-id="339ea-141">Después de definir la clase del agente, puede agregar su funcionalidad personalizada.</span><span class="sxs-lookup"><span data-stu-id="339ea-141">After you define your agent class, you can add your custom functionality.</span></span> <span data-ttu-id="339ea-142">En este ejemplo, el evento [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) se redirige a su controlador de eventos personalizado.</span><span class="sxs-lookup"><span data-stu-id="339ea-142">In this example, the [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) event is redirected to your custom event handler.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="339ea-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="339ea-143">See also</span></span>

- [<span data-ttu-id="339ea-144">Conceptos del agente de transporte en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="339ea-144">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)    
- [<span data-ttu-id="339ea-145">Referencia del agente de transporte para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="339ea-145">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)    
- [<span data-ttu-id="339ea-146">SmtpReceiveAgentFactory</span><span class="sxs-lookup"><span data-stu-id="339ea-146">SmtpReceiveAgentFactory</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)    
- [<span data-ttu-id="339ea-147">SmtpReceiveAgent</span><span class="sxs-lookup"><span data-stu-id="339ea-147">SmtpReceiveAgent</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)
    

