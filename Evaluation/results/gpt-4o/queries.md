# Generated queries --- grounded / gpt-4o

## Q1
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?account rdf:type aut:Account .
  ?account aut:id ?id .
  ?account aut:accountType ?accountType .
  ?account aut:category ?category .
  ?account aut:sourceFile ?sourceFile .
  ?account aut:sourceHost ?sourceHost .
  ?sourceHost rdf:type aut:Host .
  ?sourceHost aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?account rdf:type aut:Account .
  OPTIONAL { ?account aut:id ?id . }
  OPTIONAL { ?account aut:accountType ?accountType . }
  OPTIONAL { ?account aut:category ?category . }
  OPTIONAL { ?account aut:sourceFile ?sourceFile . }
  OPTIONAL { 
    ?account aut:sourceHost ?sourceHost .
    OPTIONAL { ?sourceHost aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q2
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?account rdf:type aut:Account .
  ?account aut:accountType ?accountType .
  ?account aut:id ?identifier .
  ?account aut:sourceHost ?sourceHost .
  ?sourceHost rdf:type aut:Host .
  ?sourceHost aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?account rdf:type aut:Account .
  ?account aut:accountType ?accountType .
  ?account aut:id ?identifier .
  OPTIONAL {
    ?account aut:sourceHost ?sourceHost .
    ?sourceHost rdf:type aut:Host .
    OPTIONAL {
      ?sourceHost aut:hostSha1 ?hostSha1 .
    }
  }
}
```

## Q3
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?program rdf:type aut:InstalledProgram .
  ?program aut:programName ?programName .
  ?program aut:installedDateTime ?installedDateTime .
  ?program aut:sourceHost ?sourceHost .
  ?sourceHost rdf:type aut:Host .
  ?sourceHost aut:hostSha1 ?hostSha1 .
} WHERE {
  ?program rdf:type aut:InstalledProgram .
  ?program aut:programName ?programName .
  OPTIONAL { ?program aut:installedDateTime ?installedDateTime . }
  OPTIONAL { 
    ?program aut:sourceHost ?sourceHost .
    ?sourceHost aut:hostSha1 ?hostSha1 .
  }
}
```

## Q4
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?program rdf:type aut:InstalledProgram .
  ?program aut:programName ?programName .
  ?program aut:installedDateTime ?installedDateTime .
  ?program aut:sourceFile ?sourceFile .
  ?program aut:category ?category .
  ?program aut:sourceHost ?sourceHost .
  ?sourceHost rdf:type aut:Host .
  ?sourceHost aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?program rdf:type aut:InstalledProgram .
  ?program aut:programName ?programName .
  ?program aut:installedDateTime ?installedDateTime .
  OPTIONAL { ?program aut:sourceFile ?sourceFile . }
  OPTIONAL { ?program aut:category ?category . }
  OPTIONAL {
    ?program aut:sourceHost ?sourceHost .
    ?sourceHost aut:hostSha1 ?hostSha1 .
  }
}
```

## Q5
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?usbDevice rdf:type aut:USBDeviceAttached .
  ?usbDevice aut:attachedDateTime ?attachedDateTime .
  ?usbDevice aut:deviceID ?deviceID .
  ?usbDevice aut:deviceMake ?deviceMake .
  ?usbDevice aut:deviceModel ?deviceModel .
  ?usbDevice aut:category ?category .
  ?usbDevice aut:sourceFile ?sourceFile .
  ?usbDevice aut:sourceHost ?sourceHost .
  ?sourceHost rdf:type aut:Host .
  ?sourceHost aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?usbDevice rdf:type aut:USBDeviceAttached .
  OPTIONAL { ?usbDevice aut:attachedDateTime ?attachedDateTime . }
  OPTIONAL { ?usbDevice aut:deviceID ?deviceID . }
  OPTIONAL { ?usbDevice aut:deviceMake ?deviceMake . }
  OPTIONAL { ?usbDevice aut:deviceModel ?deviceModel . }
  OPTIONAL { ?usbDevice aut:category ?category . }
  OPTIONAL { ?usbDevice aut:sourceFile ?sourceFile . }
  OPTIONAL {
    ?usbDevice aut:sourceHost ?sourceHost .
    OPTIONAL { ?sourceHost aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q6
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?usbDevice rdf:type aut:USBDeviceAttached.
  ?usbDevice aut:deviceMake ?deviceMake.
  ?usbDevice aut:deviceModel ?deviceModel.
  ?usbDevice aut:deviceID ?deviceID.
  ?usbDevice aut:sourceHost ?sourceHost.
  ?sourceHost rdf:type aut:Host.
  ?sourceHost aut:hostSha1 ?hostSha1.
} 
WHERE {
  ?usbDevice rdf:type aut:USBDeviceAttached.
  OPTIONAL { ?usbDevice aut:deviceMake ?deviceMake. }
  OPTIONAL { ?usbDevice aut:deviceModel ?deviceModel. }
  OPTIONAL { ?usbDevice aut:deviceID ?deviceID. }
  OPTIONAL { 
    ?usbDevice aut:sourceHost ?sourceHost.
    ?sourceHost rdf:type aut:Host.
    OPTIONAL { ?sourceHost aut:hostSha1 ?hostSha1. }
  }
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
  ?osInfo rdf:type aut:OperatingSystemInformation .
  ?osInfo aut:name ?name .
  ?osInfo aut:owner ?owner .
  ?osInfo aut:path ?path .
  ?osInfo aut:processorArchitecture ?processorArchitecture .
  ?osInfo aut:productID ?productID .
  ?osInfo aut:programName ?programName .
  ?osInfo aut:sourceFile ?sourceFile .
  ?osInfo aut:temporaryFilesDirectory ?temporaryFilesDirectory .
  ?osInfo aut:sourceHost ?sourceHost .
  ?sourceHost rdf:type aut:Host .
  ?sourceHost aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?osInfo rdf:type aut:OperatingSystemInformation .
  OPTIONAL { ?osInfo aut:name ?name . }
  OPTIONAL { ?osInfo aut:owner ?owner . }
  OPTIONAL { ?osInfo aut:path ?path . }
  OPTIONAL { ?osInfo aut:processorArchitecture ?processorArchitecture . }
  OPTIONAL { ?osInfo aut:productID ?productID . }
  OPTIONAL { ?osInfo aut:programName ?programName . }
  OPTIONAL { ?osInfo aut:sourceFile ?sourceFile . }
  OPTIONAL { ?osInfo aut:temporaryFilesDirectory ?temporaryFilesDirectory . }
  OPTIONAL {
    ?osInfo aut:sourceHost ?sourceHost .
    ?sourceHost aut:hostSha1 ?hostSha1 .
  }
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
  ?osInfo rdf:type aut:OperatingSystemInformation.
  ?osInfo aut:name ?osName.
  ?osInfo aut:productID ?productID.
  ?osInfo aut:processorArchitecture ?processorArchitecture.
  ?osInfo aut:owner ?owner.
  ?osInfo aut:sourceHost ?host.
  ?host rdf:type aut:Host.
  ?host aut:hostSha1 ?hostSha1.
}
WHERE {
  ?osInfo rdf:type aut:OperatingSystemInformation.
  ?osInfo aut:name ?osName.
  ?osInfo aut:productID ?productID.
  ?osInfo aut:processorArchitecture ?processorArchitecture.
  ?osInfo aut:owner ?owner.
  OPTIONAL {
    ?osInfo aut:sourceHost ?host.
    ?host rdf:type aut:Host.
    ?host aut:hostSha1 ?hostSha1.
  }
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
  ?document rdf:type aut:RecentDocument .
  ?document aut:accessedDateTime ?accessedDateTime .
  ?document aut:path ?path .
  ?document aut:category ?category .
  ?document aut:sourceFile ?sourceFile .
  ?document aut:sourceFileMd5 ?sourceFileMd5 .
  ?document aut:sourceMime ?sourceMime .
  ?document aut:sourceHost ?sourceHost .
  ?sourceHost rdf:type aut:Host .
  ?sourceHost aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?document rdf:type aut:RecentDocument .
  OPTIONAL { ?document aut:accessedDateTime ?accessedDateTime . }
  OPTIONAL { ?document aut:path ?path . }
  OPTIONAL { ?document aut:category ?category . }
  OPTIONAL { ?document aut:sourceFile ?sourceFile . }
  OPTIONAL { ?document aut:sourceFileMd5 ?sourceFileMd5 . }
  OPTIONAL { ?document aut:sourceMime ?sourceMime . }
  OPTIONAL { 
    ?document aut:sourceHost ?sourceHost .
    OPTIONAL { ?sourceHost aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q10
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?document rdf:type aut:RecentDocument;
            aut:path ?filePath;
            aut:accessedDateTime ?lastAccessedTime;
            aut:sourceHost ?host.
  ?host rdf:type aut:Host.
} WHERE {
  ?document rdf:type aut:RecentDocument;
            aut:path ?filePath;
            aut:accessedDateTime ?lastAccessedTime;
            aut:sourceHost ?host.
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
    ?bookmark rdf:type aut:WebBookmark.
    ?bookmark aut:title ?title.
    ?bookmark aut:url ?url.
} 
WHERE {
    ?bookmark rdf:type aut:WebBookmark.
    OPTIONAL { ?bookmark aut:title ?title. }
    OPTIONAL { ?bookmark aut:url ?url. }
}
```

