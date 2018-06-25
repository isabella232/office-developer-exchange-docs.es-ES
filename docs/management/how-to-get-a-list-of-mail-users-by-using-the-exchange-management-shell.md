---
title: Obtener una lista de usuarios de correo mediante el Shell de administración de Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b790dc8-5c4f-4acf-bbe7-63523395fbe7
description: Aprenda a usar los cmdlets del Shell de administración de Exchange para crear una herramienta que devuelva una lista de los usuarios de buzones de correo de Exchange.
ms.openlocfilehash: 6f64330a11e372bffbea2fcd88bcfa0231ec0f28
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763314"
---
# <a name="get-a-list-of-mail-users-by-using-the-exchange-management-shell"></a><span data-ttu-id="cbcad-103">Obtener una lista de usuarios de correo mediante el Shell de administración de Exchange</span><span class="sxs-lookup"><span data-stu-id="cbcad-103">Get a list of mail users by using the Exchange Management Shell</span></span>

<span data-ttu-id="cbcad-104">Aprenda a usar los cmdlets del Shell de administración de Exchange para crear una herramienta que devuelva una lista de los usuarios de buzones de correo de Exchange.</span><span class="sxs-lookup"><span data-stu-id="cbcad-104">Learn how to use Exchange Management Shell cmdlets to create a tool that returns a list of Exchange mailbox users.</span></span>
  
<span data-ttu-id="cbcad-105">**Se aplica a:** Exchange Online | Exchange Server 2013 | Office 365</span><span class="sxs-lookup"><span data-stu-id="cbcad-105">**Applies to:** Exchange Online | Exchange Server 2013 | Office 365</span></span> 
  
<span data-ttu-id="cbcad-106">Obtener una lista de usuarios de Exchange Online, Exchange Online como parte de Office 365, o una versión de Exchange a partir de Exchange 2013 mediante el uso de una herramienta administrada que llama a un cmdlet del Shell de administración de Exchange es un proceso de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="cbcad-106">Getting a list of users from Exchange Online, Exchange Online as part of Office 365, or a version of Exchange starting with Exchange 2013 by using a managed tool that calls an Exchange Management Shell cmdlet is a two-step process.</span></span> <span data-ttu-id="cbcad-107">En primer lugar, establecer un espacio de ejecución remoto en un servidor de Exchange; a continuación, ejecute el cmdlet para recuperar la información del usuario en el espacio de ejecución remoto.</span><span class="sxs-lookup"><span data-stu-id="cbcad-107">First, you establish a remote runspace on an Exchange server; then, you run the cmdlet to retrieve the user information in the remote runspace.</span></span> 

<span data-ttu-id="cbcad-108">Para conectar con el espacio de ejecución remoto, se debe autenticar con el servidor de Exchange mediante el esquema de autenticación que cumpla los requisitos de seguridad de la organización.</span><span class="sxs-lookup"><span data-stu-id="cbcad-108">To connect to the remote runspace, you have to authenticate with the Exchange server by using the authentication scheme that meets the security requirements of your organization.</span></span> 

<span data-ttu-id="cbcad-109">En este artículo se proporcionan ejemplos de código que puede usar para establecer un espacio de ejecución remoto y ejecutar un cmdlet del Shell de administración de Exchange para obtener una lista de usuarios desde un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="cbcad-109">This article provides code examples that you can use to set up a remote runspace and run an Exchange Management Shell cmdlet to get a list of users from an Exchange server.</span></span>

<span data-ttu-id="cbcad-110"><a name="bk_prerequisites"> </a></span><span class="sxs-lookup"><span data-stu-id="cbcad-110"></span></span>

## <a name="prerequisites-for-getting-a-list-of-mailbox-users"></a><span data-ttu-id="cbcad-111">Requisitos previos para conseguir una lista de usuarios de buzón de correo</span><span class="sxs-lookup"><span data-stu-id="cbcad-111">Prerequisites for getting a list of mailbox users</span></span>

