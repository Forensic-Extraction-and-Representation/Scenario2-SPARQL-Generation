# Generated queries --- grounded / gemma4-8b-local

## Q1
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
    ?account rdf:type aut:Account ;
             aut:id ?id ;
             aut:accountType ?accountType ;
             aut:sourceFile ?sourceFile ;
             aut:category ?category ;
             aut:sourceHost ?host .
}
WHERE {
    ?account rdf:type aut:Account .
    OPTIONAL { ?account aut:id ?id }
    OPTIONAL { ?account aut:accountType ?accountType }
    OPTIONAL { ?account aut:sourceFile ?sourceFile }
    OPTIONAL { ?account aut:category ?category }
    OPTIONAL { ?account aut:sourceHost ?host }
}
```

## Q2
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
    ?account rdf:type aut:Account ;
             aut:accountType ?accountType ;
             aut:id ?identifier .
}
WHERE {
    ?account rdf:type aut:Account .
    ?account aut:accountType ?accountType .
    ?account aut:id ?identifier .
}
```

## Q3
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
    ?program a aut:InstalledProgram ;
             rdfs:label ?programName ;
             aut:programName ?programName ;
             aut:path ?filePath ;
             aut:installedDateTime ?installedDateTime ;
             aut:sourceFile ?sourceFile .
}
WHERE {
    ?program rdf:type aut:InstalledProgram .
    ?program aut:programName ?programName .
    ?program aut:path ?filePath .
    ?program aut:installedDateTime ?installedDateTime .
    ?program aut:sourceFile ?sourceFile .
}
```

## Q4
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
    ?program rdf:type aut:InstalledProgram ;
             aut:programName ?programName ;
             aut:installedDateTime ?date
}
WHERE {
    ?program rdf:type aut:InstalledProgram ;
             aut:programName ?programName ;
             aut:installedDateTime ?date .
}
```

## Q5
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>.
PREFIX owl: <http://www.w3.org/2002/07/owl#>.
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>.

CONSTRUCT {
    ?device a aut:USBDeviceAttached ;
            rdfs:label ?label ;
            aut:deviceID ?deviceID ;
            aut:deviceMake ?make ;
            aut:deviceModel ?model ;
            aut:sourceFile ?sourceFile ;
            aut:sourceHost ?host .
    ?host a owl:Class ;
          rdfs:label ?hostLabel .
}
WHERE {
    ?device a aut:USBDeviceAttached .
    
    # Gather all required properties for CONSTRUCT
    ?device aut:deviceID ?deviceID .
    OPTIONAL { ?device aut:deviceMake ?make . }
    OPTIONAL { ?device aut:deviceModel ?model . }
    OPTIONAL { ?device aut:sourceFile ?sourceFile . }
    OPTIONAL { ?device aut:sourceHost ?host . }

    # Optional: Fetch labels/types for better context in the CONSTRUCT output
    ?device rdfs:label ?label .
    ?host rdfs:label ?hostLabel .
}
```

## Q6
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
    ?device rdf:type aut:USBDeviceAttached ;
            aut:deviceMake ?make ;
            aut:deviceModel ?model ;
            aut:deviceID ?id .
} WHERE {
    ?device a aut:USBDeviceAttached ;
            aut:deviceMake ?make ;
            aut:deviceModel ?model ;
            aut:deviceID ?id .
}
```

## Q7
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
    ?osInfo rdf:type aut:OperatingSystemInformation ;
            aut:name ?name ;
            aut:owner ?owner ;
            aut:path ?path ;
            aut:processorArchitecture ?arch ;
            aut:productID ?productID ;
            aut:programName ?programName ;
            aut:sourceFile ?sourceFile .
}
WHERE {
    ?osInfo a aut:OperatingSystemInformation .

    # Extracting Name
    ?osInfo aut:name ?name .

    # Extracting Owner
    ?osInfo aut:owner ?owner .

    # Extracting Path
    ?osInfo aut:path ?path .

    # Extracting Processor Architecture
    ?osInfo aut:processorArchitecture ?arch .

    # Extracting Product ID
    ?osInfo aut:productID ?productID .

    # Extracting Program Name (if applicable)
    OPTIONAL { ?osInfo aut:programName ?programName . }

    # Extracting Source File (if applicable)
    OPTIONAL { ?osInfo aut:sourceFile ?sourceFile . }
}
```

## Q8
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
    ?osInfo a aut:OperatingSystemInformation ;
            aut:name ?osName ;
            aut:productID ?productID ;
            aut:processorArchitecture ?arch ;
            aut:owner ?owner .
}
WHERE {
    ?osInfo a aut:OperatingSystemInformation .
    ?osInfo aut:name ?osName .
    ?osInfo aut:productID ?productID .
    ?osInfo aut:processorArchitecture ?arch .
    ?osInfo aut:owner ?owner .
}
```

