---
title: Obtener fotos de usuario mediante EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: f86d1099-1f57-47dc-abf2-4d5ae4e900a9
description: Obtenga información sobre cómo obtener las fotos del usuario que están asociadas a un buzón o contacto mediante la API administrada de EWS o EWS en Exchange.
localization_priority: Priority
ms.openlocfilehash: 14f2bc6bef1ce3c3529f03e213e3ada7c45a5a71
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455789"
---
# <a name="get-user-photos-by-using-ews-in-exchange"></a>Obtener fotos de usuario mediante EWS en Exchange

Obtenga información sobre cómo obtener las fotos del usuario que están asociadas a un buzón o contacto mediante la API administrada de EWS o EWS en Exchange.
  
Es estupendo colocar una cara a un nombre. Si los usuarios desean poner los nombres en caras, la aplicación puede solicitar una imagen, normalmente una foto, de Exchange que represente una cuenta de correo electrónico. Puede obtener una foto de usuario almacenada en un servidor de Exchange para un buzón de correo o puede obtener una foto de contacto de los contactos almacenados en el buzón de correo.
  
Puede usar varias tecnologías diferentes para obtener fotos de los buzones de correo o los servicios de dominio de Active Directory (AD DS). La mejor forma de obtener una foto depende del tipo de contacto del que deseas obtener una foto. 
  
**Tabla 1. Tecnologías que se deben usar para obtener las fotos del usuario según el tipo de contacto**

