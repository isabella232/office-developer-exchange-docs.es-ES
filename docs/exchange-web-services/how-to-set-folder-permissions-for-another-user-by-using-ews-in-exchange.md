---
title: Establecer permisos de carpeta de otro usuario mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb81676-a780-4c56-b4f2-c4ed2697107d
description: Obtenga información sobre cómo establecer los niveles de permisos en una carpeta mediante el uso de la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 5bf570612d6349628e7f3abf858daa33daa13745
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763178"
---
# <a name="set-folder-permissions-for-another-user-by-using-ews-in-exchange"></a>Establecer permisos de carpeta de otro usuario mediante el uso de EWS en Exchange

Obtenga información sobre cómo establecer los niveles de permisos en una carpeta mediante el uso de la API administrada de EWS o EWS en Exchange.
  
Permisos de nivel de carpeta permiten a los usuarios tener acceso a una o varias carpetas en el buzón de otro usuario. Permisos de carpeta son similares a la delegación de acceso, pero se diferencian de las siguientes maneras: 
  
- Permisos de carpeta no habilitar a un usuario para "enviar en nombre de" o "Enviar como" otro usuario. Sólo permiten el acceso a las carpetas. Los usuarios pueden crear elementos en esas carpetas, pero no puede enviarlos.
    
- Puede establecer permisos de carpetas en cualquier carpeta en el buzón de correo, pero sólo se puede agregar a un delegado a las carpetas de calendario, contactos, Bandeja de entrada, diario, notas y tareas.
    
