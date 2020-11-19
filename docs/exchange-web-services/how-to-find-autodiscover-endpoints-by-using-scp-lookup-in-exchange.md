---
title: Buscar puntos de conexión de Detección automática mediante el uso de búsqueda de SCP en Exchange
manager: kelbow
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: b24228a8-5127-4bac-aef0-9c9e8843c9ff
description: Obtenga información acerca de cómo localizar objetos SCP de Detección automática en servicios de dominio de Active Directory (AD DS) y usarlos para encontrar las direcciones URL del punto de conexión de Detección automática para usarlas con el servicio Detección automática de Exchange.
localization_priority: Priority
ms.openlocfilehash: 5468c18b6d614016915c292c2e02c1a4b570ae37
ms.sourcegitcommit: 37d4ecd4f469690ba1de87baad2f2f58c40c96ba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "49348811"
---
# <a name="find-autodiscover-endpoints-by-using-scp-lookup-in-exchange"></a><span data-ttu-id="077d0-103">Buscar puntos de conexión de Detección automática mediante el uso de búsqueda de SCP en Exchange</span><span class="sxs-lookup"><span data-stu-id="077d0-103">Find Autodiscover endpoints by using SCP lookup in Exchange</span></span>

<span data-ttu-id="077d0-104">Obtenga información acerca de cómo localizar objetos SCP de Detección automática en servicios de dominio de Active Directory (AD DS) y usarlos para encontrar las direcciones URL del punto de conexión de Detección automática para usarlas con el servicio Detección automática de Exchange.</span><span class="sxs-lookup"><span data-stu-id="077d0-104">Find out how to locate Autodiscover SCP objects in Active Directory Domain Services (AD DS) and use them to find Autodiscover endpoint URLs to use with the Exchange Autodiscover service.</span></span>
  
<span data-ttu-id="077d0-105">Detección automática facilita la recuperación de la información que necesita para conectarse a buzones de servidores Exchange.</span><span class="sxs-lookup"><span data-stu-id="077d0-105">Autodiscover makes it easy to retrieve information that you need to connect to mailboxes on Exchange servers.</span></span> <span data-ttu-id="077d0-106">Sin embargo, para usar Detección automática, necesita un modo de encontrar los servidores de detección automática que sean adecuados para el usuario al que está recuperando la configuración.</span><span class="sxs-lookup"><span data-stu-id="077d0-106">However, in order to use Autodiscover, you need a way to find Autodiscover servers that are appropriate for the user you're retrieving settings for.</span></span> <span data-ttu-id="077d0-107">Y los objetos de punto de conexión de servicio (SCP) en AD DS proporcionan una forma fácil de que los clientes unidos a un dominio busquen servidores de Detección automática.</span><span class="sxs-lookup"><span data-stu-id="077d0-107">Service connection point (SCP) objects in AD DS provide an easy way for domain-joined clients to look up Autodiscover servers.</span></span> 
  
## <a name="get-set-up-to-find-autodiscover-endpoints"></a><span data-ttu-id="077d0-108">Obtener la configuración para encontrar puntos de conexión de Detección automática</span><span class="sxs-lookup"><span data-stu-id="077d0-108">Get set up to find Autodiscover endpoints</span></span>
<span data-ttu-id="077d0-109"><a name="bk_PreReqs"> </a></span><span class="sxs-lookup"><span data-stu-id="077d0-109"><a name="bk_PreReqs"> </a></span></span>

<span data-ttu-id="077d0-110">Para localizar objetos SCP de Detección automática en AD DS, debe tener acceso a lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="077d0-110">To locate Autodiscover SCP objects in AD DS, you need to have access to the following:</span></span>
  
- <span data-ttu-id="077d0-111">Un servidor en el que se ejecuta una versión de Exchange local empezando con Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="077d0-111">A server that is running a version of Exchange on-premises starting with Exchange 2007 SP1.</span></span>
    
- <span data-ttu-id="077d0-112">Un equipo cliente que se une al dominio en el que está instalado el servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="077d0-112">A client computer that is joined to the domain that the Exchange server is installed in.</span></span>
    
- <span data-ttu-id="077d0-113">Una cuenta de usuario que tenga un buzón en el servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="077d0-113">A user account that has a mailbox on the Exchange server.</span></span> 
    
<span data-ttu-id="077d0-114">Asimismo, antes de empezar, le recomendamos que esté familiarizado con algunos conceptos básicos.</span><span class="sxs-lookup"><span data-stu-id="077d0-114">Also, before you begin, you'll want to be familiar some basic concepts.</span></span> <span data-ttu-id="077d0-115">Estos son algunos recursos que le resultarán útiles.</span><span class="sxs-lookup"><span data-stu-id="077d0-115">The following are some resources that you'll find helpful.</span></span>
  
