---
title: Busque los extremos de detección automática mediante el uso de búsqueda de SCP en Exchange
manager: kelbow
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: b24228a8-5127-4bac-aef0-9c9e8843c9ff
description: Descubra cómo ubicar objetos SCP de detección automática en los servicios de dominio de Active Directory (AD DS) y usarlos para buscar direcciones URL de extremo de detección automática para usar con el servicio de detección automática de Exchange.
ms.openlocfilehash: 59fd316d0aa0feea81b60c279040da018c51b47d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763059"
---
# <a name="find-autodiscover-endpoints-by-using-scp-lookup-in-exchange"></a><span data-ttu-id="71bc4-103">Busque los extremos de detección automática mediante el uso de búsqueda de SCP en Exchange</span><span class="sxs-lookup"><span data-stu-id="71bc4-103">Find Autodiscover endpoints by using SCP lookup in Exchange</span></span>

<span data-ttu-id="71bc4-104">Descubra cómo ubicar objetos SCP de detección automática en los servicios de dominio de Active Directory (AD DS) y usarlos para buscar direcciones URL de extremo de detección automática para usar con el servicio de detección automática de Exchange.</span><span class="sxs-lookup"><span data-stu-id="71bc4-104">Find out how to locate Autodiscover SCP objects in Active Directory Domain Services (AD DS) and use them to find Autodiscover endpoint URLs to use with the Exchange Autodiscover service.</span></span>
  
<span data-ttu-id="71bc4-105">Detección automática facilita recuperar la información que necesita para conectarse a los buzones de correo en los servidores de Exchange.</span><span class="sxs-lookup"><span data-stu-id="71bc4-105">Autodiscover makes it easy to retrieve information that you need to connect to mailboxes on Exchange servers.</span></span> <span data-ttu-id="71bc4-106">Sin embargo, para poder usar la detección automática, se necesita una forma para buscar servidores de detección automática que son adecuados para el usuario que está recuperando la configuración para.</span><span class="sxs-lookup"><span data-stu-id="71bc4-106">However, in order to use Autodiscover, you need a way to find Autodiscover servers that are appropriate for the user you're retrieving settings for.</span></span> <span data-ttu-id="71bc4-107">Objetos de punto (SCP) de conexión de servicio en AD DS proporcionan una manera fácil para los clientes Unidos a un dominio buscar servidores de detección automática.</span><span class="sxs-lookup"><span data-stu-id="71bc4-107">Service connection point (SCP) objects in AD DS provide an easy way for domain-joined clients to look up Autodiscover servers.</span></span> 
  
## <a name="get-set-up-to-find-autodiscover-endpoints"></a><span data-ttu-id="71bc4-108">Configurar la aplicación para buscar los extremos de detección automática</span><span class="sxs-lookup"><span data-stu-id="71bc4-108">Get set up to find Autodiscover endpoints</span></span>
<span data-ttu-id="71bc4-109"><a name="bk_PreReqs"> </a></span><span class="sxs-lookup"><span data-stu-id="71bc4-109"></span></span>

<span data-ttu-id="71bc4-110">Para localizar objetos SCP de detección automática en AD DS, necesita tener acceso a lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="71bc4-110">To locate Autodiscover SCP objects in AD DS, you need to have access to the following:</span></span>
  
- <span data-ttu-id="71bc4-111">Un servidor que está ejecutando una versión de Exchange local iniciando con Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="71bc4-111">A server that is running a version of Exchange on-premises starting with Exchange 2007 SP1.</span></span>
    
- <span data-ttu-id="71bc4-112">Un equipo cliente que se ha unido al dominio que se instala el servidor de Exchange en.</span><span class="sxs-lookup"><span data-stu-id="71bc4-112">A client computer that is joined to the domain that the Exchange server is installed in.</span></span>
    
- <span data-ttu-id="71bc4-113">Una cuenta de usuario que tenga un buzón en el servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="71bc4-113">A user account that has a mailbox on the Exchange server.</span></span> 
    
