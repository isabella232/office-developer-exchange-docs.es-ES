---
title: Crear herramientas de Shell de administración de Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 46e4812f-37a8-449f-bd37-bc4a94605db9
description: Obtenga información para empezar a crear herramientas de Shell de administración de Exchange para Exchange.
ms.openlocfilehash: c6e11fa5b55aa514b12f4f52bc9346ac213d3781
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463730"
---
# <a name="create-exchange-management-shell-tools"></a><span data-ttu-id="10e46-103">Crear herramientas de Shell de administración de Exchange</span><span class="sxs-lookup"><span data-stu-id="10e46-103">Create Exchange Management Shell tools</span></span>

<span data-ttu-id="10e46-104">Obtenga información para empezar a crear herramientas de Shell de administración de Exchange para Exchange.</span><span class="sxs-lookup"><span data-stu-id="10e46-104">Find information to get started creating Exchange Management Shell tools for Exchange.</span></span>

<span data-ttu-id="10e46-105">**Se aplica a:** Exchange Online | Exchange Server 2013 | Office 365</span><span class="sxs-lookup"><span data-stu-id="10e46-105">**Applies to:** Exchange Online | Exchange Server 2013 | Office 365</span></span>
  
<span data-ttu-id="10e46-106">El shell de administración de Exchange proporciona un amplio conjunto de comandos, basados en la plataforma Windows PowerShell, para administrar Exchange Online, Exchange online como parte de Office 365 o una versión local de Exchange a partir de Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="10e46-106">The Exchange Management Shell provides a rich set of commands, based on the Windows PowerShell platform, for managing Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013.</span></span> <span data-ttu-id="10e46-107">Puede usar los comandos del shell de administración de Exchange para automatizar la administración de un servidor ejecutando directamente los comandos o mediante scripts de comando.</span><span class="sxs-lookup"><span data-stu-id="10e46-107">You can use Exchange Management Shell commands to automate the administration of a server by directly executing the commands, or by using command scripts.</span></span>
  
<span data-ttu-id="10e46-108">Si necesita usar comandos del shell de administración de Exchange desde una aplicación de hospedaje, como una aplicación administrativa que se ejecuta en el escritorio del administrador o mediante una aplicación basada en Web, puede llamar a los cmdlets del shell de administración de Exchange desde la aplicación de Visual Basic o C# para administrar un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="10e46-108">If you need to use Exchange Management Shell commands from within a hosting application, such as an administrative application that is running on the administrator's desktop or through a web-based application, you can call Exchange Management Shell cmdlets from within your Visual Basic or C# application to manage an Exchange server.</span></span>
  
## <a name="get-started-with-exchange-management-shell-tools"></a><span data-ttu-id="10e46-109">Introducción a las herramientas de Shell de administración de Exchange</span><span class="sxs-lookup"><span data-stu-id="10e46-109">Get started with Exchange Management Shell tools</span></span>
<span data-ttu-id="10e46-110"><a name="SP15GettingStartedTemplate_WhatDoYouNeed"> </a></span><span class="sxs-lookup"><span data-stu-id="10e46-110"><a name="SP15GettingStartedTemplate_WhatDoYouNeed"> </a></span></span>

<span data-ttu-id="10e46-111">Si está familiarizado con la creación de aplicaciones host de Windows PowerShell y desea ver un ejemplo que muestre cómo llamar a los cmdlets del shell de administración de Exchange desde una aplicación o para ver un ejemplo de los tipos de aplicaciones que se pueden crear con los cmdlets del shell de administración de Exchange, vea [obtener una lista de usuarios de correo mediante el shell de administración de Exchange](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md).</span><span class="sxs-lookup"><span data-stu-id="10e46-111">If you are familiar with creating Windows PowerShell host applications and want to see an example that shows how to call the Exchange Management Shell cmdlets from an application, or to see an example of the types of applications that you can create by using the Exchange Management Shell cmdlets, see [Get a list of mail users by using the Exchange Management Shell](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md).</span></span>
  
