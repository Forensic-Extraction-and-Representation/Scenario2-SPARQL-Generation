# Generated queries --- grounded / qwen3-14b-local

## Q1
```sparql
CONSTRUCT {
  ?account a aut:Account ;
           aut:id ?id ;
           aut:accountType ?accountType ;
           aut:userName ?userName ;
           aut:userID ?userID .
}
WHERE {
  ?account a aut:Account .
  OPTIONAL { ?account aut:id ?id . }
  OPTIONAL { ?account aut:accountType ?accountType . }
  OPTIONAL { ?account aut:userName ?userName . }
  OPTIONAL { ?account aut:userID ?userID . }
}
```

## Q2
```sparql
prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix owl: <http://www.w3.org/2002/07/owl#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.

CONSTRUCT {
  ?account rdf:type aut:Account .
  ?account aut:accountType ?accountType .
  ?account aut:id ?accountId .
}
WHERE {
  ?account a aut:Account .
  ?account aut:accountType ?accountType .
  ?account aut:id ?accountId .
}
```

## Q3
```sparql
prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix owl: <http://www.w3.org/2002/07/owl#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.
@prefix xml: <http://www.w3.org/XML/1998/namespace>.
@prefix aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>.

CONSTRUCT {
  ?program rdf:type aut:InstalledProgram .
  ?program aut:programName ?name .
  ?program aut:installedDateTime ?installedDate .
  ?program aut:sourceFile ?source .
}
WHERE {
  ?program a aut:InstalledProgram .
  ?program aut:programName ?name .
  ?program aut:installedDateTime ?installedDate .
  ?program aut:sourceFile ?source .
}
```

## Q4
```sparql
prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix owl: <http://www.w3.org/2002/07/owl#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.

CONSTRUCT {
  ?program rdf:type aut:InstalledProgram .
  ?program aut:programName ?programName .
  ?program aut:installedDateTime ?installedDateTime .
}
WHERE {
  ?program rdf:type aut:InstalledProgram .
  ?program aut:programName ?programName .
  ?program aut:installedDateTime ?installedDateTime .
}
```

## Q5
```sparql
CONSTRUCT {
  ?usbDevice rdf:type aut:USBDeviceAttached .
  ?usbDevice aut:attachedDateTime ?attachedDateTime .
  ?usbDevice aut:deviceID ?deviceID .
  ?usbDevice aut:deviceMake ?deviceMake .
  ?usbDevice aut:deviceModel ?deviceModel .
  ?usbDevice aut:sourceFile ?sourceFile .
  ?usbDevice aut:category ?category .
}
WHERE {
  ?usbDevice rdf:type aut:USBDeviceAttached .
  OPTIONAL { ?usbDevice aut:attachedDateTime ?attachedDateTime . }
  OPTIONAL { ?usbDevice aut:deviceID ?deviceID . }
  OPTIONAL { ?usbDevice aut:deviceMake ?deviceMake . }
  OPTIONAL { ?usbDevice aut:deviceModel ?deviceModel . }
  OPTIONAL { ?usbDevice aut:sourceFile ?sourceFile . }
  OPTIONAL { ?usbDevice aut:category ?category . }
}
```

## Q6
```sparql
prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix owl: <http://www.w3.org/2002/07/owl#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.

CONSTRUCT {
  ?device rdf:type aut:USBDeviceAttached .
  ?device aut:deviceID ?deviceID .
  ?device aut:deviceMake ?deviceMake .
  ?device aut:deviceModel ?deviceModel .
}
WHERE {
  ?device rdf:type aut:USBDeviceAttached .
  ?device aut:deviceID ?deviceID .
  ?device aut:deviceMake ?deviceMake .
  ?device aut:deviceModel ?deviceModel .
}
```