## Q9
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
    ?doc rdf:type aut:RecentDocument ;
          aut:sourceFile ?sourceFile ;
          aut:sourceFileMd5 ?sourceFileMd5 ;
          aut:sourceMime ?sourceMime ;
          aut:path ?path ;
          aut:accessedDateTime ?accessedDateTime ;
          aut:category ?category ;
          aut:sourceHost ?sourceHost .
    
    # Including the sourceHost entity type definition for full context
    ?sourceHost rdf:type aut:Host .
}
WHERE {
    ?doc rdf:type aut:RecentDocument .
    
    # Variables for direct properties of RecentDocument
    ?doc aut:sourceFile ?sourceFile .
    
    # Optional properties to ensure the query doesn't fail if data is missing
    OPTIONAL { ?doc aut:sourceFileMd5 ?sourceFileMd5 . }
    OPTIONAL { ?doc aut:sourceMime ?sourceMime . }
    OPTIONAL { ?doc aut:path ?path . }
    ?doc aut:accessedDateTime ?accessedDateTime .
    OPTIONAL { ?doc aut:category ?category . }
    
    # Handling the object property sourceHost
    OPTIONAL { ?doc aut:sourceHost ?sourceHost . }
}
```

## Q10
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>.
PREFIX owl: <http://www.w3.org/2002/07/owl#>.
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>.

CONSTRUCT {
    ?doc rdf:type aut:RecentDocument ;
         aut:path ?path ;
         aut:accessedDateTime ?time .
}
WHERE {
    ?doc rdf:type aut:RecentDocument ;
         aut:path ?path ;
         aut:accessedDateTime ?time .
}
```

## Q11
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
    ?bookmark rdf:type aut:WebBookmark ;
              aut:title ?title ;
              aut:url ?url .
}
WHERE {
    ?bookmark rdf:type aut:WebBookmark ;
              aut:title ?title ;
              aut:url ?url .
}
```

## Q12
```sparql
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix owl: <http://www.w3.org/2002/07/owl#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.
@prefix aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>.

CONSTRUCT {
    ?cookie a aut:WebCookie ;
            aut:name ?nameLiteral ;
            aut:domain ?domainLiteral ;
            aut:url ?urlLiteral .
}
WHERE {
    ?cookie a aut:WebCookie ;
            aut:name ?nameLiteral ;
            aut:domain ?domainLiteral ;
            aut:url ?urlLiteral .
}
```

## Q13
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
    ?history rdf:type aut:WebHistory ;
             aut:url ?url ;
             aut:accessedDateTime ?accessedDateTime ;
             rdfs:label ?historyLabel .
}
WHERE {
    ?history rdf:type aut:WebHistory .
    ?history aut:url ?url .
    ?history aut:accessedDateTime ?accessedDateTime .
    ?history rdfs:label ?historyLabel .
}
```

## Q14
```sparql
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix owl: <http://www.w3.org/2002/07/owl#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.
@prefix aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>.

CONSTRUCT {
    ?webSearch a aut:WebSearch ;
               aut:text ?searchText .
}
WHERE {
    ?webSearch a aut:WebSearch ;
               aut:text ?searchText .
}
```

## Q15
```sparql
CONSTRUCT {
    ?item rdf:type aut:RecycleBin ;
          aut:userName ?userName ;
          aut:timeDeleted ?timeDeleted .
}
WHERE {
    ?item a aut:RecycleBin ;
          aut:userName ?userName ;
          aut:timeDeleted ?timeDeleted .
}
```

## Q16
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>.
PREFIX owl: <http://www.w3.org/2002/07/owl#>.
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>.

CONSTRUCT {
    ?msg a aut:EmailMessage ;
          aut-email:emailFrom ?sender ;
          aut-email:emailTo ?recipient ;
          aut-email:subject ?subject .
}
WHERE {
    ?msg a aut:EmailMessage ;
          aut-email:emailFrom ?sender ;
          aut-email:emailTo ?recipient ;
          aut-email:subject ?subject .
}
```

## Q17
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
    ?mismatch rdf:type aut:ExtensionMismatch ;
              aut:sourceFile ?sourceFile ;
              aut:sourceFileMd5 ?md5 ;
              aut:category ?category .

    # Include the source file as a related entity
    ?sourceFile rdf:type aut:SourceFile ; # Assuming a type definition for source files based on context/best practice, though not explicitly defined, we use the property relation
                 aut:sourceFile ?sourceFile ;
                 aut:sourceFileMd5 ?md5 .
}
WHERE {
    ?mismatch rdf:type aut:ExtensionMismatch .
    ?mismatch aut:sourceFile ?sourceFile .
    OPTIONAL { ?mismatch aut:sourceFileMd5 ?md5 . }
    OPTIONAL { ?mismatch aut:category ?category . }
}
```

