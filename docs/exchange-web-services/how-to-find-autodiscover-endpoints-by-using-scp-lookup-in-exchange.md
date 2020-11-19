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
# <a name="find-autodiscover-endpoints-by-using-scp-lookup-in-exchange"></a>Buscar puntos de conexión de Detección automática mediante el uso de búsqueda de SCP en Exchange

Obtenga información acerca de cómo localizar objetos SCP de Detección automática en servicios de dominio de Active Directory (AD DS) y usarlos para encontrar las direcciones URL del punto de conexión de Detección automática para usarlas con el servicio Detección automática de Exchange.
  
Detección automática facilita la recuperación de la información que necesita para conectarse a buzones de servidores Exchange. Sin embargo, para usar Detección automática, necesita un modo de encontrar los servidores de detección automática que sean adecuados para el usuario al que está recuperando la configuración. Y los objetos de punto de conexión de servicio (SCP) en AD DS proporcionan una forma fácil de que los clientes unidos a un dominio busquen servidores de Detección automática. 
  
## <a name="get-set-up-to-find-autodiscover-endpoints"></a>Obtener la configuración para encontrar puntos de conexión de Detección automática
<a name="bk_PreReqs"> </a>

Para localizar objetos SCP de Detección automática en AD DS, debe tener acceso a lo siguiente:
  
- Un servidor en el que se ejecuta una versión de Exchange local empezando con Exchange 2007 SP1.
    
- Un equipo cliente que se une al dominio en el que está instalado el servidor de Exchange.
    
- Una cuenta de usuario que tenga un buzón en el servidor de Exchange. 
    
Asimismo, antes de empezar, le recomendamos que esté familiarizado con algunos conceptos básicos. Estos son algunos recursos que le resultarán útiles.
  
**Tabla 1. Artículos relacionados para buscar puntos de conexión de detección automática de objetos SCP**

|**Lea este artículo:**|**Obtenga información sobre...**|
|:-----|:-----|
|[Detección automática en Exchange](autodiscover-for-exchange.md) <br/> |Cómo funciona el servicio Detección automática  <br/> |
|[Publicación con puntos de conexión de servicio](https://msdn.microsoft.com/library/3544aa64-ecb0-48a1-ae49-05247a983842%28Office.15%29.aspx) <br/> |Cómo se usan los objetos SCP para publicar datos específicos de un servicio  <br/> |
   
## <a name="locate-autodiscover-scp-objects-in-ad-ds"></a>Buscar objetos SCP de detección automática en AD DS
<a name="bk_LocateScpObjects"> </a>

El primer paso para encontrar los puntos de conexión de Detección automática publicados en AD DS es encontrar los objetos SCP de Detección automática. Exchange publica dos tipos de objetos SCP para Detección automática:
  
- **Punteros de SCP**: contiene información que apunta a servidores de LDAP específicos que se deben usar para buscar objetos SCP de Detección automática para el dominio del usuario. Los punteros de SCP se marcan con el siguiente GUID: 67661d7F-8FC4-4fa7-BFAC-E1D7794C1F68. 
    
- **Direcciones URL de SCP**: contienen las URL de los puntos de conexión de Detección automática. Las direcciones URL de SCP se marcan con el siguiente GUID: 77378F46-2C66-4aa9-A6A6-3E7A48B19596. 
    
### <a name="to-locate-autodiscover-scp-objects"></a>Buscar objetos SCP de Detección automática en AD DS

1. Lea la propiedad **configurationNamingContext** de la entrada DSE raíz en AD DS para obtener la ruta de acceso al contexto de nomenclatura de configuración del dominio. Para ello, puede usar la clase [DirectoryEntry](https://msdn2.microsoft.com/library/z9cddzaa), o cualquier otra API que pueda acceder a AD DS. 
    
2. Busque objetos SCP en el contexto de nomenclatura de configuración que tenga el GUID de puntero SCP o el GUID de la URL del SCP en la propiedad **Keywords**. 
    
3. Compruebe los objetos SCP que encontró para un puntero SCP que está en el ámbito del dominio del usuario; para ello, marque la propiedad **Keywords** de la entrada igual a `"Domain=<domain>"`. Por ejemplo, si la dirección de correo electrónico del usuario es elvin@contoso.com, buscaría un puntero SCP con una entrada en la propiedad **keywords** que es igual a `"Domain=contoso.com"`. Si se encuentra un puntero SCP coincidente, descarte el conjunto de objetos SCP y vuelva a empezar en el paso 1 con el valor de la propiedad **serviceBindingInformation** como servidor con el que se conectará para la entrada DSE raíz. 
    
4. Si no encuentra ningún puntero SCP en el ámbito del dominio del usuario, compruebe si hay punteros SCP que no estén en el ámbito de cualquier dominio y guarde el valor de la propiedad **serviceBindingInformation** como un servidor de "reserva", en caso de que el servidor actual no le dé resultados. 
    
5. Si no encuentra ningún puntero SCP en el ámbito del dominio, estará listo para pasar al siguiente paso: generar una lista con prioridades de los puntos de conexión de Detección automática de los resultados.
    
## <a name="generate-a-prioritized-list-of-autodiscover-endpoints"></a>Generar una lista con prioridades de puntos de conexión de Detección automática
<a name="bk_GenerateList"> </a>

Puede crear una lista con prioridades de direcciones URL de puntos de conexión de Detección automática, con el conjunto de objetos SCP que encontró, de la siguiente manera:
  
1. Obtener el nombre del sitio de Active Directory del equipo cliente.
    
2. Compruebe la propiedad **Keywords** en cada URL de SCP en el conjunto de objetos SCP que encontró y asigne una prioridad a la dirección URL en función de las reglas siguientes: 
    
  - Si la propiedad **keywords** contiene un valor de `"Site=<site name>"`, en el que `<site name>` es igual al nombre del sitio de Active Directory que recuperó en el paso anterior, asigne a la URL una prioridad de 1. 
    
  - Si la propiedad **Keywords** no contiene una entrada con un valor que comience por `"Site="`, asigne a la URL una prioridad 2. 
    
  - Si la propiedad **keywords** contiene un valor de `"Site=<site name>`, en el que `<site name>` no es igual al nombre del sitio de Active Directory que recuperó en el paso anterior, asigne a la URL una prioridad de 3. 
    
## <a name="code-example-performing-an-scp-lookup"></a>Ejemplo de código: realización de una búsqueda SCP
<a name="bk_CodeExample"> </a>

En el siguiente ejemplo de código, verá cómo localizar objetos SCP de Detección automática y generar una lista con prioridades de los puntos de conexión de Detección automática.
  
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

## <a name="next-steps"></a>Siguientes pasos
<a name="bk_NextSteps"> </a>

El siguiente paso del proceso de Detección automática consiste en enviar solicitudes de Detección automática a las direcciones URL que encontró, empezando por direcciones URL de prioridad 1, luego de prioridad 2 y, por último, de prioridad 3. Para obtener más información sobre cómo enviar solicitudes de Detección automática y administrar respuestas, consulte los artículos siguientes:
  
- [Obtener la configuración de usuario de Exchange mediante el uso de Detección automática](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
- [Administrar los mensajes de error de Detección automática](handling-autodiscover-error-messages.md)
    
## <a name="see-also"></a>Consulte también

- [Detección automática en Exchange](autodiscover-for-exchange.md)   
- [Configurar la aplicación EWS](setting-up-your-ews-application.md)
    

