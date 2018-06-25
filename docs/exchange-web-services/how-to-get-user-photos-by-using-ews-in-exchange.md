---
title: Obtener fotografías de usuario mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: f86d1099-1f57-47dc-abf2-4d5ae4e900a9
description: Obtenga información sobre cómo obtener fotografías de usuario que están asociadas con un buzón de correo o póngase en contacto con mediante el uso de la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: f0f5cddd41fc563fb9ed38e75b505830a3992411
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763103"
---
# <a name="get-user-photos-by-using-ews-in-exchange"></a>Obtener fotografías de usuario mediante el uso de EWS en Exchange

Obtenga información sobre cómo obtener fotografías de usuario que están asociadas con un buzón de correo o póngase en contacto con mediante el uso de la API administrada de EWS o EWS en Exchange.
  
Es interesante poner una cara a un nombre. Si le gusta a los usuarios colocar los nombres a las caras, la aplicación puede solicitar una imagen, normalmente una foto, de Exchange que representa una cuenta de correo electrónico. Puede obtener una foto de usuario almacenada en un servidor de Exchange para un buzón de correo, o puede obtener una foto de contacto de los contactos que se almacenan en su buzón de correo.
  
Puede usar varias tecnologías distintas para obtener fotos de los buzones de correo o los servicios de dominio de Active Directory (AD DS). La mejor manera de obtener una foto depende del tipo de contacto que se desea obtener una foto de. 
  
**La tabla 1. Tecnologías a usar para obtener fotos de usuario según el tipo de contacto**

