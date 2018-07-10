---
title: Creación de herramientas de Shell de administración de Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 46e4812f-37a8-449f-bd37-bc4a94605db9
description: Obtenga información para comenzar a crear herramientas de Shell de administración de Exchange para Exchange.
ms.openlocfilehash: e8414460007f333e50c9d596bf977792977b1e4e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763306"
---
# <a name="create-exchange-management-shell-tools"></a><span data-ttu-id="c4c02-103">Creación de herramientas de Shell de administración de Exchange</span><span class="sxs-lookup"><span data-stu-id="c4c02-103">Create Exchange Management Shell tools</span></span>

<span data-ttu-id="c4c02-104">Obtenga información para comenzar a crear herramientas de Shell de administración de Exchange para Exchange.</span><span class="sxs-lookup"><span data-stu-id="c4c02-104">Find information to get started creating Exchange Management Shell tools for Exchange.</span></span>

<span data-ttu-id="c4c02-105">**Se aplica a:** Exchange Online | Exchange Server 2013 | Office 365</span><span class="sxs-lookup"><span data-stu-id="c4c02-105">**Applies to:** Exchange Online | Exchange Server 2013 | Office 365</span></span>
  
<span data-ttu-id="c4c02-106">El Shell de administración de Exchange proporciona un amplio conjunto de comandos, en función de la plataforma de Windows PowerShell para la administración de Exchange Online, Exchange Online como parte de Office 365 o una versión local de Exchange comenzando con Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="c4c02-106">The Exchange Management Shell provides a rich set of commands, based on the Windows PowerShell platform, for managing Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013.</span></span> <span data-ttu-id="c4c02-107">Puede usar comandos del Shell de administración de Exchange para automatizar la administración de un servidor mediante la ejecución de los comandos directamente o mediante el uso de las secuencias de comandos.</span><span class="sxs-lookup"><span data-stu-id="c4c02-107">You can use Exchange Management Shell commands to automate the administration of a server by directly executing the commands, or by using command scripts.</span></span>
  
<span data-ttu-id="c4c02-108">Si necesita usar los comandos de Shell de administración de Exchange desde dentro de una aplicación de hospedaje, como una aplicación administrativa que se ejecuta en el escritorio del administrador o a través de una aplicación basada en web, puede llamar a los cmdlets del Shell de administración de Exchange desde dentro de la aplicación de Visual Basic o C# para administrar un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c4c02-108">If you need to use Exchange Management Shell commands from within a hosting application, such as an administrative application that is running on the administrator's desktop or through a web-based application, you can call Exchange Management Shell cmdlets from within your Visual Basic or C# application to manage an Exchange server.</span></span>
  
## <a name="get-started-with-exchange-management-shell-tools"></a><span data-ttu-id="c4c02-109">Empezar a trabajar con las herramientas de Shell de administración de Exchange</span><span class="sxs-lookup"><span data-stu-id="c4c02-109">Get started with Exchange Management Shell tools</span></span>
<span data-ttu-id="c4c02-110"><a name="SP15GettingStartedTemplate_WhatDoYouNeed"> </a></span><span class="sxs-lookup"><span data-stu-id="c4c02-110"></span></span>

<span data-ttu-id="c4c02-111">Si está familiarizado con la creación de aplicaciones de host de Windows PowerShell y desea ver un ejemplo que muestra cómo llamar a los cmdlets del Shell de administración de Exchange desde una aplicación, o para ver un ejemplo de los tipos de aplicaciones que se pueden crear mediante el uso de la Exchange Cmdlets del Shell de administración, vea [obtener una lista de usuarios de correo mediante el Shell de administración de Exchange](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md).</span><span class="sxs-lookup"><span data-stu-id="c4c02-111">If you are familiar with creating Windows PowerShell host applications and want to see an example that shows how to call the Exchange Management Shell cmdlets from an application, or to see an example of the types of applications that you can create by using the Exchange Management Shell cmdlets, see [Get a list of mail users by using the Exchange Management Shell](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md).</span></span>
  
