---
title: Trabajar con carpetas ocultas con EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7ae7c045-cd90-4c9f-baf5-0464d5058f45
description: Obtenga información sobre cómo hacer que una carpeta oculta y encontrar carpetas ocultas mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 72efc16ecc247d307b7300526e7d345fe6bdd3ac
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763194"
---
# <a name="work-with-hidden-folders-by-using-ews-in-exchange"></a><span data-ttu-id="d1779-103">Trabajar con carpetas ocultas con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d1779-103">Work with hidden folders by using EWS in Exchange</span></span>

<span data-ttu-id="d1779-104">Obtenga información sobre cómo hacer que una carpeta oculta y encontrar carpetas ocultas mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="d1779-104">Learn how to make a folder hidden and find hidden folders by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="d1779-105">Con una excepción, se ocultan las carpetas en la raíz de un buzón de Exchange (el subárbol no IPM) desde el usuario.</span><span class="sxs-lookup"><span data-stu-id="d1779-105">With one exception, folders in the root of an Exchange mailbox (the non-IPM subtree) are hidden from the user.</span></span> <span data-ttu-id="d1779-106">Por el contrario, todas las carpetas en el **MsgFolderRoot** (el subárbol IPM) están visibles para el usuario.</span><span class="sxs-lookup"><span data-stu-id="d1779-106">Conversely, all folders in the **MsgFolderRoot** (the IPM subtree) are visible to the user.</span></span> <span data-ttu-id="d1779-107">¿Cómo se oculta una carpeta bajo la **MsgFolderRoot**?</span><span class="sxs-lookup"><span data-stu-id="d1779-107">So how do you hide a folder under the **MsgFolderRoot**?</span></span> <span data-ttu-id="d1779-108">No es complicado es: se trata de una sola propiedad, la propiedad [PidTagAttributeHidden](http://msdn.microsoft.com/en-us/library/cc433490%28v=exchg.80%29.aspx) (0x10F4000B) extendido.</span><span class="sxs-lookup"><span data-stu-id="d1779-108">It's not that tricky — it comes down to just one property, the [PidTagAttributeHidden](http://msdn.microsoft.com/en-us/library/cc433490%28v=exchg.80%29.aspx) (0x10F4000B) extended property.</span></span> <span data-ttu-id="d1779-109">Cuando esta propiedad se establece en **true**, Outlook u otro cliente que utiliza la propiedad para determinar la visibilidad de la carpeta va a ocultar la carpeta de la vista del usuario.</span><span class="sxs-lookup"><span data-stu-id="d1779-109">When this property is set to **true**, Outlook or another client that uses the property to determine folder visibility will hide the folder from the user's view.</span></span> <span data-ttu-id="d1779-110">Puesto que se trata de una propiedad extendida, es más complejo de utilizar que la propiedad carpeta promedio, por lo que este artículo le guiará a través de los escenarios principales.</span><span class="sxs-lookup"><span data-stu-id="d1779-110">Because this is an extended property, it's more complex to use than your average folder property, so this article will walk you through the main scenarios.</span></span>
  
<span data-ttu-id="d1779-111">**La tabla 1. Métodos de la API administrada de EWS y las operaciones de EWS para trabajar con carpetas ocultas**</span><span class="sxs-lookup"><span data-stu-id="d1779-111">**Table 1. EWS Managed API methods and EWS operations for working with hidden folders**</span></span>

|<span data-ttu-id="d1779-112">**Tarea**</span><span class="sxs-lookup"><span data-stu-id="d1779-112">**Task**</span></span>|<span data-ttu-id="d1779-113">**Método de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="d1779-113">**EWS Managed API method**</span></span>|<span data-ttu-id="d1779-114">**Operación de EWS**</span><span class="sxs-lookup"><span data-stu-id="d1779-114">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d1779-115">Ocultar una carpeta</span><span class="sxs-lookup"><span data-stu-id="d1779-115">Hide a folder</span></span>  <br/> |<span data-ttu-id="d1779-116">[Folder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) seguido de [Folder.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1779-116">[Folder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) followed by [Folder.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="d1779-117">[GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) seguido [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1779-117">[GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) followed by [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="d1779-118">Busque las carpetas ocultas</span><span class="sxs-lookup"><span data-stu-id="d1779-118">Find hidden folders</span></span>  <br/> |[<span data-ttu-id="d1779-119">FindFolders</span><span class="sxs-lookup"><span data-stu-id="d1779-119">FindFolders</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="d1779-120">FindFolder</span><span class="sxs-lookup"><span data-stu-id="d1779-120">FindFolder</span></span>](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="d1779-121">¿Sabe de qué es la única excepción, es decir, ¿qué carpeta en la raíz es visible para los usuarios?</span><span class="sxs-lookup"><span data-stu-id="d1779-121">Are you wondering what the one exception is — that is, what folder in the root IS visible to users?</span></span> <span data-ttu-id="d1779-122">Es la carpeta de Finder (también conocido como el valor de la enumeración **SearchFolders**[WellKnownFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) , o el valor del elemento **searchfolders**[DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) ), que contiene las carpetas de búsqueda de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="d1779-122">It's the Finder folder (also known as the **SearchFolders**[WellKnownFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) enumeration value, or the **searchfolders**[DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) element value), which contains users' search folders.</span></span> <span data-ttu-id="d1779-123">Las carpetas de búsqueda creadas en la carpeta Finder están visibles para los usuarios de Outlook.</span><span class="sxs-lookup"><span data-stu-id="d1779-123">Search folders created in the Finder folder are visible to Outlook users.</span></span> <span data-ttu-id="d1779-124">Si necesita crear una carpeta de búsqueda que no es visible para los usuarios, mueva bajo la carpeta raíz para ocultarlo.</span><span class="sxs-lookup"><span data-stu-id="d1779-124">If you need to create a search folder that is not visible to users, move it under the root folder to hide it.</span></span> <span data-ttu-id="d1779-125">A diferencia de para otras carpetas, establecer la propiedad **PidTagAttributeHidden** en **true** no oculta una carpeta de búsqueda en la carpeta del Finder.</span><span class="sxs-lookup"><span data-stu-id="d1779-125">Unlike for other folders, setting the **PidTagAttributeHidden** property to **true** will not hide a search folder in the Finder folder.</span></span> 
  
## <a name="hide-a-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="d1779-126">Ocultar una carpeta mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="d1779-126">Hide a folder by using the EWS Managed API</span></span>
<span data-ttu-id="d1779-127"><a name="bk_hideewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="d1779-127"></span></span>

<span data-ttu-id="d1779-128">Puede [convertir una carpeta existente en](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_createfolderewsma) una carpeta oculta cambiando el [PidTagAttributeHidden](http://msdn.microsoft.com/en-us/library/cc433490%28v=exchg.80%29.aspx) ampliado de la propiedad en **true**.</span><span class="sxs-lookup"><span data-stu-id="d1779-128">You can [make an existing folder](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_createfolderewsma) a hidden folder by changing the [PidTagAttributeHidden](http://msdn.microsoft.com/en-us/library/cc433490%28v=exchg.80%29.aspx) extended property to **true**.</span></span> <span data-ttu-id="d1779-129">En primer lugar, cree una [definición de propiedad extendida de la propiedad](properties-and-extended-properties-in-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="d1779-129">First, create an [extended property definition for the property](properties-and-extended-properties-in-ews-in-exchange.md).</span></span> <span data-ttu-id="d1779-130">A continuación, utilice el método [Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) para llegar a la carpeta, a continuación, actualizar el valor de la propiedad **PidTagAttributeHidden** en true y utilice el método [Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="d1779-130">Next, use the [Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) method to get to the folder, then update the value of the **PidTagAttributeHidden** property to true, and use the [Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) method to save the changes.</span></span> 
  
<span data-ttu-id="d1779-131">En este ejemplo se supone que **servicio** es un válido [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) de objetos para el propietario del buzón de correo, que se ha autenticado el usuario a un servidor de Exchange, y ese **folderId** es un válido [Folder.Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx) que identifica la carpeta que se va a ocultar.</span><span class="sxs-lookup"><span data-stu-id="d1779-131">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox owner, that the user has been authenticated to an Exchange server, and that **folderId** is a valid [Folder.Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx) that identifies the folder to hide.</span></span> 
  
```cs
private static void MakeHidden(FolderId folderId, ExchangeService service)
{
    // Create an extended property definition for the PidTagAttributeHidden property.
    ExtendedPropertyDefinition isHiddenProp = new ExtendedPropertyDefinition(0x10f4, MapiPropertyType.Boolean);
    PropertySet propSet = new PropertySet(isHiddenProp);
    // Bind to a folder and retrieve the PidTagAttributeHidden property.
    Folder folder = Folder.Bind(service, folderId, propSet);
    // Set the PidTagAttributeHidden property to true.
    folder.SetExtendedProperty(isHiddenProp, true);
    // Save the changes.
    folder.Update();
}
```

## <a name="hide-a-folder-by-using-ews"></a><span data-ttu-id="d1779-132">Ocultar una carpeta mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="d1779-132">Hide a folder by using EWS</span></span>
<span data-ttu-id="d1779-133"><a name="bk_hideews"> </a></span><span class="sxs-lookup"><span data-stu-id="d1779-133"></span></span>

<span data-ttu-id="d1779-134">Puede usar EWS para [convertir una carpeta existente en](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_createfolderewsma) una carpeta oculta cambiando el [PidTagAttributeHidden](http://msdn.microsoft.com/en-us/library/cc433490%28v=exchg.80%29.aspx) ampliado de la propiedad en **true**.</span><span class="sxs-lookup"><span data-stu-id="d1779-134">You can use EWS to [make an existing folder](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_createfolderewsma) a hidden folder by changing the [PidTagAttributeHidden](http://msdn.microsoft.com/en-us/library/cc433490%28v=exchg.80%29.aspx) extended property to **true**.</span></span> <span data-ttu-id="d1779-135">En primer lugar, use la operación [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) para llegar a la carpeta, a continuación, recuperar la propiedad **PidTagAttributeHidden** , incluido el elemento [ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) y establece el valor de **PropertyTag** a 4340 y el **PropertyType **valor a Boolean.</span><span class="sxs-lookup"><span data-stu-id="d1779-135">First, use the [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) operation to get to the folder, then retrieve the **PidTagAttributeHidden** property by including the [ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) element, and setting the **PropertyTag** value to 4340 and the **PropertyType** value to Boolean.</span></span> 
  
<span data-ttu-id="d1779-136">También es la solicitud XML que la API administrada de EWS envía al usar el método **Bind** para obtener una carpeta antes de [realizar una carpeta oculta](#bk_hideewsma).</span><span class="sxs-lookup"><span data-stu-id="d1779-136">This is also the XML request that the EWS Managed API sends when you use the **Bind** method to get a folder before [making it a hidden folder](#bk_hideewsma).</span></span>
  
<span data-ttu-id="d1779-137">El valor de [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) se acorta para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="d1779-137">The [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) value is shortened for readability.</span></span> 
  
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
          <t:ExtendedFieldURI PropertyTag="4340"
                              PropertyType="Boolean" />
        </t:AdditionalProperties>
      </m:FolderShape>
      <m:FolderIds>
        <t:FolderId Id="IQywAAAA==" />
      </m:FolderIds>
    </m:GetFolder>
  </soap:Body>
</soap:Envelope>
```

El servidor responde a la solicitud de **GetFolder** con un mensaje de [GetFolderResponse](http://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que la carpeta se recuperó correctamente. La respuesta incluye también un [valor](http://msdn.microsoft.com/library/196278d4-5e77-4e0a-8af6-8ac065610510%28Office.15%29.aspx) para el [ExtendedProperty](http://msdn.microsoft.com/library/f9701409-b620-4afe-b9ee-4c1e95507af7%28Office.15%29.aspx). <span data-ttu-id="d1779-140">En este ejemplo, el **valor** se establece en **false**, lo que significa que la carpeta actualmente no está oculto.</span><span class="sxs-lookup"><span data-stu-id="d1779-140">In this example, the **Value** is set to **false**, which means that the folder is currently not hidden.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="898"
                         MinorBuildNumber="23"
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
              <t:FolderId Id="IQywAAAA=="
                          ChangeKey="AQAAABYAAAD32nSTjepyT63rYH17n9THAAAAABED" />
              <t:ExtendedProperty>
                <t:ExtendedFieldURI PropertyTag="0x10f4"
                                    PropertyType="Boolean" />
                <t:Value>false</t:Value>
              </t:ExtendedProperty>
            </t:Folder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="d1779-141">Para cambiar el valor de la **ExtendedProperty** en true, utilice la operación [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d1779-141">To change the value of the **ExtendedProperty** to true, use the [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="d1779-142">Incluir los elementos **ExtendedProperty**, **ExtendedFieldURI**y **valor** para que el **PidTagAttributeHidden** propiedad extendida y establecer el elemento de **valor** en **true** ocultar la carpeta.</span><span class="sxs-lookup"><span data-stu-id="d1779-142">Include the **ExtendedProperty**, **ExtendedFieldURI**, and **Value** elements for the **PidTagAttributeHidden** extended property, and set the **Value** element to **true** to hide the folder.</span></span> 
  
<span data-ttu-id="d1779-143">También es la solicitud XML que la API administrada de EWS envía al usar el método **Update** para actualizar una carpeta para [que sea una carpeta oculta](#bk_hideewsma).</span><span class="sxs-lookup"><span data-stu-id="d1779-143">This is also the XML request that the EWS Managed API sends when you use the **Update** method to update a folder to [make it a hidden folder](#bk_hideewsma).</span></span>
  
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
          <t:FolderId Id="IQywAAAA=="
                      ChangeKey="AQAAABYAAAD32nSTjepyT63rYH17n9THAAAAABED" />
          <t:Updates>
            <t:SetFolderField>
              <t:ExtendedFieldURI PropertyTag="4340"
                                  PropertyType="Boolean" />
              <t:Folder>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="4340"
                                      PropertyType="Boolean" />
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:Folder>
            </t:SetFolderField>
          </t:Updates>
        </t:FolderChange>
      </m:FolderChanges>
    </m:UpdateFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="d1779-144">El servidor responde a la solicitud de **UpdateFolder** con un mensaje de [UpdateFolderResponse](http://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, que indica que la carpeta se ha actualizado correctamente y ahora está oculto.</span><span class="sxs-lookup"><span data-stu-id="d1779-144">The server responds to the **UpdateFolder** request with an [UpdateFolderResponse](http://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the folder was updated successfully, and is now hidden.</span></span>
  
## <a name="find-all-hidden-folders-by-using-the-ews-managed-api"></a><span data-ttu-id="d1779-145">Buscar todas las carpetas ocultas mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="d1779-145">Find all hidden folders by using the EWS Managed API</span></span>
<span data-ttu-id="d1779-146"><a name="bk_findhiddenewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="d1779-146"></span></span>

<span data-ttu-id="d1779-147">Puede encontrar todas las carpetas ocultas dentro de una carpeta primaria mediante la creación de una [definición de la propiedad extendida](properties-and-extended-properties-in-ews-in-exchange.md) para el **PidTagAttributeHidden** propiedad extendida y, a continuación, utilizando el método [FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) para encontrar carpetas con un ** PidTagAttributeHidden** valor que se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="d1779-147">You can find all hidden folders under a parent folder by creating an [extended property definition](properties-and-extended-properties-in-ews-in-exchange.md) for the **PidTagAttributeHidden** extended property, and then using the [FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) method to find folders with a **PidTagAttributeHidden** value that is set to **true**.</span></span> <span data-ttu-id="d1779-148">En este ejemplo se usa el MsgFolderRoot, también conocido como el principio del almacén de información o subárbol IPM, como la carpeta principal para buscar en.</span><span class="sxs-lookup"><span data-stu-id="d1779-148">This example uses the MsgFolderRoot, also known as the Top of Information Store, or IPM Subtree, as the parent folder to search under.</span></span>
  
<span data-ttu-id="d1779-149">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido para el propietario del buzón, y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d1779-149">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox owner, and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
private static void FindHiddenFolders(ExchangeService service)
{
    // Create an extended property definition for the PidTagAttributeHidden property.
    ExtendedPropertyDefinition isHiddenProp = new ExtendedPropertyDefinition(0x10f4, MapiPropertyType.Boolean);
    // Create a folder view to retrieve up to 100 folders and 
    // retrieve only the PidTagAttributeHidden and the display name.
    FolderView folderView = new FolderView(100);
    folderView.PropertySet = new PropertySet(isHiddenProp, FolderSchema.DisplayName);
    // Indicate a Traversal value of Deep, so that all subfolders are retrieved.
    folderView.Traversal = FolderTraversal.Deep;
    // Find all hidden folders under the MsgFolderRoot.
    // This call results in a FindFolder call to EWS.
    FindFoldersResults findFolder = service.FindFolders(WellKnownFolderName.MsgFolderRoot,
            new SearchFilter.IsEqualTo(isHiddenProp, true), folderView);
    // Display the folder ID and display name of each hidden folder.
    foreach (Folder folder in findFolder)
    {
        Console.WriteLine("FolderId: {0}", folder.Id);
        Console.WriteLine("DisplayName: {0}", folder.DisplayName);
        Console.WriteLine("\r\n");
    }
}
```

## <a name="find-all-hidden-folders-by-using-ews"></a><span data-ttu-id="d1779-150">Buscar todas las carpetas ocultas mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="d1779-150">Find all hidden folders by using EWS</span></span>
<span data-ttu-id="d1779-151"><a name="bk_findhiddenews"> </a></span><span class="sxs-lookup"><span data-stu-id="d1779-151"></span></span>

<span data-ttu-id="d1779-152">Puede usar EWS para buscar todas las carpetas ocultas en una carpeta existente mediante una llamada a la operación [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) y buscando carpetas cuyo [PidTagAttributeHidden](http://msdn.microsoft.com/en-us/library/cc433490%28v=exchg.80%29.aspx) propiedad extendida está establecida en **true**.</span><span class="sxs-lookup"><span data-stu-id="d1779-152">You can use EWS to find all hidden folders under an existing folder by calling the [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) operation and searching for folders whose [PidTagAttributeHidden](http://msdn.microsoft.com/en-us/library/cc433490%28v=exchg.80%29.aspx) extended property is set to **true**.</span></span> <span data-ttu-id="d1779-153">Para ello, incluya un [IsEqualTo](http://msdn.microsoft.com/library/48e7e067-049c-4184-8026-071e6f558e8a%28Office.15%29.aspx)[restricción](http://msdn.microsoft.com/library/77f19014-d112-4999-8e83-ecc32a117a73%28Office.15%29.aspx) que busca el elemento [ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) para la propiedad **PidTagAttributeHidden** (valor de **PropertyTag** a 4243 y el valor de **PropertyType** a Boolean), como se muestra en la siguiente solicitud.</span><span class="sxs-lookup"><span data-stu-id="d1779-153">To do this, include an [IsEqualTo](http://msdn.microsoft.com/library/48e7e067-049c-4184-8026-071e6f558e8a%28Office.15%29.aspx)[Restriction](http://msdn.microsoft.com/library/77f19014-d112-4999-8e83-ecc32a117a73%28Office.15%29.aspx) that searches for the [ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) element for the **PidTagAttributeHidden** property ( **PropertyTag** value to 4243 and the **PropertyType** value to Boolean), as shown in the following request.</span></span> <span data-ttu-id="d1779-154">En este ejemplo se usa el MsgFolderRoot, también conocido como el principio del almacén de información o subárbol IPM, como la carpeta principal para buscar en.</span><span class="sxs-lookup"><span data-stu-id="d1779-154">This example uses the MsgFolderRoot, also known as the Top of Information Store, or IPM Subtree, as the parent folder to search under.</span></span> 
  
<span data-ttu-id="d1779-155">También es la solicitud XML que la API administrada de EWS envía cuando se utiliza el método **FindFolders** para [Buscar todas las carpetas ocultas](#bk_findhiddenewsma).</span><span class="sxs-lookup"><span data-stu-id="d1779-155">This is also the XML request that the EWS Managed API sends when you use the **FindFolders** method to [find all hidden folders](#bk_findhiddenewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Central Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindFolder Traversal="Deep">
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:ExtendedFieldURI PropertyTag="4340"
                              PropertyType="Boolean" />
          <t:FieldURI FieldURI="folder:DisplayName" />
        </t:AdditionalProperties>
      </m:FolderShape>
      <m:IndexedPageFolderView MaxEntriesReturned="100"
                               Offset="0"
                               BasePoint="Beginning" />
      <m:Restriction>
        <t:IsEqualTo>
          <t:ExtendedFieldURI PropertyTag="4340"
                              PropertyType="Boolean" />
          <t:FieldURIOrConstant>
            <t:Constant Value="true" />
          </t:FieldURIOrConstant>
        </t:IsEqualTo>
      </m:Restriction>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="msgfolderroot" />
      </m:ParentFolderIds>
    </m:FindFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="d1779-156">El servidor responde a la solicitud de **FindFolder** con un mensaje de [FindFolderResponse](http://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, que indica que la búsqueda de la carpeta se realizó correctamente, así como todos los ocultos carpetas bajo la carpeta raíz del mensaje.</span><span class="sxs-lookup"><span data-stu-id="d1779-156">The server responds to the **FindFolder** request with a [FindFolderResponse](http://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the folder search was successful, as well as all the hidden folders under the root message folder.</span></span>
  
<span data-ttu-id="d1779-157">Los valores de [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) son más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="d1779-157">The [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) values are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="898"
                         MinorBuildNumber="23"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="6"
                        TotalItemsInView="6"
                        IncludesLastItemInRange="true">
            <t:Folders>
              <t:ContactsFolder>
                <t:FolderId Id="IBHgAAAA=="
                            ChangeKey="AwAAABYAAAD32nSTjepyT63rYH17n9THAAAAAACz" />
                <t:DisplayName>{06967759-274D-40B2-A3EB-D7F9E73727D7}</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean" />
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:ContactsFolder>
              <t:ContactsFolder>
                <t:FolderId Id="IBHwAAAA=="
                            ChangeKey="AwAAABYAAAD32nSTjepyT63rYH17n9THAAAAAAC7" />
                <t:DisplayName>{A9E2BC46-B3A0-4243-B315-60D991004455}</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean" />
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:ContactsFolder>
              <t:ContactsFolder>
                <t:FolderId Id="IBIQAAAA=="
                            ChangeKey="AwAAABYAAAD32nSTjepyT63rYH17n9THAAAAAADO" />
                <t:DisplayName>GAL Contacts</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean" />
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:ContactsFolder>
              <t:ContactsFolder>
                <t:FolderId Id="IBHQAAAA=="
                            ChangeKey="AwAAABYAAAD32nSTjepyT63rYH17n9THAAAAAACa" />
                <t:DisplayName>Recipient Cache</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean" />
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:ContactsFolder>
              <t:Folder>
                <t:FolderId Id="HAAAAA=="
                            ChangeKey="AQAAABYAAAD32nSTjepyT63rYH17n9THAAAAAACS" />
                <t:DisplayName>Conversation Action Settings</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean" />
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:Folder>
              <t:Folder>
                <t:FolderId Id="IQywAAAA=="
                            ChangeKey="AQAAABYAAAD32nSTjepyT63rYH17n9THAAAeZIBf" />
                <t:DisplayName>TestFolder</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean" />
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:Folder>
            </t:Folders>
          </m:RootFolder>
        </m:FindFolderResponseMessage>
      </m:ResponseMessages>
    </m:FindFolderResponse>
  </s:Body>
</s:Envelope>
```

## 
<span data-ttu-id="d1779-158"><a name="bk_findhiddenews"> </a></span><span class="sxs-lookup"><span data-stu-id="d1779-158"></span></span>

<span data-ttu-id="d1779-159">Después de que haya ocultado o no ocultos de las carpetas, es posible que desee obtener la jerarquía de carpetas o [sincronizar la jerarquía de carpetas](how-to-synchronize-folders-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="d1779-159">After you have hidden or unhidden folders, you might want to get the folder hierarchy or [synchronize the folder hierarchy](how-to-synchronize-folders-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="d1779-160">Los ejemplos que muestran que cómo [obtener una jerarquía de carpetas mediante el uso de la API administrada de EWS](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_getfolderhierarchyewsma) u [obtener una jerarquía de carpetas mediante el uso de EWS](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_getfolderhierarchyews) también indicar qué carpetas de la jerarquía están ocultos.</span><span class="sxs-lookup"><span data-stu-id="d1779-160">The examples that show you how to [get a folder hierarchy by using the EWS Managed API](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_getfolderhierarchyewsma) or [get a folder hierarchy by using EWS](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_getfolderhierarchyews) also indicate which folders in the hierarchy are hidden.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d1779-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1779-161">See also</span></span>


- [<span data-ttu-id="d1779-162">Las carpetas y elementos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d1779-162">Folders and items in EWS in Exchange</span></span>](folders-and-items-in-ews-in-exchange.md)
    
- [<span data-ttu-id="d1779-163">Trabajar con carpetas mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d1779-163">Work with folders by using EWS in Exchange</span></span>](how-to-work-with-folders-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="d1779-164">Trabajar con las carpetas de búsqueda con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d1779-164">Work with search folders by using EWS in Exchange</span></span>](how-to-work-with-search-folders-by-using-ews-in-exchange.md)
    