## Q18
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
    ?metadata rdf:type aut:Metadata ;
              aut:sourceFile ?sourceFile ;
              aut:createdDateTime ?createdDateTime ;
              aut:modifiedDateTime ?modifiedDateTime .
}
WHERE {
    ?metadata rdf:type aut:Metadata .
    ?metadata aut:sourceFile ?sourceFile .
    ?metadata aut:createdDateTime ?createdDateTime .
    ?metadata aut:modifiedDateTime ?modifiedDateTime .
}
```

## Q19
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
    ?host rdf:type aut:Host ;
          aut:hostSha1 ?sha1 .
}
WHERE {
    ?host a aut:Host .
    ?host aut:hostSha1 ?sha1 .
}
```

## Q20
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
    ?doc rdf:type aut:RecentDocument ;
          aut:path ?docPath ;
          aut:accessedDateTime ?accessedDateTime ;
          aut:sourceFile ?sourceFile .
}
WHERE {
    ?doc rdf:type aut:RecentDocument .
    ?doc aut:accessedDateTime ?accessedDateTime .
    ?doc aut:path ?docPath .
    ?doc aut:sourceFile ?sourceFile .
    FILTER (?accessedDateTime > "2008-07-01"^^xsd:dateTime) .
}
```

## Q21
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>.
PREFIX owl: <http://www.w3.org/2002/07/owl#>.
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>.

CONSTRUCT {
    ?webHistory a aut:WebHistory ;
                aut:domain "mail.google.com" ;
                aut:url ?url ;
                aut:accessedDateTime ?date ;
                aut:category ?cat ;
                aut:sourceFile ?sourceFile .
}
WHERE {
    ?webHistory a aut:WebHistory .
    ?webHistory aut:domain "mail.google.com" .

    # Optional triples to ensure all available context is included
    OPTIONAL { ?webHistory aut:url ?url . }
    OPTIONAL { ?webHistory aut:accessedDateTime ?date . }
    OPTIONAL { ?webHistory aut:category ?cat . }
    OPTIONAL { ?webHistory aut:sourceFile ?sourceFile . }
}
```

## Q22
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
    ?search rdf:type aut:WebSearch ;
            aut:text ?text .
}
WHERE {
    ?search a aut:WebSearch ;
            aut:text ?text .
    FILTER(STR(?text) = "spreadsheet") .
}
```

## Q23
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>.
PREFIX owl: <http://www.w3.org/2002/07/owl#>.
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>.

CONSTRUCT {
    ?file a rdf:type aut:RecentDocument ;
          aut:path ?path .
}
WHERE {
    {
        ?file a aut:RecentDocument ;
              aut:path ?path .
        FILTER(CONTAINS(STR(?path), "Downloads"))
    }
    UNION
    {
        ?file a aut:OperatingSystemInformation ;
              aut:path ?path .
        FILTER(CONTAINS(STR(?path)), "Downloads")
    }
    UNION
    {
        ?file a aut:EmailMessage ;
              aut-email:path ?path .
        FILTER(CONTAINS(STR(?path)), "Downloads")
    }
}
```

## Q24
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
  ?device a aut:USBDeviceAttached ;
          aut:attachedDateTime ?dateTime ;
          aut:deviceID ?deviceID ;
          aut:deviceMake ?deviceMake ;
          aut:deviceModel ?deviceModel ;
          aut:category ?category .
}
WHERE {
  ?device rdf:type aut:USBDeviceAttached .
  ?device aut:attachedDateTime ?dateTime .
  ?device aut:deviceID ?deviceID .
  ?device aut:deviceMake ?deviceMake .
  ?device aut:deviceModel ?deviceModel .
  ?device aut:category ?category .

  FILTER (?dateTime > "2008-07-01"^^xsd:dateTime)
}
```

## Q25
```sparql
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix owl: <http://www.w3.org/2002/07/owl#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.
@prefix aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>.

PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .

CONSTRUCT {
    ?program rdf:type aut:InstalledProgram ;
             aut:programName ?programName ;
             aut:sourceFile ?sourceFile .
}
WHERE {
    ?program a aut:InstalledProgram ;
             aut:programName ?programName ;
             aut:sourceFile ?sourceFile .
    FILTER(CONTAINS(STR(?programName), "Chrome"))
}
```

## Q26
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
    ?email rdf:type aut:EmailMessage ;
           aut-email:subject ?subject ;
           aut-email:emailFrom ?from ;
           aut-email:emailTo ?to ;
           aut-email:messageId ?messageId ;
           aut-email:path ?path ;
           aut-email:receivedDateTime ?receivedDateTime ;
           aut-email:threadId ?threadId ;
           aut:sourceFile ?sourceFile .
}
WHERE {
    ?email rdf:type aut:EmailMessage .
    
    # Filter condition on the subject
    ?email aut-email:subject ?subject .
    FILTER(CONTAINS(LCASE(STR(?subject)), "spreadsheet")) .
    
    # Extracting required data points for visualization/completeness
    ?email aut-email:emailFrom ?from .
    ?email aut-email:emailTo ?to .
    ?email aut-email:messageId ?messageId .
    ?email aut-email:path ?path .
    ?email aut-email:receivedDateTime ?receivedDateTime .
    ?email aut-email:threadId ?threadId .
    ?email aut:sourceFile ?sourceFile .
}
```

