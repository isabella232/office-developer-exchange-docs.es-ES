---
title: Resolver nombres ambiguos mediante EWS en Exchange 2013
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1ba21c54-ecd2-4a1e-80d4-0f4171dea84f
description: Obtenga información sobre cómo usar la API administrada de EWS o EWS para resolver nombres ambiguos al obtener posibles coincidencias de los servicios de dominio de Active Directory (AD DS) o de una carpeta de contactos en el buzón de correo del usuario.
ms.openlocfilehash: 5e30e268f54e6ca257e188592e49d168e64332ff
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527750"
---
# <a name="resolve-ambiguous-names-by-using-ews-in-exchange-2013"></a><span data-ttu-id="a1726-103">Resolver nombres ambiguos mediante EWS en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="a1726-103">Resolve ambiguous names by using EWS in Exchange 2013</span></span>

<span data-ttu-id="a1726-104">Obtenga información sobre cómo usar la API administrada de EWS o EWS para resolver nombres ambiguos al obtener posibles coincidencias de los servicios de dominio de Active Directory (AD DS) o de una carpeta de contactos en el buzón de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="a1726-104">Learn how to use the EWS Managed API or EWS to resolve ambiguous names by getting possible matches from Active Directory Domain Services (AD DS) or a contacts folder in your user's mailbox.</span></span>
  