## Q12
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
    ?cookie rdf:type aut:WebCookie ;
            aut:name ?name ;
            aut:domain ?domain ;
            aut:url ?url .
    ?host rdf:type aut:Host ;
          aut:hostSha1 ?hostSha1 .
    ?cookie aut:sourceHost ?host.
}
WHERE {
    ?cookie rdf:type aut:WebCookie ;
            aut:name ?name ;
            aut:domain ?domain ;
            aut:url ?url ;
            aut:sourceHost ?host .
    ?host rdf:type aut:Host ;
          aut:hostSha1 ?hostSha1 .
}
```

## Q13
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
    ?webHistory rdf:type aut:WebHistory .
    ?webHistory aut:url ?url .
    ?webHistory aut:accessedDateTime ?accessedDateTime .
    ?webHistory aut:domain ?domain .
    ?webHistory aut:sourceFile ?sourceFile .
}
WHERE {
    ?webHistory rdf:type aut:WebHistory .
    ?webHistory aut:url ?url .
    ?webHistory aut:accessedDateTime ?accessedDateTime .
    ?webHistory aut:domain ?domain .
    ?webHistory aut:sourceFile ?sourceFile .
}
```

## Q14
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?webSearch rdf:type aut:WebSearch .
  ?webSearch aut:text ?searchText .
}
WHERE {
  ?webSearch rdf:type aut:WebSearch .
  ?webSearch aut:text ?searchText .
}
```

## Q15
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?recycleBin rdf:type aut:RecycleBin ;
              aut:userName ?userName ;
              aut:timeDeleted ?timeDeleted ;
              aut:sourceHost ?sourceHost .

  ?sourceHost rdf:type aut:Host ;
              aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?recycleBin rdf:type aut:RecycleBin ;
              aut:userName ?userName ;
              aut:timeDeleted ?timeDeleted ;
              aut:sourceHost ?sourceHost .
              
  OPTIONAL {
    ?sourceHost rdf:type aut:Host ;
                aut:hostSha1 ?hostSha1 .
  }
}
```