- Puede establecer un número de [permisos en una carpeta específica](#bk_folderperms). Cuando se agrega un delegado, puede asignar uno de sólo [cinco niveles de permisos](delegate-access-and-ews-in-exchange.md#bk_delegateperms).
    
- Puede establecer los permisos de carpeta anónimo y establecer como predeterminado a los usuarios. Sólo puede conceder acceso de delegado a una cuenta habilitada para correo.
    
Si está familiarizado con entradas de Control de acceso (ACE) y listas de Control de acceso discrecional (DACL), sabrá que un usuario sólo puede tener un conjunto de permisos para cada carpeta. Si intenta agregar un conjunto de permisos para un usuario y ya tienen un conjunto de permisos, obtendrá un error. Al agregar, quitar o actualizar los permisos en una carpeta, que obtener la DACL actual, agrega o quita cualquier ACE y, a continuación, enviar la DACL actualizada. No se puede agregar varias entradas ACE para el mismo usuario. Al actualizar los permisos mediante el uso de la API administrada de EWS, debe quitar la ACE actual del usuario y, a continuación, agregar su nueva ACE a la colección. Si está usando EWS, solo tendrá que cambiar el conjunto de las entradas ACE anterior con los nuevos.
  
Si está realizando varios cambios en los permisos para una sola carpeta, puede procesar por lotes las adiciones, eliminaciones o actualizaciones, tenga en cuenta que no se puede procesar por lotes las actualizaciones del usuario en varias carpetas. Es necesaria una llamada para obtener los permisos en una sola carpeta, y una segunda llamada es necesario para actualizar los permisos en esa carpeta. Al agregar, quitar o actualizar los permisos de usuario, se utiliza el mismo dos llamadas al método u operaciones para cada tarea.
  
**La tabla 1. Métodos de la API administrada de EWS y las operaciones de EWS para establecer los permisos de carpeta**

|Si quiere...|Use este método de la API administrada de EWS...|Use esta operación de EWS...|
|:-----|:-----|:-----|
|Habilitar, quitar o actualizar los permisos de carpeta  <br/> |[Folder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) seguido de [Folder.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) <br/> |[GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) seguido [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |
|Cree una carpeta y definir los permisos de carpeta  <br/> |[Folder.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx) <br/> |[CreateFolder](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
   
## <a name="folder-permissions"></a>Permisos de carpeta
<a name="bk_folderperms"> </a>

Tener unas cuantas opciones cuando se trata de establecer los permisos de carpeta en una carpeta específica. Puede establecer un nivel de permisos en una carpeta para cada usuario, que agrega un conjunto de permisos individuales predefinidos a la DACL, o puede establecer los permisos individuales en una carpeta, pero no puede mezclar y match.
  
Los siguientes permisos individuales están disponibles:
  
- Puede crear
- Puede crear subcarpetas    
- Es propietario de la carpeta    
- Es la carpeta visible    
- Es el contacto de carpeta    
- Editar elementos    
- Eliminar elementos    
- Leer elementos
    
Además, los siguientes niveles de permisos están disponibles, que definen un subconjunto de permisos individuales y los valores, como se muestra en la tabla 2:
  
- None    
- Owner    
- PublishingEditor    
- Editor    
- PublishingAuthor    
- Autor    
- NoneditingAuthor    
- Reviewer    
- Colaborador   
- Personalizado - no se puede establecer este valor por la aplicación. El servidor establece este valor si la aplicación incluye una colección personalizada de permisos individuales.    
- FreeBusyTimeOnly - esto sólo se puede establecer en las carpetas de calendario.   
- FreeBusyTimeAndSubjectAndLocation - esto sólo se puede establecer en las carpetas de calendario.
    
En la siguiente tabla muestra qué permisos individuales se aplican de forma predeterminada según el nivel de permisos.
  
**Tabla 2. Permisos individuales por nivel de permisos**

|Nivel de permisos|Puede crear los elementos|Puede crear carpetas de sub|Es propietario de la carpeta|Es la carpeta visible|Es el contacto de carpeta|Editar elementos|Eliminar elementos|Puede leer elementos|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|None  <br/> |False  <br/> |False  <br/> |False  <br/> |False  <br/> |False  <br/> |None  <br/> |None  <br/> |None  <br/> |
|Owner  <br/> |Verdadero  <br/> |Verdadero  <br/> |Verdadero  <br/> |Verdadero  <br/> |Verdadero  <br/> |Todos  <br/> |Todos  <br/> |FullDetails  <br/> |
|PublishingEditor  <br/> |Verdadero  <br/> |Verdadero  <br/> |False  <br/> |Verdadero  <br/> |False  <br/> |Todos  <br/> |Todos  <br/> |FullDetails  <br/> |
|Editor  <br/> |Verdadero  <br/> |False  <br/> |False  <br/> |Verdadero  <br/> |False  <br/> |Todos  <br/> |Todos  <br/> |FullDetails  <br/> |
|PublishingAuthor  <br/> |Verdadero  <br/> |Verdadero  <br/> |False  <br/> |Verdadero  <br/> |False  <br/> |Propiedad  <br/> |Propiedad  <br/> |FullDetails  <br/> |
|Autor  <br/> |Verdadero  <br/> |False  <br/> |False  <br/> |Verdadero  <br/> |False  <br/> |Propiedad  <br/> |Propiedad  <br/> |FullDetails  <br/> |
|NoneditingAuthor  <br/> |Verdadero  <br/> |False  <br/> |False  <br/> |Verdadero  <br/> |False  <br/> |None  <br/> |Propiedad  <br/> |FullDetails  <br/> |
|Reviewer  <br/> |False  <br/> |False  <br/> |False  <br/> |Verdadero  <br/> |False  <br/> |None  <br/> |None  <br/> |FullDetails  <br/> |
|Colaborador  <br/> |Verdadero  <br/> |False  <br/> |False  <br/> |Verdadero  <br/> |False  <br/> |None  <br/> |None  <br/> |None  <br/> |
   
Si especifica un nivel de permisos no personalizada en la solicitud de permisos de nivel de carpeta, no es necesario especificar la configuración de permisos individuales. Si especifica un permiso individual cuando se establece un nivel de permisos, se devolverá un error de **ErrorInvalidPermissionSettings** en la respuesta. 
  
## <a name="adding-folder-permissions-by-using-the-ews-managed-api"></a>Adición de permisos de carpeta mediante el uso de la API administrada de EWS
<a name="bk_enableewsma"> </a>

En el ejemplo de código siguiente se muestra cómo usar la API administrada de EWS para: 
  
- Crear un nuevo objeto [FolderPermission](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderpermission%28v=exchg.80%29.aspx) para el nuevo usuario. 
    
- Obtenga los permisos para una carpeta actuales mediante el método [enlazar](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) . 
    
- Agregue el nuevo **FolderPermissions** a la propiedad [Folder.Permissions](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.permissions%28v=exchg.80%29.aspx) . 
    
- Llame al método [Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) para guardar los nuevos permisos en el servidor. 
    
En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido para el propietario del buzón y que se ha autenticado el usuario a un servidor de Exchange. 
  
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

La siguiente línea de código, especifica el nivel de permisos.
  
```cs
    FolderPermission fldperm = new FolderPermission("sadie@contoso.com", FolderPermissionLevel.Editor);
```

Si desea usar el nivel de permisos personalizados, use este código en su lugar.
  
```cs
FolderPermission fldperm = new FolderPermission();
fldperm.UserId = "sadie@Contoso1000.onmicrosoft.com";
fldperm.CanCreateItems = true;
fldperm.CanCreateSubFolders = true;
…
```

Puede establecer cualquiera o todas las [Propiedades FolderPermission](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderpermission_properties%28v=exchg.80%29.aspx) de escritura cuando se crea un objeto **FolderPermission** con un nivel de permisos personalizados. Sin embargo, tenga en cuenta que el [FolderPermissionLevel](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderpermissionlevel%28v=exchg.80%29.aspx) nunca de forma explícita está establecida en **Custom** por la aplicación. El **FolderPermissionLevel** está establecida en Custom sólo cuando cree un objeto **FolderPermission** y establecer permisos individuales. 
  
## <a name="adding-folder-permissions-by-using-ews"></a>Adición de permisos de carpeta mediante el uso de EWS
<a name="bk_enableews"> </a>

Los siguientes ejemplos de código EWS muestran cómo agregar permisos a una carpeta específica por recuperar los permisos actuales y, a continuación, enviar una lista de nuevos permisos.
  
El primer paso es enviar una solicitud de [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) , donde el valor [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) especifica la carpeta en la que se va a agregar permisos (la carpeta Elementos enviados en este ejemplo) y el valor de [FieldURI](http://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) incluye: conjunto de permisos de carpeta. Esta solicitud recupera la configuración de permisos para la carpeta especificada. 
  
También es la solicitud XML que la API administrada de EWS envía cuando se llama al método **enlazar** para [Agregar permisos de carpeta](#bk_enableewsma).
  
```XML
  <?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                 xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

El servidor responde a la solicitud de **GetFolder** con un mensaje de [GetFolderResponse](http://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que la carpeta se recuperó correctamente. Los valores de [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) e [ID](http://msdn.microsoft.com/library/258f4b1f-367e-4c7d-9c29-eb775a2398c7%28Office.15%29.aspx) se han abreviado para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

A continuación, use la operación **UpdateFolder** para enviar el actualizado [PermissionSet](http://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx), que incluye el [permiso](http://msdn.microsoft.com/library/b8d0429a-0e58-4480-9847-4901970c7033%28Office.15%29.aspx) para el nuevo usuario. Tenga en cuenta que incluido el elemento [SetFolderField](http://msdn.microsoft.com/library/8c69db7b-54b5-4ae2-abca-4d6e0937a790%28Office.15%29.aspx) para la carpeta respectivo en la operación de [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) sobrescribirá todas las configuraciones de permisos en la carpeta. Del mismo modo, incluida la opción [DeleteFolderField](http://msdn.microsoft.com/library/f9c2187b-4c60-4358-b4b4-ede50eadae48%28Office.15%29.aspx) de la operación **UpdateFolder** , se eliminan también todas las configuraciones de permisos en la carpeta. 
  
También es la solicitud XML que la API administrada de EWS envía al llamar al método **Update** para [Agregar permisos de carpeta](#bk_enableewsma).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

La siguiente línea de código, especifica el nivel de permisos.
  
```xml
<t:Permission>
    <t:UserId>
        <t:PrimarySmtpAddress>sadie@contoso.com</t:PrimarySmtpAddress>
    </t:UserId>
    <t:PermissionLevel>Editor</t:PermissionLevel>
</t:Permission>
```

Si desea usar el nivel de permisos personalizados, use este código en su lugar.
  
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

El servidor responde a la solicitud de **UpdateFolder** con un mensaje de [UpdateFolderResponse](http://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que la carpeta se ha actualizado correctamente.
  
## <a name="removing-folder-permissions-by-using-the-ews-managed-api"></a>Eliminación de permisos de carpeta mediante el uso de la API administrada de EWS
<a name="bk_removeewsma"> </a>

En el ejemplo de código siguiente se muestra cómo utilizar la API administrada de EWS para quitar todos los permisos de usuario en una carpeta específica, excepto los permisos predeterminado y anónimo, mediante:
  
1. Obtener los permisos para una carpeta actuales mediante el método **Bind** . 
    
2. Recorrer en iteración la colección de **permisos** y quitar permisos para usuarios individuales. 
    
3. Llamar al método **Update** para guardar los cambios. 
    
En este ejemplo se quitan todos los permisos de usuario en una carpeta. Si desea modificar este ejemplo para quitar los permisos sólo para un usuario específico, cambie la siguiente línea de código para identificar el nombre para mostrar o la dirección SMTP del usuario.
  
```cs
if (sentItemsFolder.Permissions[t].UserId.DisplayName != null || sentItemsFolder.Permissions[t].UserId.PrimarySmtpAddress != null)
```

En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido para el propietario del buzón y que se ha autenticado el usuario a un servidor de Exchange. 
  
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

## <a name="removing-folder-permissions-by-using-ews"></a>Eliminación de permisos de carpeta mediante el uso de EWS
<a name="bk_removeews"> </a>

Los siguientes ejemplos de código EWS muestran cómo quitar todos los permisos de usuario en una carpeta específica, excepto los permisos predeterminado y anónimo.
  
En primer lugar, envíe una solicitud de [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) donde el valor de [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) especifica la carpeta en la que se va a quitar los permisos (la carpeta Elementos enviados en este ejemplo) y el valor de [FieldURI](http://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) incluye: conjunto de permisos de carpeta. Esta solicitud, recuperará el [conjunto de permisos](http://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx) para la carpeta especificada. 
  
También es la solicitud XML que la API administrada de EWS envía cuando se llama al método **enlazar** para [quitar permisos de carpeta](#bk_removeewsma).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

El servidor responde a la solicitud de **GetFolder** con un mensaje de [GetFolderResponse](http://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que la carpeta se recuperó correctamente. Los valores de los elementos **FolderId** e **ID** se han abreviado para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

A continuación, use la operación **UpdateFolder** para enviar el actualizado **PermissionSet**, que no incluye el **permiso** para el usuario se ha quitado. 
  
También es la solicitud XML que la API administrada de EWS envía al llamar al método **Update** para [quitar permisos de carpeta](#bk_removeewsma).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

El servidor responde a la solicitud de **UpdateFolder** con un mensaje de **UpdateFolderResponse** que incluye un valor de elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, que indica que la actualización se realizó correctamente.
  
## <a name="updating-folder-permissions-by-using-the-ews-managed-api"></a>Actualización de permisos de carpeta mediante el uso de la API administrada de EWS
<a name="bk_updateewsma"> </a>

También puede actualizar los permisos de carpeta para una carpeta específica mediante el uso de la API administrada de EWS. Para actualizar los permisos: 
  
1. [Quitar los permisos de carpeta](#bk_removeewsma) para los permisos no actualizados, pero no se llama al método **Update** (todavía). 
    
2. [Agregar permisos de carpeta para los usuarios nuevos o modificados](#bk_enableewsma).
    
3. Llame al método **Update** para guardar los cambios. 
    
Si se intenta agregar dos conjuntos de permisos para el mismo usuario, recibirá un error de **ServiceResponseException** con la siguiente descripción: "el conjunto de permisos especificado contiene identificadores de usuario duplicados". En ese caso, quitar los permisos actuales de la colección **Permission** , a continuación, agregar los nuevos permisos a la colección **Permission** . 
  
## <a name="updating-folder-permissions-by-using-ews"></a>Actualización de permisos de carpeta mediante el uso de EWS
<a name="bk_updateews"> </a>

También puede actualizar los permisos de carpeta para carpetas específicas mediante el uso de EWS combinando el proceso de adición y eliminación. Para actualizar los permisos: 
  
1. Recuperar los permisos de la carpeta actual mediante el uso de la operación **GetFolder** . 
    
2. Enviar una lista actualizada de permisos mediante la operación **UpdateFolder** . 
    
Estos son las mismas dos operaciones que se usa para [Habilitar](#bk_enableews) o [quitar el acceso](#bk_removeews) mediante el uso de EWS. La única diferencia es que cuando se recibe la respuesta **GetFolder** , contendrá un conjunto de **permisos** de usuario. Simplemente reemplace ese elemento de **permiso** existente con el nuevo elemento de **permiso** y, a continuación, envíe la operación **UpdateFolder** con el nuevo valor de **permiso** o los valores. 
  
Si se intenta agregar dos conjuntos de permisos para el mismo usuario, recibirá un valor **ResponseCode** de **ErrorDuplicateUserIdsSpecified**. En ese caso, quite el valor de permiso no actualizado para el usuario de la solicitud y, a continuación, vuelva a intentar la solicitud.

## <a name="next-steps"></a>Siguientes pasos

Después de conceder permisos de usuario para una carpeta específica, el usuario puede tener acceso a la carpeta como un delegado. Para obtener m?s informaci?n, vea:
  
- [Correo electrónico de acceso como delegado mediante el uso de EWS en Exchange](how-to-access-email-as-a-delegate-by-using-ews-in-exchange.md)
    
- [Obtener acceso a un calendario como delegado mediante el uso de EWS en Exchange](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md)
    
- [Contactos de acceso como delegado mediante el uso de EWS en Exchange](how-to-access-contacts-as-a-delegate-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>Ver también

- [Acceso delegado y EWS en Exchange](delegate-access-and-ews-in-exchange.md)   
- [Agregar y quitar delegados mediante EWS en Exchange](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)    
- [Las carpetas y elementos de EWS en Exchange](folders-and-items-in-ews-in-exchange.md)
    