## Q7
```sparql
CONSTRUCT {
  ?osInfo rdf:type aut:OperatingSystemInformation .
  ?osInfo aut:name ?name .
  ?osInfo aut:path ?path .
  ?osInfo aut:productID ?productID .
  ?osInfo aut:processorArchitecture ?processorArchitecture .
  ?osInfo aut:temporaryFilesDirectory ?temporaryFilesDirectory .
  ?osInfo aut:owner ?owner .
  ?osInfo aut:programName ?programName .
  ?osInfo aut:category ?category .
  ?osInfo aut:sourceFile ?sourceFile .
}
WHERE {
  ?osInfo a aut:OperatingSystemInformation .
  ?osInfo aut:name ?name .
  ?osInfo aut:path ?path .
  ?osInfo aut:productID ?productID .
  ?osInfo aut:processorArchitecture ?processorArchitecture .
  ?osInfo aut:temporaryFilesDirectory ?temporaryFilesDirectory .
  ?osInfo aut:owner ?owner .
  ?osInfo aut:programName ?programName .
  ?osInfo aut:category ?category .
  ?osInfo aut:sourceFile ?sourceFile .
}
```

## Q8
```sparql
prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.

CONSTRUCT {
  ?os rdf:type aut:OperatingSystemInformation .
  ?os aut:name ?osName .
  ?os aut:productID ?productId .
  ?os aut:processorArchitecture ?arch .
  ?os aut:owner ?owner .
}
WHERE {
  ?os a aut:OperatingSystemInformation .
  OPTIONAL { ?os aut:name ?osName }
  OPTIONAL { ?os aut:productID ?productId }
  OPTIONAL { ?os aut:processorArchitecture ?arch }
  OPTIONAL { ?os aut:owner ?owner }
}
```

## Q9
```sparql
CONSTRUCT {
  ?doc rdf:type aut:RecentDocument .
  ?doc aut:accessedDateTime ?accessedDateTime .
  ?doc aut:path ?path .
  ?doc aut:sourceFileMd5 ?sourceFileMd5 .
  ?doc aut:sourceMime ?sourceMime .
}
WHERE {
  ?doc rdf:type aut:RecentDocument .
  OPTIONAL { ?doc aut:accessedDateTime ?accessedDateTime }
  OPTIONAL { ?doc aut:path ?path }
  OPTIONAL { ?doc aut:sourceFileMd5 ?sourceFileMd5 }
  OPTIONAL { ?doc aut:sourceMime ?sourceMime }
}
```

## Q10
```sparql
prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix owl: <http://www.w3.org/2002/07/owl#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.

CONSTRUCT {
  ?document rdf:type aut:RecentDocument .
  ?document aut:accessedDateTime ?accessedTime .
  ?document aut:path ?filePath .
}
WHERE {
  ?document a aut:RecentDocument .
  ?document aut:accessedDateTime ?accessedTime .
  ?document aut:path ?filePath .
}
```

## Q11
```sparql
CONSTRUCT {
  ?bookmark rdf:type aut:WebBookmark .
  ?bookmark aut:title ?title .
  ?bookmark aut:url ?url .
}
WHERE {
  ?bookmark a aut:WebBookmark .
  ?bookmark aut:title ?title .
  ?bookmark aut:url ?url .
}
```

## Q12
```sparql
prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.

CONSTRUCT {
  ?cookie rdf:type aut:WebCookie .
  ?cookie aut:name ?name .
  ?cookie aut:domain ?domain .
  ?cookie aut:url ?url .
}
WHERE {
  ?cookie a aut:WebCookie .
  ?cookie aut:name ?name .
  ?cookie aut:domain ?domain .
  ?cookie aut:url ?url .
}
```

## Q13
```sparql
prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix owl: <http://www.w3.org/2002/07/owl#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.
@prefix xml: <http://www.w3.org/XML/1998/namespace>.
@prefix aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>.

CONSTRUCT {
  ?history rdf:type aut:WebHistory .
  ?history aut:url ?url .
  ?history aut:accessedDateTime ?dateTime .
}
WHERE {
  ?history a aut:WebHistory .
  ?history aut:url ?url .
  ?history aut:accessedDateTime ?dateTime .
}
```

