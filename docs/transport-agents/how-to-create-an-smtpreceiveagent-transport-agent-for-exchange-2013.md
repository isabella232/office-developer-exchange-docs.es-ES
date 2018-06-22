---
title: Crear a un agente de transporte SmtpReceiveAgent para Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cdc7c462-74a7-49d6-95b2-155d783840e9
description: Encuentre información acerca de cómo crear un agente de transporte SmtpReceiveAgent personalizado para usar con Exchange 2013.
ms.openlocfilehash: a74d5baae6334c5e17acb6335206964b48f320e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763473"
---
# <a name="create-an-smtpreceiveagent-transport-agent-for-exchange-2013"></a><span data-ttu-id="b6e9d-103">Crear a un agente de transporte SmtpReceiveAgent para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="b6e9d-103">Create an SmtpReceiveAgent transport agent for Exchange 2013</span></span>

<span data-ttu-id="b6e9d-104">Encuentre información acerca de cómo crear un agente de transporte SmtpReceiveAgent personalizado para usar con Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="b6e9d-104">Find out how to create a custom SmtpReceiveAgent transport agent to use with Exchange 2013.</span></span>
  
<span data-ttu-id="b6e9d-105">**Se aplica a:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="b6e9d-105">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="b6e9d-106">Aplicaciones de ejemplo y fragmentos de código relacionados:</span><span class="sxs-lookup"><span data-stu-id="b6e9d-106">Related code snippets and sample apps:</span></span>

- [<span data-ttu-id="b6e9d-107">Exchange 2013: Crear a un agente de transporte de conversión de cuerpo</span><span class="sxs-lookup"><span data-stu-id="b6e9d-107">Exchange 2013: Build a body conversion transport agent</span></span>](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0)
  
<span data-ttu-id="b6e9d-108">Las clases [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) y [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) permiten ampliar el comportamiento del servicio de transporte Front-End en un servidor de acceso de cliente o el servicio de transporte en un servidor de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="b6e9d-108">The [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) and [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) classes enable you to extend the behavior of the Front End Transport service on a Client Access Server or the Transport service on a Mailbox server.</span></span> <span data-ttu-id="b6e9d-109">Puede utilizar estas clases para implementar a los agentes de transporte que están diseñados para responder a los mensajes según entran en la organización.</span><span class="sxs-lookup"><span data-stu-id="b6e9d-109">You can use these classes to implement transport agents that are designed to respond to messages as they come into your organization.</span></span> 
  
<span data-ttu-id="b6e9d-110">Las clases [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) y [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) incluyen los eventos que aparecen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="b6e9d-110">The [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) and [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) classes include the events listed in the following table.</span></span> 
  
<span data-ttu-id="b6e9d-111">**La tabla 1. Eventos de clase SmtpReceiveAgent**</span><span class="sxs-lookup"><span data-stu-id="b6e9d-111">**Table 1. SmtpReceiveAgent class events**</span></span>