<span data-ttu-id="cbcad-112">Para realizar esta tarea, se necesita una referencia para los siguientes espacios de nombres:</span><span class="sxs-lookup"><span data-stu-id="cbcad-112">To perform this task, you need a reference to the following namespaces:</span></span>
  
- <span data-ttu-id="cbcad-113">**System.Collections.ObjectModel**</span><span class="sxs-lookup"><span data-stu-id="cbcad-113">**System.Collections.ObjectModel**</span></span>
- <span data-ttu-id="cbcad-114">**System.Management.Automation**</span><span class="sxs-lookup"><span data-stu-id="cbcad-114">**System.Management.Automation**</span></span>
- <span data-ttu-id="cbcad-115">**System.Management.Automation.Remoting**</span><span class="sxs-lookup"><span data-stu-id="cbcad-115">**System.Management.Automation.Remoting**</span></span>
- <span data-ttu-id="cbcad-116">**System.Management.Automation.Runspaces**</span><span class="sxs-lookup"><span data-stu-id="cbcad-116">**System.Management.Automation.Runspaces**</span></span>
    
> [!NOTE]
>  <span data-ttu-id="cbcad-p102">Cuando utiliza Visual Studio para crear una aplicación, debe agregar una referencia al ensamblado System.Management.Automation.dll para el proyecto. El ensamblado puede encontrarse en una de las siguientes ubicaciones:</span><span class="sxs-lookup"><span data-stu-id="cbcad-p102">When you are using Visual Studio to create an application, you must add a reference to the System.Management.Automation.dll assembly to the project. The assembly can be found in one of the following locations:</span></span>
> - <span data-ttu-id="cbcad-119">En los sistemas operativos Windows XP y Windows Vista, el directorio de instalación de Windows PowerShell ($PSHOME).</span><span class="sxs-lookup"><span data-stu-id="cbcad-119">For Windows XP and Windows Vista operating systems, the Windows PowerShell installation directory ($PSHOME).</span></span>
> - <span data-ttu-id="cbcad-120">En los sistemas operativos Windows 7 y Windows 8, la siguiente carpeta: Windows\assembly\GAC_MSIL\System.Management.Automation.</span><span class="sxs-lookup"><span data-stu-id="cbcad-120">For the Windows 7 and Windows 8 operating systems, the following folder: Windows\assembly\GAC_MSIL\System.Management.Automation.</span></span> 
  
<span data-ttu-id="cbcad-121">No se cargue el complemento de administración de Exchange 2013 en el espacio de ejecución en los equipos que ejecutan aplicaciones que automatizan los cmdlets del Shell de administración de Exchange.</span><span class="sxs-lookup"><span data-stu-id="cbcad-121">Do not load the Exchange 2013 Management snap-in into the runspace on computers that are running applications that automate Exchange Management Shell cmdlets.</span></span> <span data-ttu-id="cbcad-122">La aplicación en su lugar, debe crear un espacio de ejecución remoto, tal como se describe más adelante en este artículo.</span><span class="sxs-lookup"><span data-stu-id="cbcad-122">The application should instead create a remote runspace, as described later in this article.</span></span>

<span data-ttu-id="cbcad-123"><a name="bk_gettinglistmailbox"> </a></span><span class="sxs-lookup"><span data-stu-id="cbcad-123"></span></span>

## <a name="connect-to-a-remote-runspace-on-an-exchange-server"></a><span data-ttu-id="cbcad-124">Conectarse a un espacio de ejecución remoto en un servidor Exchange</span><span class="sxs-lookup"><span data-stu-id="cbcad-124">Connect to a remote runspace on an Exchange server</span></span>

<span data-ttu-id="cbcad-p104">El método que utilice para conectarse a un espacio de ejecución remoto para usar un cmdlet de Shell de administración de Exchange varía en función del esquema de autenticación que esté utilizando. Esta sección proporciona ejemplos de código que muestran cómo conectarse a un espacio de ejecución remoto cuando utiliza un método de autenticación indicado en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="cbcad-p104">The method that you use to connect to a remote runspace to use an Exchange Management Shell cmdlet varies based on the authentication scheme that you are using. This section provides code examples that show how to connect to a remote runspace when you are using an authentication method listed in the following table.</span></span>
  