<span data-ttu-id="a1726-105">Un usuario de la organización recibe una lista de nombres y direcciones que se escriben a mano para los empleados que hayan asistido a una sesión de formación.</span><span class="sxs-lookup"><span data-stu-id="a1726-105">A user in your organization is given a hand-written list of names and addresses for employees that attended a training session.</span></span> <span data-ttu-id="a1726-106">Quieren enviar un mensaje de correo electrónico con información adicional a las personas de la lista, pero no pueden leer la dirección de correo electrónico de todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="a1726-106">They want to send an email with some additional information to people on the list, but they can't read everyone's email address.</span></span> <span data-ttu-id="a1726-107">Si desea solucionar este problema para los usuarios de su aplicación, EWS puede ayudarle.</span><span class="sxs-lookup"><span data-stu-id="a1726-107">If you want to solve this problem for your users in your application, EWS can help.</span></span> <span data-ttu-id="a1726-108">Puede usar el método de la API administrada de EWS [ExchangeService. ResolveName](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) o la operación de EWS [ResolveNames](https://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) para devolver una lista de posibles coincidencias para una selección de texto, como parte de un apellido.</span><span class="sxs-lookup"><span data-stu-id="a1726-108">You can use the [ExchangeService.ResolveName](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) EWS Managed API method or the [ResolveNames](https://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) EWS operation to return a list of potential matches for a selection of text, such as part of a last name.</span></span> <span data-ttu-id="a1726-109">Los elementos devueltos pueden ser buzones de usuario públicos, grupos de distribución y contactos.</span><span class="sxs-lookup"><span data-stu-id="a1726-109">The returned items can be public user mailboxes, distribution groups, and contacts.</span></span> 
  
<span data-ttu-id="a1726-110">Tenga en cuenta que Exchange guarda direcciones de correo electrónico con tipos de enrutamiento con prefijo, como SMTP o SIP, en una matriz de varios valores.</span><span class="sxs-lookup"><span data-stu-id="a1726-110">Note that Exchange saves email addresses with prefixed routing types, such as smtp or sip, in a multivalue array.</span></span> <span data-ttu-id="a1726-111">El método **ResolveName** y la operación **ResolveNames** realizan una coincidencia parcial con cada valor de la matriz cuando se agrega el tipo de enrutamiento al principio del nombre sin resolver, como "SIP: user1".</span><span class="sxs-lookup"><span data-stu-id="a1726-111">The **ResolveName** method and the **ResolveNames** operation perform a partial match against each value of that array when you add the routing type at the beginning of the unresolved name, such as "sip:User1".</span></span> <span data-ttu-id="a1726-112">Si no especifica un tipo de enrutamiento, el método o la operación tomarán el valor predeterminado SMTP, se hará coincidir con una propiedad de dirección SMTP principal y no buscarán en la matriz de varios valores.</span><span class="sxs-lookup"><span data-stu-id="a1726-112">If you don't specify a routing type, the method or operation will default to smtp, match it to a primary smtp address property, and not search the multivalue array.</span></span> <span data-ttu-id="a1726-113">Por ejemplo, si busca user1 y no incluye el prefijo SIP, no recibirá sip:User1@Contoso.com como resultado, incluso si es un buzón válido.</span><span class="sxs-lookup"><span data-stu-id="a1726-113">For example, if you search for User1 and do not include the sip prefix, you will not receive sip:User1@Contoso.com as a result, even if that is a valid mailbox.</span></span> 
  
<span data-ttu-id="a1726-114">Solo se puede especificar un nombre ambiguo en una sola solicitud.</span><span class="sxs-lookup"><span data-stu-id="a1726-114">You can only specify one ambiguous name in a single request.</span></span> <span data-ttu-id="a1726-115">Si tiene una lista de nombres ambiguos que se van a resolver, deberá recorrer la lista y llamar al método o la operación para cada entrada.</span><span class="sxs-lookup"><span data-stu-id="a1726-115">If you have a list of ambiguous names to resolve, you will need to loop through the list and call the method or operation for each entry.</span></span> <span data-ttu-id="a1726-116">Los candidatos de la carpeta de contactos de un usuario tendrán un valor de identificador de elemento no NULL, que se puede usar en una llamada al método [Contact. bind](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) o en una solicitud de operación [GetItem](https://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) para recuperar información adicional.</span><span class="sxs-lookup"><span data-stu-id="a1726-116">Candidates from a user's Contacts folder will have a non-null item ID value, which can then be used in a [Contact.Bind](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) method call or [GetItem](https://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) operation request to retrieve additional information.</span></span> <span data-ttu-id="a1726-117">Si el candidato es un grupo de distribución, puede usar el método de la API administrada EWS de [ExpandGroup (Itemid)](https://msdn.microsoft.com/library/office/ee356407%28v=exchg.80%29.aspx) o la operación de EWS [ExpandDL](https://msdn.microsoft.com/library/affe84a5-ad98-4aba-83f4-8732938b763d%28Office.15%29.aspx) para obtener la lista de miembros.</span><span class="sxs-lookup"><span data-stu-id="a1726-117">If the candidate is a distribution group, you can use the [ExpandGroup(ItemId)](https://msdn.microsoft.com/library/office/ee356407%28v=exchg.80%29.aspx) EWS Managed API method or the [ExpandDL](https://msdn.microsoft.com/library/affe84a5-ad98-4aba-83f4-8732938b763d%28Office.15%29.aspx) EWS operation to get the list of members.</span></span> <span data-ttu-id="a1726-118">Si el parámetro _returnContactDetails_ o el atributo EWS **ReturnFullContactData** está establecido en true, las entradas de Active Directory devueltas a través de un método **ResolveName** o una operación **ResolveNames** incluirán propiedades adicionales que describen el contacto.</span><span class="sxs-lookup"><span data-stu-id="a1726-118">If the  _returnContactDetails_ parameter or the **ReturnFullContactData** EWS attribute is set to true, Active Directory entries returned via a **ResolveName** method or **ResolveNames** operation will include additional properties that describe the contact.</span></span> <span data-ttu-id="a1726-119">El parámetro _returnContactDetails_ o el atributo **ReturnFullContactData** no afectan a los datos que se devuelven para contactos y grupos de contactos.</span><span class="sxs-lookup"><span data-stu-id="a1726-119">The  _returnContactDetails_ parameter or the **ReturnFullContactData** attribute does not affect the data that is returned for contacts and contact groups.</span></span> 
  
## <a name="resolve-ambiguous-names-by-using-ews-managed-api"></a><span data-ttu-id="a1726-120">Resolución de nombres ambiguos mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="a1726-120">Resolve ambiguous names by using EWS Managed API</span></span>
<span data-ttu-id="a1726-121"><a name="bk_EWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="a1726-121"><a name="bk_EWSMA"> </a></span></span>

<span data-ttu-id="a1726-122">Puede usar el método [ResolveName](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) para buscar candidatos que coinciden con el nombre ambiguo que ha pasado.</span><span class="sxs-lookup"><span data-stu-id="a1726-122">You can use the [ResolveName](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) method to find candidates that match the ambiguous name you pass.</span></span> <span data-ttu-id="a1726-123">Puede usar sobrecargas del método **ResolveName** para buscar candidatos de cinco maneras diferentes.</span><span class="sxs-lookup"><span data-stu-id="a1726-123">You can use overloads of the **ResolveName** method to search for candidates in five different ways.</span></span> 
  
<span data-ttu-id="a1726-124">**Tabla 1. Métodos ResolveName sobrecargados**</span><span class="sxs-lookup"><span data-stu-id="a1726-124">**Table 1. Overloaded ResolveName methods**</span></span>

|<span data-ttu-id="a1726-125">**Método**</span><span class="sxs-lookup"><span data-stu-id="a1726-125">**Method**</span></span>|<span data-ttu-id="a1726-126">**Funcionamiento**</span><span class="sxs-lookup"><span data-stu-id="a1726-126">**How it works**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a1726-127">ResolveName (cadena)</span><span class="sxs-lookup"><span data-stu-id="a1726-127">ResolveName(String)</span></span>](https://msdn.microsoft.com/library/dd635548%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="a1726-128">Busca contactos en la carpeta de contactos del usuario y en la lista global de direcciones (GAL), en ese orden.</span><span class="sxs-lookup"><span data-stu-id="a1726-128">Finds contacts in the user's Contacts folder and the Global Address List (GAL) — in that order.</span></span> <span data-ttu-id="a1726-129">La variable de cadena es el nombre ambiguo que está intentando resolver.</span><span class="sxs-lookup"><span data-stu-id="a1726-129">The string variable is the ambiguous name you are trying to resolve.</span></span>  <br/> |
|[<span data-ttu-id="a1726-130">ResolveName (String, ResolveNameSearchLocation, Boolean)</span><span class="sxs-lookup"><span data-stu-id="a1726-130">ResolveName(String, ResolveNameSearchLocation, Boolean)</span></span>](https://msdn.microsoft.com/library/dd634595%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="a1726-131">Busca contactos en la carpeta contactos predeterminada o en la lista global de direcciones (GAL).</span><span class="sxs-lookup"><span data-stu-id="a1726-131">Finds contacts in the default Contacts folder and/or the Global Address List (GAL).</span></span> <span data-ttu-id="a1726-132">El valor de cadena es el nombre ambiguo, la ubicación de búsqueda especifica la carpeta de contactos o la GAL, y el valor booleano indica si se debe devolver la información de contacto completa.</span><span class="sxs-lookup"><span data-stu-id="a1726-132">The string value is the ambiguous name, the search location specifies the Contacts folder and/or the GAL, and the Boolean value indicates whether to return the full contact information.</span></span>  <br/> |
|[<span data-ttu-id="a1726-133">ResolveName (String, ResolveNameSearchLocation, Boolean, PropertySet)</span><span class="sxs-lookup"><span data-stu-id="a1726-133">ResolveName(String, ResolveNameSearchLocation, Boolean, PropertySet)</span></span>](https://msdn.microsoft.com/library/hh532803%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="a1726-134">Busca contactos en la carpeta contactos predeterminada o en la lista global de direcciones (GAL).</span><span class="sxs-lookup"><span data-stu-id="a1726-134">Finds contacts in the default Contacts folder and/or Global Address List (GAL).</span></span> <span data-ttu-id="a1726-135">Este método permite establecer las propiedades que se devuelven.</span><span class="sxs-lookup"><span data-stu-id="a1726-135">This method enables you to set the properties that are returned.</span></span>  <br/> |
|[<span data-ttu-id="a1726-136">ResolveName (String, IEnumerable \<FolderId\> , ResolveNameSearchLocation, Boolean)</span><span class="sxs-lookup"><span data-stu-id="a1726-136">ResolveName(String, IEnumerable\<FolderId\>, ResolveNameSearchLocation, Boolean)</span></span>](https://msdn.microsoft.com/library/dd636014%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="a1726-137">Busca contactos en las carpetas de contactos especificadas o en la lista global de direcciones (GAL).</span><span class="sxs-lookup"><span data-stu-id="a1726-137">Finds contacts in specified contact folders and/or the Global Address List (GAL).</span></span> <span data-ttu-id="a1726-138">Puede usar este método para pasar una colección de carpetas para buscar.</span><span class="sxs-lookup"><span data-stu-id="a1726-138">You can use this method to pass a collection of folders to search.</span></span> <span data-ttu-id="a1726-139">Esto le permite buscar en carpetas de contactos distintas de la carpeta de contactos predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a1726-139">This enables you to look in contact folders other than the default Contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="a1726-140">ResolveName (String, IEnumerable \<FolderId\> , ResolveNameSearchLocation, Boolean, PropertySet)</span><span class="sxs-lookup"><span data-stu-id="a1726-140">ResolveName(String, IEnumerable\<FolderId\>, ResolveNameSearchLocation, Boolean, PropertySet)</span></span>](https://msdn.microsoft.com/library/hh532581%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="a1726-141">Busca contactos en la lista global de direcciones (GAL) o en carpetas de contactos específicas.</span><span class="sxs-lookup"><span data-stu-id="a1726-141">Finds contacts in the Global Address List (GAL) and/or in specific contact folders.</span></span> <span data-ttu-id="a1726-142">Este método permite establecer las propiedades que se devuelven.</span><span class="sxs-lookup"><span data-stu-id="a1726-142">This method enables you to set the properties that are returned.</span></span>  <br/> |
   
<span data-ttu-id="a1726-143">Comencemos con un ejemplo sencillo.</span><span class="sxs-lookup"><span data-stu-id="a1726-143">Let's start with a simple example.</span></span> <span data-ttu-id="a1726-144">En el siguiente ejemplo, se muestra cómo resolver la cadena de texto "dan" y se muestra el nombre y la dirección de correo electrónico de cada candidato encontrado.</span><span class="sxs-lookup"><span data-stu-id="a1726-144">The following example shows how to resolve the text string "dan" and output the name and email address of each candidate found.</span></span> <span data-ttu-id="a1726-145">En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a1726-145">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
// Resolve the ambiguous name "dan".
   NameResolutionCollection resolvedNames = service.ResolveName("dan");
   // Output the list of candidates.
   foreach (NameResolution nameRes in resolvedNames)
   {
      Console.WriteLine("Contact name: " + nameRes.Mailbox.Name);
      Console.WriteLine("Contact e-mail address: " + nameRes.Mailbox.Address);
      Console.WriteLine("Mailbox type: " + nameRes.Mailbox.MailboxType);
   }

```

<span data-ttu-id="a1726-146">La respuesta devuelve un máximo de 100 candidatos, aunque podría haber más de 100 candidatos potenciales.</span><span class="sxs-lookup"><span data-stu-id="a1726-146">The response returns a maximum of 100 candidates, although there might be more than 100 potential candidates.</span></span> <span data-ttu-id="a1726-147">Para determinar si solo se devolvieron los primeros 100 candidatos de un número mayor de candidatos, compruebe el valor de [IncludesAllResolutions](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.includesallresolutions%28v=exchg.80%29.aspx) en el objeto [NameResolutionCollection](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1726-147">To determine whether only the first 100 candidates of a larger number of candidates were returned, check the value of [IncludesAllResolutions](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.includesallresolutions%28v=exchg.80%29.aspx) in the [NameResolutionCollection](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx) object.</span></span> <span data-ttu-id="a1726-148">Si el valor es true, no hay más candidatos posibles; Si el valor es false, el método sólo devuelve el primer 100 de un número mayor de candidatos potenciales.</span><span class="sxs-lookup"><span data-stu-id="a1726-148">If the value is true, there are no more possible candidates; if the value is false, the method only returned the first 100 of a larger number of potential candidates.</span></span> 
  
<span data-ttu-id="a1726-149">Si trabaja en una organización de gran tamaño, es probable que un nombre como "dan" devuelva el número máximo de 100 candidatos.</span><span class="sxs-lookup"><span data-stu-id="a1726-149">If you work in a large organization, it's likely that a name like "dan" will return the maximum number of 100 candidates.</span></span> <span data-ttu-id="a1726-150">Para reducir el número de candidatos devueltos, limite dónde realiza la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a1726-150">To reduce the number of candidates returned, limit where you search.</span></span> <span data-ttu-id="a1726-151">El siguiente ejemplo usa la enumeración [ResolveNameSearchLocation](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.resolvenamesearchlocation%28v=exchg.80%29.aspx) para especificar dónde buscar para resolver el nombre ambiguo.</span><span class="sxs-lookup"><span data-stu-id="a1726-151">The next example uses the [ResolveNameSearchLocation](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.resolvenamesearchlocation%28v=exchg.80%29.aspx) enumeration to specify where to search to resolve the ambiguous name.</span></span> 
  
```cs
// Resolve the ambiguous name "dan".
// Only use the Contacts folder.
   NameResolutionCollection resolvedNames = service.ResolveName("dan", ResolveNameSearchLocation.ContactsOnly, false);
   // Output the list of candidates.   
   foreach (NameResolution nameRes in resolvedNames)
   {
      Console.WriteLine("Contact name: " + nameRes.Mailbox.Name);
      Console.WriteLine("Contact e-mail address: " + nameRes.Mailbox.Address);
      Console.WriteLine("Mailbox type: " + nameRes.Mailbox.MailboxType);
   }

```

<span data-ttu-id="a1726-152">Si almacena los contactos en una carpeta que no sea la carpeta de contactos conocida, use uno de los métodos sobrecargados para especificar dónde buscar candidatos.</span><span class="sxs-lookup"><span data-stu-id="a1726-152">If you store your contacts in a folder other than the well-known Contacts folder, use one of the overloaded methods to specify where to look for candidates.</span></span> <span data-ttu-id="a1726-153">En el ejemplo siguiente se crea una lista de carpetas para el método **ResolveName** basándose en el identificador de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a1726-153">The following example creates a folder list for the **ResolveName** method based on the folder ID.</span></span> <span data-ttu-id="a1726-154">La **FolderId** se ha abreviado para facilitar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="a1726-154">The **FolderId** has been shortened for readability.</span></span> 
  
```cs
// Create a list to store folders to search.
List<FolderId> folders = new List<FolderId>();
// Add a folder to the list based on the FolderId.
folders.Add(new FolderId("AABR8mboAAA="));
// Resolve the ambiguous name "dan".
// Only use the folders specified.
NameResolutionCollection resolvedNames = service.ResolveName("dan", folders, ResolveNameSearchLocation.ContactsOnly, false);
   foreach (NameResolution nameRes in resolvedNames)
   {
      Console.WriteLine("Contact name: " + nameRes.Mailbox.Name);
      Console.WriteLine("Contact e-mail address: " + nameRes.Mailbox.Address);
      Console.WriteLine("Mailbox type: " + nameRes.Mailbox.MailboxType);
   }

```

<span data-ttu-id="a1726-155">Si se aplican filtros y no se devuelven candidatos, el [NameResolutionCollection](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx) no contendrá ninguna entrada.</span><span class="sxs-lookup"><span data-stu-id="a1726-155">If you apply filters and no candidates are returned, the [NameResolutionCollection](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx) will contain zero entries.</span></span> <span data-ttu-id="a1726-156">Puede comprobarlo observando la propiedad [Count](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.count%28v=exchg.80%29.aspx) de la colección.</span><span class="sxs-lookup"><span data-stu-id="a1726-156">You can verify this by looking at the [Count](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.count%28v=exchg.80%29.aspx) property of the collection.</span></span> 
  
## <a name="resolve-ambiguous-names-by-using-ews"></a><span data-ttu-id="a1726-157">Resolución de nombres ambiguos mediante EWS</span><span class="sxs-lookup"><span data-stu-id="a1726-157">Resolve ambiguous names by using EWS</span></span>
<span data-ttu-id="a1726-158"><a name="bk_EWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="a1726-158"><a name="bk_EWSMA"> </a></span></span>

<span data-ttu-id="a1726-159">Puede usar la operación de EWS de [ResolveNames](https://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) para identificar posibles candidatos para un nombre ambiguo.</span><span class="sxs-lookup"><span data-stu-id="a1726-159">You can use the [ResolveNames](https://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) EWS operation to identify possible candidates for an ambiguous name.</span></span> <span data-ttu-id="a1726-160">El elemento [UnresolvedEntry](https://msdn.microsoft.com/library/5ac6116a-3b24-40f8-a877-dbe9a6935919%28Office.15%29.aspx) contiene el nombre ambiguo que desea resolver.</span><span class="sxs-lookup"><span data-stu-id="a1726-160">The [UnresolvedEntry](https://msdn.microsoft.com/library/5ac6116a-3b24-40f8-a877-dbe9a6935919%28Office.15%29.aspx) element contains the ambiguous name you want to resolve.</span></span> <span data-ttu-id="a1726-161">En el siguiente ejemplo, se muestra cómo resolver el nombre Sadie.</span><span class="sxs-lookup"><span data-stu-id="a1726-161">The following example shows how to resolve the name Sadie.</span></span> <span data-ttu-id="a1726-162">También es la solicitud XML que usa la API administrada de EWS cuando usa [el método ResolveName](#bk_EWSMA), excepto que usa un nombre diferente para los ejemplos de resultados válidos.</span><span class="sxs-lookup"><span data-stu-id="a1726-162">This is also the XML request that the EWS Managed API uses when you [use the ResolveName method](#bk_EWSMA), except that it uses a different name for valid output examples.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ResolveNames xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                  ReturnFullContactData="true">
      <UnresolvedEntry>Sadie</UnresolvedEntry>
    </ResolveNames>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="a1726-163">La respuesta devuelve un máximo de 100 candidatos, aunque es posible que haya más de 100 candidatos potenciales para determinar si solo se devolvieron los primeros 100 candidatos de un número mayor de candidatos, compruebe el valor del atributo [IncludesLastItemInRange](https://msdn.microsoft.com/library/e7d6c7d3-548e-48b0-a313-bfef81e4832a%28Office.15%29.aspx) del elemento [ResolutionSet](https://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a1726-163">The response returns a maximum of 100 candidates, although there might be more than 100 potential candidates To determine whether only the first 100 candidates of a larger number of candidates were returned, check the value of the [IncludesLastItemInRange](https://msdn.microsoft.com/library/e7d6c7d3-548e-48b0-a313-bfef81e4832a%28Office.15%29.aspx) attribute of the [ResolutionSet](https://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="a1726-164">Si el valor es true, no hay más candidatos posibles; Si el valor es false, la operación sólo devuelve el primer 100 de un número mayor de candidatos potenciales.</span><span class="sxs-lookup"><span data-stu-id="a1726-164">If the value is true, there are no more possible candidates; if the value is false, the operation only returned the first 100 of a larger number of potential candidates.</span></span> 
  
<span data-ttu-id="a1726-165">En el ejemplo siguiente se muestra la respuesta XML cuando se encuentra un candidato.</span><span class="sxs-lookup"><span data-stu-id="a1726-165">The following example shows the XML response when one candidate is found.</span></span> <span data-ttu-id="a1726-166">Recuerde que [ResolutionSet](https://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx) puede contener hasta 100 candidatos, cada uno de los cuales está representado por el elemento [Resolution](https://msdn.microsoft.com/library/573bed4b-d7b1-4baf-b16f-0795cdebf1a7%28Office.15%29.aspx) y sus elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="a1726-166">Remember, the [ResolutionSet](https://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx) can contain up to 100 candidates, each one represented by the [Resolution](https://msdn.microsoft.com/library/573bed4b-d7b1-4baf-b16f-0795cdebf1a7%28Office.15%29.aspx) element and its child elements.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResolveNamesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ResolveNamesResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ResolutionSet TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Resolution>
              <t:Mailbox>
                <t:Name>Sadie Daniels</t:Name>
                <t:EmailAddress>Sadie@Contoso.com</t:EmailAddress>
                <t:RoutingType>SMTP</t:RoutingType>
                <t:MailboxType>Mailbox</t:MailboxType>
              </t:Mailbox>
              <t:Contact>
                <t:DisplayName>Sadie Daniels</t:DisplayName>
                <t:EmailAddresses>
                  <t:Entry Key="EmailAddress1">SMTP:Sadie@Contoso.com</t:Entry>
                </t:EmailAddresses>
                <t:ContactSource>ActiveDirectory</t:ContactSource>
              </t:Contact>
            </t:Resolution>
          </m:ResolutionSet>
        </m:ResolveNamesResponseMessage>
      </m:ResponseMessages>
    </ResolveNamesResponse>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="a1726-167">No siempre irá a los candidatos para su nombre ambiguo.</span><span class="sxs-lookup"><span data-stu-id="a1726-167">You're not always going to come up with candidates for your ambiguous name.</span></span> <span data-ttu-id="a1726-168">En el ejemplo siguiente se muestra la respuesta XML, como un error, cuando no se encuentran candidatos.</span><span class="sxs-lookup"><span data-stu-id="a1726-168">The following example shows the XML response, as an error, when no candidates are found.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResolveNamesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ResolveNamesResponseMessage ResponseClass="Error">
          <m:MessageText>No results were found.</m:MessageText>
          <m:ResponseCode>ErrorNameResolutionNoResults</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:ResolveNamesResponseMessage>
      </m:ResponseMessages>
    </ResolveNamesResponse>
  </soap:Body>
</soap:Envelope>

```

## <a name="see-also"></a><span data-ttu-id="a1726-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1726-169">See also</span></span>


- [<span data-ttu-id="a1726-170">Personas y contactos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a1726-170">People and contacts in EWS in Exchange</span></span>](people-and-contacts-in-ews-in-exchange.md)
    
- [<span data-ttu-id="a1726-171">Expandir grupos de distribución mediante EWS en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="a1726-171">Expand distribution groups by using EWS in Exchange 2013</span></span>](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    