## Q16
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
  ?email rdf:type aut:EmailMessage ;
         aut-email:emailFrom ?sender ;
         aut-email:emailTo ?recipient ;
         aut-email:subject ?subject .
}
WHERE {
  ?email rdf:type aut:EmailMessage ;
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

CONSTRUCT {
  ?file rdf:type aut:ExtensionMismatch.
  ?file aut:category ?category.
  ?file aut:sourceFile ?sourceFile.
  ?file aut:sourceFileMd5 ?sourceFileMd5.
  ?file aut:sourceHost ?sourceHost.
  ?sourceHost rdf:type aut:Host.
  ?sourceHost aut:hostSha1 ?hostSha1.
}
WHERE {
  ?file rdf:type aut:ExtensionMismatch.
  OPTIONAL { ?file aut:category ?category. }
  OPTIONAL { ?file aut:sourceFile ?sourceFile. }
  OPTIONAL { ?file aut:sourceFileMd5 ?sourceFileMd5. }
  OPTIONAL { 
    ?file aut:sourceHost ?sourceHost.
    OPTIONAL { ?sourceHost rdf:type aut:Host. }
    OPTIONAL { ?sourceHost aut:hostSha1 ?hostSha1. }
  }
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
    ?metadata rdf:type aut:Metadata.
    ?metadata aut:sourceFile ?sourceFile.
    ?metadata aut:createdDateTime ?createdTime.
    ?metadata aut:modifiedDateTime ?modifiedTime.
}
WHERE {
    ?metadata rdf:type aut:Metadata.
    ?metadata aut:sourceFile ?sourceFile.
    ?metadata aut:createdDateTime ?createdTime.
    ?metadata aut:modifiedDateTime ?modifiedTime.
}
```

## Q19
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?host rdf:type aut:Host.
  ?host aut:hostSha1 ?sha1.
}
WHERE {
  ?host rdf:type aut:Host.
  ?host aut:hostSha1 ?sha1.
}
```

## Q20
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?doc rdf:type aut:RecentDocument .
  ?doc aut:accessedDateTime ?accessedDateTime .
  ?doc aut:path ?path .
  ?doc aut:sourceMime ?sourceMime .
  ?doc aut:sourceFile ?sourceFile .
  ?doc aut:sourceFileMd5 ?sourceFileMd5 .
  ?doc aut:sourceHost ?host .
  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?doc rdf:type aut:RecentDocument ;
       aut:accessedDateTime ?accessedDateTime ;
       aut:path ?path ;
       aut:sourceMime ?sourceMime ;
       aut:sourceFile ?sourceFile ;
       aut:sourceFileMd5 ?sourceFileMd5 ;
       aut:sourceHost ?host .
  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
  FILTER (?accessedDateTime > "2008-07-01T00:00:00"^^xsd:dateTime)
}
```

## Q21
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?webHistory rdf:type aut:WebHistory .
  ?webHistory aut:domain "mail.google.com" .
  ?webHistory aut:url ?url .
  ?webHistory aut:accessedDateTime ?accessedDateTime .
  ?webHistory aut:category ?category .
  ?webHistory aut:sourceFile ?sourceFile .
  ?webHistory aut:sourceHost ?sourceHost .
  ?sourceHost rdf:type aut:Host .
  ?sourceHost aut:hostSha1 ?hostSha1 .
}

WHERE {
  ?webHistory rdf:type aut:WebHistory .
  ?webHistory aut:domain "mail.google.com" .
  ?webHistory aut:url ?url .
  OPTIONAL { ?webHistory aut:accessedDateTime ?accessedDateTime . }
  OPTIONAL { ?webHistory aut:category ?category . }
  OPTIONAL { ?webHistory aut:sourceFile ?sourceFile . }
  OPTIONAL { 
    ?webHistory aut:sourceHost ?sourceHost .
    OPTIONAL { ?sourceHost aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q22
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?webSearch rdf:type aut:WebSearch.
  ?webSearch aut:text ?text.
  ?webSearch aut:category ?category.
  ?webSearch aut:domain ?domain.
  ?webSearch aut:sourceFile ?sourceFile.
  ?webSearch aut:sourceHost ?sourceHost.
  ?sourceHost rdf:type aut:Host.
  ?sourceHost aut:hostSha1 ?hostSha1.
} WHERE {
  ?webSearch rdf:type aut:WebSearch.
  ?webSearch aut:text ?text.
  FILTER CONTAINS(LCASE(?text), "spreadsheet").
  OPTIONAL { ?webSearch aut:category ?category. }
  OPTIONAL { ?webSearch aut:domain ?domain. }
  OPTIONAL { ?webSearch aut:sourceFile ?sourceFile. }
  OPTIONAL { ?webSearch aut:sourceHost ?sourceHost. 
             ?sourceHost rdf:type aut:Host.
             OPTIONAL { ?sourceHost aut:hostSha1 ?hostSha1. }
           }
}
```