|<span data-ttu-id="cbcad-127">**Método de autenticación**</span><span class="sxs-lookup"><span data-stu-id="cbcad-127">**Authentication method**</span></span>|<span data-ttu-id="cbcad-128">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="cbcad-128">**Applies to**</span></span>|<span data-ttu-id="cbcad-129">**URI**</span><span class="sxs-lookup"><span data-stu-id="cbcad-129">**URI**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cbcad-130">Conectarse a un espacio de ejecución remoto en Exchange Online mediante el uso de la autenticación básica</span><span class="sxs-lookup"><span data-stu-id="cbcad-130">Connect to a remote runspace on Exchange Online by using basic authentication</span></span>](#bk_basic) <br/> |<span data-ttu-id="cbcad-131">Servidores Exchange Online</span><span class="sxs-lookup"><span data-stu-id="cbcad-131">Exchange Online servers</span></span>  <br/> |`https://outlook.office365.com/PowerShell-LiveID`<br/><br/>`https://<server>/PowerShell-LiveID`  <br/> |
|[<span data-ttu-id="cbcad-132">Conectarse a un espacio de ejecución remoto mediante el uso de la autenticación de certificados</span><span class="sxs-lookup"><span data-stu-id="cbcad-132">Connect to a remote runspace by using certificate authentication</span></span>](#bk_cert) <br/> |<span data-ttu-id="cbcad-133">Servidores Exchange Online y Exchange local</span><span class="sxs-lookup"><span data-stu-id="cbcad-133">Exchange Online and Exchange on-premises servers</span></span>  <br/> |`https://outlook.office365.com/PowerShell`<br/><br/>`https://<server>/PowerShell`<br/><br/>`http://<server>/PowerShell`  <br/> |
|[<span data-ttu-id="cbcad-134">Conectarse a un espacio de ejecución remoto en un servidor de Exchange mediante la autenticación Kerberos</span><span class="sxs-lookup"><span data-stu-id="cbcad-134">Connect to a remote runspace on an Exchange server by using Kerberos authentication</span></span>](#bk_Kerberos) <br/> |<span data-ttu-id="cbcad-135">Servidores Exchange Online y Exchange local</span><span class="sxs-lookup"><span data-stu-id="cbcad-135">Exchange Online and Exchange on-premises servers</span></span>  <br/> |`https://<server>/PowerShell`<br/><br/>`http://<server>/PowerShell`  <br/> |

<span data-ttu-id="cbcad-136"><a name="bk_basic"> </a></span><span class="sxs-lookup"><span data-stu-id="cbcad-136"></span></span>

### <a name="connect-to-a-remote-runspace-on-exchange-online-by-using-basic-authentication"></a><span data-ttu-id="cbcad-137">Conéctese a un espacio de ejecución remoto de Exchange Online mediante una autenticación básica</span><span class="sxs-lookup"><span data-stu-id="cbcad-137">Connect to a remote runspace on Exchange Online by using basic authentication</span></span>

<span data-ttu-id="cbcad-138">En el ejemplo de código siguiente se define el método **GetUsersUsingBasicAuth** , que crea un espacio de ejecución de Shell de administración de Exchange en un servidor de Exchange Online remoto mediante el uso de la autenticación básica.</span><span class="sxs-lookup"><span data-stu-id="cbcad-138">The following code example defines the **GetUsersUsingBasicAuth** method, which creates an Exchange Management Shell runspace on a remote Exchange Online server by using basic authentication.</span></span> <span data-ttu-id="cbcad-139">El método llama, a continuación, el método **GetUserInformation** , tal como se define en la sección [obtener una lista de los usuarios del buzón de un espacio de ejecución remoto](#bk_remote), para devolver una lista de usuarios en el servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="cbcad-139">The method then calls the **GetUserInformation** method, as defined in the section [Get a list of mailbox users from a remote runspace](#bk_remote), to return a list of users on the remote server.</span></span>
  
<span data-ttu-id="cbcad-140">Este método requiere los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="cbcad-140">This method requires the following parameters:</span></span>
  
-  <span data-ttu-id="cbcad-141">**liveIDConnectionUri** &ndash; Una cadena que contiene el identificador URI del servidor de Exchange Online que va a realizar la autenticación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cbcad-141">**liveIDConnectionUri** &ndash; A string that contains the URI of the Exchange Online server that will authenticate the application.</span></span> <span data-ttu-id="cbcad-142">Si se está ejecutando Exchange Online en Office 365, el URI es https://outlook.office365.com/PowerShell-LiveID; de lo contrario, el URI es https://\<nombreDeServidor\>/PowerShell-LiveID.</span><span class="sxs-lookup"><span data-stu-id="cbcad-142">If Exchange Online is running in Office 365, the URI is https://outlook.office365.com/PowerShell-LiveID; otherwise, the URI is https://\<servername\>/PowerShell-LiveID.</span></span> 
    
-  <span data-ttu-id="cbcad-143">**schemaUri** &ndash; Una cadena que contiene el URI del documento de esquema que define el esquema de Shell de administración de Exchange.</span><span class="sxs-lookup"><span data-stu-id="cbcad-143">**schemaUri** &ndash; A string that contains the URI of the schema document that defines the Exchange Management Shell schema.</span></span> <span data-ttu-id="cbcad-144">El esquema de URI es http://schemas.microsoft.com/powershell/Microsoft.Exchange.</span><span class="sxs-lookup"><span data-stu-id="cbcad-144">The schema URI is http://schemas.microsoft.com/powershell/Microsoft.Exchange.</span></span> 
    
-  <span data-ttu-id="cbcad-145">**credenciales** &ndash; Un objeto [PSCredential](http://msdn.microsoft.com/en-us/library/system.management.automation.pscredential%28VS.85%29.aspx) que contiene las credenciales del usuario que está ejecutando la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cbcad-145">**credentials** &ndash; A [PSCredential](http://msdn.microsoft.com/en-us/library/system.management.automation.pscredential%28VS.85%29.aspx) object that contains the credentials of the user who is running the application.</span></span> 
    
-  <span data-ttu-id="cbcad-146">**recuento** &ndash; El número de usuarios de buzón de correo de Exchange para devolver.</span><span class="sxs-lookup"><span data-stu-id="cbcad-146">**count** &ndash; The number of Exchange mailbox users to return.</span></span> 
    
```cs
public Collection<PSObject> GetUsersUsingBasicAuth(
    string liveIDConnectionUri, string schemaUri, PSCredential credentials, int count)
{
    WSManConnectionInfo connectionInfo = new WSManConnectionInfo(
        new Uri(liveIDConnectionUri),
        schemaUri, credentials);
    connectionInfo.AuthenticationMechanism = AuthenticationMechanism.Basic;
    using (Runspace runspace = RunspaceFactory.CreateRunspace(connectionInfo))
    {
        return GetUserInformation(count, runspace);
    }
}
```


```vb
  Function GetUsersUsingBasicAuth( _
    ByVal LiveIDConnectionUri As String, ByVal ScehmaUri As String, _
    ByVal Credentials As PSCredential, ByVal Count As Integer) As Collection(Of PSObject)
    Dim ConnectionInfo As WSManConnectionInfo = _
        New WSManConnectionInfo(New Uri(LiveIDConnectionUri), ScehmaUri, Credentials)
    ConnectionInfo.AuthenticationMechanism = AuthenticationMechanism.Basic
    Dim RemoteRunspace As Runspace
    RemoteRunspace = RunspaceFactory.CreateRunspace(ConnectionInfo)
    Return GetUserInformation(Count, RemoteRunspace)
  End Function

```

<span data-ttu-id="cbcad-147"><a name="bk_cert"> </a></span><span class="sxs-lookup"><span data-stu-id="cbcad-147"></span></span>

### <a name="connect-to-a-remote-runspace-by-using-certificate-authentication"></a><span data-ttu-id="cbcad-148">Conectarse a un espacio de ejecución remoto mediante la autenticación de certificados</span><span class="sxs-lookup"><span data-stu-id="cbcad-148">Connect to a remote runspace by using certificate authentication</span></span>

<span data-ttu-id="cbcad-149">En el ejemplo de código siguiente se define el método **GetUsersUsingCertificate** , que crea un espacio de ejecución de Shell de administración de Exchange en un servidor remoto mediante el uso de un certificado.</span><span class="sxs-lookup"><span data-stu-id="cbcad-149">The following code example defines the **GetUsersUsingCertificate** method, which creates an Exchange Management Shell runspace on a remote server by using a certificate.</span></span> <span data-ttu-id="cbcad-150">El método llama, a continuación, el método **GetUserInformation** , tal como se define en la sección [obtener una lista de los usuarios del buzón de un espacio de ejecución remoto](#bk_remote), para devolver una lista de usuarios en el servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="cbcad-150">The method then calls the **GetUserInformation** method, as defined in the section [Get a list of mailbox users from a remote runspace](#bk_remote), to return a list of users on the remote server.</span></span>
  
<span data-ttu-id="cbcad-151">Este método requiere los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="cbcad-151">This method requires the following parameters:</span></span>
  
-  <span data-ttu-id="cbcad-152">**huella digital** &ndash; Una cadena que contiene la huella digital del certificado que se usa para autenticar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cbcad-152">**thumbprint** &ndash; A string that contains the thumbprint of the certificate that is used to authenticate the application.</span></span> 
    
-  <span data-ttu-id="cbcad-153">**certConnectionUri** &ndash; Una cadena que contiene el identificador URI del servidor que se va a autenticar el certificado.</span><span class="sxs-lookup"><span data-stu-id="cbcad-153">**certConnectionUri** &ndash; A string that contains the URI of the server that will authenticate the certificate.</span></span> <span data-ttu-id="cbcad-154">El identificador URI será uno de los que se indican en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="cbcad-154">The URI will be one of those listed in the following table.</span></span> 
    
    <span data-ttu-id="cbcad-155">**La tabla 1. certConnectionUri los URI**</span><span class="sxs-lookup"><span data-stu-id="cbcad-155">**Table 1. certConnectionUri URIs**</span></span>

    |<span data-ttu-id="cbcad-156">**Server**</span><span class="sxs-lookup"><span data-stu-id="cbcad-156">**Server**</span></span>|<span data-ttu-id="cbcad-157">**URI**</span><span class="sxs-lookup"><span data-stu-id="cbcad-157">**URI**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="cbcad-158">Servidor Exchange sin SSL</span><span class="sxs-lookup"><span data-stu-id="cbcad-158">Exchange server without using SSL</span></span>  <br/> |`http://<servername>/PowerShell`  <br/> |
    |<span data-ttu-id="cbcad-159">Servidor Exchange con SSL</span><span class="sxs-lookup"><span data-stu-id="cbcad-159">Exchange server using SSL</span></span>  <br/> |`https://<servername>/PowerShell`  <br/> |
    |<span data-ttu-id="cbcad-160">Exchange Online como parte de Office 365</span><span class="sxs-lookup"><span data-stu-id="cbcad-160">Exchange Online as part of Office 365</span></span>  <br/> |`https://outlook.office365.com/PowerShell`  <br/> |
   
- <span data-ttu-id="cbcad-161">**schemaUri** &ndash; Una cadena que contiene el URI del documento de esquema que define el esquema de Shell de administración de Exchange.</span><span class="sxs-lookup"><span data-stu-id="cbcad-161">**schemaUri** &ndash; A string that contains the URI of the schema document that defines the Exchange Management Shell schema.</span></span> <span data-ttu-id="cbcad-162">El esquema de URI es http://schemas.microsoft.com/powershell/Microsoft.Exchange.</span><span class="sxs-lookup"><span data-stu-id="cbcad-162">The schema URI is http://schemas.microsoft.com/powershell/Microsoft.Exchange.</span></span> 
    
- <span data-ttu-id="cbcad-163">**recuento** &ndash; El número de usuarios de buzón de correo de Exchange para devolver.</span><span class="sxs-lookup"><span data-stu-id="cbcad-163">**count** &ndash; The number of Exchange mailbox users to return.</span></span> 
    
```cs
public Collection<PSObject> GetUsersUsingCertificate(
    string thumbprint, string certConnectionUri, string schemaUri, int count)
{
    WSManConnectionInfo connectionInfo = new WSManConnectionInfo(
        new Uri(certConnectionUri),
        schemaUri,
        thumbprint)
    using (Runspace runspace = RunspaceFactory.CreateRunspace(connectionInfo))
    {
        return GetUserInformation(count, runspace);
    }
}
```


```vb
  Function GetUsersUsingCertificate( _
    ByVal Thumbprint As String, ByVal CertConnectionUri As String, _
    ByVal SchemaUri As String, ByVal Count As Integer) As Collection(Of PSObject)
    Dim ConnectionInfo As WSManConnectionInfo
    ConnectionInfo = New WSManConnectionInfo(New Uri(CertConnectionUri), SchemaUri, Thumbprint)
    Dim RemoteRunspace As Runspace
    RemoteRunspace = RunspaceFactory.CreateRunspace(ConnectionInfo)
    Return GetUserInformation(Count, RemoteRunspace)
  End Function

```

<span data-ttu-id="cbcad-164"><a name="bk_Kerberos"> </a></span><span class="sxs-lookup"><span data-stu-id="cbcad-164"></span></span>

### <a name="connect-to-a-remote-runspace-on-an-exchange-server-by-using-kerberos-authentication"></a><span data-ttu-id="cbcad-165">Conectarse a un espacio de ejecución remoto del servidor Exchange mediante una autenticación Kerberos</span><span class="sxs-lookup"><span data-stu-id="cbcad-165">Connect to a remote runspace on an Exchange server by using Kerberos authentication</span></span>

<span data-ttu-id="cbcad-166">En el ejemplo de código siguiente se define el método **GetUsersUsingKerberos** , que crea un espacio de ejecución de Shell de administración de Exchange en un servidor remoto mediante el uso de la autenticación Kerberos.</span><span class="sxs-lookup"><span data-stu-id="cbcad-166">The following code example defines the **GetUsersUsingKerberos** method, which creates an Exchange Management Shell runspace on a remote server by using Kerberos authentication.</span></span> <span data-ttu-id="cbcad-167">El método llama, a continuación, el método **GetUserInformation** , tal como se define en la sección [obtener una lista de los usuarios del buzón de un espacio de ejecución remoto](#bk_remote), para devolver una lista de usuarios en el servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="cbcad-167">The method then calls the **GetUserInformation** method, as defined in the section [Get a list of mailbox users from a remote runspace](#bk_remote), to return a list of users on the remote server.</span></span>
  
<span data-ttu-id="cbcad-168">Este método requiere los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="cbcad-168">This method requires the following parameters:</span></span>
  
- <span data-ttu-id="cbcad-169">**kerberosUri** &ndash; Una cadena que contiene el identificador URI del servidor de Kerberos que se autenticará a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cbcad-169">**kerberosUri** &ndash; A string that contains the URI of the Kerberos server that will authenticate the application.</span></span> <span data-ttu-id="cbcad-170">El identificador URI será uno de los que se indican en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="cbcad-170">The URI will be one of those listed in the following table.</span></span> 
    
    <span data-ttu-id="cbcad-171">**Tabla 2. kerberosUri los URI**</span><span class="sxs-lookup"><span data-stu-id="cbcad-171">**Table 2. kerberosUri URIs**</span></span>

    |<span data-ttu-id="cbcad-172">**Server**</span><span class="sxs-lookup"><span data-stu-id="cbcad-172">**Server**</span></span>|<span data-ttu-id="cbcad-173">**URI**</span><span class="sxs-lookup"><span data-stu-id="cbcad-173">**URI**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="cbcad-174">Servidor Exchange sin SSL</span><span class="sxs-lookup"><span data-stu-id="cbcad-174">Exchange server without using SSL</span></span>  <br/> |`http://<servername>/PowerShell`  <br/> |
    |<span data-ttu-id="cbcad-175">Servidor Exchange con SSL</span><span class="sxs-lookup"><span data-stu-id="cbcad-175">Exchange server using SSL</span></span>  <br/> |`https://<servername>/PowerShell`  <br/> |
   
- <span data-ttu-id="cbcad-176">**schemaUri** &ndash; Una cadena que contiene el URI del documento de esquema que define el esquema de Shell de administración de Exchange.</span><span class="sxs-lookup"><span data-stu-id="cbcad-176">**schemaUri** &ndash; A string that contains the URI of the schema document that defines the Exchange Management Shell schema.</span></span> <span data-ttu-id="cbcad-177">El esquema de URI es http://schemas.microsoft.com/powershell/Microsoft.Exchange.</span><span class="sxs-lookup"><span data-stu-id="cbcad-177">The schema URI is http://schemas.microsoft.com/powershell/Microsoft.Exchange.</span></span> 
    
- <span data-ttu-id="cbcad-178">**credenciales** &ndash; Un objeto [PSCredential](http://msdn.microsoft.com/en-us/library/system.management.automation.pscredential%28VS.85%29.aspx) que contiene las credenciales del usuario que está ejecutando la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cbcad-178">**credentials** &ndash; A [PSCredential](http://msdn.microsoft.com/en-us/library/system.management.automation.pscredential%28VS.85%29.aspx) object that contains the credentials of the user who is running the application.</span></span> 
    
- <span data-ttu-id="cbcad-179">**recuento** &ndash; El número de usuarios de buzón de correo de Exchange para devolver.</span><span class="sxs-lookup"><span data-stu-id="cbcad-179">**count** &ndash; The number of Exchange mailbox users to return.</span></span> 
    
```cs
public Collection<PSObject> GetUsersUsingKerberos(
    string kerberosUri, string schemaUri, PSCredential credentials, int count)
{
    WSManConnectionInfo connectionInfo = new WSManConnectionInfo(
        new Uri(kerberosUri),
        schemaUri, credentials);
    connectionInfo.AuthenticationMechanism = AuthenticationMechanism.Kerberos;
    using (Runspace runspace = RunspaceFactory.CreateRunspace(connectionInfo))
    {
        return GetUserInformation(count, runspace);
    }
}
```

```vb
  Function GetUsersUsingKerberos( _
    ByVal KerberosUri As String, ByVal ScehmaUri As String, _
    ByVal Credentials As PSCredential, ByVal Count As Integer) As Collection(Of PSObject)
    Dim ConnectionInfo As WSManConnectionInfo = _
        New WSManConnectionInfo(New Uri(KerberosUri), ScehmaUri, Credentials)
    ConnectionInfo.AuthenticationMechanism = AuthenticationMechanism.Kerberos
    Dim RemoteRunspace As Runspace
    RemoteRunspace = RunspaceFactory.CreateRunspace(ConnectionInfo)
    Return GetUserInformation(Count, RemoteRunspace)
  End Function

```

<span data-ttu-id="cbcad-180"><a name="bk_remote"> </a></span><span class="sxs-lookup"><span data-stu-id="cbcad-180"></span></span>

## <a name="get-a-list-of-mailbox-users-from-a-remote-runspace"></a><span data-ttu-id="cbcad-181">Conseguir una lista de los usuarios de buzones de correo desde un espacio de ejecución remoto</span><span class="sxs-lookup"><span data-stu-id="cbcad-181">Get a list of mailbox users from a remote runspace</span></span>

<span data-ttu-id="cbcad-182">En el ejemplo de código siguiente se define el método **GetUserInformation** , que devuelve una colección de instancias de [PSObject](http://msdn.microsoft.com/en-us/library/system.management.automation.pscredential%28VS.85%29.aspx) que representan los usuarios del buzón de Exchange.</span><span class="sxs-lookup"><span data-stu-id="cbcad-182">The following code example defines the **GetUserInformation** method, which returns a collection of [PSObject](http://msdn.microsoft.com/en-us/library/system.management.automation.pscredential%28VS.85%29.aspx) instances that represent Exchange mailbox users.</span></span> <span data-ttu-id="cbcad-183">Este método es invocado por los métodos **GetUsersUsingBasicAuth**, **GetUsersUsingCertificate**y **GetUsersUsingKerberos** para devolver la lista de usuarios desde el servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="cbcad-183">This method is called by the **GetUsersUsingBasicAuth**, **GetUsersUsingCertificate**, and **GetUsersUsingKerberos** methods to return the list of users from the remote server.</span></span> 
  
<span data-ttu-id="cbcad-184">Este método requiere los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="cbcad-184">This method requires the following parameters:</span></span>
  
- <span data-ttu-id="cbcad-185">**recuento** &ndash; El número de usuarios de buzón de correo de Exchange para devolver.</span><span class="sxs-lookup"><span data-stu-id="cbcad-185">**count** &ndash; The number of Exchange mailbox users to return.</span></span> 
    
- <span data-ttu-id="cbcad-186">**espacio de ejecución** &ndash; El espacio de ejecución remoto que se haya establecido para el servidor de Exchange remoto.</span><span class="sxs-lookup"><span data-stu-id="cbcad-186">**runspace** &ndash; The remote runspace that is established for the remote Exchange server.</span></span> 
    
```cs
public Collection<PSObject> GetUserInformation(int count, Runspace runspace)
{
    using (PowerShell powershell = PowerShell.Create())
    {
        powershell.AddCommand("Get-Users");
        powershell.AddParameter("ResultSize", count);
        runspace.Open();
        powershell.Runspace = runspace;
        return powershell.Invoke();
    }
}
```

```vb
Function GetUserInformation(ByVal Count As Integer, ByVal RemoteRunspace As Runspace) As Collection(Of PSObject)
    Dim RemotePowerShell As PowerShell = PowerShell.Create
    RemotePowerShell.AddCommand("Get-Users")
    RemotePowerShell.AddParameter("ResultSize", Count)
    ' Open the remote runspace on the server.
    RemoteRunspace.Open()
    ' Associate the runspace with the Exchange Management Shell.
    RemotePowerShell.Runspace = RemoteRunspace
    ' Invoke the Exchange Management Shell to run the command.
    Return RemotePowerShell.Invoke
End Function

```

<span data-ttu-id="cbcad-187">El método **GetUserInformation** no devolverá más de _recuento de_ usuarios del buzón.</span><span class="sxs-lookup"><span data-stu-id="cbcad-187">The **GetUserInformation** method will return no more than  _count_ mailbox users.</span></span> <span data-ttu-id="cbcad-188">Para simplificar el código de este ejemplo, el método no filtrar o limitar en caso contrario, los usuarios de buzón de correo que se devuelven.</span><span class="sxs-lookup"><span data-stu-id="cbcad-188">To simplify the code for this example, the method does not filter or otherwise limit the mailbox users that are returned.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cbcad-189">Vea también</span><span class="sxs-lookup"><span data-stu-id="cbcad-189">See also</span></span>

- [<span data-ttu-id="cbcad-190">Creación de herramientas de Shell de administración de Exchange</span><span class="sxs-lookup"><span data-stu-id="cbcad-190">Create Exchange Management Shell tools</span></span>](create-exchange-management-shell-tools.md)   
- [<span data-ttu-id="cbcad-191">Usar la respuesta de cmdlet del Shell de administración de Exchange</span><span class="sxs-lookup"><span data-stu-id="cbcad-191">Use the Exchange Management Shell cmdlet response</span></span>](how-to-use-the-exchange-management-shell-cmdlet-response.md)
    

