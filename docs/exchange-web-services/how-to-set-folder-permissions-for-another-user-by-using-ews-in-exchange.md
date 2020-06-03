---
title: Establecer los permisos de carpeta para otro usuario mediante EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb81676-a780-4c56-b4f2-c4ed2697107d
description: Obtenga información sobre cómo establecer niveles de permisos en una carpeta mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: e25f1a49a430e8c95829d404fa53451b76cab167
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455873"
---
# <a name="set-folder-permissions-for-another-user-by-using-ews-in-exchange"></a>Establecer los permisos de carpeta para otro usuario mediante EWS en Exchange

Obtenga información sobre cómo establecer niveles de permisos en una carpeta mediante la API administrada de EWS o EWS en Exchange.
  
Los permisos de nivel de carpeta permiten a los usuarios tener acceso a una o más carpetas en el buzón de otro usuario. Los permisos de carpeta son similares a acceso delegado, pero se diferencian en los siguientes aspectos: 
  
- Los permisos de carpeta no permiten a un usuario "enviar en nombre de" o "enviar como" otro usuario. Solo permiten el acceso a las carpetas. Los usuarios pueden crear elementos en esas carpetas, pero no pueden enviarlos.
    
- Puede establecer los permisos de carpeta en cualquier carpeta del buzón, pero solo puede Agregar un delegado a las carpetas calendario, contactos, bandeja de entrada, diario, notas y tareas.
    
