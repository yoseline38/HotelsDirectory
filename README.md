Hotel Directory XML & JSON Processing
Overview
This project was developed as part of a course assignment to demonstrate understanding and practical application of XML technologies including:

XML Elements, Attributes, and Structure

XML Schema Definition (XSD)

XML Validation

XML Transformation (XSL)

JSON Conversion using C#

Working with URLs and remote file access

It includes the creation of an XML-based hotel directory, schema validation, JSON conversion, and error-handling mechanisms via a .NET C# console application.

📁 Project Structure
pgsql
Copy
Edit
 HotelDirectoryProject
├── Hotels.xml              # Valid XML instance of the hotel directory
├── Hotels.xsd              # XML Schema (XSD) defining the structure of the XML
├── HotelsErrors.xml        # Invalid XML with injected errors for validation testing
├── Program.cs              # C# console application for validation and XML to JSON conversion
├── README.md               # Project description and usage
 Technologies Used
C# (.NET Framework 4.7, C# 7.0)

System.Xml & Newtonsoft.Json Libraries

GitHub Pages (to host XML/XSD files remotely)

 Features
XML Validation

Validates Hotels.xml against Hotels.xsd

Detects and reports errors in HotelsErrors.xml

JSON Conversion

Converts a valid XML document into a JSON format

Produces a structure compatible with JsonConvert.DeserializeXmlNode()

Hosted File Access

Uses remote URLs hosted via GitHub Pages for XML and XSD access

 Example JSON Output
json
Copy
Edit
{
  "Hotels": {
    "Hotel": [
      {
        "Name": "Westin",
        "Phone": [
          "480-968-8885",
          "800-937-8461"
        ],
        "Address": {
          "Number": "11",
          "Street": "E 7th St",
          "City": "Tempe",
          "State": "AZ",
          "Zip": "85281",
          "_NearestAirport": "Sky Habor"
        },
        "_Rating": "4.2"
      }
    ]
  }
}
🧪 How to Run
Prerequisites:
Visual Studio or .NET CLI installed

Internet connection to access hosted files

Steps:
Clone this repository:

bash
Copy
Edit
git clone https://github.com/your-username/hotel-directory-project.git
Open the project in Visual Studio.

Replace the placeholder URLs in Program.cs:

csharp
Copy
Edit
public static string xmlURL = "https://your-github-username.github.io/hotel-directory/Hotels.xml";
public static string xmlErrorURL = "https://your-github-username.github.io/hotel-directory/HotelsErrors.xml";
public static string xsdURL = "https://your-github-username.github.io/hotel-directory/Hotels.xsd";
Run the program:

bash
Copy
Edit
dotnet run