## Q27
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
    ?item rdf:type aut:RecycleBin ;
          aut:userName ?user ;
          aut:sourceFile ?sourceFile ;
          aut:title ?title ;
          aut:createdDateTime ?createdDateTime .
}
WHERE {
    ?item a aut:RecycleBin .
    ?item aut:userName ?user .
    OPTIONAL { ?item aut:sourceFile ?sourceFile . }
    OPTIONAL { ?item aut:title ?title . }
    OPTIONAL { ?item aut:createdDateTime ?createdDateTime . }
    # You can add more optional properties here if needed, e.g., ?item aut:category ?category .
}
```

## Q28
```sparql
CONSTRUCT {
    ?artefact a ?artefactClass .
    ?host a aut:Host ;
          aut:hostSha1 ?hostSha1 .
    ?artefact aut:sourceHost ?host .
    
    # Include other literals for context/visualization
    ?artefact aut:sourceFile ?sourceFile .
    ?artefact aut:name ?name .
}
WHERE {
    {
        # Web Bookmark
        ?artefact a aut:WebBookmark .
        ?artefact aut:sourceHost ?host .
        BIND(aut:WebBookmark AS ?artefactClass)
        BIND(?artefact AS ?artefact)
        OPTIONAL { ?artefact aut:sourceFile ?sourceFile . }
        OPTIONAL { ?artefact aut:title ?name . }
    }
    UNION
    {
        # Web Search
        ?artefact a aut:WebSearch .
        ?artefact aut:sourceHost ?host .
        BIND(aut:WebSearch AS ?artefactClass)
        BIND(?artefact AS ?artefact)
        OPTIONAL { ?artefact aut:sourceFile ?sourceFile . }
        OPTIONAL { ?artefact aut:text ?name . }
    }
    UNION
    {
        # Email Message
        ?artefact a aut:EmailMessage .
        ?artefact aut:sourceHost ?host .
        BIND(aut:EmailMessage AS ?artefactClass)
        BIND(?artefact AS ?artefact)
        OPTIONAL { ?artefact aut-email:subject ?name . }
    }
    UNION
    {
        # USB Device Attached
        ?artefact a aut:USBDeviceAttached .
        ?artefact aut:sourceHost ?host .
        BIND(aut:USBDeviceAttached AS ?artefactClass)
        BIND(?artefact AS ?artefact)
        OPTIONAL { ?artefact aut:deviceMake ?name . }
    }
    UNION
    {
        # Extension Mismatch
        ?artefact a aut:ExtensionMismatch .
        ?artefact aut:sourceHost ?host .
        BIND(aut:ExtensionMismatch AS ?artefactClass)
        BIND(?artefact AS ?artefact)
        OPTIONAL { ?artefact aut:sourceFileMd5 ?sourceFile . }
    }
    UNION
    {
        # Web Cookie
        ?artefact a aut:WebCookie .
        ?artefact aut:sourceHost ?host .
        BIND(aut:WebCookie AS ?artefactClass)
        BIND(?artefact AS ?artefact)
        OPTIONAL { ?artefact aut:url ?sourceFile . }
        OPTIONAL { ?artefact aut:name ?name . }
    }
    UNION
    {
        # Account
        ?artefact a aut:Account .
        ?artefact aut:sourceHost ?host .
        BIND(aut:Account AS ?artefactClass)
        BIND(?artefact AS ?artefact)
        OPTIONAL { ?artefact aut:id ?name . }
    }
    UNION
    {
        # Installed Program
        ?artefact a aut:InstalledProgram .
        ?artefact aut:sourceHost ?host .
        BIND(aut:InstalledProgram AS ?artefactClass)
        BIND(?artefact AS ?artefact)
        OPTIONAL { ?artefact aut:programName ?name . }
    }
    UNION
    {
        # Metadata
        ?artefact a aut:Metadata .
        ?artefact aut:sourceHost ?host .
        BIND(aut:Metadata AS ?artefactClass)
        BIND(?artefact AS ?artefact)
        OPTIONAL { ?artefact aut:owner ?name . }
    }
    UNION
    {
        # Web History
        ?artefact a aut:WebHistory .
        ?artefact aut:sourceHost ?host .
        BIND(aut:WebHistory AS ?artefactClass)
        BIND(?artefact AS ?artefact)
        OPTIONAL { ?artefact aut:url ?sourceFile . }
    }
    UNION
    {
        # Recycle Bin
        ?artefact a aut:RecycleBin .
        ?artefact aut:sourceHost ?host .
        BIND(aut:RecycleBin AS ?artefactClass)
        BIND(?artefact AS ?artefact)
        OPTIONAL { ?artefact aut:userName ?name . }
    }
    UNION
    {
        # Recent Document
        ?artefact a aut:RecentDocument .
        ?artefact aut:sourceHost ?host .
        BIND(aut:RecentDocument AS ?artefactClass)
        BIND(?artefact AS ?artefact)
        OPTIONAL { ?artefact aut:path ?sourceFile . }
    }
    UNION
    {
        # Operating System Information
        ?artefact a aut:OperatingSystemInformation .
        ?artefact aut:sourceHost ?host .
        BIND(aut:OperatingSystemInformation AS ?artefactClass)
        BIND(?artefact AS ?artefact)
        OPTIONAL { ?artefact aut:programName ?name . }
    }
}
```

## Q29
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
    ?host rdf:type aut:Host ;
          aut:hostSha1 ?sha1 ;
          ?p ?o .

    # --- WebBookmarking Data ---
    ?bookmark rdf:type aut:WebBookmark ;
               aut:title ?bookmarkTitle ;
               aut:url ?bookmarkUrl ;
               aut:sourceFile ?bookmarkSourceFile ;
               aut:domain ?bookmarkDomain ;
               rdfs:comment ?bookmarkComment .

    # --- Web Search History ---
    ?history rdf:type aut:WebHistory ;
             aut:sourceFile ?historySourceFile ;
             aut:domain ?historyDomain ;
             aut:text ?historyText ;
             aut:accessedDateTime ?historyDate .

    # --- Email Messages ---
    ?email rdf:type aut:EmailMessage ;
           aut-email:subject ?subject ;
           aut-email:from ?fromEmail ;
           aut-email:to ?toEmail ;
           aut-email:receivedDateTime ?receivedDate .

    # --- Installed Programs ---
    ?program rdf:type aut:InstalledProgram ;
              aut:programName ?programName ;
              aut:installedDateTime ?installedDate ;
              aut:sourceFile ?programSourceFile .

    # --- Operating System Info ---
    ?osInfo rdf:type aut:OperatingSystemInformation ;
            aut:productID ?productID ;
            aut:name ?osName ;
            aut:processorArchitecture ?arch ;
            aut:sourceFile ?osSourceFile .

    # --- Metadata ---
    ?meta rdf:type aut:Metadata ;
          aut:programName ?metaProgramName ;
          aut:owner ?owner ;
          aut:sourceFile ?metaSourceFile ;
          aut:userID ?userID .

    # --- Accounts ---
    ?account rdf:type aut:Account ;
              aut:id ?accountID ;
              aut:accountType ?accountType ;
              aut:sourceFile ?accountSourceFile .
}
WHERE {
    # 1. Find the primary Host using the SHA-1 hash
    ?host rdf:type aut:Host .
    ?host aut:hostSha1 "THE_GIVEN_SHA1_HASH" . # IMPORTANT: Replace "THE_GIVEN_SHA1_HASH" with the actual SHA-1 hash

    # 2. Define the common pattern: ?s sourceHost ?o
    # Retrieve all directly related objects that link back to the host
    OPTIONAL { ?s aut:sourceHost ?host }
    
    # --- WebBookmarking Details ---
    OPTIONAL { ?bookmark rdf:type aut:WebBookmark ; aut:sourceHost ?host ; aut:title ?bookmarkTitle ; aut:url ?bookmarkUrl ; aut:sourceFile ?bookmarkSourceFile . }
    
    # --- Web History Details ---
    OPTIONAL { ?history rdf:type aut:WebHistory ; aut:sourceHost ?host ; aut:text ?historyText ; aut:domain ?historyDomain ; aut:accessedDateTime ?historyDate ; aut:sourceFile ?historySourceFile . }
    
    # --- Email Message Details ---
    OPTIONAL { ?email rdf:type aut:EmailMessage ; aut:sourceHost ?host ; aut-email:subject ?subject ; aut-email:from ?fromEmail ; aut-email:to ?toEmail ; aut-email:receivedDateTime ?receivedDate . }

    # --- Installed Program Details ---
    OPTIONAL { ?program rdf:type aut:InstalledProgram ; aut:sourceHost ?host ; aut:programName ?programName ; aut:installedDateTime ?installedDate ; aut:sourceFile ?programSourceFile . }

    # --- Operating System Information Details ---
    OPTIONAL { ?osInfo rdf:type aut:OperatingSystemInformation ; aut:sourceHost ?host ; aut:name ?osName ; aut:productID ?productID ; aut:processorArchitecture ?arch ; aut:sourceFile ?osSourceFile . }

    # --- Metadata Details ---
    OPTIONAL { ?meta rdf:type aut:Metadata ; aut:sourceHost ?host ; aut:programName ?metaProgramName ; aut:owner ?owner ; aut:userID ?userID ; aut:sourceFile ?metaSourceFile . }

    # --- Account Details ---
    OPTIONAL { ?account rdf:type aut:Account ; aut:sourceHost ?host ; aut:id ?accountID ; aut:accountType ?accountType ; aut:sourceFile ?accountSourceFile . }
    
    # 3. Collect all variables needed for CONSTRUCT (to define the graph edges)
    BIND(STR(?host) AS ?host)
    BIND(xsd:string(?sha1) AS ?sha1)
    BIND(IF(BOUND(?bookmark) || BOUND(?history) || BOUND(?email) || BOUND(?program) || BOUND(?osInfo) || BOUND(?meta) || BOUND(?account), TRUE, FALSE) AS ?p)
    BIND(COALESCE(?bookmark, ?history, ?email, ?program, ?osInfo, ?meta, ?account) AS ?o)
}
```