## Q23
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
  ?file rdf:type aut:RecentDocument ;
        aut:path ?path ;
        aut:sourceFile ?sourceFile ;
        aut:sourceFileMd5 ?sourceFileMd5 .
  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
  ?file aut:sourceHost ?host .
} WHERE {
  ?file rdf:type aut:RecentDocument ;
        aut:path ?path ;
        aut:sourceFile ?sourceFile ;
        aut:sourceFileMd5 ?sourceFileMd5 ;
        aut:sourceHost ?host .
  FILTER CONTAINS(?path, "Downloads")
  
  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
```

## Q24
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?usbDevice rdf:type aut:USBDeviceAttached.
  ?usbDevice aut:attachedDateTime ?attachedDateTime.
  ?usbDevice aut:deviceID ?deviceID.
  ?usbDevice aut:deviceMake ?deviceMake.
  ?usbDevice aut:deviceModel ?deviceModel.
  ?usbDevice aut:category ?category.
  ?usbDevice aut:sourceFile ?sourceFile.
  ?usbDevice aut:sourceHost ?sourceHost.
  ?sourceHost rdf:type aut:Host.
  ?sourceHost aut:hostSha1 ?hostSha1.
} WHERE {
  ?usbDevice rdf:type aut:USBDeviceAttached.
  ?usbDevice aut:attachedDateTime ?attachedDateTime.
  FILTER(?attachedDateTime > "2008-07-01T00:00:00"^^xsd:dateTime)
  OPTIONAL { ?usbDevice aut:deviceID ?deviceID. }
  OPTIONAL { ?usbDevice aut:deviceMake ?deviceMake. }
  OPTIONAL { ?usbDevice aut:deviceModel ?deviceModel. }
  OPTIONAL { ?usbDevice aut:category ?category. }
  OPTIONAL { ?usbDevice aut:sourceFile ?sourceFile. }
  OPTIONAL { 
    ?usbDevice aut:sourceHost ?sourceHost.
    ?sourceHost aut:hostSha1 ?hostSha1.
  }
}
```

## Q25
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?program rdf:type aut:InstalledProgram .
  ?program aut:programName ?programName .
  ?program aut:installedDateTime ?installedDateTime .
  ?program aut:sourceFile ?sourceFile .
  ?program aut:sourceHost ?sourceHost .
  ?sourceHost rdf:type aut:Host .
  ?sourceHost aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?program rdf:type aut:InstalledProgram .
  ?program aut:programName ?programName .
  FILTER(CONTAINS(LCASE(?programName), "chrome")) .
  OPTIONAL { ?program aut:installedDateTime ?installedDateTime . }
  OPTIONAL { ?program aut:sourceFile ?sourceFile . }
  OPTIONAL { 
    ?program aut:sourceHost ?sourceHost . 
    OPTIONAL { ?sourceHost aut:hostSha1 ?hostSha1 . }
  }
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
         aut-email:emailFrom ?emailFrom ;
         aut-email:emailTo ?emailTo ;
         aut-email:messageId ?messageId ;
         aut-email:path ?path ;
         aut-email:receivedDateTime ?receivedDateTime ;
         aut-email:threadId ?threadId ;
         aut:category ?category ;
         aut:sourceFile ?sourceFile ;
         aut:sourceHost ?sourceHost .

  ?sourceHost rdf:type aut:Host .
}
WHERE {
  ?email rdf:type aut:EmailMessage ;
         aut-email:subject ?subject ;
         aut-email:emailFrom ?emailFrom ;
         aut-email:emailTo ?emailTo ;
         aut-email:messageId ?messageId ;
         aut-email:path ?path ;
         aut-email:receivedDateTime ?receivedDateTime ;
         aut-email:threadId ?threadId ;
         aut:category ?category ;
         aut:sourceFile ?sourceFile ;
         aut:sourceHost ?sourceHost .
         
  ?sourceHost rdf:type aut:Host .

  FILTER(CONTAINS(LCASE(?subject), "spreadsheet"))
}
```

## Q27
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?recycleBinItem rdf:type aut:RecycleBin.
  ?recycleBinItem aut:timeDeleted ?timeDeleted.
  ?recycleBinItem aut:category ?category.
  ?recycleBinItem aut:sourceFile ?sourceFile.
  ?recycleBinItem aut:sourceHost ?sourceHost.
  ?recycleBinItem aut:userName ?userName.
  
  ?relatedHost rdf:type aut:Host.
  ?relatedHost aut:hostSha1 ?hostSha1.
} 
WHERE {
  ?recycleBinItem rdf:type aut:RecycleBin.
  ?recycleBinItem aut:timeDeleted ?timeDeleted.
  ?recycleBinItem aut:category ?category.
  ?recycleBinItem aut:sourceFile ?sourceFile.
  ?recycleBinItem aut:userName "specifiedUser".  # Replace "specifiedUser" with the actual user's name.
  
  OPTIONAL { 
    ?recycleBinItem aut:sourceHost ?relatedHost.
    ?relatedHost aut:hostSha1 ?hostSha1.
  }
}
```