## Q14
```sparql
prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix owl: <http://www.w3.org/2002/07/owl#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.
CONSTRUCT {
  ?search rdf:type aut:WebSearch .
  ?search aut:text ?text .
}
WHERE {
  ?search a aut:WebSearch .
  ?search aut:text ?text .
}
```

## Q15
```sparql
CONSTRUCT {
  ?item rdf:type aut:RecycleBin .
  ?item aut:userName ?user .
  ?item aut:timeDeleted ?time .
  ?item aut:sourceFile ?file .
}
WHERE {
  ?item a aut:RecycleBin .
  OPTIONAL { ?item aut:userName ?user . }
  OPTIONAL { ?item aut:timeDeleted ?time . }
  OPTIONAL { ?item aut:sourceFile ?file . }
}
```

## Q16
```sparql
prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix owl: <http://www.w3.org/2002/07/owl#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.
@prefix aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>.

CONSTRUCT {
  ?emailMessage rdf:type aut:EmailMessage .
  ?emailMessage aut-email:emailFrom ?sender .
  ?emailMessage aut-email:emailTo ?recipient .
  ?emailMessage aut-email:subject ?subject .
}
WHERE {
  ?emailMessage a aut:EmailMessage .
  ?emailMessage aut-email:emailFrom ?sender .
  ?emailMessage aut-email:emailTo ?recipient .
  ?emailMessage aut-email:subject ?subject .
}
```

## Q17
```sparql
prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix owl: <http://www.w3.org/2002/07/owl#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.

CONSTRUCT {
  ?file rdf:type aut:ExtensionMismatch ;
        aut:sourceFile ?sourceFile ;
        aut:sourceFileMd5 ?sourceFileMd5 ;
        aut:category ?category .
}
WHERE {
  ?file a aut:ExtensionMismatch .
  OPTIONAL { ?file aut:sourceFile ?sourceFile . }
  OPTIONAL { ?file aut:sourceFileMd5 ?sourceFileMd5 . }
  OPTIONAL { ?file aut:category ?category . }
}
```

## Q18
```sparql
CONSTRUCT {
  ?metadata rdf:type aut:Metadata .
  ?metadata aut:sourceFile ?sourceFile .
  ?metadata aut:createdDateTime ?createdDateTime .
  ?metadata aut:modifiedDateTime ?modifiedDateTime .
}
WHERE {
  ?metadata a aut:Metadata .
  ?metadata aut:sourceFile ?sourceFile .
  ?metadata aut:createdDateTime ?createdDateTime .
  ?metadata aut:modifiedDateTime ?modifiedDateTime .
}
```

## Q19
```sparql
prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix owl: <http://www.w3.org/2002/07/owl#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.

CONSTRUCT {
  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?sha1 .
}
WHERE {
  ?host a aut:Host .
  ?host aut:hostSha1 ?sha1 .
}
```

## Q20
```sparql
CONSTRUCT {
  ?document rdf:type aut:RecentDocument .
  ?document aut:accessedDateTime ?accessedTime .
  ?document aut:sourceFile ?sourceFile .
  ?document aut:sourceFileMd5 ?sourceFileMd5 .
  ?document aut:sourceMime ?sourceMime .
  ?document aut:path ?path .
}
WHERE {
  ?document a aut:RecentDocument .
  ?document aut:accessedDateTime ?accessedTime .
  ?document aut:sourceFile ?sourceFile .
  ?document aut:sourceFileMd5 ?sourceFileMd5 .
  ?document aut:sourceMime ?sourceMime .
  ?document aut:path ?path .
  FILTER (?accessedTime > "2008-07-01T00:00:00Z"^^xsd:dateTime)
}
```