## Q30
```sparql
CONSTRUCT {
  ?file rdf:type aut:RecentDocument ;
        aut:sourceHost ?host ;
        aut:sourceFile ?sourceFileLiteral .
  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1Literal .
}
WHERE {
  ?file rdf:type aut:RecentDocument .
  ?file aut:sourceHost ?host .
  ?host rdf:type aut:Host .
  OPTIONAL { ?file aut:sourceFile ?sourceFileLiteral . }
  OPTIONAL { ?host aut:hostSha1 ?hostSha1Literal . }
}
```

## Q31
```sparql
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix owl: <http://www.w3.org/2002/07/owl#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.
@prefix aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>.

CONSTRUCT {
    # Host definition
    ?host rdf:type aut:Host .
    
    # Account definition and relation to the host
    ?account rdf:type aut:Account ;
             aut:sourceHost ?host ;
             aut:sourceFile ?sourceFile ;
             aut:id ?accountId ;
             aut:accountType ?accountType .
}
WHERE {
    # Find the relationship: Account pointing to a Host
    ?account aut:sourceHost ?host .
    
    # Ensure the entities are correctly typed
    ?account rdf:type aut:Account .
    ?host rdf:type aut:Host .
    
    # Retrieve all necessary literals for the Account node
    ?account aut:sourceFile ?sourceFile .
    ?account aut:id ?accountId .
    ?account aut:accountType ?accountType .
}
```