<span data-ttu-id="c4c02-112">Los cmdlets del Shell de administración de Exchange son las extensiones de Windows PowerShell, un shell de línea de comandos basados en tareas y lenguaje de scripting que está diseñado específicamente para la administración del sistema.</span><span class="sxs-lookup"><span data-stu-id="c4c02-112">The Exchange Management Shell cmdlets are extensions to Windows PowerShell, a task-based command-line shell and scripting language that is designed specifically for system administration.</span></span> <span data-ttu-id="c4c02-113">Windows PowerShell se basa en .NET Framework y proporciona una API orientada a objetos para los desarrolladores de aplicaciones de host, proveedor y cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4c02-113">Windows PowerShell is built on the .NET Framework, and provides an object-oriented API for cmdlet, provider, and host application developers.</span></span> <span data-ttu-id="c4c02-114">Para obtener información acerca de la programación de Windows PowerShell, vea el [SDK de Windows PowerShell](http://msdn.microsoft.com/es-es/library/dd835506%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c4c02-114">To learn about Windows PowerShell programming, see the [Windows PowerShell SDK](http://msdn.microsoft.com/es-es/library/dd835506%28VS.85%29.aspx).</span></span>
  
<span data-ttu-id="c4c02-115">Los cmdlets del Shell de administración de Exchange acepte y devolver objetos.</span><span class="sxs-lookup"><span data-stu-id="c4c02-115">The Exchange Management Shell cmdlets accept and return objects.</span></span> <span data-ttu-id="c4c02-116">Para obtener una lista de cmdlets del shell de administración de Exchange y sus tipos de entrada y salidas, vea [cmdlet del Shell de administración de Exchange de entrada y salida tipos](exchange-management-shell-cmdlet-input-and-output-types.md).</span><span class="sxs-lookup"><span data-stu-id="c4c02-116">For a list of Exchange management shell cmdlets and their input and output types, see [Exchange Management Shell cmdlet input and output types](exchange-management-shell-cmdlet-input-and-output-types.md).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="c4c02-117">En esta sección</span><span class="sxs-lookup"><span data-stu-id="c4c02-117">In this section</span></span>

- [<span data-ttu-id="c4c02-118">Nuevos y actualizados cmdlets del Shell de administración de Exchange</span><span class="sxs-lookup"><span data-stu-id="c4c02-118">New and updated Exchange Management Shell cmdlets</span></span>](new-and-updated-exchange-management-shell-cmdlets.md)  
- [<span data-ttu-id="c4c02-119">Entrada de cmdlet del Shell de administración de Exchange y tipos de salida</span><span class="sxs-lookup"><span data-stu-id="c4c02-119">Exchange Management Shell cmdlet input and output types</span></span>](exchange-management-shell-cmdlet-input-and-output-types.md)
- [<span data-ttu-id="c4c02-120">Obtener una lista de usuarios de correo mediante el Shell de administración de Exchange</span><span class="sxs-lookup"><span data-stu-id="c4c02-120">Get a list of mail users by using the Exchange Management Shell</span></span>](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md)
- [<span data-ttu-id="c4c02-121">Usar la respuesta de cmdlet del Shell de administración de Exchange</span><span class="sxs-lookup"><span data-stu-id="c4c02-121">Use the Exchange Management Shell cmdlet response</span></span>](how-to-use-the-exchange-management-shell-cmdlet-response.md)


## <a name="see-also"></a><span data-ttu-id="c4c02-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4c02-122">See also</span></span>

- [<span data-ttu-id="c4c02-123">Espacios de nombres de Shell de administración de Exchange</span><span class="sxs-lookup"><span data-stu-id="c4c02-123">Exchange Management Shell namespaces</span></span>](exchange-management-shell-namespaces.md)  
- [<span data-ttu-id="c4c02-124">Exchange Server PowerShell (Shell de administración de Exchange)</span><span class="sxs-lookup"><span data-stu-id="c4c02-124">Exchange Server PowerShell (Exchange Management Shell)</span></span>](https://docs.microsoft.com/es-es/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)  
- [<span data-ttu-id="c4c02-125">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c4c02-125">Windows PowerShell</span></span>](http://msdn.microsoft.com/es-es/library/dd835506%28v=vs.85%29.aspx)
    