## Q28
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?artifact rdf:type ?artifactType .
  ?artifact aut:category ?category .
  ?artifact aut:sourceFile ?sourceFile .
  ?artifact aut:sourceHost ?host .
  
  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?hostSha1 .
} 
WHERE {
  ?artifact aut:sourceHost ?host .
  
  ?artifact rdf:type ?artifactType .
  ?artifact aut:category ?category .
  ?artifact aut:sourceFile ?sourceFile .
  
  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?hostSha1 .
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
    ?entity rdf:type ?type .
    ?entity ?property ?value .
    ?entity aut:sourceHost ?host .
    ?host rdf:type aut:Host .
    ?host aut:hostSha1 ?hostSha1 .
} WHERE {
    ?host rdf:type aut:Host .
    ?host aut:hostSha1 ?hostSha1 .
    FILTER(?hostSha1 = "<PUT_SHA1_HASH_HERE>") .
    ?entity aut:sourceHost ?host .
    ?entity rdf:type ?type .
    ?entity ?property ?value .
}
```

## Q30
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?document rdf:type aut:RecentDocument .
  ?document aut:sourceHost ?host .
  ?document aut:accessedDateTime ?accessedDateTime .
  ?document aut:path ?path .
  ?document aut:sourceFile ?sourceFile .
  ?document aut:sourceFileMd5 ?sourceFileMd5 .
  ?document aut:sourceMime ?sourceMime .
  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?document rdf:type aut:RecentDocument .
  ?document aut:sourceHost ?host .
  ?document aut:accessedDateTime ?accessedDateTime .
  ?document aut:path ?path .
  ?document aut:sourceFile ?sourceFile .
  ?document aut:sourceFileMd5 ?sourceFileMd5 .
  ?document aut:sourceMime ?sourceMime .
  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?hostSha1 .
  FILTER(?path = "/path/to/your/file")  # Replace with the specific file path
}
```

## Q31
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?hostSha1 .
  ?account rdf:type aut:Account .
  ?account aut:id ?id .
  ?account aut:accountType ?accountType .
  ?account aut:sourceHost ?host .
} WHERE {
  ?account rdf:type aut:Account .
  ?account aut:id ?id .
  OPTIONAL { ?account aut:accountType ?accountType . }
  ?account aut:sourceHost ?host .
  ?host rdf:type aut:Host .
  OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
}
```

## Q32
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?host rdf:type aut:Host .
  ?host aut:sourceHost ?os .
  ?os rdf:type aut:OperatingSystemInformation .
  ?os aut:name ?osName .
  
  ?account rdf:type aut:Account .
  ?account aut:sourceHost ?host .
  ?account aut:id ?accountId .
}
WHERE {
  ?host rdf:type aut:Host .
  ?os rdf:type aut:OperatingSystemInformation .
  ?os aut:sourceHost ?host .
  ?os aut:name ?osName .
  
  ?account rdf:type aut:Account .
  ?account aut:sourceHost ?host .
  ?account aut:id ?accountId .
}
```