## Q32
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
    ?host a aut:Host ;
          aut:sourceHost ?host ;
          aut:name ?hostName .
    ?osInfo a aut:OperatingSystemInformation ;
            aut:name ?osName ;
            aut:sourceHost ?host .
    ?account a aut:Account ;
             aut:name ?accountName ;
             aut:sourceHost ?host .
}
WHERE {
    ?host a aut:Host .
    
    # Find related OperatingSystemInformation
    ?host aut:sourceHost ?osInfo .
    ?osInfo a aut:OperatingSystemInformation ;
            aut:name ?osName .
            
    # Find related Accounts
    ?host aut:sourceHost ?account .
    ?account a aut:Account ;
             aut:name ?accountName .
}
```

## Q33
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
    # Construct the bookmark entity
    << ?bookmark ;
        rdf:type aut:WebBookmark ;
        aut:url ?bookmarkUrl ;
        aut:title ?bookmarkTitle ;
        aut:category ?bookmarkCategory . >>

    # Construct the history entity
    << ?history ;
        rdf:type aut:WebHistory ;
        aut:url ?historyUrl ;
        aut:category ?historyCategory . >>

    # Define the shared domain literal
    ?domain rdfs:label ?domainLabel .
}

WHERE {
    # Find WebBookmark instances and their associated domain
    ?bookmark a aut:WebBookmark .
    ?bookmark aut:domain ?domain .
    ?bookmark aut:url ?bookmarkUrl .
    ?bookmark aut:title ?bookmarkTitle .
    ?bookmark aut:category ?bookmarkCategory .

    # Find WebHistory instances and their associated domain, matching the same domain
    ?history a aut:WebHistory .
    ?history aut:domain ?domain .
    ?history aut:url ?historyUrl .
    ?history aut:category ?historyCategory .

    # Optional: Use rdfs:label to confirm the domain as a resource, though it's primarily a literal
    BIND(xsd:string(?domain) AS ?domainLabel)
}
```

## Q34
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
    ?webHistory rdf:type aut:WebHistory ;
                aut:domain ?domainLiteral ;
                aut:url ?url ;
                aut:sourceFile ?sourceFile .
    ?domainLiteral rdf:type xsd:string ;
                   rdfs:comment "Domain literal for WebHistory visits" .
    ?webHistory rdfs:comment "Web history visit record" .
}
WHERE {
    ?webHistory rdf:type aut:WebHistory ;
                aut:domain ?domainLiteral ;
                aut:url ?url ;
                aut:sourceFile ?sourceFile .
}
```

## Q35
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?domain rdf:type aut:domain ;
          rdfs:label ?domain ;
          aut:category ?count .
}
WHERE {
  ?history a aut:WebHistory ;
           aut:domain ?domain .
}
GROUP BY ?domain ?count
HAVING (COUNT(?history) > 0)
ORDER BY count(?history) DESC
LIMIT 5
```

