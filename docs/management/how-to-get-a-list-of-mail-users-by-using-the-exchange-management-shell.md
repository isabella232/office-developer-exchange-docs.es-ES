---
title: Obtener una lista de usuarios de correo mediante el shell de administración de Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.assetid: 8b790dc8-5c4f-4acf-bbe7-63523395fbe7
description: Aprenda a usar los cmdlets del Shell de administración de Exchange para crear una herramienta que devuelva una lista de los usuarios de buzones de correo de Exchange.
localization_priority: Priority
ms.openlocfilehash: 817d92ef1bb88017f471681b448c052ecaa54e7e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44435712"
---
# <a name="get-a-list-of-mail-users-by-using-the-exchange-management-shell"></a><span data-ttu-id="2facc-103">Obtener una lista de usuarios de correo mediante el shell de administración de Exchange</span><span class="sxs-lookup"><span data-stu-id="2facc-103">Get a list of mail users by using the Exchange Management Shell</span></span>

<span data-ttu-id="2facc-104">Aprenda a usar los cmdlets del Shell de administración de Exchange para crear una herramienta que devuelva una lista de los usuarios de buzones de correo de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2facc-104">Learn how to use Exchange Management Shell cmdlets to create a tool that returns a list of Exchange mailbox users.</span></span>
  
<span data-ttu-id="2facc-105">**Se aplica a:** Exchange Online | Exchange Server 2013 | Office 365</span><span class="sxs-lookup"><span data-stu-id="2facc-105">**Applies to:** Exchange Online | Exchange Server 2013 | Office 365</span></span> 
  
<span data-ttu-id="2facc-106">Conseguir una lista de usuarios de Exchange Online, Exchange Online como parte de Office 365, o una versión de Exchange a partir de Exchange 2013 usando una herramienta administrada que invoque un cmdlet del Shell de administración de Exchange es un proceso dividido en dos pasos.</span><span class="sxs-lookup"><span data-stu-id="2facc-106">Getting a list of users from Exchange Online, Exchange Online as part of Office 365, or a version of Exchange starting with Exchange 2013 by using a managed tool that calls an Exchange Management Shell cmdlet is a two-step process.</span></span> <span data-ttu-id="2facc-107">En primer lugar, establezca un espacio de ejecución remoto en un servidor de Exchange; a continuación, ejecute el cmdlet para obtener la información de usuario en el espacio de ejecución remoto.</span><span class="sxs-lookup"><span data-stu-id="2facc-107">First, you establish a remote runspace on an Exchange server; then, you run the cmdlet to retrieve the user information in the remote runspace.</span></span> 

<span data-ttu-id="2facc-108">Para conectar con el espacio de ejecución remoto, tendrá que autenticarse con el servidor de Exchange mediante el esquema de autenticación que cumpla los requisitos de seguridad de la organización.</span><span class="sxs-lookup"><span data-stu-id="2facc-108">To connect to the remote runspace, you have to authenticate with the Exchange server by using the authentication scheme that meets the security requirements of your organization.</span></span> 

<span data-ttu-id="2facc-109">Este artículo proporciona ejemplos de código que puede utilizar para configurar un espacio de ejecución remoto y ejecutar un cmdlet del Shell de administración de Exchange para conseguir una lista de usuarios desde un servidor Exchange.</span><span class="sxs-lookup"><span data-stu-id="2facc-109">This article provides code examples that you can use to set up a remote runspace and run an Exchange Management Shell cmdlet to get a list of users from an Exchange server.</span></span>

<span data-ttu-id="2facc-110"><a name="bk_prerequisites"> </a></span><span class="sxs-lookup"><span data-stu-id="2facc-110"><a name="bk_prerequisites"> </a></span></span>

## <a name="prerequisites-for-getting-a-list-of-mailbox-users"></a><span data-ttu-id="2facc-111">Requisitos previos para conseguir una lista de usuarios de buzón de correo</span><span class="sxs-lookup"><span data-stu-id="2facc-111">Prerequisites for getting a list of mailbox users</span></span>

<span data-ttu-id="2facc-112">Para realizar esta tarea, se necesita una referencia para los siguientes espacios de nombres:</span><span class="sxs-lookup"><span data-stu-id="2facc-112">To perform this task, you need a reference to the following namespaces:</span></span>
  