|**Tipo de contacto**|**Tecnologías para usar**|
|:-----|:-----|
|Foto del usuario del buzón  <br/> |[Obtener una foto de usuario de buzón de correo con REST](#bk_REST)<br/><br/> [Obtener una foto de usuario mediante EWS](#bk_EWS) <br/> |
|Foto de contacto del usuario  <br/> |[Obtener una foto de contacto del usuario mediante la API administrada de EWS](#bk_EWSMA)<br/><br/> [Obtener una foto de usuario mediante EWS](#bk_EWS) <br/> |

<a name="bk_REST"> </a>

## <a name="get-a-mailbox-user-photo-by-using-rest"></a>Obtener una foto de usuario de buzón de correo con REST

Puede solicitar fotos de usuario de un servidor de Exchange mediante una solicitud HTTP **Get** estándar. En la solicitud, especifique la dirección de la cuenta de correo electrónico y un código de tamaño para la imagen, como se muestra en el ejemplo siguiente. 
  
```HTML
https://Exchange Server/ews/Exchange.asmx/s/GetUserPhoto?email=email address&amp;size=size code
```

Use la operación [GetUserSettings](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) del servicio Detección automática para recuperar la configuración de **ExternalEwsUrl** , que contiene la dirección URL del extremo de los servicios web Exchange (EWS) y la ubicación del controlador HTTP de **Exchange. asmx** que devuelve las fotos del usuario. 
  
Cada código de tamaño indica el alto y el ancho de la imagen en píxeles. Por ejemplo, el código de tamaño **HR48x48** devuelve una imagen de 48 píxeles de alto por 48 píxeles de ancho. Los valores posibles para el parámetro de código de tamaño son los mismos que los valores posibles para el elemento [SizeRequested](https://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx) . Si la solicitud especifica un tamaño que no está disponible, se devolverá la foto más grande disponible. Si no hay ninguna foto almacenada en el servidor Exchange, se devolverá la imagen en miniatura almacenada en AD DS para la cuenta. 
  
> [!NOTE]
> El código de tamaño **HR48x48** siempre devuelve la imagen en miniatura de AD DS si está disponible. 
  
El siguiente ejemplo muestra cómo se puede usar la solicitud GET para recuperar la foto de usuario para Sadie y guardarla en el equipo local.
  
```cs
// Create the web request with the REST URL.
HttpWebRequest request = 
   WebRequest.Create("https://www.contoso.com/ews/exchange.asmx/s/GetUserPhoto?email=sadie@contoso.com&amp;size=HR240x240") 
   as HttpWebRequest;
// Submit the request.
using (HttpWebResponse resp = request.GetResponse() as HttpWebResponse)
{
   // Take the response and save it as an image.
   Bitmap image = new Bitmap(resp.GetResponseStream());
   image.Save("Sadie.jpg");
}

```

La solicitud devolverá una respuesta HTTP. 
  
**Tabla 2. Códigos de respuesta para una solicitud GetUserPhoto**

|**Código de respuesta**|**Descripción**|
|:-----|:-----|
|200  <br/> |Hay una imagen disponible para la cuenta de correo electrónico especificada y la imagen binaria está contenida en la respuesta.  <br/> |
|304  <br/> |La imagen no ha cambiado desde la última vez que la **ETag** se devolvió a la aplicación.  <br/> |
|404  <br/> |No hay ninguna imagen disponible para la cuenta de correo electrónico especificada.  <br/> |

<a name="bk_REST"> </a>

## <a name="cache-user-photos"></a>Almacenar en caché fotos de usuario

Exchange devuelve los datos con un tipo de contenido image/JPEG, junto con una colección de valores de encabezado. El encabezado **ETag** es similar a una clave de cambio. El valor es una cadena que representa la última vez que se actualizó la foto. La **ETag** sigue siendo la misma para la foto del usuario hasta que se modifique la foto. Puede enviar este valor de **ETag** al servidor en la solicitud HTTPS **Get** en un encabezado **If-None-Match** . Si la foto no se ha modificado desde la última solicitud, el servidor responderá con una respuesta HTTP 304 que indique como tal. Esto significa que puede usar la foto de usuario que solicitó y guardó anteriormente en lugar de procesar una nueva. 

<a name="bk_EWSMA"> </a>

## <a name="get-a-contact-user-photo-by-using-ews-managed-api"></a>Obtener una foto de contacto del usuario mediante la API administrada de EWS

La aplicación puede usar la API administrada de EWS para recuperar las fotos de los contactos, si el contacto se almacena en una carpeta de contactos en el buzón del usuario. Para ello, en primer lugar, busque el **Itemid** del contacto que desea usar. A continuación, después de enlazar a ese contacto, cárguelo a la colección Attachments. Si el contacto tiene una foto, la foto será uno de los datos adjuntos. Recorrer en bucle la colección Attachments, comprobando el valor de la propiedad **IsContactPhoto** . Cuando encuentre la foto del contacto, puede guardarla en el equipo local y su aplicación puede acceder a ella. 
  
En el ejemplo siguiente se muestra este proceso. En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un servidor de Exchange. 
  
```cs
private static void GetContactPhoto(ExchangeService service, string ItemId)
{
   // Bind to an existing contact by using the ItemId passed into this function.
   Contact contact = Contact.Bind(service, ItemId);
   // Load the contact to get access to the collection of attachments.
   contact.Load(new PropertySet(ContactSchema.Attachments));
   // Loop through the attachments looking for a contact photo.
   foreach (Attachment attachment in contact.Attachments)
   {
      if ((attachment as FileAttachment).IsContactPhoto)
      {
         // Load the attachment to access the content.
         attachment.Load();
      }
   }
   FileAttachment photo = contact.GetContactPictureAttachment();
   // Create a file stream and save the contact photo to your computer.
   using (FileStream file = new FileStream(photo.Name, FileMode.Create, System.IO.FileAccess.Write))
   {
      photo.Load(file);
   }
}

```

<a name="bk_EWS"> </a>

## <a name="get-a-user-photo-by-using-ews"></a>Obtener una foto de usuario mediante EWS

Si está recibiendo una foto de usuario de AD DS, puede usar la operación [GetUserPhoto](https://msdn.microsoft.com/library/f6e8143d-4235-428e-8f9c-ab6e9b1cfa6e%28Office.15%29.aspx) (si conoce la dirección de correo electrónico) o la operación [ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) (si no conoce la dirección de correo electrónico). Si va a obtener una foto de usuario de una carpeta de contactos en el buzón de correo, use la operación [GetItem](https://msdn.microsoft.com/library/6b96dace-1260-4b83-869a-7c31c5583daa%28Office.15%29.aspx) seguida de la operación [GetAttachment](https://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx) . En cualquier caso, la foto se devuelve como una cadena codificada en Base64 en la respuesta XML. 
  
### <a name="get-a-mailbox-user-photo-by-using-the-getuserphoto-operation"></a>Obtener una foto de usuario de buzón de correo mediante la operación GetUserPhoto

El uso de la operación **GetUserPhoto** es sencillo. En la solicitud XML, especifique la dirección de correo electrónico del usuario y el [tamaño de la foto](https://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx) que se va a devolver (en el elemento [SizeRequested](https://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx) ). El siguiente ejemplo de solicitud XML muestra cómo obtener una foto para Sadie Daniels de 360 píxeles de ancho por 360 píxeles de alto. 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013 "/>
   </soap:Header>
   <soap:Body>
      <m:GetUserPhoto>
         <m:Email>sadie@contoso.com</m:Email>
         <m:SizeRequested>HR360x360</m:SizeRequested>
      </m:GetUserPhoto>
   </soap:Body>
</soap:Envelope>

```

A continuación se encuentra la respuesta XML. La foto codificada en Base64 se incluye en el elemento [PictureData](https://msdn.microsoft.com/library/1124eac3-ebf2-4b81-96d3-96838c840433%28Office.15%29.aspx) (el contenido se ha abreviado para facilitar la lectura). 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetUserPhotoResponse ResponseClass="Success" 
         xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <HasChanged>true</HasChanged>
      <PictureData>/9j/4AAQSkZJRgABAQEAYABgAAD/2wBDAAg... wATRRRSuB//2Q==</PictureData>
    </GetUserPhotoResponse>
  </s:Body>
</s:Envelope>

```

### <a name="get-a-mailbox-user-photo-by-using-the-resolvenames-operation"></a>Obtener una foto de usuario de buzón de correo mediante la operación ResolveNames

Si no conoce la dirección de correo electrónico del usuario para el que obtiene una foto, puede [usar la operación ResolveNames](how-to-resolve-ambiguous-names-by-using-ews-in-exchange-2013.md) para obtener candidatos para una posible coincidencia. Si especifica "AllProperties" para el atributo **ContactDataShape** del elemento [ResolveNames](https://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) , se devolverán muchos datos, incluidas las fotos de los usuarios, para cada candidato. En el ejemplo siguiente se muestra la solicitud XML para resolver el nombre "Sadie" y devolver todas las propiedades de cada candidato. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
<soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>  
<soap:Body>
  <m:ResolveNames ReturnFullContactData="true" ContactDataShape="AllProperties">
      <m:UnresolvedEntry>sadie</m:UnresolvedEntry>
    </m:ResolveNames>
  </soap:Body>
</soap:Envelope>
```

Se devolverá una gran cantidad de datos en la respuesta. En el ejemplo siguiente se muestran solo los datos relevantes para la foto del usuario. El elemento **Photo** contiene la foto de usuario con codificación base64 (el contenido se ha reducido para facilitar la lectura). 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:ResolveNamesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:ResolveNamesResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ResolutionSet TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Resolution>
              <t:Mailbox>
                <t:Name>Sadie Daniels</t:Name>
                <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
                <t:RoutingType>SMTP</t:RoutingType>
                <t:MailboxType>Mailbox</t:MailboxType>
              </t:Mailbox>
              <t:Contact>
                <t:DisplayName>Sadie Daniels</t:DisplayName>
                <t:GivenName>Sadie</t:GivenName>
                <t:Initials/>
                <t:CompanyName>CONTOSO</t:CompanyName>
......
                <t:Photo>/9j/4AAQSkZJRgABAQE...qKKKAP/2Q==</t:Photo>
......
              </t:Contact>
            </t:Resolution>
          </m:ResolutionSet>
        </m:ResolveNamesResponseMessage>
      </m:ResponseMessages>
    </m:ResolveNamesResponse>
  </s:Body>
</s:Envelope>

```

### <a name="get-a-contact-user-photo-by-using-the-getattachment-operation"></a>Obtener una foto de contacto del usuario mediante la operación GetAttachment

Puede usar EWS para obtener fotos de los contactos almacenados en su buzón de correo. En primer lugar, use la operación **GetItem** para devolver todas las propiedades para que pueda buscar fotografías. En el ejemplo siguiente se muestra una solicitud XML para obtener un elemento de contacto. El identificador de elemento se ha abreviado para facilitar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns='https://schemas.microsoft.com/exchange/services/2006/messages'>
      <ItemShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </ItemShape>
      <ItemIds>
        <t:ItemId Id="AAAAGECXAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AABLzXRv"/>
      </ItemIds>
    </GetItem>
  </soap:Body>
</soap:Envelope>

```

Busque el elemento [HasPicture](https://msdn.microsoft.com/library/922a43fe-01bd-49f2-9261-e00e4699b8da%28Office.15%29.aspx) para comprobar que el contacto tiene una foto asociada. A continuación, busque en la colección de datos adjuntos uno que tenga un valor de true para el elemento [IsContactPhoto](https://msdn.microsoft.com/library/ae36b5f9-a787-4863-9dbc-258ad724801d%28Office.15%29.aspx) . El siguiente ejemplo de respuesta muestra solo los datos relevantes. Los valores de ID se acortan para facilitar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Contact>
              <t:ItemId Id="AAAAGECXAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AABLzXRv"/>
              <t:ParentFolderId Id="nIxIAAA=" ChangeKey="AQAAAA=="/>
              <t:ItemClass>IPM.Contact</t:ItemClass>
              <t:Subject>Hope Gross</t:Subject>
              <t:Sensitivity>Normal</t:Sensitivity>
......
              <t:Attachments>
                <t:FileAttachment>
                  <t:AttachmentId Id="1LGlhgpgoA="/>
                  <t:Name>ContactPicture.jpg</t:Name>
                  <t:Size>6260</t:Size>
                  <t:LastModifiedTime>2011-03-09T16:55:55</t:LastModifiedTime>
                  <t:IsInline>false</t:IsInline>
                  <t:IsContactPhoto>true</t:IsContactPhoto>
                </t:FileAttachment>
              </t:Attachments>
......
              <t:HasPicture>true</t:HasPicture>
            </t:Contact>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>

```

A continuación, use la operación **GetAttachment** con **AttachmentId** para solicitar los datos adjuntos que tienen la foto de contacto. En el ejemplo siguiente se muestra la solicitud XML para obtener los datos adjuntos. El identificador se acorta para facilitar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentShape/>
      <AttachmentIds>
         <t:AttachmentId Id="1LGlhgpgoA="/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>

```

En el ejemplo siguiente se muestra la respuesta XML con información sobre los datos adjuntos solicitados. El elemento [Content](https://msdn.microsoft.com/library/24f8c54a-505f-4fc0-b7e7-93ad50b97070%28Office.15%29.aspx) contiene la cadena codificada en base64 para la foto del usuario, abreviada en este ejemplo para facilitar su lectura. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Attachments>
            <t:FileAttachment>
              <t:AttachmentId Id="+KsDBEr1LGlhgpgoA="/>
              <t:Name>ContactPicture.jpg</t:Name>
              <t:Content>/9j/4AAQSkZJRgABAQEAYABgAAD/2wBDAAg...D//2Q==</t:Content>
            </t:FileAttachment>
          </m:Attachments>
        </m:GetAttachmentResponseMessage>
      </m:ResponseMessages>
    </m:GetAttachmentResponse>
  </s:Body>
</s:Envelope>

```

<a name="bk_EWS"> </a>

## <a name="decode-a-base64-encoded-string"></a>Descodificar una cadena codificada en Base64

Independientemente de la operación que use para obtener una foto del usuario, debe descodificar esa cadena para poder usarla en la aplicación. En el siguiente ejemplo, se muestra cómo descodificar la cadena y, a continuación, guardarla en el equipo local para que la aplicación pueda tener acceso a ella más adelante.
  
```cs
// Convert the encoded string into a byte array.
byte[] data = System.Convert.FromBase64String(Photo);
// Create a memory stream to read the data.
MemoryStream ms = new MemoryStream(data);
// Save the data on your local computer as a JPG image.
using (FileStream file = new FileStream(ContactName + ".jpg", FileMode.Create, System.IO.FileAccess.Write))
{
   byte[] bytes = new byte[ms.Length];
   ms.Read(bytes, 0, (int)ms.Length);
   file.Write(bytes, 0, bytes.Length);
   ms.Close();
}

```

## <a name="see-also"></a>Vea también

- [Personas y contactos de EWS en Exchange](people-and-contacts-in-ews-in-exchange.md)    
- [Resolver nombres ambiguos mediante EWS en Exchange 2013](how-to-resolve-ambiguous-names-by-using-ews-in-exchange-2013.md)    
- [Procesar contactos en lotes mediante EWS en Exchange](how-to-process-contacts-in-batches-by-using-ews-in-exchange.md)
    