## Q21
```sparql
prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix owl: <http://www.w3.org/2002/07/owl#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.

CONSTRUCT {
  ?entry rdf:type aut:WebHistory .
  ?entry aut:domain ?domain .
  ?entry aut:url ?url .
  ?entry aut:accessedDateTime ?accessedDateTime .
}
WHERE {
  ?entry a aut:WebHistory .
  ?entry aut:domain "mail.google.com" .
  ?entry aut:url ?url .
  ?entry aut:accessedDateTime ?accessedDateTime .
}
```

## Q22
```sparql
prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix owl: <http://www.w3.org/2002/07/owl#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.
@prefix aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>.

CONSTRUCT {
  ?search rdf:type aut:WebSearch .
  ?search aut:text ?text .
}
WHERE {
  ?search a aut:WebSearch .
  ?search aut:text ?text .
  FILTER (CONTAINS(?text, "spreadsheet"))
}
```

## Q23
```sparql
prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix owl: <http://www.w3.org/2002/07/owl#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.

CONSTRUCT {
  ?file rdf:type ?type ;
        aut:path ?path .
}
WHERE {
  {
    ?file rdf:type aut:RecentDocument .
  }
  UNION
  {
    ?file rdf:type aut:OperatingSystemInformation .
  }
  ?file aut:path ?path .
  FILTER(CONTAINS(?path, "Downloads"))
}
```

## Q24
```sparql
prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix owl: <http://www.w3.org/2002/07/owl#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.
@prefix xml: <http://www.w3.org/XML/1998/namespace>.
@prefix aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>.

CONSTRUCT {
  ?usbDevice rdf:type aut:USBDeviceAttached ;
             aut:attachedDateTime ?attachedTime ;
             aut:deviceID ?deviceID ;
             aut:deviceMake ?deviceMake ;
             aut:deviceModel ?deviceModel ;
             aut:category ?category ;
             aut:sourceFile ?sourceFile .
}
WHERE {
  ?usbDevice a aut:USBDeviceAttached ;
             aut:attachedDateTime ?attachedTime ;
             aut:deviceID ?deviceID ;
             aut:deviceMake ?deviceMake ;
             aut:deviceModel ?deviceModel ;
             aut:category ?category ;
             aut:sourceFile ?sourceFile .
  FILTER (?attachedTime > "2008-07-01T00:00:00"^^xsd:dateTime)
}
```

## Q25
```sparql
prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix owl: <http://www.w3.org/2002/07/owl#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.

CONSTRUCT {
  ?program rdf:type aut:InstalledProgram .
  ?program aut:programName ?name .
}
WHERE {
  ?program a aut:InstalledProgram .
  ?program aut:programName ?name .
  FILTER (CONTAINS(?name, 'Chrome'))
}
```

## Q26
```sparql
CONSTRUCT {
  ?email a aut:EmailMessage .
  ?email aut-email:emailFrom ?from .
  ?email aut-email:emailTo ?to .
  ?email aut-email:messageId ?messageId .
  ?email aut-email:path ?path .
  ?email aut-email:receivedDateTime ?receivedDateTime .
  ?email aut-email:subject ?subject .
  ?email aut-email:threadId ?threadId .
}
WHERE {
  ?email a aut:EmailMessage .
  ?email aut-email:subject ?subject .
  FILTER (CONTAINS(?subject, "spreadsheet"))
}
```

## Q27
```sparql
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix owl: <http://www.w3.org/2002/07/owl#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.
@prefix xml: <http://www.w3.org/XML/1998/namespace>.
@prefix aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>.

CONSTRUCT {
  ?recycleBinItem rdf:type aut:RecycleBin .
  ?recycleBinItem aut:userName ?userName .
  ?recycleBinItem aut:timeDeleted ?timeDeleted .
}
WHERE {
  ?recycleBinItem rdf:type aut:RecycleBin .
  ?recycleBinItem aut:userName ?userName .
  ?recycleBinItem aut:timeDeleted ?timeDeleted .
  FILTER (?userName = "specific_user_name")
}
```