|**Tipo de contacto**|**Para usar las tecnologías**|
|:-----|:-----|
|Foto de usuario de buzón de correo  <br/> |[Obtener una foto de usuario de buzón de correo con REST](#bk_REST)<br/><br/> [Obtener una foto de usuario mediante el uso de EWS](#bk_EWS) <br/> |
|Foto de contacto de usuario  <br/> |[Obtener una foto de usuario de contacto mediante el uso de API administrada de EWS](#bk_EWSMA)<br/><br/> [Obtener una foto de usuario mediante el uso de EWS](#bk_EWS) <br/> |

<a name="bk_REST"> </a>

## <a name="get-a-mailbox-user-photo-by-using-rest"></a>Obtener una foto de usuario de buzón de correo con REST

Puede solicitar fotografías de usuario desde un servidor de Exchange mediante el uso de una solicitud HTTPS **obtener** estándar. En la solicitud, especifique la dirección de la cuenta de correo electrónico y un código de tamaño de la imagen, tal como se muestra en el siguiente ejemplo. 
  
```HTML
https://Exchange Server/ews/Exchange.asmx/s/GetUserPhoto?email=email address&amp;size=size code
```

Use la operación de [GetUserSettings](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) del servicio de detección automática para recuperar la configuración de **ExternalEwsUrl** , que contiene la dirección URL del extremo de servicios Web de Exchange (EWS) y la ubicación del controlador **Exchange.asmx** HTTP que devuelve el fotos de usuario. 
  
Cada código de tamaño indica el alto y el ancho de la imagen en píxeles. Por ejemplo, el código de tamaño **HR48x48** devuelve una imagen que es 48 píxeles de alto por 48 píxeles de ancho. Los valores posibles para el parámetro de código de tamaño son los mismos que los valores posibles para el elemento [SizeRequested](http://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx) . Si la solicitud especifica un tamaño que no está disponible, se devolverá la foto disponible más grande. Si no hay foto se almacena en el servidor de Exchange, se devolverá la imagen en miniatura que se almacena en AD DS para la cuenta. 
  
> [!NOTE]
> El código de tamaño **HR48x48** siempre devuelve la imagen en miniatura de AD DS, si está disponible. 
  
En el ejemplo siguiente se muestra cómo puede usar la solicitud GET para recuperar la foto de usuario para Sadie y guárdelo en su equipo local.
  
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
  
**Tabla 2. Códigos de respuesta para una solicitud de GetUserPhoto**

|**Código de respuesta**|**Descripción**|
|:-----|:-----|
|200  <br/> |Una imagen está disponible para la cuenta de correo electrónico especificada y la imagen binaria se encuentra en la respuesta.  <br/> |
|304  <br/> |La imagen no ha cambiado desde la última vez que se devolvió el **ETag** a la aplicación.  <br/> |
|404  <br/> |No hay ninguna imagen está disponible para la cuenta de correo electrónico especificada.  <br/> |

<a name="bk_REST"> </a>

## <a name="cache-user-photos"></a>Fotos de usuario de la memoria caché

Exchange devuelve los datos con un tipo de contenido de imagen/jpeg, junto con una colección de valores de encabezado. El encabezado **ETag** es similar a una clave de cambio. El valor es una cadena que representa la última vez que se actualizó la foto. El **valor ETag** sigue siendo la misma para la foto de usuario hasta que se modifica la foto. Puede enviar este valor de **ETag** para el servidor en la solicitud HTTPS **obtener** en un encabezado **If--Match** . Si la foto no ha cambiado desde la última solicitud, el servidor responde con una respuesta HTTP 304 que se indica como tales. Esto significa que se puede utilizar la foto de usuario que solicita y guardado previamente en lugar de procesar una nueva. 

<a name="bk_EWSMA"> </a>

## <a name="get-a-contact-user-photo-by-using-ews-managed-api"></a>Obtener una foto de usuario de contacto mediante el uso de API administrada de EWS

La aplicación puede utilizar la API administrada de EWS para recuperar las fotos de contactos, si el contacto se almacena en una carpeta de contactos en el buzón del usuario. Para ello, en primer lugar, busque la **ItemId** para el contacto que desee usar. A continuación, después de enlazar a ese contacto, cargarlo a la colección attachments. Si el contacto tiene una foto, la foto será uno de los datos adjuntos. Recorrer en iteración la colección de datos adjuntos, comprobar el valor de la propiedad **IsContactPhoto** . Cuando encuentre la foto del contacto, puede guardar en el equipo local y la aplicación puede tener acceso a él. 
  
En el ejemplo siguiente se muestra este proceso. En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange. 
  
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

## <a name="get-a-user-photo-by-using-ews"></a>Obtener una foto de usuario mediante el uso de EWS

Si va a recibir una foto de usuario de AD DS, puede usar la operación de [GetUserPhoto](http://msdn.microsoft.com/library/f6e8143d-4235-428e-8f9c-ab6e9b1cfa6e%28Office.15%29.aspx) (si conoce la dirección de correo electrónico) o la operación [ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) (si no conoce la dirección de correo electrónico). Si va a recibir una foto de usuario desde una carpeta de contactos en el buzón de correo, use la operación de [GetItem](http://msdn.microsoft.com/library/6b96dace-1260-4b83-869a-7c31c5583daa%28Office.15%29.aspx) seguida de la operación [GetAttachment](http://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx) . En cualquier caso, la foto se devuelve como una cadena con codificación Base64 en la respuesta XML. 
  
### <a name="get-a-mailbox-user-photo-by-using-the-getuserphoto-operation"></a>Obtener una foto de usuario de buzón de correo mediante el uso de la operación de GetUserPhoto

Mediante la operación de **GetUserPhoto** es un proceso sencillo. En la solicitud XML, especifique la dirección de correo electrónico del usuario y el [tamaño de la foto](http://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx) para devolver (en el elemento [SizeRequested](http://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx) ). El siguiente ejemplo de solicitud XML muestra cómo obtener una foto para Sadie Daniels que es 360 píxeles de ancho por 360 píxeles de alto. 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

La siguiente es la respuesta XML. La foto con codificación Base64 está contenida en el elemento [PictureData](http://msdn.microsoft.com/library/1124eac3-ebf2-4b81-96d3-96838c840433%28Office.15%29.aspx) (el contenido se ha acortado para mejorar la legibilidad). 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetUserPhotoResponse ResponseClass="Success" 
         xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <HasChanged>true</HasChanged>
      <PictureData>/9j/4AAQSkZJRgABAQEAYABgAAD/2wBDAAg... wATRRRSuB//2Q==</PictureData>
    </GetUserPhotoResponse>
  </s:Body>
</s:Envelope>

```

### <a name="get-a-mailbox-user-photo-by-using-the-resolvenames-operation"></a>Obtener una foto de usuario de buzón de correo mediante el uso de la operación ResolveNames

Si no conoce la dirección de correo electrónico del usuario para el que va a obtener una foto, puede [usar la operación ResolveNames](how-to-resolve-ambiguous-names-by-using-ews-in-exchange-2013.md) para obtener a candidatos para una coincidencia de posible. Si se especifica "AllProperties" para el atributo **ContactDataShape** del elemento [ResolveNames](http://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) , se devolverá una gran cantidad de datos, incluidas las fotos de usuario, para cada candidato. En el ejemplo siguiente se muestra la solicitud XML para resolver el nombre "Sadie" y devolver todas las propiedades para cada candidato. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

Se devuelve una gran cantidad de datos en la respuesta. En el ejemplo siguiente se muestra sólo los datos que es relevantes para la foto de usuario. El elemento de **foto** contiene la foto de usuario con codificación Base64 (el contenido se ha acortado para mejorar la legibilidad). 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:ResolveNamesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="get-a-contact-user-photo-by-using-the-getattachment-operation"></a>Obtener una foto de usuario de contacto mediante el uso de la operación GetAttachment

Puede usar EWS para obtener fotos de contactos almacenados en su buzón de correo. En primer lugar, use la operación **GetItem** para devolver todas las propiedades, por lo que puede buscar las fotografías. En el ejemplo siguiente se muestra una solicitud XML para obtener un elemento de contacto. El identificador de elemento se ha acortado para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns='http://schemas.microsoft.com/exchange/services/2006/messages'>
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

Busque el elemento [HasPicture](http://msdn.microsoft.com/library/922a43fe-01bd-49f2-9261-e00e4699b8da%28Office.15%29.aspx) comprobar que el contacto tiene una foto asociada. A continuación, mire a través de la colección de datos adjuntos para uno que tenga el valor true para el elemento [IsContactPhoto](http://msdn.microsoft.com/library/ae36b5f9-a787-4863-9dbc-258ad724801d%28Office.15%29.aspx) . El siguiente ejemplo de respuesta muestra sólo los datos relevantes. Los valores de ID se acortan para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

A continuación, use la operación **GetAttachment** con el **AttachmentId** para solicitar los datos adjuntos que tiene la foto del contacto. En el ejemplo siguiente se muestra la solicitud XML para obtener los datos adjuntos. El identificador es más cortos para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentShape/>
      <AttachmentIds>
         <t:AttachmentId Id="1LGlhgpgoA="/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>

```

En el ejemplo siguiente se muestra la respuesta XML con la información acerca de los datos adjuntos que ha solicitado. El elemento de [contenido](http://msdn.microsoft.com/library/24f8c54a-505f-4fc0-b7e7-93ad50b97070%28Office.15%29.aspx) contiene la cadena con codificación Base64 para la foto de usuario más cortos en este ejemplo para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetAttachmentResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="decode-a-base64-encoded-string"></a>Descodifica una cadena con codificación Base64

Independientemente de la operación que se utiliza para obtener una foto de usuario, debe descodificar dicha cadena, por lo que puede usar en la aplicación. En el ejemplo siguiente se muestra cómo descodificar la cadena y, a continuación, guárdelo en el equipo local para su aplicación puede tener acceso a él más adelante.
  
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

- [Las personas y los contactos de EWS en Exchange](people-and-contacts-in-ews-in-exchange.md)    
- [Resolver nombres ambiguos mediante el uso de EWS en Exchange 2013](how-to-resolve-ambiguous-names-by-using-ews-in-exchange-2013.md)    
- [Contactos de proceso por lotes mediante EWS en Exchange](how-to-process-contacts-in-batches-by-using-ews-in-exchange.md)
    