<span data-ttu-id="077d0-116">**Tabla 1. Artículos relacionados para buscar puntos de conexión de detección automática de objetos SCP**</span><span class="sxs-lookup"><span data-stu-id="077d0-116">**Table 1. Related articles for finding Autodiscover endpoints from SCP objects**</span></span>

|<span data-ttu-id="077d0-117">**Lea este artículo:**</span><span class="sxs-lookup"><span data-stu-id="077d0-117">**Read this article**</span></span>|<span data-ttu-id="077d0-118">**Obtenga información sobre...**</span><span class="sxs-lookup"><span data-stu-id="077d0-118">**To learn about…**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="077d0-119">Detección automática en Exchange</span><span class="sxs-lookup"><span data-stu-id="077d0-119">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md) <br/> |<span data-ttu-id="077d0-120">Cómo funciona el servicio Detección automática</span><span class="sxs-lookup"><span data-stu-id="077d0-120">How the Autodiscover service works.</span></span>  <br/> |
|[<span data-ttu-id="077d0-121">Publicación con puntos de conexión de servicio</span><span class="sxs-lookup"><span data-stu-id="077d0-121">Publishing with Service Connection Points</span></span>](https://msdn.microsoft.com/library/3544aa64-ecb0-48a1-ae49-05247a983842%28Office.15%29.aspx) <br/> |<span data-ttu-id="077d0-122">Cómo se usan los objetos SCP para publicar datos específicos de un servicio</span><span class="sxs-lookup"><span data-stu-id="077d0-122">How SCP objects are used to publish service-specific data.</span></span>  <br/> |
   
## <a name="locate-autodiscover-scp-objects-in-ad-ds"></a><span data-ttu-id="077d0-123">Buscar objetos SCP de detección automática en AD DS</span><span class="sxs-lookup"><span data-stu-id="077d0-123">Locate Autodiscover SCP objects in AD DS</span></span>
<span data-ttu-id="077d0-124"><a name="bk_LocateScpObjects"> </a></span><span class="sxs-lookup"><span data-stu-id="077d0-124"><a name="bk_LocateScpObjects"> </a></span></span>

<span data-ttu-id="077d0-125">El primer paso para encontrar los puntos de conexión de Detección automática publicados en AD DS es encontrar los objetos SCP de Detección automática.</span><span class="sxs-lookup"><span data-stu-id="077d0-125">The first step toward finding Autodiscover endpoints published in AD DS is to locate the Autodiscover SCP objects.</span></span> <span data-ttu-id="077d0-126">Exchange publica dos tipos de objetos SCP para Detección automática:</span><span class="sxs-lookup"><span data-stu-id="077d0-126">Exchange publishes two types of SCP objects for Autodiscover:</span></span>
  
- <span data-ttu-id="077d0-127">**Punteros de SCP**: contiene información que apunta a servidores de LDAP específicos que se deben usar para buscar objetos SCP de Detección automática para el dominio del usuario.</span><span class="sxs-lookup"><span data-stu-id="077d0-127">**SCP pointers** — These contain information that points to specific LDAP servers that should be used to locate Autodiscover SCP objects for the user's domain.</span></span> <span data-ttu-id="077d0-128">Los punteros de SCP se marcan con el siguiente GUID: 67661d7F-8FC4-4fa7-BFAC-E1D7794C1F68.</span><span class="sxs-lookup"><span data-stu-id="077d0-128">SCP pointers are stamped with the following GUID: 67661d7F-8FC4-4fa7-BFAC-E1D7794C1F68.</span></span> 
    
- <span data-ttu-id="077d0-129">**Direcciones URL de SCP**: contienen las URL de los puntos de conexión de Detección automática.</span><span class="sxs-lookup"><span data-stu-id="077d0-129">**SCP URLs** — These contain URLs for Autodiscover endpoints.</span></span> <span data-ttu-id="077d0-130">Las direcciones URL de SCP se marcan con el siguiente GUID: 77378F46-2C66-4aa9-A6A6-3E7A48B19596.</span><span class="sxs-lookup"><span data-stu-id="077d0-130">SCP URLs are stamped with the following GUID: 77378F46-2C66-4aa9-A6A6-3E7A48B19596.</span></span> 
    
### <a name="to-locate-autodiscover-scp-objects"></a><span data-ttu-id="077d0-131">Buscar objetos SCP de Detección automática en AD DS</span><span class="sxs-lookup"><span data-stu-id="077d0-131">To locate Autodiscover SCP objects</span></span>

1. <span data-ttu-id="077d0-132">Lea la propiedad **configurationNamingContext** de la entrada DSE raíz en AD DS para obtener la ruta de acceso al contexto de nomenclatura de configuración del dominio.</span><span class="sxs-lookup"><span data-stu-id="077d0-132">Read the **configurationNamingContext** property of the root DSE entry in AD DS to get the path to the configuration naming context for the domain.</span></span> <span data-ttu-id="077d0-133">Para ello, puede usar la clase [DirectoryEntry](https://msdn2.microsoft.com/library/z9cddzaa), o cualquier otra API que pueda acceder a AD DS.</span><span class="sxs-lookup"><span data-stu-id="077d0-133">You can do this by using the [DirectoryEntry](https://msdn2.microsoft.com/library/z9cddzaa) class, or any other API that can acces AD DS.</span></span> 
    
2. <span data-ttu-id="077d0-134">Busque objetos SCP en el contexto de nomenclatura de configuración que tenga el GUID de puntero SCP o el GUID de la URL del SCP en la propiedad **Keywords**.</span><span class="sxs-lookup"><span data-stu-id="077d0-134">Search for SCP objects in the configuration naming context that have either the SCP pointer GUID or the SCP URL GUID in the **keywords** property.</span></span> 
    
3. <span data-ttu-id="077d0-135">Compruebe los objetos SCP que encontró para un puntero SCP que está en el ámbito del dominio del usuario; para ello, marque la propiedad **Keywords** de la entrada igual a `"Domain=<domain>"`.</span><span class="sxs-lookup"><span data-stu-id="077d0-135">Check the SCP objects you found for an SCP pointer that is scoped to the user's domain by checking the **keywords** property for an entry equal to `"Domain=<domain>"`.</span></span> <span data-ttu-id="077d0-136">Por ejemplo, si la dirección de correo electrónico del usuario es elvin@contoso.com, buscaría un puntero SCP con una entrada en la propiedad **keywords** que es igual a `"Domain=contoso.com"`.</span><span class="sxs-lookup"><span data-stu-id="077d0-136">For example, if the user's email address is elvin@contoso.com, you would look for an SCP pointer with an entry in the **keywords** property that is equal to `"Domain=contoso.com"`.</span></span> <span data-ttu-id="077d0-137">Si se encuentra un puntero SCP coincidente, descarte el conjunto de objetos SCP y vuelva a empezar en el paso 1 con el valor de la propiedad **serviceBindingInformation** como servidor con el que se conectará para la entrada DSE raíz.</span><span class="sxs-lookup"><span data-stu-id="077d0-137">If a matching SCP pointer is found, discard the set of SCP objects and start over at step 1 using the value of the **serviceBindingInformation** property as the server to connect to for the Root DSE entry.</span></span> 
    
4. <span data-ttu-id="077d0-138">Si no encuentra ningún puntero SCP en el ámbito del dominio del usuario, compruebe si hay punteros SCP que no estén en el ámbito de cualquier dominio y guarde el valor de la propiedad **serviceBindingInformation** como un servidor de "reserva", en caso de que el servidor actual no le dé resultados.</span><span class="sxs-lookup"><span data-stu-id="077d0-138">If you don't find any SCP pointers scoped to the user's domain, check for any SCP pointers that aren't scoped to any domain, and save the value of the **serviceBindingInformation** property as a "fallback" server, in case the current server doesn't give you any results.</span></span> 
    
5. <span data-ttu-id="077d0-139">Si no encuentra ningún puntero SCP en el ámbito del dominio, estará listo para pasar al siguiente paso: generar una lista con prioridades de los puntos de conexión de Detección automática de los resultados.</span><span class="sxs-lookup"><span data-stu-id="077d0-139">If you didn't find any SCP pointers scoped to the domain, you're ready to move on to the next step: generating a prioritized list of Autodiscover endpoints from your results.</span></span>
    
## <a name="generate-a-prioritized-list-of-autodiscover-endpoints"></a><span data-ttu-id="077d0-140">Generar una lista con prioridades de puntos de conexión de Detección automática</span><span class="sxs-lookup"><span data-stu-id="077d0-140">Generate a prioritized list of Autodiscover endpoints</span></span>
<span data-ttu-id="077d0-141"><a name="bk_GenerateList"> </a></span><span class="sxs-lookup"><span data-stu-id="077d0-141"><a name="bk_GenerateList"> </a></span></span>

<span data-ttu-id="077d0-142">Puede crear una lista con prioridades de direcciones URL de puntos de conexión de Detección automática, con el conjunto de objetos SCP que encontró, de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="077d0-142">You can generate a prioritized list of Autodiscover endpoint URLs, using the set of SCP objects that you located, by doing the following:</span></span>
  
1. <span data-ttu-id="077d0-143">Obtener el nombre del sitio de Active Directory del equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="077d0-143">Get the Active Directory site name of the client computer.</span></span>
    
2. <span data-ttu-id="077d0-144">Compruebe la propiedad **Keywords** en cada URL de SCP en el conjunto de objetos SCP que encontró y asigne una prioridad a la dirección URL en función de las reglas siguientes:</span><span class="sxs-lookup"><span data-stu-id="077d0-144">Check the **keywords** property on each SCP URL in the set of SCP objects you found, and assign a priority to the URL based on the following rules:</span></span> 
    
  - <span data-ttu-id="077d0-145">Si la propiedad **keywords** contiene un valor de `"Site=<site name>"`, en el que `<site name>` es igual al nombre del sitio de Active Directory que recuperó en el paso anterior, asigne a la URL una prioridad de 1.</span><span class="sxs-lookup"><span data-stu-id="077d0-145">If the **keywords** property contains a value of `"Site=<site name>"`, where `<site name>` equals the name of the Active Directory site you retrieved in the previous step, assign the URL a priority of 1.</span></span> 
    
  - <span data-ttu-id="077d0-146">Si la propiedad **Keywords** no contiene una entrada con un valor que comience por `"Site="`, asigne a la URL una prioridad 2.</span><span class="sxs-lookup"><span data-stu-id="077d0-146">If the **keywords** property does not contain an entry with a value that starts with `"Site="`, assign the URL a priority of 2.</span></span> 
    
  - <span data-ttu-id="077d0-147">Si la propiedad **keywords** contiene un valor de `"Site=<site name>`, en el que `<site name>` no es igual al nombre del sitio de Active Directory que recuperó en el paso anterior, asigne a la URL una prioridad de 3.</span><span class="sxs-lookup"><span data-stu-id="077d0-147">If the **keywords** property contains a value of `"Site=<site name>`, where `<site name>` does not equal the name of the Active Directory site you retrieved in the previous step, assign the URL a priority of 3.</span></span> 
    
## <a name="code-example-performing-an-scp-lookup"></a><span data-ttu-id="077d0-148">Ejemplo de código: realización de una búsqueda SCP</span><span class="sxs-lookup"><span data-stu-id="077d0-148">Code example: Performing an SCP lookup</span></span>
<span data-ttu-id="077d0-149"><a name="bk_CodeExample"> </a></span><span class="sxs-lookup"><span data-stu-id="077d0-149"><a name="bk_CodeExample"> </a></span></span>

<span data-ttu-id="077d0-150">En el siguiente ejemplo de código, verá cómo localizar objetos SCP de Detección automática y generar una lista con prioridades de los puntos de conexión de Detección automática.</span><span class="sxs-lookup"><span data-stu-id="077d0-150">In the following code example, you'll see how to locate Autodiscover SCP objects and generate a prioritized list of Autodiscover endpoints.</span></span>
  
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
                        if (entryKeywords.Count == 1 && string.IsNullOrEmpty(fallBackLdapPath))
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
                if (scpUrlList.Count == 0 && fallBackLdapPath != null)
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

## <a name="next-steps"></a><span data-ttu-id="077d0-151">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="077d0-151">Next steps</span></span>
<span data-ttu-id="077d0-152"><a name="bk_NextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="077d0-152"><a name="bk_NextSteps"> </a></span></span>

<span data-ttu-id="077d0-153">El siguiente paso del proceso de Detección automática consiste en enviar solicitudes de Detección automática a las direcciones URL que encontró, empezando por direcciones URL de prioridad 1, luego de prioridad 2 y, por último, de prioridad 3.</span><span class="sxs-lookup"><span data-stu-id="077d0-153">The next step in the Autodiscover process is to send Autodiscover requests to the URLs that you found, starting with priority 1 URLs, then priority 2 URLs, and finally priority 3 URLs.</span></span> <span data-ttu-id="077d0-154">Para obtener más información sobre cómo enviar solicitudes de Detección automática y administrar respuestas, consulte los artículos siguientes:</span><span class="sxs-lookup"><span data-stu-id="077d0-154">To learn more about how to send Autodiscover requests and handle responses, read the following articles:</span></span>
  
- [<span data-ttu-id="077d0-155">Obtener la configuración de usuario de Exchange mediante el uso de Detección automática</span><span class="sxs-lookup"><span data-stu-id="077d0-155">Get user settings from Exchange by using Autodiscover</span></span>](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
- [<span data-ttu-id="077d0-156">Administrar los mensajes de error de Detección automática</span><span class="sxs-lookup"><span data-stu-id="077d0-156">Handling Autodiscover error messages</span></span>](handling-autodiscover-error-messages.md)
    
## <a name="see-also"></a><span data-ttu-id="077d0-157">Consulte también</span><span class="sxs-lookup"><span data-stu-id="077d0-157">See also</span></span>

- [<span data-ttu-id="077d0-158">Detección automática en Exchange</span><span class="sxs-lookup"><span data-stu-id="077d0-158">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md)   
- [<span data-ttu-id="077d0-159">Configurar la aplicación EWS</span><span class="sxs-lookup"><span data-stu-id="077d0-159">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)
    