## Q28
```sparql
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix owl: <http://www.w3.org/2002/07/owl#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.
@prefix xml: <http://www.w3.org/XML/1998/namespace>.
@prefix aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>.

CONSTRUCT {
  ?artefact rdf:type ?artefactType .
  ?host rdf:type ?hostType .
  ?artefact aut:sourceHost ?host .
  ?artefact aut:sourceFile ?sourceFile .
  ?artefact aut:category ?category .
  ?host aut:hostSha1 ?hostSha1 .
}
WHERE {
  {
    ?artefact rdf:type aut:WebBookmark .
  } UNION {
    ?artefact rdf:type aut:WebSearch .
  } UNION {
    ?artefact rdf:type aut:EmailMessage .
  } UNION {
    ?artefact rdf:type aut:USBDeviceAttached .
  } UNION {
    ?artefact rdf:type aut:ExtensionMismatch .
  } UNION {
    ?artefact rdf:type aut:WebCookie .
  } UNION {
    ?artefact rdf:type aut:Account .
  } UNION {
    ?artefact rdf:type aut:InstalledProgram .
  } UNION {
    ?artefact rdf:type aut:Metadata .
  } UNION {
    ?artefact rdf:type aut:WebHistory .
  } UNION {
    ?artefact rdf:type aut:RecycleBin .
  } UNION {
    ?artefact rdf:type aut:RecentDocument .
  } UNION {
    ?artefact rdf:type aut:OperatingSystemInformation .
  }
  ?artefact aut:sourceHost ?host .
  ?host rdf:type ?hostType .
  OPTIONAL { ?artefact aut:sourceFile ?sourceFile . }
  OPTIONAL { ?artefact aut:category ?category . }
  OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
}
```

## Q29
```sparql
CONSTRUCT {
  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hash .
  ?entity rdf:type ?entityType .
  ?entity aut:sourceHost ?host .
  ?entity aut:category ?category .
  ?entity aut:sourceFile ?sourceFile .
  ?entity aut:sourceFileMd5 ?sourceFileMd5 .
  ?entity aut:domain ?domain .
  ?entity aut:programName ?programName .
  ?entity aut:installedDateTime ?installedDateTime .
  ?entity aut:modifiedDateTime ?modifiedDateTime .
  ?entity aut:accessedDateTime ?accessedDateTime .
  ?entity aut:timeDeleted ?timeDeleted .
  ?entity aut:userName ?userName .
  ?entity aut:temporaryFilesDirectory ?temporaryFilesDirectory .
  ?entity aut:processorArchitecture ?processorArchitecture .
  ?entity aut:productID ?productID .
  ?entity aut:deviceID ?deviceID .
  ?entity aut:deviceMake ?deviceMake .
  ?entity aut:deviceModel ?deviceModel .
  ?entity aut:attachedDateTime ?attachedDateTime .
  ?entity aut:emailFrom ?emailFrom .
  ?entity aut:emailTo ?emailTo .
  ?entity aut:subject ?subject .
  ?entity aut:messageId ?messageId .
  ?entity aut:threadId ?threadId .
  ?entity aut:receivedDateTime ?receivedDateTime .
  ?entity aut:title ?title .
  ?entity aut:url ?url .
  ?entity aut:text ?text .
  ?entity aut:id ?id .
  ?entity aut:accountType ?accountType .
  ?entity aut:owner ?owner .
  ?entity aut:path ?path .
  ?entity aut:name ?name .
  ?entity aut:userID ?userID .
} WHERE {
  BIND("<given_sha1_hash>" AS ?hash) .
  ?host aut:hostSha1 ?hash .
  ?entity aut:sourceHost ?host .
  ?entity rdf:type ?entityType .
}
```

## Q30
```sparql
CONSTRUCT {
  ?entity rdf:type ?entityType .
  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?hostSha1 .
  ?entity aut:sourceFile ?file .
  ?entity aut:sourceHost ?host .
}
WHERE {
  ?entity aut:sourceHost ?host .
  ?entity aut:sourceFile ?file .
  ?entity rdf:type ?entityType .
  ?host aut:hostSha1 ?hostSha1 .
}
```