- Puede establecer un número de [permisos en una carpeta específica](#bk_folderperms). Al agregar un delegado, puede asignar uno de estos [cinco niveles de permisos](delegate-access-and-ews-in-exchange.md#bk_delegateperms).
    
- Puede establecer los permisos de carpeta para usuarios anónimos y predeterminados. Solo puede conceder acceso delegado a una cuenta habilitada para correo.
    
Si está familiarizado con las entradas de control de acceso (ACE) y las listas de control de acceso discrecional (DACL), sabrá que un usuario solo puede tener un conjunto de permisos para cada carpeta. Si intenta agregar un conjunto de permisos para un usuario y ya tienen un conjunto de permisos, recibirá un error. Al agregar, quitar o actualizar permisos en una carpeta, se obtiene la DACL actual, se agregan o se quitan todas las ACE y, a continuación, se envía la DACL actualizada. No se pueden agregar varias ACE para el mismo usuario. Al actualizar los permisos mediante la API administrada de EWS, debe quitar la ACE actual del usuario y, a continuación, agregar la nueva ACE a la colección. Si está usando EWS, solo tiene que reemplazar el conjunto anterior de ACE por los nuevos.
  
Si está realizando varios cambios de permisos en una sola carpeta, puede realizar adiciones, eliminaciones o actualizaciones por lotes (solo tiene en cuenta que no puede realizar actualizaciones de usuario por lotes en varias carpetas). Se necesita una llamada para obtener los permisos en una carpeta única y se necesita una segunda llamada para actualizar los permisos en esa carpeta. Cuando se agregan, quitan o actualizan permisos de usuario, se usan las mismas dos llamadas a métodos u operaciones para cada tarea.
  
**Tabla 1. Métodos de API administrada de EWS y operaciones EWS para establecer permisos de carpeta**

|Si quiere...|Use este método de API administrada de EWS...|Usar esta operación de EWS...|
|:-----|:-----|:-----|
|Habilitar, quitar o actualizar los permisos de carpeta  <br/> |[Folder. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) seguido de [Folder. Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) <br/> |[GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) seguida de [UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |
|Crear una carpeta y definir los permisos de carpeta  <br/> |[Folder. Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx) <br/> |[CreateFolder](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
   
## <a name="folder-permissions"></a>Permisos de carpeta
<a name="bk_folderperms"> </a>

Tiene algunas opciones cuando se trata de establecer los permisos de carpeta en una carpeta específica. Puede establecer un nivel de permisos en una carpeta para cada usuario, que agrega un conjunto de permisos individuales predefinidos a la DACL, o puede establecer permisos individuales en una carpeta, pero no puede combinar y hacer coincidir.
  
Están disponibles los siguientes permisos individuales:
  
- Puede crear
- Puede crear subcarpetas    
- Es el propietario de la carpeta    
- La carpeta es visible    
- Es contacto de carpeta    
- Editar elementos    
- Eliminar elementos    
- Leer elementos
    
Además, están disponibles los siguientes niveles de permisos, que definen un subconjunto de valores y permisos individuales, como se muestra en la tabla 2:
  
- None    
- Owner    
- Publishingeditorcreateitems    
- Editor    
- Publishingauthorcreateitems    
- Autor    
- Noneditingauthorcreateitems    
- Reviewer    
- Colaborador   
- Custom: la aplicación no puede establecer este valor. El servidor establece este valor si la aplicación incluye una colección personalizada de permisos individuales.    
- FreeBusyTimeOnly: solo puede establecerse en las carpetas de calendario.   
- FreeBusyTimeAndSubjectAndLocation: solo puede establecerse en las carpetas de calendario.
    
En la siguiente tabla se muestran los permisos individuales que se aplican de forma predeterminada en función del nivel de permisos.
  
**Tabla 2. Permisos individuales por nivel de permisos**

|Nivel de permisos|Puede crear elementos|Puede crear subcarpetas|Es el propietario de la carpeta|La carpeta es visible|Es contacto de carpeta|Editar elementos|Eliminar elementos|Puede leer elementos|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|None  <br/> |Falso  <br/> |Falso  <br/> |Falso  <br/> |Falso  <br/> |Falso  <br/> |Ninguno  <br/> |Ninguno  <br/> |Ninguno  <br/> |
|Owner  <br/> |True  <br/> |True  <br/> |True  <br/> |True  <br/> |Verdadero  <br/> |Todo  <br/> |Todo  <br/> |FullDetails  <br/> |
|Publishingeditorcreateitems  <br/> |True  <br/> |Verdadero  <br/> |False  <br/> |True  <br/> |Falso  <br/> |Todo  <br/> |Todo  <br/> |FullDetails  <br/> |
|Editor  <br/> |Verdadero  <br/> |Falso  <br/> |False  <br/> |True  <br/> |Falso  <br/> |Todo  <br/> |Todo  <br/> |FullDetails  <br/> |
|Publishingauthorcreateitems  <br/> |True  <br/> |Verdadero  <br/> |False  <br/> |True  <br/> |Falso  <br/> |Estatal  <br/> |Estatal  <br/> |FullDetails  <br/> |
|Autor  <br/> |Verdadero  <br/> |Falso  <br/> |False  <br/> |True  <br/> |Falso  <br/> |Estatal  <br/> |Estatal  <br/> |FullDetails  <br/> |
|Noneditingauthorcreateitems  <br/> |Verdadero  <br/> |Falso  <br/> |False  <br/> |True  <br/> |Falso  <br/> |None  <br/> |Estatal  <br/> |FullDetails  <br/> |
|Reviewer  <br/> |Falso  <br/> |Falso  <br/> |False  <br/> |True  <br/> |Falso  <br/> |Ninguno  <br/> |Ninguno  <br/> |FullDetails  <br/> |
|Colaborador  <br/> |Verdadero  <br/> |Falso  <br/> |False  <br/> |True  <br/> |Falso  <br/> |Ninguno  <br/> |Ninguno  <br/> |Ninguno  <br/> |
   
Si especifica un nivel de permisos no personalizado en la solicitud de permisos de nivel de carpeta, no es necesario especificar la configuración de permisos individuales. Si especifica un permiso individual al establecer un nivel de permisos, se devolverá un error **ErrorInvalidPermissionSettings** en la respuesta. 
  
## <a name="adding-folder-permissions-by-using-the-ews-managed-api"></a>Adición de permisos de carpeta mediante la API administrada de EWS
<a name="bk_enableewsma"> </a>

En el siguiente ejemplo de código se muestra cómo usar la API administrada de EWS para: 
  
- Cree un nuevo objeto [FolderPermission](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderpermission%28v=exchg.80%29.aspx) para el nuevo usuario. 
    
- Obtener los permisos actuales para una carpeta mediante el método [BIND](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) . 
    
- Agregue el nuevo **FolderPermissions** a la propiedad [Folder. Permissions](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.permissions%28v=exchg.80%29.aspx) . 
    
- Llame al método [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) para guardar los nuevos permisos en el servidor. 
    
En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido para el propietario del buzón y que el usuario se ha autenticado en un servidor de Exchange. 
  
```cs
static void EnableFolderPermissions(ExchangeService service)
{
    // Create a property set to use for folder binding.
    PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, FolderSchema.Permissions);
    // Specify the SMTP address of the new user and the folder permissions level.
    FolderPermission fldperm = new FolderPermission("sadie@contoso.com", FolderPermissionLevel.Editor);
    
    // Bind to the folder and get the current permissions. 
    // This call results in a GetFolder call to EWS.
    Folder sentItemsFolder = Folder.Bind(service, WellKnownFolderName.SentItems, propSet);
 
    // Add the permissions for the new user to the Sent Items DACL.
    sentItemsFolder.Permissions.Add(fldperm);
    // This call results in a UpdateFolder call to EWS.
    sentItemsFolder.Update();
}
```

La siguiente línea de código especifica el nivel de permisos.
  
```cs
    FolderPermission fldperm = new FolderPermission("sadie@contoso.com", FolderPermissionLevel.Editor);
```

Si desea usar el nivel de permisos personalizado, use este código en su lugar.
  
```cs
FolderPermission fldperm = new FolderPermission();
fldperm.UserId = "sadie@Contoso1000.onmicrosoft.com";
fldperm.CanCreateItems = true;
fldperm.CanCreateSubFolders = true;
…
```

Puede establecer cualquiera o todas las [propiedades FolderPermission](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderpermission_properties%28v=exchg.80%29.aspx) de escritura al crear un objeto **FolderPermission** con un nivel de permisos personalizado. Sin embargo, tenga en cuenta que [FolderPermissionLevel](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderpermissionlevel%28v=exchg.80%29.aspx) nunca se establece de forma explícita en **personalizada** por la aplicación. **FolderPermissionLevel** se establece en personalizado solo cuando se crea un objeto **FolderPermission** y se establecen permisos individuales. 
  
## <a name="adding-folder-permissions-by-using-ews"></a>Adición de permisos de carpeta mediante EWS
<a name="bk_enableews"> </a>

Los siguientes ejemplos de código de EWS muestran cómo agregar permisos a una carpeta específica mediante la recuperación de los permisos actuales y el envío de una lista de nuevos permisos.
  
El primer paso es enviar una solicitud [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) , donde el valor [DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) especifica la carpeta en la que se van a agregar permisos (la carpeta elementos enviados en este ejemplo) y el valor [FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) incluye Folder: PermissionSet. Esta solicitud recuperará la configuración de permisos para la carpeta especificada. 
  
También es la solicitud XML que la API administrada de EWS envía cuando se llama al método **BIND** para [Agregar permisos de carpeta](#bk_enableewsma).
  
```XML
  <?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                 xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
    <soap:Header>
      <t:RequestServerVersion Version="Exchange2007_SP1" />
    </soap:Header>
    <soap:Body>
      <m:GetFolder>
        <m:FolderShape>
          <t:BaseShape>IdOnly</t:BaseShape>
          <t:AdditionalProperties>
            <t:FieldURI FieldURI="folder:PermissionSet" />
          </t:AdditionalProperties>
        </m:FolderShape>
        <m:FolderIds>
          <t:DistinguishedFolderId Id="sentitems" />
        </m:FolderIds>
      </m:GetFolder>
    </soap:Body>
  </soap:Envelope>
```

El servidor responde a la solicitud **GetFolder** con un mensaje [GetFolderResponse](https://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que la carpeta se recuperó correctamente. Los valores [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) y [ParentFolderId](https://msdn.microsoft.com/library/258f4b1f-367e-4c7d-9c29-eb775a2398c7%28Office.15%29.aspx) se han abreviado por legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="CgAAAA=="
                          ChangeKey="AQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiRd1" />
              <t:PermissionSet>
                <t:Permissions>
                  <t:Permission>
                    <t:UserId>
                      <t:DistinguishedUser>Default</t:DistinguishedUser>
                    </t:UserId>
                    <t:CanCreateItems>false</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>false</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>None</t:EditItems>
                    <t:DeleteItems>None</t:DeleteItems>
                    <t:ReadItems>None</t:ReadItems>
                    <t:PermissionLevel>None</t:PermissionLevel>
                  </t:Permission>
                  <t:Permission>
                    <t:UserId>
                      <t:DistinguishedUser>Anonymous</t:DistinguishedUser>
                    </t:UserId>
                    <t:CanCreateItems>false</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>false</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>None</t:EditItems>
                    <t:DeleteItems>None</t:DeleteItems>
                    <t:ReadItems>None</t:ReadItems>
                    <t:PermissionLevel>None</t:PermissionLevel>
                  </t:Permission>
                </t:Permissions>
              </t:PermissionSet>
            </t:Folder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

A continuación, use la operación **UpdateFolder** para enviar el [PermissionSet](https://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx)actualizado, que incluye el [permiso](https://msdn.microsoft.com/library/b8d0429a-0e58-4480-9847-4901970c7033%28Office.15%29.aspx) para el nuevo usuario. Tenga en cuenta que, si se incluye el elemento [SetFolderField](https://msdn.microsoft.com/library/8c69db7b-54b5-4ae2-abca-4d6e0937a790%28Office.15%29.aspx) para la carpeta respectiva en la operación [UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) , se sobrescribirá toda la configuración de permisos de la carpeta. Del mismo modo, si se incluye la opción [DeleteFolderField](https://msdn.microsoft.com/library/f9c2187b-4c60-4358-b4b4-ede50eadae48%28Office.15%29.aspx) de la operación **UpdateFolder** , también se eliminará la configuración de todos los permisos de la carpeta. 
  
También es la solicitud XML que la API administrada de EWS envía cuando se llama al método **Update** para [Agregar permisos de carpeta](#bk_enableewsma).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:UpdateFolder>
      <m:FolderChanges>
        <t:FolderChange>
          <t:FolderId Id="CgAAAA=="
                      ChangeKey="AQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiRd1" />
          <t:Updates>
            <t:SetFolderField>
              <t:FieldURI FieldURI="folder:PermissionSet" />
              <t:Folder>
                <t:PermissionSet>
                  <t:Permissions>
                    <t:Permission>
                      <t:UserId>
                        <t:DistinguishedUser>Default</t:DistinguishedUser>
                      </t:UserId>
                      <t:PermissionLevel>None</t:PermissionLevel>
                    </t:Permission>
                    <t:Permission>
                      <t:UserId>
                        <t:DistinguishedUser>Anonymous</t:DistinguishedUser>
                      </t:UserId>
                      <t:PermissionLevel>None</t:PermissionLevel>
                    </t:Permission>
                    <t:Permission>
                      <t:UserId>
                        <t:PrimarySmtpAddress>sadie@contoso.com</t:PrimarySmtpAddress>
                      </t:UserId>
                      <t:PermissionLevel>Editor</t:PermissionLevel>
                    </t:Permission>
                  </t:Permissions>
                </t:PermissionSet>
              </t:Folder>
            </t:SetFolderField>
          </t:Updates>
        </t:FolderChange>
      </m:FolderChanges>
    </m:UpdateFolder>
  </soap:Body>
</soap:Envelope>
```

La siguiente línea de código especifica el nivel de permisos.
  
```xml
<t:Permission>
    <t:UserId>
        <t:PrimarySmtpAddress>sadie@contoso.com</t:PrimarySmtpAddress>
    </t:UserId>
    <t:PermissionLevel>Editor</t:PermissionLevel>
</t:Permission>
```

Si desea usar el nivel de permisos personalizado, use este código en su lugar.
  
```xml
<t:Permission>
    <t:UserId>
        <t:PrimarySmtpAddress> sadie@contoso.com </t:PrimarySmtpAddress>
    </t:UserId>
    <t:CanCreateItems>true</t:CanCreateItems>
    <t:CanCreateSubFolders>true</t:CanCreateSubFolders>
    <t:IsFolderOwner>false</t:IsFolderOwner>
    <t:IsFolderVisible>false</t:IsFolderVisible>
    <t:IsFolderContact>false</t:IsFolderContact>
    <t:EditItems>None</t:EditItems>
    <t:DeleteItems>None</t:DeleteItems>
    <t:ReadItems>None</t:ReadItems>
    <t:PermissionLevel>Custom</t:PermissionLevel>
</t:Permission>
```

El servidor responde a la solicitud **UpdateFolder** con un mensaje [UpdateFolderResponse](https://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) que incluye el valor de un elemento [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que la carpeta se actualizó correctamente.
  
## <a name="removing-folder-permissions-by-using-the-ews-managed-api"></a>Eliminación de los permisos de carpeta mediante la API administrada de EWS
<a name="bk_removeewsma"> </a>

En el siguiente ejemplo de código se muestra cómo usar la API administrada de EWS para quitar todos los permisos de usuario en una carpeta específica, excepto para los permisos predeterminados y anónimos, por:
  
1. Obtener los permisos actuales para una carpeta mediante el método **BIND** . 
    
2. Recorrer en iteración la colección de **permisos** y quitar permisos para usuarios individuales. 
    
3. Llamar al método **Update** para guardar los cambios. 
    
En este ejemplo se quitan todos los permisos de usuario de una carpeta. Si desea modificar este ejemplo para quitar permisos sólo para un usuario específico, cambie la siguiente línea de código para identificar el nombre para mostrar o la dirección SMTP del usuario.
  
```cs
if (sentItemsFolder.Permissions[t].UserId.DisplayName != null || sentItemsFolder.Permissions[t].UserId.PrimarySmtpAddress != null)
```

En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido para el propietario del buzón y que el usuario se ha autenticado en un servidor de Exchange. 
  
```cs
static void RemoveFolderPermissions(ExchangeService service)
{
    // Create a property set to use for folder binding.
    PropertySet propSet = new PropertySet(BasePropertySet.FirstClassProperties, FolderSchema.Permissions);
    // Bind to the folder and get the current permissions. 
    // This call results in a GetFolder call to EWS.
    Folder sentItemsFolder = Folder.Bind(service, new FolderId(WellKnownFolderName.SentItems, "primary@contoso.com"), propSet);
    // Iterate through the collection of permissions and remove permissions for any 
    // user with a display name or SMTP address. This leaves the anonymous and 
    // default user permissions unchanged. 
    if (sentItemsFolder.Permissions.Count != 0)
    {
        for (int t = 0; t < sentItemsFolder.Permissions.Count; t++)
        {
            // Find any permissions associated with the specified user and remove them from the DACL
            if (sentItemsFolder.Permissions[t].UserId.DisplayName != null || sentItemsFolder.Permissions[t].UserId.PrimarySmtpAddress != null)
            {
                sentItemsFolder.Permissions.Remove(sentItemsFolder.Permissions[t]);
            }
        }
    }
    // This call results in an UpdateFolder call to EWS.
    sentItemsFolder.Update();
}
```

## <a name="removing-folder-permissions-by-using-ews"></a>Quitar permisos de carpeta mediante EWS
<a name="bk_removeews"> </a>

Los siguientes ejemplos de código de EWS muestran cómo quitar todos los permisos de usuario en una carpeta específica, excepto los permisos predeterminados y anónimos.
  
En primer lugar, envíe una solicitud [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) donde el valor [DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) especifica la carpeta en la que se van a quitar los permisos (la carpeta elementos enviados en este ejemplo) y el valor [FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) incluye Folder: PermissionSet. Esta solicitud recuperará el [PermissionSet](https://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx) para la carpeta especificada. 
  
También es la solicitud XML que la API administrada de EWS envía cuando se llama al método **BIND** para [quitar permisos de carpeta](#bk_removeewsma).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:GetFolder>
      <m:FolderShape>
        <t:BaseShape>AllProperties</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="folder:PermissionSet" />
        </t:AdditionalProperties>
      </m:FolderShape>
      <m:FolderIds>
        <t:DistinguishedFolderId Id="drafts">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:FolderIds>
    </m:GetFolder>
  </soap:Body>
</soap:Envelope>
```

El servidor responde a la solicitud **GetFolder** con un mensaje [GetFolderResponse](https://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que la carpeta se recuperó correctamente. Los valores de los elementos **FolderId** y **ParentFolderId** se han abreviado para facilitar su lectura. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="EAAAAA=="
                          ChangeKey="AQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiRd5" />
              <t:ParentFolderId Id="CQAAAA=="
                                ChangeKey="AQAAAA==" />
              <t:FolderClass>IPF.Note</t:FolderClass>
              <t:DisplayName>Drafts</t:DisplayName>
              <t:TotalCount>0</t:TotalCount>
              <t:ChildFolderCount>0</t:ChildFolderCount>
              <t:EffectiveRights>
                <t:CreateAssociated>true</t:CreateAssociated>
                <t:CreateContents>true</t:CreateContents>
                <t:CreateHierarchy>true</t:CreateHierarchy>
                <t:Delete>true</t:Delete>
                <t:Modify>true</t:Modify>
                <t:Read>true</t:Read>
                <t:ViewPrivateItems>true</t:ViewPrivateItems>
              </t:EffectiveRights>
              <t:PermissionSet>
                <t:Permissions>
                  <t:Permission>
                    <t:UserId>
                      <t:DistinguishedUser>Default</t:DistinguishedUser>
                    </t:UserId>
                    <t:CanCreateItems>false</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>false</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>None</t:EditItems>
                    <t:DeleteItems>None</t:DeleteItems>
                    <t:ReadItems>None</t:ReadItems>
                    <t:PermissionLevel>None</t:PermissionLevel>
                  </t:Permission>
                  <t:Permission>
                    <t:UserId>
                      <t:DistinguishedUser>Anonymous</t:DistinguishedUser>
                    </t:UserId>
                    <t:CanCreateItems>false</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>false</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>None</t:EditItems>
                    <t:DeleteItems>None</t:DeleteItems>
                    <t:ReadItems>None</t:ReadItems>
                    <t:PermissionLevel>None</t:PermissionLevel>
                  </t:Permission>
                  <t:Permission>
                    <t:UserId>
                      <t:SID>S-1-5-21-1337771579-694202782-848329751-1535223</t:SID>
                      <t:PrimarySmtpAddress>sadie@Contoso.com</t:PrimarySmtpAddress>
                      <t:DisplayName>Sadie Daniels</t:DisplayName>
                    </t:UserId>
                    <t:CanCreateItems>true</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>true</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>All</t:EditItems>
                    <t:DeleteItems>All</t:DeleteItems>
                    <t:ReadItems>FullDetails</t:ReadItems>
                    <t:PermissionLevel>Editor</t:PermissionLevel>
                  </t:Permission>
                </t:Permissions>
              </t:PermissionSet>
              <t:UnreadCount>0</t:UnreadCount>
            </t:Folder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

A continuación, use la operación **UpdateFolder** para enviar el **PermissionSet**actualizado, que no incluye el **permiso** para el usuario quitado. 
  
También es la solicitud XML que la API administrada de EWS envía cuando se llama al método **Update** para [quitar los permisos de carpeta](#bk_removeewsma).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:UpdateFolder>
      <m:FolderChanges>
        <t:FolderChange>
          <t:FolderId Id="EAAAAA=="
                      ChangeKey="AQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiRd5" />
          <t:Updates>
            <t:SetFolderField>
              <t:FieldURI FieldURI="folder:PermissionSet" />
              <t:Folder>
                <t:PermissionSet>
                  <t:Permissions>
                    <t:Permission>
                      <t:UserId>
                        <t:DistinguishedUser>Default</t:DistinguishedUser>
                      </t:UserId>
                      <t:PermissionLevel>None</t:PermissionLevel>
                    </t:Permission>
                    <t:Permission>
                      <t:UserId>
                        <t:DistinguishedUser>Anonymous</t:DistinguishedUser>
                      </t:UserId>
                      <t:PermissionLevel>None</t:PermissionLevel>
                    </t:Permission>
                  </t:Permissions>
                </t:PermissionSet>
              </t:Folder>
            </t:SetFolderField>
          </t:Updates>
        </t:FolderChange>
      </m:FolderChanges>
    </m:UpdateFolder>
  </soap:Body>
</soap:Envelope>
```

El servidor responde a la solicitud **UpdateFolder** con un mensaje **UpdateFolderResponse** que incluye un valor de elemento [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que la actualización se realizó correctamente.
  
## <a name="updating-folder-permissions-by-using-the-ews-managed-api"></a>Actualización de permisos de carpeta mediante la API administrada de EWS
<a name="bk_updateewsma"> </a>

También puede actualizar los permisos de carpeta para una carpeta específica mediante la API administrada de EWS. Para actualizar los permisos: 
  
1. [Quite los permisos de carpeta](#bk_removeewsma) para los permisos obsoletos, pero no llame al método **Update** (todavía). 
    
2. [Agregar permisos de carpeta para los usuarios nuevos o modificados](#bk_enableewsma).
    
3. Llame al método **Update** para guardar los cambios. 
    
Si intenta agregar dos conjuntos de permisos para el mismo usuario, recibirá un error **ServiceResponseException** con la siguiente descripción: "el conjunto de permisos especificado contiene identificadores de usuario duplicados". En ese caso, quite los permisos actuales de la colección **Permission** y, a continuación, agregue los nuevos permisos a la colección **Permission** . 
  
## <a name="updating-folder-permissions-by-using-ews"></a>Actualización de permisos de carpeta mediante EWS
<a name="bk_updateews"> </a>

También puede actualizar los permisos de carpeta para carpetas específicas usando EWS mediante la combinación del proceso de eliminación y adición. Para actualizar los permisos: 
  
1. Recupere los permisos actuales de la carpeta mediante la operación **GetFolder** . 
    
2. Envíe una lista actualizada de permisos mediante la operación **UpdateFolder** . 
    
Estas son las mismas dos operaciones que se usan para [Habilitar](#bk_enableews) o [quitar el acceso](#bk_removeews) mediante EWS. La única diferencia es que, cuando recibe la respuesta **GetFolder** , contendrá un conjunto de **permisos** para User. Simplemente reemplace el elemento de **permiso** existente con el nuevo elemento **Permission** y, a continuación, envíe la operación **UpdateFolder** con el nuevo valor o valores de **permiso** . 
  
Si intenta agregar dos conjuntos de permisos para el mismo usuario, recibirá un valor **ResponseCode** de **ErrorDuplicateUserIdsSpecified**. En ese caso, quite el valor de permiso obsoleto del usuario de la solicitud y, a continuación, vuelva a intentar la solicitud.

## <a name="next-steps"></a>Siguientes pasos

Después de conceder a un usuario permiso para una carpeta específica, el usuario puede tener acceso a la carpeta como delegado. Para más información, consulte lo siguiente:
  
- [Obtener acceso al correo electrónico como delegado mediante EWS en Exchange](how-to-access-email-as-a-delegate-by-using-ews-in-exchange.md)
    
- [Obtener acceso a un calendario como delegado mediante EWS en Exchange](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md)
    
- [Obtener acceso a los contactos como un delegado mediante EWS en Exchange](how-to-access-contacts-as-a-delegate-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>Vea también

- [Acceso delegado y EWS en Exchange](delegate-access-and-ews-in-exchange.md)   
- [Agregar y quitar delegados mediante EWS en Exchange](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)    
- [Carpetas y elementos de EWS en Exchange](folders-and-items-in-ews-in-exchange.md)
    