|<span data-ttu-id="b6e9d-112">**Evento**</span><span class="sxs-lookup"><span data-stu-id="b6e9d-112">**Event**</span></span>|<span data-ttu-id="b6e9d-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b6e9d-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b6e9d-114">OnAuthCommand</span><span class="sxs-lookup"><span data-stu-id="b6e9d-114">OnAuthCommand</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnAuthCommand.aspx) <br/> |<span data-ttu-id="b6e9d-115">Se usa cuando el agente requiere información que sólo se proporciona en el comando **AUTH** de SMTP, como un agente que acepta o rechaza intenta entregar un mensaje en función del tipo de método de autenticación usado.</span><span class="sxs-lookup"><span data-stu-id="b6e9d-115">Use when your agent requires information that is provided only in the SMTP **AUTH** command, such as an agent that accepts or rejects attempts to deliver a message based on the type of authentication method used.</span></span>  <br/> |
|[<span data-ttu-id="b6e9d-116">OnConnect</span><span class="sxs-lookup"><span data-stu-id="b6e9d-116">OnConnect</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnConnect.aspx) <br/> |<span data-ttu-id="b6e9d-117">Se utiliza cuando el agente requiere información que se proporciona únicamente cuando se abre una conexión a través de SMTP para el servicio de transporte Front-End, como un agente que lleva a cabo una acción basada en la dirección o el dominio del servidor SMTP remoto.</span><span class="sxs-lookup"><span data-stu-id="b6e9d-117">Use when your agent requires information that is provided only when a connection is opened via SMTP to the Front End Transport service, such as an agent that performs an action based on the address or domain of the remote SMTP server.</span></span>  <br/> |
|[<span data-ttu-id="b6e9d-118">OnDataCommand</span><span class="sxs-lookup"><span data-stu-id="b6e9d-118">OnDataCommand</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDataCommand.aspx) <br/> |<span data-ttu-id="b6e9d-119">Utilice este evento cuando el agente requiere información que se proporciona en el comando SMTP **datos** .</span><span class="sxs-lookup"><span data-stu-id="b6e9d-119">Use this event when your agent requires information that is provided in the SMTP **DATA** command.</span></span>  <br/> |
|[<span data-ttu-id="b6e9d-120">OnDisconnect</span><span class="sxs-lookup"><span data-stu-id="b6e9d-120">OnDisconnect</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDisconnect.aspx) <br/> |<span data-ttu-id="b6e9d-121">Se utiliza cuando el agente requiere información que está disponible en el momento de desconexión, como la fecha y hora actuales, con el fin de realizar los cálculos de tiempo.</span><span class="sxs-lookup"><span data-stu-id="b6e9d-121">Use when your agent requires information that is available at the time of disconnection, such as the current date and time, in order to perform time calculations.</span></span>  <br/> |
|[<span data-ttu-id="b6e9d-122">OnEhloCommand</span><span class="sxs-lookup"><span data-stu-id="b6e9d-122">OnEhloCommand</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEhloCommand.aspx) <br/> |<span data-ttu-id="b6e9d-123">Se usa cuando el agente requiere información que se proporciona en el comando SMTP **EHLO** ; Por ejemplo, si el agente acepta o rechaza mensajes en función de la identidad proporcionada en el comando **EHLO** .</span><span class="sxs-lookup"><span data-stu-id="b6e9d-123">Use when your agent requires information that is provided in the SMTP **EHLO** command; for example, if your agent accepts or rejects messages based on the identity provided in the **EHLO** command.</span></span>  <br/> |
|[<span data-ttu-id="b6e9d-124">OnEndOfAuthentication</span><span class="sxs-lookup"><span data-stu-id="b6e9d-124">OnEndOfAuthentication</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfAuthentication.aspx) <br/> |<span data-ttu-id="b6e9d-125">Se usa cuando el agente requiere información que está disponible después de que el servidor remoto finaliza el proceso de autenticación; Por ejemplo, un agente que realiza una acción en un mensaje en función de la información de autenticación proporcionada por el servidor SMTP remoto o el cliente.</span><span class="sxs-lookup"><span data-stu-id="b6e9d-125">Use when your agent requires information that is available after the remote server completes the authentication process; for example, for an agent that performs an action on a message based on the authentication information provided by the remote SMTP server or client.</span></span>  <br/> |
|[<span data-ttu-id="b6e9d-126">OnEndOfData</span><span class="sxs-lookup"><span data-stu-id="b6e9d-126">OnEndOfData</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) <br/> |<span data-ttu-id="b6e9d-127">Se utiliza cuando el agente debe llevar a cabo una acción basándose en los datos que está disponibles en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="b6e9d-127">Use when your agent must perform an action based on data that is available in the message.</span></span> <span data-ttu-id="b6e9d-128">Este evento no se desencadenará en el servicio de transporte Front-End.</span><span class="sxs-lookup"><span data-stu-id="b6e9d-128">This event will not fire on the Front End Transport service.</span></span> <span data-ttu-id="b6e9d-129">Si el agente de transporte tiene que usar este evento, se debe instalar en un servidor de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="b6e9d-129">If your transport agent has to use this event, you have to install it on a Mailbox server.</span></span>  <br/> |
|[<span data-ttu-id="b6e9d-130">OnEndOfHeaders</span><span class="sxs-lookup"><span data-stu-id="b6e9d-130">OnEndOfHeaders</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) <br/> |<span data-ttu-id="b6e9d-131">Se utiliza cuando el agente debe llevar a cabo una acción según la información que está disponible en los encabezados del mensaje enviado.</span><span class="sxs-lookup"><span data-stu-id="b6e9d-131">Use when your agent must perform an action based on information that is available in the headers of the submitted message.</span></span>  <br/> |
   