## Q31
```sparql
CONSTRUCT {
  ?account rdf:type aut:Account .
  ?account aut:id ?accountId .
  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?hostSha1 .
  ?account aut:sourceHost ?host .
}
WHERE {
  ?account aut:sourceHost ?host .
  ?account aut:id ?accountId .
  ?host aut:hostSha1 ?hostSha1 .
}
```

## Q32
```sparql
prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix owl: <http://www.w3.org/2002/07/owl#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.

CONSTRUCT {
  ?host rdf:type aut:Host .
  ?host aut:sourceHost ?osInfo .
  ?osInfo rdf:type aut:OperatingSystemInformation .
  ?osInfo aut:name ?osName .
  ?host aut:sourceHost ?account .
  ?account rdf:type aut:Account .
  ?account aut:userName ?accountName .
}
WHERE {
  ?host a aut:Host .
  ?host aut:sourceHost ?osInfo .
  ?osInfo a aut:OperatingSystemInformation .
  ?osInfo aut:name ?osName .
  ?host aut:sourceHost ?account .
  ?account a aut:Account .
  ?account aut:userName ?accountName .
}
```

## Q33
```sparql
CONSTRUCT {
  ?bookmark rdf:type aut:WebBookmark .
  ?history rdf:type aut:WebHistory .
  ?domain rdf:type xsd:string .
  ?bookmark aut:domain ?domain .
  ?history aut:domain ?domain .
}
WHERE {
  ?bookmark a aut:WebBookmark .
  ?bookmark aut:domain ?domain .
  ?history a aut:WebHistory .
  ?history aut:domain ?domain .
}
```

## Q34
```sparql
CONSTRUCT {
  ?domain aut:domain ?domainLiteral .
  ?domain aut:category ?count .
}
WHERE {
  SELECT (GROUP_CONCAT(?domain; SEPARATOR=",") AS ?domain) (COUNT(?webHistory) AS ?count)
  WHERE {
    ?webHistory a aut:WebHistory ;
                aut:domain ?domainLiteral .
  }
  GROUP BY ?domainLiteral
}
```

## Q35
```sparql
CONSTRUCT {
  ?domain aut:domain ?domain .
  ?domain aut:count ?count .
}
WHERE {
  SELECT (COUNT(?webHistory) AS ?count) ?domain
  WHERE {
    ?webHistory a aut:WebHistory .
    ?webHistory aut:domain ?domain .
  }
  GROUP BY ?domain
}
```

## Q36
```sparql
CONSTRUCT {
  ?networkConnection rdf:type aut:WebHistory .
  ?networkConnection aut:sourceHost ?contactedHost .
  ?contactedHost rdf:type aut:Host .
  ?contactedHost aut:hostSha1 ?ipAddress .
}
WHERE {
  ?networkConnection a aut:WebHistory .
  ?networkConnection aut:sourceHost ?contactedHost .
  ?contactedHost aut:hostSha1 ?ipAddress .
}
```

## Q37
```sparql
CONSTRUCT {
  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?hostSha1 .
  ?host aut:sourceFile ?sourceFile .
}
WHERE {
  ?host rdf:type aut:Host .
  OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  OPTIONAL { ?host aut:sourceFile ?sourceFile . }
}
```

## Q38
```sparql
CONSTRUCT {
  ?file rdf:type aut:File .
  ?file aut:sourceFile ?file .
  ?file aut:deletedBy ?user .
  ?file aut:deletedAt ?time .
  ?user rdf:type aut:User .
  ?user aut:userName ?user .
}
WHERE {
  ?recycleBin a aut:RecycleBin .
  ?recycleBin aut:sourceFile ?file .
  ?recycleBin aut:userName ?user .
  ?recycleBin aut:timeDeleted ?time .
}
```

