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
# <a name="get-a-list-of-mail-users-by-using-the-exchange-management-shell"></a>Obtener una lista de usuarios de correo mediante el shell de administración de Exchange

Aprenda a usar los cmdlets del Shell de administración de Exchange para crear una herramienta que devuelva una lista de los usuarios de buzones de correo de Exchange.
  
**Se aplica a:** Exchange Online | Exchange Server 2013 | Office 365 
  
Conseguir una lista de usuarios de Exchange Online, Exchange Online como parte de Office 365, o una versión de Exchange a partir de Exchange 2013 usando una herramienta administrada que invoque un cmdlet del Shell de administración de Exchange es un proceso dividido en dos pasos. En primer lugar, establezca un espacio de ejecución remoto en un servidor de Exchange; a continuación, ejecute el cmdlet para obtener la información de usuario en el espacio de ejecución remoto. 

Para conectar con el espacio de ejecución remoto, tendrá que autenticarse con el servidor de Exchange mediante el esquema de autenticación que cumpla los requisitos de seguridad de la organización. 

Este artículo proporciona ejemplos de código que puede utilizar para configurar un espacio de ejecución remoto y ejecutar un cmdlet del Shell de administración de Exchange para conseguir una lista de usuarios desde un servidor Exchange.

<a name="bk_prerequisites"> </a>

## <a name="prerequisites-for-getting-a-list-of-mailbox-users"></a>Requisitos previos para conseguir una lista de usuarios de buzón de correo

Para realizar esta tarea, se necesita una referencia para los siguientes espacios de nombres:
  
- **System. Collections. ObjectModel**
- **System. Management. Automation**
- **System. Management. Automation. Remoting**
- **System. Management. Automation. espacios de**
    
> [!NOTE]
>  Cuando utiliza Visual Studio para crear una aplicación, debe agregar una referencia al ensamblado System.Management.Automation.dll para el proyecto. El ensamblado puede encontrarse en una de las siguientes ubicaciones:
> - En los sistemas operativos Windows XP y Windows Vista, el directorio de instalación de Windows PowerShell ($PSHOME).
> - En los sistemas operativos Windows 7 y Windows 8, la siguiente carpeta: Windows\assembly\GAC_MSIL\System.Management.Automation. 
  
No cargue el complemento de administración de Exchange 2013 en el espacio de ejecución en los equipos que ejecutan aplicaciones que automatizan los cmdlets del shell de administración de Exchange. La aplicación debe crear en su lugar un espacio de ejecución remoto, tal como se describe más adelante en este artículo.

<a name="bk_gettinglistmailbox"> </a>

## <a name="connect-to-a-remote-runspace-on-an-exchange-server"></a>Conectarse a un espacio de ejecución remoto en un servidor Exchange

El método que utilice para conectarse a un espacio de ejecución remoto para usar un cmdlet de Shell de administración de Exchange varía en función del esquema de autenticación que esté utilizando. Esta sección proporciona ejemplos de código que muestran cómo conectarse a un espacio de ejecución remoto cuando utiliza un método de autenticación indicado en la tabla siguiente.
  