## Q33
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?bookmark rdf:type aut:WebBookmark .
  ?history rdf:type aut:WebHistory .
  ?host rdf:type aut:Host .
  ?bookmark aut:domain ?domain .
  ?history aut:domain ?domain .
  ?bookmark aut:sourceHost ?host .
  ?history aut:sourceHost ?host .
  ?host aut:hostSha1 ?hostSha1 .
  ?bookmark aut:createdDateTime ?createdDateTime .
  ?history aut:accessedDateTime ?accessedDateTime .
} WHERE {
  ?bookmark rdf:type aut:WebBookmark ;
            aut:domain ?domain ;
            aut:sourceHost ?host .
  ?history rdf:type aut:WebHistory ;
           aut:domain ?domain ;
           aut:sourceHost ?host .
  ?host aut:hostSha1 ?hostSha1 .
  OPTIONAL { ?bookmark aut:createdDateTime ?createdDateTime . }
  OPTIONAL { ?history aut:accessedDateTime ?accessedDateTime . }
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
  ?webHistory rdf:type aut:WebHistory .
  ?webHistory aut:domain ?domain .
  ?sourceHost rdf:type aut:Host .
  ?webHistory aut:sourceHost ?sourceHost .
  ?domainStats rdf:type aut:DomainStats .
  ?domainStats aut:domain ?domain .
  ?domainStats aut:visitCount ?visitCount .
} 
WHERE {
  SELECT ?domain (COUNT(?webHistory) AS ?visitCount)
  WHERE {
    ?webHistory rdf:type aut:WebHistory .
    ?webHistory aut:domain ?domain .
    OPTIONAL {
      ?webHistory aut:sourceHost ?sourceHost .
      ?sourceHost rdf:type aut:Host .
    }
  }
  GROUP BY ?domain
}
```

## Q35
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
    ?webHistory rdf:type aut:WebHistory ;
                aut:domain ?domain ;
                aut:accessedDateTime ?accessedDateTime ;
                aut:url ?url ;
                aut:sourceFile ?sourceFile ;
                aut:sourceHost ?sourceHost .
    ?sourceHost rdf:type aut:Host ;
                aut:hostSha1 ?hostSha1 .
}
WHERE {
    {
        SELECT ?domain (COUNT(?webHistory) AS ?visitCount)
        WHERE {
            ?webHistory rdf:type aut:WebHistory ;
                        aut:domain ?domain ;
                        aut:accessedDateTime ?accessedDateTime ;
                        aut:url ?url ;
                        aut:sourceFile ?sourceFile ;
                        aut:sourceHost ?sourceHost .
            ?sourceHost rdf:type aut:Host ;
                        aut:hostSha1 ?hostSha1 .
        }
        GROUP BY ?domain
        ORDER BY DESC(?visitCount)
        LIMIT 5
    }
    ?webHistory rdf:type aut:WebHistory ;
                aut:domain ?domain ;
                aut:accessedDateTime ?accessedDateTime ;
                aut:url ?url ;
                aut:sourceFile ?sourceFile ;
                aut:sourceHost ?sourceHost .
    ?sourceHost rdf:type aut:Host ;
                aut:hostSha1 ?hostSha1 .
}
```

## Q36
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?connection rdf:type aut:WebHistory.
  ?connection aut:domain ?domain.
  ?connection aut:url ?url.
  ?connection aut:accessedDateTime ?accessedDateTime.
  ?connection aut:sourceHost ?host.
  ?host rdf:type aut:Host.
  ?host aut:hostSha1 ?hostSha1.
}
WHERE {
  ?connection rdf:type aut:WebHistory.
  ?connection aut:domain ?domain.
  ?connection aut:url ?url.
  ?connection aut:accessedDateTime ?accessedDateTime.
  ?connection aut:sourceHost ?host.
  ?host rdf:type aut:Host.
  ?host aut:hostSha1 ?hostSha1.
}
```

## Q37
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?sha1 .
  ?host aut:sourceHost ?sourceHost .
}
WHERE {
  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?sha1 .
}
```

## Q38
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?file rdf:type aut:RecycleBin.
  ?file aut:userName ?userName.
  ?file aut:timeDeleted ?timeDeleted.
}
WHERE {
  ?file rdf:type aut:RecycleBin.
  ?file aut:userName ?userName.
  ?file aut:timeDeleted ?timeDeleted.
}
```

## Q39
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?alert rdf:type aut:ExtensionMismatch .
  ?alert aut:category ?category .
  ?alert aut:sourceFile ?sourceFile .
  ?alert aut:sourceFileMd5 ?sourceFileMd5 .
  ?alert aut:sourceHost ?host .

  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?alert rdf:type aut:ExtensionMismatch .
  ?alert aut:category ?category .
  ?alert aut:sourceFile ?sourceFile .
  ?alert aut:sourceFileMd5 ?sourceFileMd5 .
  OPTIONAL {
    ?alert aut:sourceHost ?host .
    ?host aut:hostSha1 ?hostSha1 .
  }
}
```