<span data-ttu-id="10e46-112">Los cmdlets del shell de administración de Exchange son extensiones de Windows PowerShell, un shell de línea de comandos basado en tareas y un lenguaje de scripting diseñado específicamente para la administración del sistema.</span><span class="sxs-lookup"><span data-stu-id="10e46-112">The Exchange Management Shell cmdlets are extensions to Windows PowerShell, a task-based command-line shell and scripting language that is designed specifically for system administration.</span></span> <span data-ttu-id="10e46-113">Windows PowerShell se basa en .NET Framework y proporciona una API orientada a objetos para los desarrolladores de cmdlets, proveedores y aplicaciones host.</span><span class="sxs-lookup"><span data-stu-id="10e46-113">Windows PowerShell is built on the .NET Framework, and provides an object-oriented API for cmdlet, provider, and host application developers.</span></span> <span data-ttu-id="10e46-114">Para obtener más información acerca de la programación de Windows PowerShell, consulte el [SDK de Windows PowerShell](https://msdn.microsoft.com/library/dd835506%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="10e46-114">To learn about Windows PowerShell programming, see the [Windows PowerShell SDK](https://msdn.microsoft.com/library/dd835506%28VS.85%29.aspx).</span></span>
  
<span data-ttu-id="10e46-115">Los cmdlets del shell de administración de Exchange aceptan y devuelven objetos.</span><span class="sxs-lookup"><span data-stu-id="10e46-115">The Exchange Management Shell cmdlets accept and return objects.</span></span> <span data-ttu-id="10e46-116">Para obtener una lista de los cmdlets del shell de administración de Exchange y los tipos de entrada y salida, consulte [tipos de entrada y salida del cmdlet del shell de administración de Exchange](exchange-management-shell-cmdlet-input-and-output-types.md).</span><span class="sxs-lookup"><span data-stu-id="10e46-116">For a list of Exchange management shell cmdlets and their input and output types, see [Exchange Management Shell cmdlet input and output types](exchange-management-shell-cmdlet-input-and-output-types.md).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="10e46-117">En esta sección</span><span class="sxs-lookup"><span data-stu-id="10e46-117">In this section</span></span>

- [<span data-ttu-id="10e46-118">Cmdlets del shell de administración de Exchange nuevos y actualizados</span><span class="sxs-lookup"><span data-stu-id="10e46-118">New and updated Exchange Management Shell cmdlets</span></span>](new-and-updated-exchange-management-shell-cmdlets.md)  
- [<span data-ttu-id="10e46-119">Tipos de entrada y salida del cmdlet del Shell de administración de Exchange</span><span class="sxs-lookup"><span data-stu-id="10e46-119">Exchange Management Shell cmdlet input and output types</span></span>](exchange-management-shell-cmdlet-input-and-output-types.md)
- [<span data-ttu-id="10e46-120">Obtener una lista de usuarios de correo mediante el shell de administración de Exchange</span><span class="sxs-lookup"><span data-stu-id="10e46-120">Get a list of mail users by using the Exchange Management Shell</span></span>](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md)
- [<span data-ttu-id="10e46-121">Usar la respuesta del cmdlet de Shell de administración de Exchange</span><span class="sxs-lookup"><span data-stu-id="10e46-121">Use the Exchange Management Shell cmdlet response</span></span>](how-to-use-the-exchange-management-shell-cmdlet-response.md)


## <a name="see-also"></a><span data-ttu-id="10e46-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="10e46-122">See also</span></span>

- [<span data-ttu-id="10e46-123">Espacios de nombres del shell de administración de Exchange</span><span class="sxs-lookup"><span data-stu-id="10e46-123">Exchange Management Shell namespaces</span></span>](exchange-management-shell-namespaces.md)  
- [<span data-ttu-id="10e46-124">PowerShell de Exchange Server (Shell de administración de Exchange)</span><span class="sxs-lookup"><span data-stu-id="10e46-124">Exchange Server PowerShell (Exchange Management Shell)</span></span>](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)  
- [<span data-ttu-id="10e46-125">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="10e46-125">Windows PowerShell</span></span>](https://msdn.microsoft.com/library/dd835506%28v=vs.85%29.aspx)
    