## Q36
```sparql
CONSTRUCT {
  ?webHistory
    a aut:WebHistory ;
    aut:sourceHost ?host ;
    aut:url ?url ;
    ?predicateLiteral ?object ;
  ?host
    a aut:Host ;
    aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?webHistory a aut:WebHistory .
  ?webHistory aut:sourceHost ?host .
  ?webHistory aut:url ?url .
  
  # We use the destination host itself to represent the connected entity.
  # We are including the type assertion (a aut:Host) and a key literal (aut:hostSha1) for the destination.
  ?host aut:hostSha1 ?hostSha1 .
}
```

## Q37
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>.
PREFIX owl: <http://www.w3.org/2002/07/owl#>.
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.

CONSTRUCT {
    ?host a aut:Host ;
          aut:hostSha1 ?sha1 .
}
WHERE {
    ?host a aut:Host ;
          aut:hostSha1 ?sha1 .
}
```

## Q38
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>.
PREFIX owl: <http://www.w3.org/2002/07/owl#>.
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>.

CONSTRUCT {
    ?file rdf:type aut:RecycleBin ;
          aut:userName ?user ;
          aut:timeDeleted ?timestamp .
}
WHERE {
    ?file rdf:type aut:RecycleBin ;
          aut:userName ?user ;
          aut:timeDeleted ?timestamp .
}
```

## Q39
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
    ?alert rdf:type aut:ExtensionMismatch ;
           aut:sourceFile ?sourceFile ;
           aut:sourceFileMd5 ?sourceFileMd5 ;
           aut:category ?category ;
           ?p ?o .
}
WHERE {
    ?alert rdf:type aut:ExtensionMismatch .
    OPTIONAL { ?alert aut:sourceFile ?sourceFile }
    OPTIONAL { ?alert aut:sourceFileMd5 ?sourceFileMd5 }
    OPTIONAL { ?alert aut:category ?category }
    # Include all other predicates for comprehensive linking if they existed on aut:ExtensionMismatch,
    # but sticking to defined ones and those commonly used for entity data.
    # Since no other properties were defined on aut:ExtensionMismatch, we only use the ones listed above.
}
```

## Q40
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
    ?account rdf:type aut:Account ;
             aut:id ?accountId ;
             aut:name ?accountName ;
             aut:owner ?owner ;
             aut:sourceFile ?sourceFile ;
             ?s rdfs:label ?accountLabel .
}
WHERE {
    ?account rdf:type aut:Account .
    
    # Extracting properties associated with the Account entity
    OPTIONAL { ?account aut:id ?accountId . }
    OPTIONAL { ?account aut:name ?accountName . }
    OPTIONAL { ?account aut:owner ?owner . }
    OPTIONAL { ?account aut:sourceFile ?sourceFile . }
    
    # Providing a label for display purposes
    OPTIONAL { ?account rdfs:label ?accountLabel . }
}
```

## Q41
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
    ?program rdf:type aut:InstalledProgram ;
             aut:programName ?programName ;
             aut:sourceFile ?sourceFile ;
             aut:sourceHost ?sourceHost ;
             aut:installedDateTime ?installedDateTime ;
             aut:category ?category .
    # Including the related host entity if present
    ?sourceHost rdf:type aut:Host .
}
WHERE {
    ?program rdf:type aut:InstalledProgram ;
             aut:programName ?programName ;
             aut:sourceFile ?sourceFile ;
             aut:sourceHost ?sourceHost ;
             aut:installedDateTime ?installedDateTime ;
             aut:category ?category .
}
```

## Q42
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
  ?program a aut:InstalledProgram ;
           aut:programName ?programName ;
           aut:sourceFile ?sourceFile ;
           aut:category ?programCategory .
}
WHERE {
  ?program a aut:InstalledProgram .
  OPTIONAL { ?program aut:programName ?programName . }
  OPTIONAL { ?program aut:sourceFile ?sourceFile . }
  OPTIONAL { ?program aut:category ?programCategory . }
}
```