## Q40
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?account rdf:type aut:Account .
  ?account aut:id ?accountId .
  ?account aut:category ?category .
  ?account aut:accountType ?accountType .
  ?account aut:sourceFile ?sourceFile .
  ?account aut:sourceHost ?sourceHost .
  ?sourceHost rdf:type aut:Host .
} WHERE {
  ?account rdf:type aut:Account .
  ?account aut:id ?accountId .
  OPTIONAL { ?account aut:category ?category . }
  OPTIONAL { ?account aut:accountType ?accountType . }
  OPTIONAL { ?account aut:sourceFile ?sourceFile . }
  OPTIONAL {
    ?account aut:sourceHost ?sourceHost .
    ?sourceHost rdf:type aut:Host .
  }
}
```

## Q41
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?program rdf:type aut:InstalledProgram.
  ?program aut:programName ?programName.
  ?program aut:installedDateTime ?installedDateTime.
  ?program aut:category ?category.
  ?program aut:sourceFile ?sourceFile.
  ?program aut:sourceHost ?sourceHost.
  ?sourceHost rdf:type aut:Host.
  ?sourceHost aut:hostSha1 ?hostSha1.
}
WHERE {
  ?program rdf:type aut:InstalledProgram.
  OPTIONAL { ?program aut:programName ?programName. }
  OPTIONAL { ?program aut:installedDateTime ?installedDateTime. }
  OPTIONAL { ?program aut:category ?category. }
  OPTIONAL { ?program aut:sourceFile ?sourceFile. }
  OPTIONAL {
    ?program aut:sourceHost ?sourceHost.
    ?sourceHost rdf:type aut:Host.
    OPTIONAL { ?sourceHost aut:hostSha1 ?hostSha1. }
  }
}
```

## Q42
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?program rdf:type aut:InstalledProgram .
  ?program aut:programName ?programName .
  ?program aut:installedDateTime ?installedDateTime .
  ?program aut:sourceHost ?host .
  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?program rdf:type aut:InstalledProgram .
  ?program aut:programName ?programName .
  OPTIONAL { ?program aut:installedDateTime ?installedDateTime . }
  OPTIONAL {
    ?program aut:sourceHost ?host .
    ?host aut:hostSha1 ?hostSha1 .
  }
}
```

## Q43
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?program rdf:type aut:InstalledProgram .
  ?program aut:programName ?name .
  ?program aut:installedDateTime ?installDate .
  ?program aut:sourceFile ?sourceFile .
  ?program aut:category ?category .
  ?program aut:sourceHost ?host .
  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?program rdf:type aut:InstalledProgram .
  ?program aut:programName ?name .
  OPTIONAL { ?program aut:installedDateTime ?installDate . }
  OPTIONAL { ?program aut:sourceFile ?sourceFile . }
  OPTIONAL { ?program aut:category ?category . }
  OPTIONAL { 
    ?program aut:sourceHost ?host .
    ?host aut:hostSha1 ?hostSha1 .
  }
}
```

## Q44
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?usbDevice rdf:type aut:USBDeviceAttached.
  ?usbDevice aut:attachedDateTime ?attachedDateTime.
  ?usbDevice aut:deviceID ?deviceID.
  ?usbDevice aut:deviceMake ?deviceMake.
  ?usbDevice aut:deviceModel ?deviceModel.
  ?usbDevice aut:sourceFile ?sourceFile.
  ?usbDevice aut:category ?category.
  ?usbDevice aut:sourceHost ?sourceHost.
  ?sourceHost rdf:type aut:Host.
  ?sourceHost aut:hostSha1 ?hostSha1.
} WHERE {
  ?usbDevice rdf:type aut:USBDeviceAttached.
  ?usbDevice aut:attachedDateTime ?attachedDateTime.
  ?usbDevice aut:deviceID ?deviceID.
  ?usbDevice aut:deviceMake ?deviceMake.
  ?usbDevice aut:deviceModel ?deviceModel.
  OPTIONAL { ?usbDevice aut:sourceFile ?sourceFile. }
  OPTIONAL { ?usbDevice aut:category ?category. }
  OPTIONAL {
    ?usbDevice aut:sourceHost ?sourceHost.
    ?sourceHost aut:hostSha1 ?hostSha1.
  }
}
```

## Q45
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?device a aut:USBDeviceAttached ;
          aut:deviceID ?deviceID ;
          aut:deviceMake ?deviceMake ;
          aut:deviceModel ?deviceModel ;
          aut:attachedDateTime ?attachedDateTime ;
          aut:category ?category ;
          aut:sourceFile ?sourceFile ;
          aut:sourceHost ?host .
  ?host a aut:Host ;
        aut:hostSha1 ?hostSha1 .
} WHERE {
  ?device a aut:USBDeviceAttached ;
          aut:deviceID ?deviceID ;
          aut:deviceMake ?deviceMake ;
          aut:deviceModel ?deviceModel ;
          aut:attachedDateTime ?attachedDateTime ;
          aut:category ?category ;
          aut:sourceFile ?sourceFile ;
          aut:sourceHost ?host .
  ?host a aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
```