## <a name="creating-a-custom-smtpreceiveagent-transport-agent"></a><span data-ttu-id="b6e9d-132">Creación de un agente de transporte SmtpReceiveAgent personalizado</span><span class="sxs-lookup"><span data-stu-id="b6e9d-132">Creating a custom SmtpReceiveAgent transport agent</span></span>

<span data-ttu-id="b6e9d-133">El siguiente procedimiento describe cómo crear a un agente de transporte SmtpReceiveAgent personalizado.</span><span class="sxs-lookup"><span data-stu-id="b6e9d-133">The following procedure describes how to create a custom SmtpReceiveAgent transport agent.</span></span> 
  
### <a name="to-create-the-transport-agent"></a><span data-ttu-id="b6e9d-134">Para crear al agente de transporte</span><span class="sxs-lookup"><span data-stu-id="b6e9d-134">To create the transport agent</span></span>

1. <span data-ttu-id="b6e9d-135">Agregue referencias a los espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="b6e9d-135">Add references to the namespaces.</span></span>
    
   ```cs
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Smtp;
      using Microsoft.Exchange.Data.Transport.Email;
      using Microsoft.Exchange.Data.TextConverters;
  
   ```

   <span data-ttu-id="b6e9d-136">Puede encontrar estos espacios de nombres en el servidor de Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="b6e9d-136">You can find these namespaces on your Exchange 2013 server.</span></span> <span data-ttu-id="b6e9d-137">Cuando se agrega una referencia a estos espacios de nombres, tendrá acceso a los miembros de [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) así como otras clases que se usan en el [Exchange 2013: crear un agente de transporte de conversión de cuerpo](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0) ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b6e9d-137">When you add a reference to these namespaces, you will have access to the [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) members as well as other classes used in the [Exchange 2013: Build a body conversion transport agent](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0) sample.</span></span> 
    
2. <span data-ttu-id="b6e9d-138">Implementar la clase derivada de la clase [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b6e9d-138">Implement the derived class for the [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) class.</span></span> 
    
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

   <span data-ttu-id="b6e9d-139">Este código se cree una instancia de la clase derivada y reemplace el método **CreateAgent** para crear una instancia de su nuevo agente personalizado.</span><span class="sxs-lookup"><span data-stu-id="b6e9d-139">This code will instantiate the derived class and override the **CreateAgent** method to create an instance of your new custom agent.</span></span> 
    
3. <span data-ttu-id="b6e9d-140">Definir al agente.</span><span class="sxs-lookup"><span data-stu-id="b6e9d-140">Define your agent.</span></span>
    
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

   <span data-ttu-id="b6e9d-141">Después de definir la clase del agente, puede agregar la funcionalidad personalizada.</span><span class="sxs-lookup"><span data-stu-id="b6e9d-141">After you define your agent class, you can add your custom functionality.</span></span> <span data-ttu-id="b6e9d-142">En este ejemplo, el evento [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) se redirige a su controlador de eventos personalizado.</span><span class="sxs-lookup"><span data-stu-id="b6e9d-142">In this example, the [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) event is redirected to your custom event handler.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="b6e9d-143">Ver también</span><span class="sxs-lookup"><span data-stu-id="b6e9d-143">See also</span></span>

- [<span data-ttu-id="b6e9d-144">Conceptos de agente en Exchange 2013 de transporte</span><span class="sxs-lookup"><span data-stu-id="b6e9d-144">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)    
- [<span data-ttu-id="b6e9d-145">Referencia de agente de transporte de Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="b6e9d-145">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)    
- [<span data-ttu-id="b6e9d-146">SmtpReceiveAgentFactory</span><span class="sxs-lookup"><span data-stu-id="b6e9d-146">SmtpReceiveAgentFactory</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)    
- [<span data-ttu-id="b6e9d-147">SmtpReceiveAgent</span><span class="sxs-lookup"><span data-stu-id="b6e9d-147">SmtpReceiveAgent</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)
    