|**Método de autenticación**|**Se aplica a**|**URI**|
|:-----|:-----|:-----|
|[Conéctese a un espacio de ejecución remoto de Exchange Online mediante una autenticación básica](#bk_basic) <br/> |Servidores Exchange Online  <br/> |`https://outlook.office365.com/PowerShell-LiveID`<br/><br/>`https://<server>/PowerShell-LiveID`  <br/> |
|[Conectarse a un espacio de ejecución remoto mediante la autenticación de certificados](#bk_cert) <br/> |Servidores Exchange Online y Exchange local  <br/> |`https://outlook.office365.com/PowerShell`<br/><br/>`https://<server>/PowerShell`<br/><br/>`http://<server>/PowerShell`  <br/> |
|[Conectarse a un espacio de ejecución remoto del servidor Exchange mediante una autenticación Kerberos](#bk_Kerberos) <br/> |Servidores Exchange Online y Exchange local  <br/> |`https://<server>/PowerShell`<br/><br/>`http://<server>/PowerShell`  <br/> |

<a name="bk_basic"> </a>

### <a name="connect-to-a-remote-runspace-on-exchange-online-by-using-basic-authentication"></a>Conéctese a un espacio de ejecución remoto de Exchange Online mediante una autenticación básica

El siguiente ejemplo de código define el método **GetUsersUsingBasicAuth**, que crea un espacio de ejecución de Shell de administración de Exchange en un servidor remoto de Exchange Online mediante autenticación básica. A continuación, el método invoca al método **GetUserInformation**, tal como se define en la sección [Conseguir una lista de los usuarios de buzones de correo desde un espacio de ejecución remoto](#bk_remote), para devolver una lista de usuarios en el servidor remoto.
  
Este método requiere los siguientes parámetros:
  
-  **liveIDConnectionUri** &ndash; Una cadena que contiene el URI del servidor de Exchange online que autenticará la aplicación. Si Exchange Online se está ejecutando en Office 365, el URI es `https://outlook.office365.com/PowerShell-LiveID` ; de lo contrario, el URI es `https://<servername>/PowerShell-LiveID` . 
    
-  **schemaUri** &ndash; Una cadena que contiene el URI del documento de esquema que define el esquema del shell de administración de Exchange. El URI del esquema es `https://schemas.microsoft.com/powershell/Microsoft.Exchange` . 
    
-  **credenciales** &ndash; Un objeto [PSCredential](https://msdn.microsoft.com/library/system.management.automation.pscredential%28VS.85%29.aspx) que contiene las credenciales del usuario que está ejecutando la aplicación. 
    
-  **número** &ndash; de Número de usuarios de buzones de Exchange que se van a devolver. 
    
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

<a name="bk_cert"> </a>

### <a name="connect-to-a-remote-runspace-by-using-certificate-authentication"></a>Conectarse a un espacio de ejecución remoto mediante la autenticación de certificados

El siguiente ejemplo de código define el método **GetUsersUsingCertificate**, que crea un espacio de ejecución del Shell de administración de Exchange en un servidor remoto mediante un certificado. A continuación, el método invoca al método **GetUserInformation**, tal como se define en la sección [Conseguir una lista de los usuarios de buzones de correo desde un espacio de ejecución remoto](#bk_remote), para devolver una lista de usuarios en el servidor remoto.
  
Este método requiere los siguientes parámetros:
  
-  **huella digital** &ndash; Una cadena que contiene la huella digital del certificado que se usa para autenticar la aplicación. 
    
-  **certConnectionUri** &ndash; Una cadena que contiene el URI del servidor que va a autenticar el certificado. El URI será uno de los recogidos en la tabla siguiente. 
    
    **Tabla 1. URI de certConnectionUri**

    |**Servidor**|**URI**|
    |:-----|:-----|
    |Servidor Exchange sin SSL  <br/> |`http://<servername>/PowerShell`  <br/> |
    |Servidor Exchange con SSL  <br/> |`https://<servername>/PowerShell`  <br/> |
    |Exchange Online como parte de Office 365  <br/> |`https://outlook.office365.com/PowerShell`  <br/> |
   
- **schemaUri** &ndash; Una cadena que contiene el URI del documento de esquema que define el esquema del shell de administración de Exchange. El URI del esquema es https://schemas.microsoft.com/powershell/Microsoft.Exchange . 
    
- **número** &ndash; de Número de usuarios de buzones de Exchange que se van a devolver. 
    
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

<a name="bk_Kerberos"> </a>

### <a name="connect-to-a-remote-runspace-on-an-exchange-server-by-using-kerberos-authentication"></a>Conectarse a un espacio de ejecución remoto del servidor Exchange mediante una autenticación Kerberos

El siguiente ejemplo de código define el método **GetUsersUsingKerberos**, que crea un espacio de ejecución del Shell de administración de Exchange en un servidor remoto mediante la autenticación Kerberos. A continuación, el método invoca al método **GetUserInformation**, tal como se define en la sección [Conseguir una lista de los usuarios de buzones de correo desde un espacio de ejecución remoto](#bk_remote), para devolver una lista de usuarios en el servidor remoto.
  
Este método requiere los siguientes parámetros:
  
- **kerberosUri** &ndash; Una cadena que contiene el URI del servidor Kerberos que autenticará la aplicación. El URI será uno de los recogidos en la tabla siguiente. 
    
    **Tabla 2. URI de kerberosUri**

    |**Servidor**|**URI**|
    |:-----|:-----|
    |Servidor Exchange sin SSL  <br/> |`http://<servername>/PowerShell`  <br/> |
    |Servidor Exchange con SSL  <br/> |`https://<servername>/PowerShell`  <br/> |
   
- **schemaUri** &ndash; Una cadena que contiene el URI del documento de esquema que define el esquema del shell de administración de Exchange. El URI del esquema es https://schemas.microsoft.com/powershell/Microsoft.Exchange . 
    
- **credenciales** &ndash; Un objeto [PSCredential](https://msdn.microsoft.com/library/system.management.automation.pscredential%28VS.85%29.aspx) que contiene las credenciales del usuario que está ejecutando la aplicación. 
    
- **número** &ndash; de Número de usuarios de buzones de Exchange que se van a devolver. 
    
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

<a name="bk_remote"> </a>

## <a name="get-a-list-of-mailbox-users-from-a-remote-runspace"></a>Conseguir una lista de los usuarios de buzones de correo desde un espacio de ejecución remoto

El siguiente ejemplo de código define el método **GetUserInformation** , que devuelve una colección de instancias de [PSObject](https://msdn.microsoft.com/library/system.management.automation.pscredential%28VS.85%29.aspx) que representan usuarios de buzones de correo de Exchange. También se puede invocar este método mediante los métodos **GetUsersUsingBasicAuth**, **GetUsersUsingCertificate** y **GetUsersUsingKerberos** para obtener la lista de usuarios desde el servidor remoto. 
  
Este método requiere los siguientes parámetros:
  
- **número** &ndash; de Número de usuarios de buzones de Exchange que se van a devolver. 
    
- **runspace** &ndash; El espacio de ejecución remoto que se establece para el servidor remoto de Exchange. 
    
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

El método **GetUserInformation** no devolverá más que el _número_ de usuarios de buzones. Para simplificar el código de este ejemplo, el método no filtra ni limita a los usuarios del buzón de correo que se obtienen. 
  
## <a name="see-also"></a>Vea también

- [Crear herramientas de Shell de administración de Exchange](create-exchange-management-shell-tools.md)   
- [Usar la respuesta del cmdlet de Shell de administración de Exchange](how-to-use-the-exchange-management-shell-cmdlet-response.md)
    