## Q46
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?bookmark rdf:type aut:WebBookmark;
            aut:title ?title;
            aut:url ?url;
            aut:domain ?domain;
            aut:createdDateTime ?createdDateTime;
            aut:category ?category;
            aut:sourceFile ?sourceFile;
            aut:sourceHost ?sourceHost.
  ?sourceHost rdf:type aut:Host.
} 
WHERE {
  ?bookmark rdf:type aut:WebBookmark;
            aut:title ?title;
            aut:url ?url;
            aut:domain ?domain;
            aut:createdDateTime ?createdDateTime;
            aut:category ?category;
            aut:sourceFile ?sourceFile;
            aut:sourceHost ?sourceHost.
  ?sourceHost rdf:type aut:Host.
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
  ?bookmark rdf:type aut:WebBookmark .
  ?bookmark aut:title ?title .
  ?bookmark aut:createdDateTime ?createdDateTime .
  ?bookmark aut:domain ?domain .
  ?bookmark aut:url ?url .
  ?bookmark aut:sourceFile ?sourceFile .
  ?bookmark aut:sourceHost ?sourceHost .
} 
WHERE {
  ?bookmark rdf:type aut:WebBookmark ;
            aut:title ?title ;
            aut:createdDateTime ?createdDateTime ;
            aut:domain ?domain ;
            aut:url ?url ;
            aut:sourceFile ?sourceFile ;
            aut:sourceHost ?sourceHost .
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
  ?search rdf:type aut:WebSearch;
          aut:text ?text;
          aut:domain ?domain;
          aut:category ?category;
          aut:sourceHost ?sourceHostUri;
          aut:sourceFile ?sourceFileUri.
  ?sourceHostUri rdf:type aut:Host.
} 
WHERE {
  ?search rdf:type aut:WebSearch;
          aut:text ?text;
          aut:domain ?domain;
          aut:category ?category;
          aut:sourceHost ?sourceHostUri;
          aut:sourceFile ?sourceFileUri.
          
  ?sourceHostUri rdf:type aut:Host.
}
```

## Q49
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?search a aut:WebSearch ;
          aut:category ?category ;
          aut:domain ?domain ;
          aut:sourceFile ?sourceFile ;
          aut:text ?text ;
          aut:sourceHost ?host .
  ?host a aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?search a aut:WebSearch ;
          aut:category ?category ;
          aut:domain ?domain ;
          aut:sourceFile ?sourceFile ;
          aut:text ?text ;
          aut:sourceHost ?host .
  ?host a aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
```

## Q50
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
  ?email rdf:type aut:EmailMessage.
  ?email aut-email:emailFrom ?from.
  ?email aut-email:emailTo ?to.
  ?email aut-email:messageId ?messageId.
  ?email aut-email:path ?path.
  ?email aut-email:receivedDateTime ?receivedDateTime.
  ?email aut-email:subject ?subject.
  ?email aut-email:threadId ?threadId.
} WHERE {
  ?email rdf:type aut:EmailMessage.
  OPTIONAL { ?email aut-email:emailFrom ?from. }
  OPTIONAL { ?email aut-email:emailTo ?to. }
  OPTIONAL { ?email aut-email:messageId ?messageId. }
  OPTIONAL { ?email aut-email:path ?path. }
  OPTIONAL { ?email aut-email:receivedDateTime ?receivedDateTime. }
  OPTIONAL { ?email aut-email:subject ?subject. }
  OPTIONAL { ?email aut-email:threadId ?threadId. }
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
  ?email rdf:type aut:EmailMessage;
         aut-email:emailFrom ?emailFrom;
         aut-email:emailTo ?emailTo;
         aut-email:messageId ?messageId;
         aut-email:path ?path;
         aut-email:receivedDateTime ?receivedDateTime;
         aut-email:subject ?subject;
         aut-email:threadId ?threadId;
         aut:category ?category;
         aut:sourceFile ?sourceFile;
         aut:sourceHost ?sourceHost.

  ?sourceHost rdf:type aut:Host.
} WHERE {
  ?email rdf:type aut:EmailMessage;
         aut-email:emailFrom ?emailFrom;
         aut-email:emailTo ?emailTo;
         aut-email:messageId ?messageId;
         aut-email:path ?path;
         aut-email:receivedDateTime ?receivedDateTime;
         aut-email:subject ?subject;
         aut-email:threadId ?threadId;
         aut:category ?category;
         aut:sourceFile ?sourceFile;
         aut:sourceHost ?sourceHost.

  ?sourceHost rdf:type aut:Host.
}
```