## Q39
```sparql
CONSTRUCT {
  ?alert rdf:type ?type .
  ?alert aut:category ?category .
  ?alert aut:sourceFile ?sourceFile .
  ?alert aut:sourceHost ?host .
  ?host rdf:type ?hostType .
  ?host aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?alert a aut:ExtensionMismatch .
  ?alert aut:category ?category .
  ?alert aut:sourceFile ?sourceFile .
  OPTIONAL { ?alert aut:sourceHost ?host .
             ?host rdf:type ?hostType .
             ?host aut:hostSha1 ?hostSha1 . }
}
```

## Q40
```sparql
construct a SPARQL query that retrieves password information based on the given ontology.
```

## Q41
```sparql
prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix owl: <http://www.w3.org/2002/07/owl#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.
@prefix xml: <http://www.w3.org/XML/1998/namespace>.
@prefix aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>.

CONSTRUCT {
  ?program rdf:type aut:InstalledProgram .
  ?program aut:programName ?programName .
  ?program aut:installedDateTime ?installedDateTime .
  ?program aut:sourceFile ?sourceFile .
  ?program aut:sourceHost ?host .
  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?program rdf:type aut:InstalledProgram .
  ?program aut:programName ?programName .
  ?program aut:installedDateTime ?installedDateTime .
  ?program aut:sourceFile ?sourceFile .
  ?program aut:sourceHost ?host .
  ?host aut:hostSha1 ?hostSha1 .
}
```

## Q42
```sparql
prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix owl: <http://www.w3.org/2002/07/owl#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.
@prefix xml: <http://www.w3.org/XML/1998/namespace>.
@prefix aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>.

CONSTRUCT {
  ?program rdf:type aut:InstalledProgram .
  ?program aut:programName ?name .
}
WHERE {
  ?program a aut:InstalledProgram .
  ?program aut:programName ?name .
}
```

## Q43
```sparql
prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix owl: <http://www.w3.org/2002/07/owl#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.

CONSTRUCT {
  ?app rdf:type aut:InstalledProgram .
  ?app aut:programName ?name .
}
WHERE {
  ?app a aut:InstalledProgram .
  ?app aut:programName ?name .
}
```

## Q44
```sparql
CONSTRUCT {
  ?usbDevice rdf:type aut:USBDeviceAttached .
  ?usbDevice aut:attachedDateTime ?attachedDateTime .
  ?usbDevice aut:deviceID ?deviceID .
  ?usbDevice aut:deviceMake ?deviceMake .
  ?usbDevice aut:deviceModel ?deviceModel .
}
WHERE {
  ?usbDevice rdf:type aut:USBDeviceAttached .
  ?usbDevice aut:attachedDateTime ?attachedDateTime .
  ?usbDevice aut:deviceID ?deviceID .
  ?usbDevice aut:deviceMake ?deviceMake .
  ?usbDevice aut:deviceModel ?deviceModel .
}
```

## Q45
```sparql
CONSTRUCT {
  ?device rdf:type aut:USBDeviceAttached .
  ?device aut:attachedDateTime ?attachedDateTime .
  ?device aut:deviceID ?deviceID .
  ?device aut:deviceMake ?deviceMake .
  ?device aut:deviceModel ?deviceModel .
  ?device aut:sourceHost ?host .
  ?host rdf:type aut:Host .
}
WHERE {
  ?device a aut:USBDeviceAttached .
  ?device aut:attachedDateTime ?attachedDateTime .
  ?device aut:deviceID ?deviceID .
  ?device aut:deviceMake ?deviceMake .
  ?device aut:deviceModel ?deviceModel .
  ?device aut:sourceHost ?host .
}
```

## Q46
```sparql
CONSTRUCT {
  ?bookmark rdf:type aut:WebBookmark .
  ?bookmark aut:title ?title .
  ?bookmark aut:url ?url .
}
WHERE {
  ?bookmark rdf:type aut:WebBookmark .
  OPTIONAL { ?bookmark aut:title ?title }
  OPTIONAL { ?bookmark aut:url ?url }
}
```