- <span data-ttu-id="2facc-113">**System. Collections. ObjectModel**</span><span class="sxs-lookup"><span data-stu-id="2facc-113">**System.Collections.ObjectModel**</span></span>
- <span data-ttu-id="2facc-114">**System. Management. Automation**</span><span class="sxs-lookup"><span data-stu-id="2facc-114">**System.Management.Automation**</span></span>
- <span data-ttu-id="2facc-115">**System. Management. Automation. Remoting**</span><span class="sxs-lookup"><span data-stu-id="2facc-115">**System.Management.Automation.Remoting**</span></span>
- <span data-ttu-id="2facc-116">**System. Management. Automation. espacios de**</span><span class="sxs-lookup"><span data-stu-id="2facc-116">**System.Management.Automation.Runspaces**</span></span>
    
> [!NOTE]
>  <span data-ttu-id="2facc-p102">Cuando utiliza Visual Studio para crear una aplicación, debe agregar una referencia al ensamblado System.Management.Automation.dll para el proyecto. El ensamblado puede encontrarse en una de las siguientes ubicaciones:</span><span class="sxs-lookup"><span data-stu-id="2facc-p102">When you are using Visual Studio to create an application, you must add a reference to the System.Management.Automation.dll assembly to the project. The assembly can be found in one of the following locations:</span></span>
> - <span data-ttu-id="2facc-119">En los sistemas operativos Windows XP y Windows Vista, el directorio de instalación de Windows PowerShell ($PSHOME).</span><span class="sxs-lookup"><span data-stu-id="2facc-119">For Windows XP and Windows Vista operating systems, the Windows PowerShell installation directory ($PSHOME).</span></span>
> - <span data-ttu-id="2facc-120">En los sistemas operativos Windows 7 y Windows 8, la siguiente carpeta: Windows\assembly\GAC_MSIL\System.Management.Automation.</span><span class="sxs-lookup"><span data-stu-id="2facc-120">For the Windows 7 and Windows 8 operating systems, the following folder: Windows\assembly\GAC_MSIL\System.Management.Automation.</span></span> 
  
<span data-ttu-id="2facc-121">No cargue el complemento de administración de Exchange 2013 en el espacio de ejecución en los equipos que ejecutan aplicaciones que automatizan los cmdlets del shell de administración de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2facc-121">Do not load the Exchange 2013 Management snap-in into the runspace on computers that are running applications that automate Exchange Management Shell cmdlets.</span></span> <span data-ttu-id="2facc-122">La aplicación debe crear en su lugar un espacio de ejecución remoto, tal como se describe más adelante en este artículo.</span><span class="sxs-lookup"><span data-stu-id="2facc-122">The application should instead create a remote runspace, as described later in this article.</span></span>

<span data-ttu-id="2facc-123"><a name="bk_gettinglistmailbox"> </a></span><span class="sxs-lookup"><span data-stu-id="2facc-123"><a name="bk_gettinglistmailbox"> </a></span></span>

## <a name="connect-to-a-remote-runspace-on-an-exchange-server"></a><span data-ttu-id="2facc-124">Conectarse a un espacio de ejecución remoto en un servidor Exchange</span><span class="sxs-lookup"><span data-stu-id="2facc-124">Connect to a remote runspace on an Exchange server</span></span>

<span data-ttu-id="2facc-p104">El método que utilice para conectarse a un espacio de ejecución remoto para usar un cmdlet de Shell de administración de Exchange varía en función del esquema de autenticación que esté utilizando. Esta sección proporciona ejemplos de código que muestran cómo conectarse a un espacio de ejecución remoto cuando utiliza un método de autenticación indicado en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2facc-p104">The method that you use to connect to a remote runspace to use an Exchange Management Shell cmdlet varies based on the authentication scheme that you are using. This section provides code examples that show how to connect to a remote runspace when you are using an authentication method listed in the following table.</span></span>
  