## Q43
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
    ?app rdf:type aut:InstalledProgram ;
          aut:programName ?programName ;
          aut:sourceFile ?sourceFile ;
          aut:installedDateTime ?installedDateTime .
}
WHERE {
    ?app rdf:type aut:InstalledProgram ;
         aut:programName ?programName ;
         aut:sourceFile ?sourceFile ;
         aut:installedDateTime ?installedDateTime .
}
```

## Q44
```sparql
CONSTRUCT {
    ?usbDevice a aut:USBDeviceAttached ;
               aut:deviceID ?deviceID ;
               aut:deviceMake ?deviceMake ;
               aut:deviceModel ?deviceModel ;
               aut:attachedDateTime ?attachedDateTime ;
               aut:sourceFile ?sourceFile ;
               aut:sourceHost ?sourceHost .
}
WHERE {
    ?usbDevice a aut:USBDeviceAttached ;
               aut:deviceID ?deviceID ;
               aut:deviceMake ?deviceMake ;
               aut:deviceModel ?deviceModel ;
               aut:attachedDateTime ?attachedDateTime ;
               aut:sourceFile ?sourceFile ;
               aut:sourceHost ?sourceHost .
}
```

## Q45
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
    ?device rdf:type aut:USBDeviceAttached ;
            aut:deviceMake ?deviceMake ;
            aut:deviceModel ?deviceModel ;
            aut:deviceID ?deviceID ;
            aut:sourceFile ?sourceFile ;
            aut:category ?category .
}
WHERE {
    ?device a aut:USBDeviceAttached .
    OPTIONAL { ?device aut:deviceMake ?deviceMake . }
    OPTIONAL { ?device aut:deviceModel ?deviceModel . }
    OPTIONAL { ?device aut:deviceID ?deviceID . }
    OPTIONAL { ?device aut:sourceFile ?sourceFile . }
    OPTIONAL { ?device aut:category ?category . }
}
```

## Q46
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
    ?bookmark rdf:type aut:WebBookmark ;
              aut:url ?url ;
              aut:title ?title ;
              aut:category ?category .
}
WHERE {
    ?bookmark rdf:type aut:WebBookmark .
    ?bookmark aut:url ?url .
    OPTIONAL { ?bookmark aut:title ?title . }
    OPTIONAL { ?bookmark aut:category ?category . }
}
```

## Q47
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
    ?bookmark a aut:WebBookmark ;
              aut:title ?title ;
              aut:url ?url ;
              aut:sourceFile ?sourceFile ;
              aut:sourceHost ?sourceHost .
}
WHERE {
    ?bookmark a aut:WebBookmark .
    OPTIONAL { ?bookmark aut:title ?title . }
    OPTIONAL { ?bookmark aut:url ?url . }
    OPTIONAL { ?bookmark aut:sourceFile ?sourceFile . }
    OPTIONAL { ?bookmark aut:sourceHost ?sourceHost . }
}
```

## Q48
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
    ?webSearch rdf:type aut:WebSearch .
    ?webSearch aut:text ?searchText .
    ?webSearch aut:domain ?domain .
    OPTIONAL { ?webSearch aut:sourceHost ?host . }
    OPTIONAL { ?webSearch aut:sourceFile ?sourceFile . }
}
WHERE {
    ?webSearch rdf:type aut:WebSearch .
    ?webSearch aut:text ?searchText .
    ?webSearch aut:domain ?domain .
    OPTIONAL { ?webSearch aut:sourceHost ?host . }
    OPTIONAL { ?webSearch aut:sourceFile ?sourceFile . }
}
```

## Q49
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
    ?search rdf:type aut:WebSearch ;
            aut:text ?queryText .
}
WHERE {
    ?search a aut:WebSearch ;
            aut:text ?queryText .
}
```

## Q50
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>.
PREFIX owl: <http://www.w3.org/2002/07/owl#>.
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>.

CONSTRUCT {
    ?email rdf:type aut:EmailMessage ;
           aut-email:emailFrom ?from .
    ?email aut-email:emailTo ?to ;
           aut-email:messageId ?msgId ;
           aut-email:path ?emailPath ;
           aut-email:receivedDateTime ?receivedDt ;
           aut-email:subject ?subject ;
           aut-email:threadId ?threadId ;
           aut:category ?category .
}
WHERE {
    ?email rdf:type aut:EmailMessage .
    OPTIONAL { ?email aut-email:emailFrom ?from }
    OPTIONAL { ?email aut-email:emailTo ?to }
    OPTIONAL { ?email aut-email:messageId ?msgId }
    OPTIONAL { ?email aut-email:path ?emailPath }
    OPTIONAL { ?email aut-email:receivedDateTime ?receivedDt }
    OPTIONAL { ?email aut-email:subject ?subject }
    OPTIONAL { ?email aut-email:threadId ?threadId }
    OPTIONAL { ?email aut:category ?category }
}
```

## Q51
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
    ?message rdf:type aut:EmailMessage ;
             aut-email:emailFrom ?sender ;
             aut-email:emailTo ?recipient ;
             aut-email:messageId ?messageId ;
             aut-email:path ?path ;
             aut-email:receivedDateTime ?receivedDateTime ;
             aut-email:subject ?subject ;
             aut-email:threadId ?threadId ;
             aut:sourceFile ?sourceFile .
}
WHERE {
    ?message a aut:EmailMessage ;
             aut-email:emailFrom ?sender ;
             aut-email:emailTo ?recipient ;
             aut-email:messageId ?messageId ;
             aut-email:path ?path ;
             aut-email:receivedDateTime ?receivedDateTime ;
             aut-email:subject ?subject ;
             aut-email:threadId ?threadId ;
             aut:sourceFile ?sourceFile .
}
```