## Q47
```sparql
CONSTRUCT {
  ?bookmark rdf:type aut:WebBookmark ;
            aut:title ?title ;
            aut:url ?url .
}
WHERE {
  ?bookmark a aut:WebBookmark .
  OPTIONAL { ?bookmark aut:title ?title . }
  OPTIONAL { ?bookmark aut:url ?url . }
}
```

## Q48
```sparql
prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix owl: <http://www.w3.org/2002/07/owl#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.
@prefix xml: <http://www.w3.org/XML/1998/namespace>.
@prefix aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>.

CONSTRUCT {
  ?search rdf:type aut:WebSearch .
  ?search aut:text ?text .
}
WHERE {
  ?search a aut:WebSearch .
  ?search aut:text ?text .
}
```

## Q49
```sparql
prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix owl: <http://www.w3.org/2002/07/owl#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.

CONSTRUCT {
  ?search rdf:type aut:WebSearch .
  ?search aut:text ?queryText .
}
WHERE {
  ?search a aut:WebSearch .
  ?search aut:text ?queryText .
}
```

## Q50
```sparql
prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix owl: <http://www.w3.org/2002/07/owl#>.
@prefix aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.
@prefix aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>.

CONSTRUCT {
  ?email rdf:type aut:EmailMessage .
  ?email aut-email:emailFrom ?from .
  ?email aut-email:emailTo ?to .
  ?email aut-email:messageId ?messageId .
  ?email aut-email:path ?path .
  ?email aut-email:receivedDateTime ?receivedDateTime .
  ?email aut-email:subject ?subject .
  ?email aut-email:threadId ?threadId .
}
WHERE {
  ?email rdf:type aut:EmailMessage .
  OPTIONAL { ?email aut-email:emailFrom ?from . }
  OPTIONAL { ?email aut-email:emailTo ?to . }
  OPTIONAL { ?email aut-email:messageId ?messageId . }
  OPTIONAL { ?email aut-email:path ?path . }
  OPTIONAL { ?email aut-email:receivedDateTime ?receivedDateTime . }
  OPTIONAL { ?email aut-email:subject ?subject . }
  OPTIONAL { ?email aut-email:threadId ?threadId . }
}
```

## Q51
```sparql
CONSTRUCT {
  ?message rdf:type aut:EmailMessage .
  ?message aut-email:emailFrom ?emailFrom .
  ?message aut-email:emailTo ?emailTo .
  ?message aut-email:messageId ?messageId .
  ?message aut-email:path ?path .
  ?message aut-email:receivedDateTime ?receivedDateTime .
  ?message aut-email:subject ?subject .
  ?message aut-email:threadId ?threadId .
  ?message aut:sourceFile ?sourceFile .
  ?message aut:category ?category .
  ?message aut:sourceFileMd5 ?sourceFileMd5 .
  ?message aut:sourceHost ?sourceHost .
} WHERE {
  ?message rdf:type aut:EmailMessage .
  OPTIONAL { ?message aut-email:emailFrom ?emailFrom }
  OPTIONAL { ?message aut-email:emailTo ?emailTo }
  OPTIONAL { ?message aut-email:messageId ?messageId }
  OPTIONAL { ?message aut-email:path ?path }
  OPTIONAL { ?message aut-email:receivedDateTime ?receivedDateTime }
  OPTIONAL { ?message aut-email:subject ?subject }
  OPTIONAL { ?message aut-email:threadId ?threadId }
  OPTIONAL { ?message aut:sourceFile ?sourceFile }
  OPTIONAL { ?message aut:category ?category }
  OPTIONAL { ?message aut:sourceFileMd5 ?sourceFileMd5 }
  OPTIONAL { ?message aut:sourceHost ?sourceHost }
}
```
