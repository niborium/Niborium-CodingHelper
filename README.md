# Niborium-CodingHelper

Programmet körs med ```dotnet run``` från Terminalen.\
Du kommer få mata in din sökfråga direkt i Terminal-fönstret och sedan så öppnar den webbläsaren åt dig och gör sökförfrågan.\
```
using System.Diagnostics;

namespace search
{
    class SearchGoogleAndStackoverflow{
        static void Main()
        {
            Console.WriteLine("Vad behöver du hjälp med?");
            string query = Console.ReadLine();
            var google = "https://www.google.se/search?q=";
            var stackoverflow = "https://stackoverflow.com/search?q=";
            var searchQuery = query;
            System.Web.HttpUtility.UrlEncode(searchQuery);

            Process.Start("explorer.exe", $"\"{google}\"{searchQuery}");
            Process.Start("explorer.exe", $"\"{stackoverflow}\"{searchQuery}");
        }
    }
}
```