|<span data-ttu-id="2facc-127">**Método de autenticación**</span><span class="sxs-lookup"><span data-stu-id="2facc-127">**Authentication method**</span></span>|<span data-ttu-id="2facc-128">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="2facc-128">**Applies to**</span></span>|<span data-ttu-id="2facc-129">**URI**</span><span class="sxs-lookup"><span data-stu-id="2facc-129">**URI**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2facc-130">Conéctese a un espacio de ejecución remoto de Exchange Online mediante una autenticación básica</span><span class="sxs-lookup"><span data-stu-id="2facc-130">Connect to a remote runspace on Exchange Online by using basic authentication</span></span>](#bk_basic) <br/> |<span data-ttu-id="2facc-131">Servidores Exchange Online</span><span class="sxs-lookup"><span data-stu-id="2facc-131">Exchange Online servers</span></span>  <br/> |`https://outlook.office365.com/PowerShell-LiveID`<br/><br/>`https://<server>/PowerShell-LiveID`  <br/> |
|[<span data-ttu-id="2facc-132">Conectarse a un espacio de ejecución remoto mediante la autenticación de certificados</span><span class="sxs-lookup"><span data-stu-id="2facc-132">Connect to a remote runspace by using certificate authentication</span></span>](#bk_cert) <br/> |<span data-ttu-id="2facc-133">Servidores Exchange Online y Exchange local</span><span class="sxs-lookup"><span data-stu-id="2facc-133">Exchange Online and Exchange on-premises servers</span></span>  <br/> |`https://outlook.office365.com/PowerShell`<br/><br/>`https://<server>/PowerShell`<br/><br/>`http://<server>/PowerShell`  <br/> |
|[<span data-ttu-id="2facc-134">Conectarse a un espacio de ejecución remoto del servidor Exchange mediante una autenticación Kerberos</span><span class="sxs-lookup"><span data-stu-id="2facc-134">Connect to a remote runspace on an Exchange server by using Kerberos authentication</span></span>](#bk_Kerberos) <br/> |<span data-ttu-id="2facc-135">Servidores Exchange Online y Exchange local</span><span class="sxs-lookup"><span data-stu-id="2facc-135">Exchange Online and Exchange on-premises servers</span></span>  <br/> |`https://<server>/PowerShell`<br/><br/>`http://<server>/PowerShell`  <br/> |

<span data-ttu-id="2facc-136"><a name="bk_basic"> </a></span><span class="sxs-lookup"><span data-stu-id="2facc-136"><a name="bk_basic"> </a></span></span>

### <a name="connect-to-a-remote-runspace-on-exchange-online-by-using-basic-authentication"></a><span data-ttu-id="2facc-137">Conéctese a un espacio de ejecución remoto de Exchange Online mediante una autenticación básica</span><span class="sxs-lookup"><span data-stu-id="2facc-137">Connect to a remote runspace on Exchange Online by using basic authentication</span></span>

<span data-ttu-id="2facc-138">El siguiente ejemplo de código define el método **GetUsersUsingBasicAuth**, que crea un espacio de ejecución de Shell de administración de Exchange en un servidor remoto de Exchange Online mediante autenticación básica.</span><span class="sxs-lookup"><span data-stu-id="2facc-138">The following code example defines the **GetUsersUsingBasicAuth** method, which creates an Exchange Management Shell runspace on a remote Exchange Online server by using basic authentication.</span></span> <span data-ttu-id="2facc-139">A continuación, el método invoca al método **GetUserInformation**, tal como se define en la sección [Conseguir una lista de los usuarios de buzones de correo desde un espacio de ejecución remoto](#bk_remote), para devolver una lista de usuarios en el servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="2facc-139">The method then calls the **GetUserInformation** method, as defined in the section [Get a list of mailbox users from a remote runspace](#bk_remote), to return a list of users on the remote server.</span></span>
  
<span data-ttu-id="2facc-140">Este método requiere los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="2facc-140">This method requires the following parameters:</span></span>
  
-  <span data-ttu-id="2facc-141">**liveIDConnectionUri** &ndash; Una cadena que contiene el URI del servidor de Exchange online que autenticará la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2facc-141">**liveIDConnectionUri** &ndash; A string that contains the URI of the Exchange Online server that will authenticate the application.</span></span> <span data-ttu-id="2facc-142">Si Exchange Online se está ejecutando en Office 365, el URI es `https://outlook.office365.com/PowerShell-LiveID` ; de lo contrario, el URI es `https://<servername>/PowerShell-LiveID` .</span><span class="sxs-lookup"><span data-stu-id="2facc-142">If Exchange Online is running in Office 365, the URI is `https://outlook.office365.com/PowerShell-LiveID`; otherwise, the URI is `https://<servername>/PowerShell-LiveID`.</span></span> 
    
-  <span data-ttu-id="2facc-143">**schemaUri** &ndash; Una cadena que contiene el URI del documento de esquema que define el esquema del shell de administración de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2facc-143">**schemaUri** &ndash; A string that contains the URI of the schema document that defines the Exchange Management Shell schema.</span></span> <span data-ttu-id="2facc-144">El URI del esquema es `https://schemas.microsoft.com/powershell/Microsoft.Exchange` .</span><span class="sxs-lookup"><span data-stu-id="2facc-144">The schema URI is `https://schemas.microsoft.com/powershell/Microsoft.Exchange`.</span></span> 
    
-  <span data-ttu-id="2facc-145">**credenciales** &ndash; Un objeto [PSCredential](https://msdn.microsoft.com/library/system.management.automation.pscredential%28VS.85%29.aspx) que contiene las credenciales del usuario que está ejecutando la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2facc-145">**credentials** &ndash; A [PSCredential](https://msdn.microsoft.com/library/system.management.automation.pscredential%28VS.85%29.aspx) object that contains the credentials of the user who is running the application.</span></span> 
    
-  <span data-ttu-id="2facc-146">**número** &ndash; de Número de usuarios de buzones de Exchange que se van a devolver.</span><span class="sxs-lookup"><span data-stu-id="2facc-146">**count** &ndash; The number of Exchange mailbox users to return.</span></span> 
    
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

<span data-ttu-id="2facc-147"><a name="bk_cert"> </a></span><span class="sxs-lookup"><span data-stu-id="2facc-147"><a name="bk_cert"> </a></span></span>

### <a name="connect-to-a-remote-runspace-by-using-certificate-authentication"></a><span data-ttu-id="2facc-148">Conectarse a un espacio de ejecución remoto mediante la autenticación de certificados</span><span class="sxs-lookup"><span data-stu-id="2facc-148">Connect to a remote runspace by using certificate authentication</span></span>

<span data-ttu-id="2facc-149">El siguiente ejemplo de código define el método **GetUsersUsingCertificate**, que crea un espacio de ejecución del Shell de administración de Exchange en un servidor remoto mediante un certificado.</span><span class="sxs-lookup"><span data-stu-id="2facc-149">The following code example defines the **GetUsersUsingCertificate** method, which creates an Exchange Management Shell runspace on a remote server by using a certificate.</span></span> <span data-ttu-id="2facc-150">A continuación, el método invoca al método **GetUserInformation**, tal como se define en la sección [Conseguir una lista de los usuarios de buzones de correo desde un espacio de ejecución remoto](#bk_remote), para devolver una lista de usuarios en el servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="2facc-150">The method then calls the **GetUserInformation** method, as defined in the section [Get a list of mailbox users from a remote runspace](#bk_remote), to return a list of users on the remote server.</span></span>
  
<span data-ttu-id="2facc-151">Este método requiere los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="2facc-151">This method requires the following parameters:</span></span>
  
-  <span data-ttu-id="2facc-152">**huella digital** &ndash; Una cadena que contiene la huella digital del certificado que se usa para autenticar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2facc-152">**thumbprint** &ndash; A string that contains the thumbprint of the certificate that is used to authenticate the application.</span></span> 
    
-  <span data-ttu-id="2facc-153">**certConnectionUri** &ndash; Una cadena que contiene el URI del servidor que va a autenticar el certificado.</span><span class="sxs-lookup"><span data-stu-id="2facc-153">**certConnectionUri** &ndash; A string that contains the URI of the server that will authenticate the certificate.</span></span> <span data-ttu-id="2facc-154">El URI será uno de los recogidos en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2facc-154">The URI will be one of those listed in the following table.</span></span> 
    
    <span data-ttu-id="2facc-155">**Tabla 1. URI de certConnectionUri**</span><span class="sxs-lookup"><span data-stu-id="2facc-155">**Table 1. certConnectionUri URIs**</span></span>

    |<span data-ttu-id="2facc-156">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="2facc-156">**Server**</span></span>|<span data-ttu-id="2facc-157">**URI**</span><span class="sxs-lookup"><span data-stu-id="2facc-157">**URI**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="2facc-158">Servidor Exchange sin SSL</span><span class="sxs-lookup"><span data-stu-id="2facc-158">Exchange server without using SSL</span></span>  <br/> |`http://<servername>/PowerShell`  <br/> |
    |<span data-ttu-id="2facc-159">Servidor Exchange con SSL</span><span class="sxs-lookup"><span data-stu-id="2facc-159">Exchange server using SSL</span></span>  <br/> |`https://<servername>/PowerShell`  <br/> |
    |<span data-ttu-id="2facc-160">Exchange Online como parte de Office 365</span><span class="sxs-lookup"><span data-stu-id="2facc-160">Exchange Online as part of Office 365</span></span>  <br/> |`https://outlook.office365.com/PowerShell`  <br/> |
   
- <span data-ttu-id="2facc-161">**schemaUri** &ndash; Una cadena que contiene el URI del documento de esquema que define el esquema del shell de administración de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2facc-161">**schemaUri** &ndash; A string that contains the URI of the schema document that defines the Exchange Management Shell schema.</span></span> <span data-ttu-id="2facc-162">El URI del esquema es https://schemas.microsoft.com/powershell/Microsoft.Exchange .</span><span class="sxs-lookup"><span data-stu-id="2facc-162">The schema URI is https://schemas.microsoft.com/powershell/Microsoft.Exchange.</span></span> 
    
- <span data-ttu-id="2facc-163">**número** &ndash; de Número de usuarios de buzones de Exchange que se van a devolver.</span><span class="sxs-lookup"><span data-stu-id="2facc-163">**count** &ndash; The number of Exchange mailbox users to return.</span></span> 
    
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

<span data-ttu-id="2facc-164"><a name="bk_Kerberos"> </a></span><span class="sxs-lookup"><span data-stu-id="2facc-164"><a name="bk_Kerberos"> </a></span></span>

### <a name="connect-to-a-remote-runspace-on-an-exchange-server-by-using-kerberos-authentication"></a><span data-ttu-id="2facc-165">Conectarse a un espacio de ejecución remoto del servidor Exchange mediante una autenticación Kerberos</span><span class="sxs-lookup"><span data-stu-id="2facc-165">Connect to a remote runspace on an Exchange server by using Kerberos authentication</span></span>

<span data-ttu-id="2facc-166">El siguiente ejemplo de código define el método **GetUsersUsingKerberos**, que crea un espacio de ejecución del Shell de administración de Exchange en un servidor remoto mediante la autenticación Kerberos.</span><span class="sxs-lookup"><span data-stu-id="2facc-166">The following code example defines the **GetUsersUsingKerberos** method, which creates an Exchange Management Shell runspace on a remote server by using Kerberos authentication.</span></span> <span data-ttu-id="2facc-167">A continuación, el método invoca al método **GetUserInformation**, tal como se define en la sección [Conseguir una lista de los usuarios de buzones de correo desde un espacio de ejecución remoto](#bk_remote), para devolver una lista de usuarios en el servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="2facc-167">The method then calls the **GetUserInformation** method, as defined in the section [Get a list of mailbox users from a remote runspace](#bk_remote), to return a list of users on the remote server.</span></span>
  
<span data-ttu-id="2facc-168">Este método requiere los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="2facc-168">This method requires the following parameters:</span></span>
  
- <span data-ttu-id="2facc-169">**kerberosUri** &ndash; Una cadena que contiene el URI del servidor Kerberos que autenticará la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2facc-169">**kerberosUri** &ndash; A string that contains the URI of the Kerberos server that will authenticate the application.</span></span> <span data-ttu-id="2facc-170">El URI será uno de los recogidos en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2facc-170">The URI will be one of those listed in the following table.</span></span> 
    
    <span data-ttu-id="2facc-171">**Tabla 2. URI de kerberosUri**</span><span class="sxs-lookup"><span data-stu-id="2facc-171">**Table 2. kerberosUri URIs**</span></span>

    |<span data-ttu-id="2facc-172">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="2facc-172">**Server**</span></span>|<span data-ttu-id="2facc-173">**URI**</span><span class="sxs-lookup"><span data-stu-id="2facc-173">**URI**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="2facc-174">Servidor Exchange sin SSL</span><span class="sxs-lookup"><span data-stu-id="2facc-174">Exchange server without using SSL</span></span>  <br/> |`http://<servername>/PowerShell`  <br/> |
    |<span data-ttu-id="2facc-175">Servidor Exchange con SSL</span><span class="sxs-lookup"><span data-stu-id="2facc-175">Exchange server using SSL</span></span>  <br/> |`https://<servername>/PowerShell`  <br/> |
   
- <span data-ttu-id="2facc-176">**schemaUri** &ndash; Una cadena que contiene el URI del documento de esquema que define el esquema del shell de administración de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2facc-176">**schemaUri** &ndash; A string that contains the URI of the schema document that defines the Exchange Management Shell schema.</span></span> <span data-ttu-id="2facc-177">El URI del esquema es https://schemas.microsoft.com/powershell/Microsoft.Exchange .</span><span class="sxs-lookup"><span data-stu-id="2facc-177">The schema URI is https://schemas.microsoft.com/powershell/Microsoft.Exchange.</span></span> 
    
- <span data-ttu-id="2facc-178">**credenciales** &ndash; Un objeto [PSCredential](https://msdn.microsoft.com/library/system.management.automation.pscredential%28VS.85%29.aspx) que contiene las credenciales del usuario que está ejecutando la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2facc-178">**credentials** &ndash; A [PSCredential](https://msdn.microsoft.com/library/system.management.automation.pscredential%28VS.85%29.aspx) object that contains the credentials of the user who is running the application.</span></span> 
    
- <span data-ttu-id="2facc-179">**número** &ndash; de Número de usuarios de buzones de Exchange que se van a devolver.</span><span class="sxs-lookup"><span data-stu-id="2facc-179">**count** &ndash; The number of Exchange mailbox users to return.</span></span> 
    
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

<span data-ttu-id="2facc-180"><a name="bk_remote"> </a></span><span class="sxs-lookup"><span data-stu-id="2facc-180"><a name="bk_remote"> </a></span></span>

## <a name="get-a-list-of-mailbox-users-from-a-remote-runspace"></a><span data-ttu-id="2facc-181">Conseguir una lista de los usuarios de buzones de correo desde un espacio de ejecución remoto</span><span class="sxs-lookup"><span data-stu-id="2facc-181">Get a list of mailbox users from a remote runspace</span></span>

<span data-ttu-id="2facc-182">El siguiente ejemplo de código define el método **GetUserInformation** , que devuelve una colección de instancias de [PSObject](https://msdn.microsoft.com/library/system.management.automation.pscredential%28VS.85%29.aspx) que representan usuarios de buzones de correo de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2facc-182">The following code example defines the **GetUserInformation** method, which returns a collection of [PSObject](https://msdn.microsoft.com/library/system.management.automation.pscredential%28VS.85%29.aspx) instances that represent Exchange mailbox users.</span></span> <span data-ttu-id="2facc-183">También se puede invocar este método mediante los métodos **GetUsersUsingBasicAuth**, **GetUsersUsingCertificate** y **GetUsersUsingKerberos** para obtener la lista de usuarios desde el servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="2facc-183">This method is called by the **GetUsersUsingBasicAuth**, **GetUsersUsingCertificate**, and **GetUsersUsingKerberos** methods to return the list of users from the remote server.</span></span> 
  
<span data-ttu-id="2facc-184">Este método requiere los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="2facc-184">This method requires the following parameters:</span></span>
  
- <span data-ttu-id="2facc-185">**número** &ndash; de Número de usuarios de buzones de Exchange que se van a devolver.</span><span class="sxs-lookup"><span data-stu-id="2facc-185">**count** &ndash; The number of Exchange mailbox users to return.</span></span> 
    
- <span data-ttu-id="2facc-186">**runspace** &ndash; El espacio de ejecución remoto que se establece para el servidor remoto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2facc-186">**runspace** &ndash; The remote runspace that is established for the remote Exchange server.</span></span> 
    
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

<span data-ttu-id="2facc-187">El método **GetUserInformation** no devolverá más que el _número_ de usuarios de buzones.</span><span class="sxs-lookup"><span data-stu-id="2facc-187">The **GetUserInformation** method will return no more than  _count_ mailbox users.</span></span> <span data-ttu-id="2facc-188">Para simplificar el código de este ejemplo, el método no filtra ni limita a los usuarios del buzón de correo que se obtienen.</span><span class="sxs-lookup"><span data-stu-id="2facc-188">To simplify the code for this example, the method does not filter or otherwise limit the mailbox users that are returned.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2facc-189">Vea también</span><span class="sxs-lookup"><span data-stu-id="2facc-189">See also</span></span>

- [<span data-ttu-id="2facc-190">Crear herramientas de Shell de administración de Exchange</span><span class="sxs-lookup"><span data-stu-id="2facc-190">Create Exchange Management Shell tools</span></span>](create-exchange-management-shell-tools.md)   
- [<span data-ttu-id="2facc-191">Usar la respuesta del cmdlet de Shell de administración de Exchange</span><span class="sxs-lookup"><span data-stu-id="2facc-191">Use the Exchange Management Shell cmdlet response</span></span>](how-to-use-the-exchange-management-shell-cmdlet-response.md)
    