<span data-ttu-id="71bc4-114">Además, antes de empezar, deberá estar familiarizado algunos conceptos básicos.</span><span class="sxs-lookup"><span data-stu-id="71bc4-114">Also, before you begin, you'll want to be familiar some basic concepts.</span></span> <span data-ttu-id="71bc4-115">Los siguientes son algunos recursos que le resultarán útiles.</span><span class="sxs-lookup"><span data-stu-id="71bc4-115">The following are some resources that you'll find helpful.</span></span>
  
<span data-ttu-id="71bc4-116">**La tabla 1. Artículos relacionados de la búsqueda de los extremos de detección automática de objetos SCP**</span><span class="sxs-lookup"><span data-stu-id="71bc4-116">**Table 1. Related articles for finding Autodiscover endpoints from SCP objects**</span></span>

|<span data-ttu-id="71bc4-117">**Lea este artículo**</span><span class="sxs-lookup"><span data-stu-id="71bc4-117">**Read this article**</span></span>|<span data-ttu-id="71bc4-118">**Para obtener más información acerca de...**</span><span class="sxs-lookup"><span data-stu-id="71bc4-118">**To learn about…**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="71bc4-119">Detección automática de Exchange</span><span class="sxs-lookup"><span data-stu-id="71bc4-119">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md) <br/> |<span data-ttu-id="71bc4-120">Cómo funciona el servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="71bc4-120">How the Autodiscover service works.</span></span>  <br/> |
|[<span data-ttu-id="71bc4-121">Publicación con puntos de conexión de servicio</span><span class="sxs-lookup"><span data-stu-id="71bc4-121">Publishing with Service Connection Points</span></span>](http://msdn.microsoft.com/library/3544aa64-ecb0-48a1-ae49-05247a983842%28Office.15%29.aspx) <br/> |<span data-ttu-id="71bc4-122">Cómo se usan los objetos SCP para publicar datos específicos de servicio.</span><span class="sxs-lookup"><span data-stu-id="71bc4-122">How SCP objects are used to publish service-specific data.</span></span>  <br/> |
   
## <a name="locate-autodiscover-scp-objects-in-ad-ds"></a><span data-ttu-id="71bc4-123">Busque objetos SCP de detección automática en AD DS</span><span class="sxs-lookup"><span data-stu-id="71bc4-123">Locate Autodiscover SCP objects in AD DS</span></span>
<span data-ttu-id="71bc4-124"><a name="bk_LocateScpObjects"> </a></span><span class="sxs-lookup"><span data-stu-id="71bc4-124"></span></span>

<span data-ttu-id="71bc4-125">Es el primer paso para buscar los extremos de detección automática que se publican en AD DS localizar los objetos SCP de detección automática.</span><span class="sxs-lookup"><span data-stu-id="71bc4-125">The first step toward finding Autodiscover endpoints published in AD DS is to locate the Autodiscover SCP objects.</span></span> <span data-ttu-id="71bc4-126">Exchange publica dos tipos de objetos SCP para la detección automática:</span><span class="sxs-lookup"><span data-stu-id="71bc4-126">Exchange publishes two types of SCP objects for Autodiscover:</span></span>
  
- <span data-ttu-id="71bc4-127">**Punteros de SCP** : contienen información que señala a servidores LDAP específicos que se deben usar para localizar objetos SCP de detección automática para el dominio del usuario.</span><span class="sxs-lookup"><span data-stu-id="71bc4-127">**SCP pointers** — These contain information that points to specific LDAP servers that should be used to locate Autodiscover SCP objects for the user's domain.</span></span> <span data-ttu-id="71bc4-128">Punteros de SCP están marcados con el siguiente GUID: 67661d7F - 8FC 4-4fa7-BFAC-E1D7794C1F68.</span><span class="sxs-lookup"><span data-stu-id="71bc4-128">SCP pointers are stamped with the following GUID: 67661d7F-8FC4-4fa7-BFAC-E1D7794C1F68.</span></span> 
    
- <span data-ttu-id="71bc4-129">**Direcciones URL de la SCP** : estos contienen direcciones URL de los extremos de detección automática.</span><span class="sxs-lookup"><span data-stu-id="71bc4-129">**SCP URLs** — These contain URLs for Autodiscover endpoints.</span></span> <span data-ttu-id="71bc4-130">Direcciones URL de la SCP están marcadas con el siguiente GUID: 77378F46-2 66 C-4aa9-A6A6-3E7A48B19596.</span><span class="sxs-lookup"><span data-stu-id="71bc4-130">SCP URLs are stamped with the following GUID: 77378F46-2C66-4aa9-A6A6-3E7A48B19596.</span></span> 
    
### <a name="to-locate-autodiscover-scp-objects"></a><span data-ttu-id="71bc4-131">Para buscar objetos SCP de detección automática</span><span class="sxs-lookup"><span data-stu-id="71bc4-131">To locate Autodiscover SCP objects</span></span>

1. <span data-ttu-id="71bc4-132">Leer la propiedad **configurationNamingContext** de la entrada DSE en AD DS para obtener la ruta de acceso para el contexto de nomenclatura de configuración para el dominio raíz.</span><span class="sxs-lookup"><span data-stu-id="71bc4-132">Read the **configurationNamingContext** property of the root DSE entry in AD DS to get the path to the configuration naming context for the domain.</span></span> <span data-ttu-id="71bc4-133">Puede hacerlo mediante el uso de la clase [DirectoryEntry](http://msdn2.microsoft.com/EN-US/library/z9cddzaa) , o cualquier otra API que puede obtener acceso a AD DS.</span><span class="sxs-lookup"><span data-stu-id="71bc4-133">You can do this by using the [DirectoryEntry](http://msdn2.microsoft.com/EN-US/library/z9cddzaa) class, or any other API that can acces AD DS.</span></span> 
    
2. <span data-ttu-id="71bc4-134">Para buscar objetos SCP en el contexto de nomenclatura de configuración que tienen ya sea la SCP puntero GUID o el GUID de la dirección URL de SCP en la propiedad **keywords** .</span><span class="sxs-lookup"><span data-stu-id="71bc4-134">Search for SCP objects in the configuration naming context that have either the SCP pointer GUID or the SCP URL GUID in the **keywords** property.</span></span> 
    
3. <span data-ttu-id="71bc4-135">Compruebe que se ha encontrado un puntero de SCP que tiene como ámbito el dominio del usuario mediante la comprobación de la propiedad **palabras clave** para una entrada igual a los objetos de la SCP `"Domain=<domain>"`.</span><span class="sxs-lookup"><span data-stu-id="71bc4-135">Check the SCP objects you found for an SCP pointer that is scoped to the user's domain by checking the **keywords** property for an entry equal to `"Domain=<domain>"`.</span></span> <span data-ttu-id="71bc4-136">Por ejemplo, si la dirección de correo electrónico del usuario es elvin@contoso.com, debe buscar un puntero SCP con una entrada en la propiedad de **las palabras clave** que es igual a `"Domain=contoso.com"`.</span><span class="sxs-lookup"><span data-stu-id="71bc4-136">For example, if the user's email address is elvin@contoso.com, you would look for an SCP pointer with an entry in the **keywords** property that is equal to `"Domain=contoso.com"`.</span></span> <span data-ttu-id="71bc4-137">Si se encuentra un puntero SCP coincidente, descartar el conjunto de objetos SCP y empezar de nuevo en el paso 1 con el valor de la propiedad **serviceBindingInformation** como el servidor para conectarse a la entrada de DSE raíz.</span><span class="sxs-lookup"><span data-stu-id="71bc4-137">If a matching SCP pointer is found, discard the set of SCP objects and start over at step 1 using the value of the **serviceBindingInformation** property as the server to connect to for the Root DSE entry.</span></span> 
    
4. <span data-ttu-id="71bc4-138">Si no encuentra ningún punteros SCP en el ámbito el dominio del usuario, buscando cualquier punteros de SCP que no son el ámbito de cualquier dominio y guarda el valor de la propiedad **serviceBindingInformation** como un servidor de "reserva", en caso de que el servidor actual no obtendrá ninguna resultados.</span><span class="sxs-lookup"><span data-stu-id="71bc4-138">If you don't find any SCP pointers scoped to the user's domain, check for any SCP pointers that aren't scoped to any domain, and save the value of the **serviceBindingInformation** property as a "fallback" server, in case the current server doesn't give you any results.</span></span> 
    
5. <span data-ttu-id="71bc4-139">Si no encuentra ningún punteros SCP en el ámbito del dominio, estará listo pasar a la siguiente paso: generación de una lista de prioridades de los extremos de detección automática de los resultados.</span><span class="sxs-lookup"><span data-stu-id="71bc4-139">If you didn't find any SCP pointers scoped to the domain, you're ready to move on to the next step: generating a prioritized list of Autodiscover endpoints from your results.</span></span>
    
## <a name="generate-a-prioritized-list-of-autodiscover-endpoints"></a><span data-ttu-id="71bc4-140">Generar una lista de prioridades de los extremos de detección automática</span><span class="sxs-lookup"><span data-stu-id="71bc4-140">Generate a prioritized list of Autodiscover endpoints</span></span>
<span data-ttu-id="71bc4-141"><a name="bk_GenerateList"> </a></span><span class="sxs-lookup"><span data-stu-id="71bc4-141"></span></span>

<span data-ttu-id="71bc4-142">Puede generar una lista de prioridades de direcciones URL de extremo de detección automática, con el conjunto de objetos SCP que encuentra, haciendo lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="71bc4-142">You can generate a prioritized list of Autodiscover endpoint URLs, using the set of SCP objects that you located, by doing the following:</span></span>
  
1. <span data-ttu-id="71bc4-143">Obtenga el nombre del sitio de Active Directory del equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="71bc4-143">Get the Active Directory site name of the client computer.</span></span>
    
2. <span data-ttu-id="71bc4-144">Compruebe la propiedad **palabras clave** en cada dirección URL de SCP en el conjunto de objetos SCP encontró y asignar una prioridad a la dirección URL en función de las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="71bc4-144">Check the **keywords** property on each SCP URL in the set of SCP objects you found, and assign a priority to the URL based on the following rules:</span></span> 
    
  - <span data-ttu-id="71bc4-145">Si la propiedad **palabras clave** contiene un valor de `"Site=<site name>"`, donde `<site name>` es igual a sitio el nombre de Active Directory recuperado en el paso anterior, asigne la dirección URL de una prioridad de 1.</span><span class="sxs-lookup"><span data-stu-id="71bc4-145">If the **keywords** property contains a value of `"Site=<site name>"`, where `<site name>` equals the name of the Active Directory site you retrieved in the previous step, assign the URL a priority of 1.</span></span> 
    
  - <span data-ttu-id="71bc4-146">Si la propiedad **palabras clave** no contiene una entrada con un valor que comienza por `"Site="`, asigne una prioridad de 2 de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="71bc4-146">If the **keywords** property does not contain an entry with a value that starts with `"Site="`, assign the URL a priority of 2.</span></span> 
    
  - <span data-ttu-id="71bc4-147">Si la propiedad **palabras clave** contiene un valor de `"Site=<site name>`, donde `<site name>` no ser igual al nombre del sitio de Active Directory que ha recuperado en el paso anterior, asigne una prioridad de 3 de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="71bc4-147">If the **keywords** property contains a value of `"Site=<site name>`, where `<site name>` does not equal the name of the Active Directory site you retrieved in the previous step, assign the URL a priority of 3.</span></span> 
    
## <a name="code-example-performing-an-scp-lookup"></a><span data-ttu-id="71bc4-148">Ejemplo de código: realiza una búsqueda de SCP</span><span class="sxs-lookup"><span data-stu-id="71bc4-148">Code example: Performing an SCP lookup</span></span>
<span data-ttu-id="71bc4-149"><a name="bk_CodeExample"> </a></span><span class="sxs-lookup"><span data-stu-id="71bc4-149"></span></span>

<span data-ttu-id="71bc4-150">En el siguiente ejemplo de código, verá cómo ubicar objetos SCP de detección automática y generar una lista de prioridades de los extremos de detección automática.</span><span class="sxs-lookup"><span data-stu-id="71bc4-150">In the following code example, you'll see how to locate Autodiscover SCP objects and generate a prioritized list of Autodiscover endpoints.</span></span>
  
```cs
using System;
using System.Collections.Generic;
using System.DirectoryServices;
using System.DirectoryServices.ActiveDirectory;
namespace ScpLookup
{
    // This sample is for demonstration purposes only. Before you run this sample, make sure 
    // that the code meets the coding requirements of your organization. 
    class Program
    {
        static void Main(string[] args)
        {
            string domain = args[0];
            Console.WriteLine("Performing SCP lookup for {0}.", domain);
            List<string> scpUrls = GetScpUrls(null, domain);
            Console.WriteLine("\nOrdered List of Autodiscover endpoints:");
            foreach (string url in scpUrls)
            {
                Console.WriteLine("  {0}", url);
            }
            Console.WriteLine("SCP lookup done.");
        }
        // GUID for SCP URL keyword.
        private const string ScpUrlGuidString = @"77378F46-2C66-4aa9-A6A6-3E7A48B19596";
        // GUID for SCP pointer keyword.
        private const string ScpPtrGuidString = @"67661d7F-8FC4-4fa7-BFAC-E1D7794C1F68";
        static List<string> GetScpUrls(string ldapServer, string domain)
        {
            // Create a new list to return.
            List<string> scpUrlList = new List<string>();
            string rootDSEPath = null;
            // If ldapServer is null/empty, use LDAP://RootDSE to
            // connect to Active Directory Domain Services (AD DS). Otherwise, use
            // LDAP://SERVERNAME/RootDSE to connect to a specific server.
            if (string.IsNullOrEmpty(ldapServer))
            {
                rootDSEPath = "LDAP://RootDSE";
            }
            else
            {
                rootDSEPath = ldapServer + "/RootDSE";
            }
            SearchResultCollection scpEntries = null;
            try
            {
                // Get the root directory entry.
                DirectoryEntry rootDSE = new DirectoryEntry(rootDSEPath);
                // Get the configuration path.
                string configPath = rootDSE.Properties["configurationNamingContext"].Value as string;
                // Get the configuration entry.
                DirectoryEntry configEntry = new DirectoryEntry("LDAP://" + configPath);
                // Create a search object for the configuration entry.
                DirectorySearcher configSearch = new DirectorySearcher(configEntry);
                // Set the search filter to find SCP URLs and SCP pointers.
                configSearch.Filter = "(&amp;(objectClass=serviceConnectionPoint)" +
                    "(|(keywords=" + ScpPtrGuidString + ")(keywords=" + ScpUrlGuidString + ")))";
                // Specify which properties you want to retrieve.
                configSearch.PropertiesToLoad.Add("keywords");
                configSearch.PropertiesToLoad.Add("serviceBindingInformation");
                scpEntries = configSearch.FindAll();
            }
            catch (Exception ex)
            {
                Console.WriteLine("SCP lookup failed with: ");
                Console.WriteLine(ex.ToString());
            }
            // If no SCP entries were found, then exit.
            if (scpEntries == null || scpEntries.Count <= 0)
            {
                Console.WriteLine("No SCP records found.");
                return null;
            }
            string fallBackLdapPath = null;
            // Check for SCP pointers.
            foreach (SearchResult scpEntry in scpEntries)
            {
                ResultPropertyValueCollection entryKeywords = scpEntry.Properties["keywords"];
                if (CollectionContainsExactValue(entryKeywords, ScpPtrGuidString))
                {
                    string ptrLdapPath = scpEntry.Properties["serviceBindingInformation"][0] as string;
                    // Determine whether this pointer is scoped to the user's domain.
                    if (CollectionContainsExactValue(entryKeywords, "Domain=" + domain))
                    {
                        Console.WriteLine("Found SCP pointer for " + domain + " in " + scpEntry.Path);
                        // Restart SCP lookup with the server assigned for the domain.
                        Console.WriteLine("Restarting SCP lookup in " + ptrLdapPath);
                        return GetScpUrls(ptrLdapPath, domain);
                    }
                    else
                    {
                        // Save the first SCP pointer that is not scoped to a domain as a fallback
                        // in case you do not get any results from this server.
                        if (entryKeywords.Count == 1 &amp;&amp; string.IsNullOrEmpty(fallBackLdapPath))
                        {
                            fallBackLdapPath = ptrLdapPath;
                            Console.WriteLine("Saved fallback SCP pointer: " + fallBackLdapPath);
                        }
                    }
                }
            }
            string computerSiteName = null;
            try
            {
                // Get the name of the ActiveDirectorySite the computer
                // belongs to (if it belongs to one).
                ActiveDirectorySite site = ActiveDirectorySite.GetComputerSite();
                computerSiteName = site.Name;
                Console.WriteLine("Local computer in site: " + computerSiteName);
            }
            catch (Exception ex)
            {
                Console.WriteLine("Unable to get computer site name.");
                Console.WriteLine(ex.ToString());
            }
            if (!string.IsNullOrEmpty(computerSiteName))
            {
                // Scan the search results for SCP URLs.
                // SCP URLs fit into three tiers:
                //   Priority 1: The URL is scoped to the computer's Active Directory site.
                //   Priority 2: The URL is not scoped to any Active Directory site.
                //   Priority 3: The URL is scoped to a different Active Directory site.
                // Temporary lists to hold priority 2 and 3 URLs.
                List<string> priorityTwoUrls = new List<string>();
                List<string> priorityThreeUrls = new List<string>();
                foreach (SearchResult scpEntry in scpEntries)
                {
                    ResultPropertyValueCollection entryKeywords = scpEntry.Properties["keywords"];
                    // Check for SCP URLs.
                    if (CollectionContainsExactValue(entryKeywords, ScpUrlGuidString))
                    {
                        string scpUrlPath = scpEntry.Properties["adsPath"][0] as string;
                        Console.WriteLine("SCP URL found at {0}", scpUrlPath);
                        string scpUrl = scpEntry.Properties["serviceBindingInformation"][0] as string;
                        scpUrl = scpUrl.ToLower();
                        // Determine whether this entry is scoped to the computer's site.
                        if (CollectionContainsExactValue(entryKeywords, "Site=" + computerSiteName))
                        {
                            // Priority 1.
                            if (!scpUrlList.Contains(scpUrl.ToLower()))
                            {
                                Console.WriteLine("Adding priority 1 SCP URL: {0}", scpUrl.ToLower());
                                scpUrlList.Add(scpUrl);
                            }
                            else
                            {
                                Console.WriteLine("Priority 1 SCP URL already found: {0}", scpUrl);
                            }
                        }
                        else
                        {
                            // Determine whether this is a priority 2 or 3 URL.
                            if (CollectionContainsPrefixValue(entryKeywords, "Site="))
                            {
                                // Priority 3.
                                if (!priorityThreeUrls.Contains(scpUrl))
                                {
                                    Console.WriteLine("Adding priority 3 SCP URL: {0}", scpUrl);
                                    priorityThreeUrls.Add(scpUrl);
                                }
                                else
                                {
                                    Console.WriteLine("Priority 3 SCP URL already found: {0}", scpUrl);
                                }
                            }
                            else
                            {
                                // Priority 2.
                                if (!priorityTwoUrls.Contains(scpUrl))
                                {
                                    Console.WriteLine("Adding priority 2 SCP URL: {0}", scpUrl);
                                    priorityTwoUrls.Add(scpUrl);
                                }
                                else
                                {
                                    Console.WriteLine("Priority 2 SCP URL already found: {0}", scpUrl);
                                }
                            }
                        }
                    }
                }
                // Now add the priority 2 URLs into the main list.
                foreach (string priorityTwoUrl in priorityTwoUrls)
                {
                    // If the URL is already in the list as a priority 1, 
                    // don't add it again.
                    if (!scpUrlList.Contains(priorityTwoUrl))
                    {
                        scpUrlList.Add(priorityTwoUrl);
                    }
                }
                // Now add the priority 3 URLs into the main list.
                foreach (string priorityThreeUrl in priorityThreeUrls)
                {
                    // If the URL is already in the list as a priority 1
                    // or priority 2, don't add it again.
                    if (!scpUrlList.Contains(priorityThreeUrl))
                    {
                        scpUrlList.Add(priorityThreeUrl);
                    }
                }
                // If after all this, you still have no URLs in your list,
                // try the fallback SCP pointer, if you have one.
                if (scpUrlList.Count == 0 &amp;&amp; fallBackLdapPath != null)
                {
                    return GetScpUrls(fallBackLdapPath, domain);
                }
            }
            return scpUrlList;
        }
        private static bool CollectionContainsExactValue(ResultPropertyValueCollection collection, string value)
        {
            foreach (object obj in collection)
            {
                string entry = obj as string;
                if (entry != null)
                {
                    if (string.Compare(value, entry, true) == 0)
                        return true;
                }
            }
            return false;
        }
        private static bool CollectionContainsPrefixValue(ResultPropertyValueCollection collection, string value)
        {
            foreach (object obj in collection)
            {
                string entry = obj as string;
                if (entry != null)
                {
                    if (entry.StartsWith(value))
                        return true;
                }
            }
            return false;
        }
    }
}
```

## <a name="next-steps"></a><span data-ttu-id="71bc4-151">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="71bc4-151">Next steps</span></span>
<span data-ttu-id="71bc4-152"><a name="bk_NextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="71bc4-152"></span></span>

<span data-ttu-id="71bc4-153">El siguiente paso en el proceso de detección automática es enviar solicitudes de detección automática para las direcciones URL que encuentran, comenzando con direcciones URL de prioridad 1, a continuación, las direcciones URL de prioridad 2 y por último direcciones URL de prioridad 3.</span><span class="sxs-lookup"><span data-stu-id="71bc4-153">The next step in the Autodiscover process is to send Autodiscover requests to the URLs that you found, starting with priority 1 URLs, then priority 2 URLs, and finally priority 3 URLs.</span></span> <span data-ttu-id="71bc4-154">Para obtener más información acerca de cómo enviar solicitudes de detección automática y controlar las respuestas, lea los siguientes artículos:</span><span class="sxs-lookup"><span data-stu-id="71bc4-154">To learn more about how to send Autodiscover requests and handle responses, read the following articles:</span></span>
  
- [<span data-ttu-id="71bc4-155">Obtener la configuración de usuario de Exchange mediante el uso de detección automática</span><span class="sxs-lookup"><span data-stu-id="71bc4-155">Get user settings from Exchange by using Autodiscover</span></span>](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
- [<span data-ttu-id="71bc4-156">Administrar los mensajes de error de detección automática</span><span class="sxs-lookup"><span data-stu-id="71bc4-156">Handling Autodiscover error messages</span></span>](handling-autodiscover-error-messages.md)
    
## <a name="see-also"></a><span data-ttu-id="71bc4-157">Ver también</span><span class="sxs-lookup"><span data-stu-id="71bc4-157">See also</span></span>

- [<span data-ttu-id="71bc4-158">Detección automática de Exchange</span><span class="sxs-lookup"><span data-stu-id="71bc4-158">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md)   
- [<span data-ttu-id="71bc4-159">Configurar una aplicación de EWS</span><span class="sxs-lookup"><span data-stu-id="71bc4-159">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)
    

