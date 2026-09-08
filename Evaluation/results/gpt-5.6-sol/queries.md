# Generated queries --- grounded / gpt-5.6-sol

## Q1
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?account rdf:type aut:Account ;
           aut:accountType ?accountType ;
           aut:category ?category ;
           aut:id ?id ;
           aut:sourceFile ?sourceFile ;
           aut:sourceHost ?host .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?account rdf:type aut:Account .

  OPTIONAL { ?account aut:accountType ?accountType . }
  OPTIONAL { ?account aut:category ?category . }
  OPTIONAL { ?account aut:id ?id . }
  OPTIONAL { ?account aut:sourceFile ?sourceFile . }
  OPTIONAL {
    ?account aut:sourceHost ?host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q2
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?account rdf:type aut:Account ;
           aut:accountType ?accountType ;
           aut:id ?identifier .
}
WHERE {
  ?account rdf:type aut:Account ;
           aut:accountType ?accountType ;
           aut:id ?identifier .
}
```

## Q3
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?program rdf:type aut:InstalledProgram ;
           aut:programName ?programName ;
           aut:installedDateTime ?installedDateTime ;
           aut:category ?category ;
           aut:sourceFile ?sourceFile ;
           aut:sourceHost ?host .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?program rdf:type aut:InstalledProgram .

  OPTIONAL { ?program aut:programName ?programName . }
  OPTIONAL { ?program aut:installedDateTime ?installedDateTime . }
  OPTIONAL { ?program aut:category ?category . }
  OPTIONAL { ?program aut:sourceFile ?sourceFile . }

  OPTIONAL {
    ?program aut:sourceHost ?host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q4
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?program rdf:type aut:InstalledProgram ;
           aut:programName ?programName ;
           aut:installedDateTime ?installedDateTime .
}
WHERE {
  ?program rdf:type aut:InstalledProgram ;
           aut:programName ?programName ;
           aut:installedDateTime ?installedDateTime .
}
```

## Q5
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?usb rdf:type aut:USBDeviceAttached ;
       aut:attachedDateTime ?attachedDateTime ;
       aut:deviceID ?deviceID ;
       aut:deviceMake ?deviceMake ;
       aut:deviceModel ?deviceModel ;
       aut:category ?category ;
       aut:sourceFile ?sourceFile ;
       aut:sourceHost ?host .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?usb rdf:type aut:USBDeviceAttached .

  OPTIONAL { ?usb aut:attachedDateTime ?attachedDateTime . }
  OPTIONAL { ?usb aut:deviceID ?deviceID . }
  OPTIONAL { ?usb aut:deviceMake ?deviceMake . }
  OPTIONAL { ?usb aut:deviceModel ?deviceModel . }
  OPTIONAL { ?usb aut:category ?category . }
  OPTIONAL { ?usb aut:sourceFile ?sourceFile . }
  OPTIONAL {
    ?usb aut:sourceHost ?host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q6
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?device rdf:type aut:USBDeviceAttached ;
          aut:deviceMake ?make ;
          aut:deviceModel ?model ;
          aut:deviceID ?deviceID .
}
WHERE {
  ?device rdf:type aut:USBDeviceAttached ;
          aut:deviceMake ?make ;
          aut:deviceModel ?model ;
          aut:deviceID ?deviceID .
}
```

## Q7
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?os rdf:type aut:OperatingSystemInformation ;
      aut:category ?category ;
      aut:name ?name ;
      aut:owner ?owner ;
      aut:path ?path ;
      aut:processorArchitecture ?processorArchitecture ;
      aut:productID ?productID ;
      aut:programName ?programName ;
      aut:sourceFile ?sourceFile ;
      aut:temporaryFilesDirectory ?temporaryFilesDirectory ;
      aut:sourceHost ?host .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?os rdf:type aut:OperatingSystemInformation .

  OPTIONAL { ?os aut:category ?category . }
  OPTIONAL { ?os aut:name ?name . }
  OPTIONAL { ?os aut:owner ?owner . }
  OPTIONAL { ?os aut:path ?path . }
  OPTIONAL { ?os aut:processorArchitecture ?processorArchitecture . }
  OPTIONAL { ?os aut:productID ?productID . }
  OPTIONAL { ?os aut:programName ?programName . }
  OPTIONAL { ?os aut:sourceFile ?sourceFile . }
  OPTIONAL { ?os aut:temporaryFilesDirectory ?temporaryFilesDirectory . }
  OPTIONAL {
    ?os aut:sourceHost ?host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q8
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?os rdf:type aut:OperatingSystemInformation ;
      aut:name ?name ;
      aut:productID ?productID ;
      aut:processorArchitecture ?processorArchitecture ;
      aut:owner ?owner .
}
WHERE {
  ?os rdf:type aut:OperatingSystemInformation ;
      aut:name ?name ;
      aut:productID ?productID ;
      aut:processorArchitecture ?processorArchitecture ;
      aut:owner ?owner .
}
```

## Q9
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?document rdf:type aut:RecentDocument ;
            aut:accessedDateTime ?accessedDateTime ;
            aut:category ?category ;
            aut:path ?path ;
            aut:sourceFile ?sourceFile ;
            aut:sourceFileMd5 ?sourceFileMd5 ;
            aut:sourceMime ?sourceMime ;
            aut:sourceHost ?host .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?document rdf:type aut:RecentDocument .

  OPTIONAL { ?document aut:accessedDateTime ?accessedDateTime . }
  OPTIONAL { ?document aut:category ?category . }
  OPTIONAL { ?document aut:path ?path . }
  OPTIONAL { ?document aut:sourceFile ?sourceFile . }
  OPTIONAL { ?document aut:sourceFileMd5 ?sourceFileMd5 . }
  OPTIONAL { ?document aut:sourceMime ?sourceMime . }

  OPTIONAL {
    ?document aut:sourceHost ?host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q10
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?document rdf:type aut:RecentDocument ;
            aut:path ?filePath ;
            aut:accessedDateTime ?lastAccessedTime .
}
WHERE {
  ?document rdf:type aut:RecentDocument ;
            aut:path ?filePath ;
            aut:accessedDateTime ?lastAccessedTime .
}
```

## Q11
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
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
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?cookie rdf:type aut:WebCookie ;
          aut:name ?name ;
          aut:domain ?domain ;
          aut:url ?url .
}
WHERE {
  ?cookie rdf:type aut:WebCookie ;
          aut:name ?name ;
          aut:domain ?domain ;
          aut:url ?url .
}
```

## Q13
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?history rdf:type aut:WebHistory ;
           aut:url ?url ;
           aut:accessedDateTime ?accessedDateTime .
}
WHERE {
  ?history rdf:type aut:WebHistory ;
           aut:url ?url ;
           aut:accessedDateTime ?accessedDateTime .
}
```

## Q14
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?webSearch rdf:type aut:WebSearch ;
             aut:text ?searchText .
}
WHERE {
  ?webSearch rdf:type aut:WebSearch ;
             aut:text ?searchText .
}
```

## Q15
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?item rdf:type aut:RecycleBin ;
        aut:userName ?userName ;
        aut:timeDeleted ?timeDeleted ;
        aut:category ?category ;
        aut:sourceFile ?sourceFile ;
        aut:sourceHost ?host .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?item rdf:type aut:RecycleBin .

  OPTIONAL { ?item aut:userName ?userName . }
  OPTIONAL { ?item aut:timeDeleted ?timeDeleted . }
  OPTIONAL { ?item aut:category ?category . }
  OPTIONAL { ?item aut:sourceFile ?sourceFile . }
  OPTIONAL {
    ?item aut:sourceHost ?host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q16
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
  ?message rdf:type aut:EmailMessage ;
           aut-email:emailFrom ?sender ;
           aut-email:emailTo ?recipient ;
           aut-email:subject ?subject .
}
WHERE {
  ?message rdf:type aut:EmailMessage ;
           aut-email:emailFrom ?sender ;
           aut-email:emailTo ?recipient ;
           aut-email:subject ?subject .
}
```

## Q17
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?file rdf:type aut:ExtensionMismatch ;
        aut:category ?category ;
        aut:sourceFile ?sourceFile ;
        aut:sourceFileMd5 ?sourceFileMd5 ;
        aut:sourceHost ?host .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?file rdf:type aut:ExtensionMismatch .

  OPTIONAL { ?file aut:category ?category . }
  OPTIONAL { ?file aut:sourceFile ?sourceFile . }
  OPTIONAL { ?file aut:sourceFileMd5 ?sourceFileMd5 . }
  OPTIONAL {
    ?file aut:sourceHost ?host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q18
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?metadata rdf:type aut:Metadata ;
            aut:sourceFile ?sourceFile ;
            aut:createdDateTime ?createdDateTime ;
            aut:modifiedDateTime ?modifiedDateTime .
}
WHERE {
  ?metadata rdf:type aut:Metadata ;
            aut:sourceFile ?sourceFile ;
            aut:createdDateTime ?createdDateTime ;
            aut:modifiedDateTime ?modifiedDateTime .
}
```

## Q19
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?host rdf:type aut:Host ;
        aut:hostSha1 ?sha1 .
}
WHERE {
  ?host rdf:type aut:Host ;
        aut:hostSha1 ?sha1 .
}
```

## Q20
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?document rdf:type aut:RecentDocument ;
            aut:accessedDateTime ?accessedDateTime ;
            aut:category ?category ;
            aut:path ?path ;
            aut:sourceFile ?sourceFile ;
            aut:sourceFileMd5 ?sourceFileMd5 ;
            aut:sourceMime ?sourceMime ;
            aut:sourceHost ?host .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?document rdf:type aut:RecentDocument ;
            aut:accessedDateTime ?accessedDateTime .

  FILTER(
    ?accessedDateTime > "2008-07-01T00:00:00"^^xsd:dateTime
  )

  OPTIONAL { ?document aut:category ?category . }
  OPTIONAL { ?document aut:path ?path . }
  OPTIONAL { ?document aut:sourceFile ?sourceFile . }
  OPTIONAL { ?document aut:sourceFileMd5 ?sourceFileMd5 . }
  OPTIONAL { ?document aut:sourceMime ?sourceMime . }
  OPTIONAL {
    ?document aut:sourceHost ?host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q21
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?history rdf:type aut:WebHistory ;
           aut:domain ?domain .
  ?history aut:url ?url ;
           aut:accessedDateTime ?accessedDateTime ;
           aut:category ?category ;
           aut:sourceFile ?sourceFile ;
           aut:sourceHost ?host .
  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?history rdf:type aut:WebHistory ;
           aut:domain ?domain .
  FILTER(STR(?domain) = "mail.google.com")

  OPTIONAL { ?history aut:url ?url . }
  OPTIONAL { ?history aut:accessedDateTime ?accessedDateTime . }
  OPTIONAL { ?history aut:category ?category . }
  OPTIONAL { ?history aut:sourceFile ?sourceFile . }
  OPTIONAL {
    ?history aut:sourceHost ?host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q22
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?search rdf:type aut:WebSearch ;
          aut:text ?text ;
          aut:category ?category ;
          aut:domain ?domain ;
          aut:sourceFile ?sourceFile ;
          aut:sourceHost ?host .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?search rdf:type aut:WebSearch ;
          aut:text ?text .

  FILTER(CONTAINS(LCASE(STR(?text)), "spreadsheet"))

  OPTIONAL { ?search aut:category ?category . }
  OPTIONAL { ?search aut:domain ?domain . }
  OPTIONAL { ?search aut:sourceFile ?sourceFile . }
  OPTIONAL {
    ?search aut:sourceHost ?host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q23
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?file rdf:type aut:RecentDocument ;
        aut:path ?path ;
        aut:accessedDateTime ?accessedDateTime ;
        aut:category ?category ;
        aut:sourceFile ?sourceFile ;
        aut:sourceFileMd5 ?sourceFileMd5 ;
        aut:sourceMime ?sourceMime ;
        aut:sourceHost ?host .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?file rdf:type aut:RecentDocument ;
        aut:path ?path .

  FILTER(CONTAINS(STR(?path), "Downloads"))

  OPTIONAL { ?file aut:accessedDateTime ?accessedDateTime . }
  OPTIONAL { ?file aut:category ?category . }
  OPTIONAL { ?file aut:sourceFile ?sourceFile . }
  OPTIONAL { ?file aut:sourceFileMd5 ?sourceFileMd5 . }
  OPTIONAL { ?file aut:sourceMime ?sourceMime . }
  OPTIONAL {
    ?file aut:sourceHost ?host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q24
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?usbDevice rdf:type aut:USBDeviceAttached ;
             aut:attachedDateTime ?attachedDateTime ;
             aut:deviceID ?deviceID ;
             aut:deviceMake ?deviceMake ;
             aut:deviceModel ?deviceModel ;
             aut:category ?category ;
             aut:sourceFile ?sourceFile ;
             aut:sourceHost ?host .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?usbDevice rdf:type aut:USBDeviceAttached ;
             aut:attachedDateTime ?attachedDateTime .

  FILTER(
    ?attachedDateTime > "2008-07-01T00:00:00"^^xsd:dateTime
  )

  OPTIONAL { ?usbDevice aut:deviceID ?deviceID . }
  OPTIONAL { ?usbDevice aut:deviceMake ?deviceMake . }
  OPTIONAL { ?usbDevice aut:deviceModel ?deviceModel . }
  OPTIONAL { ?usbDevice aut:category ?category . }
  OPTIONAL { ?usbDevice aut:sourceFile ?sourceFile . }
  OPTIONAL {
    ?usbDevice aut:sourceHost ?host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q25
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?program rdf:type aut:InstalledProgram ;
           aut:programName ?programName ;
           aut:category ?category ;
           aut:installedDateTime ?installedDateTime ;
           aut:sourceFile ?sourceFile ;
           aut:sourceHost ?host .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?program rdf:type aut:InstalledProgram ;
           aut:programName ?programName .

  FILTER(CONTAINS(STR(?programName), "Chrome"))

  OPTIONAL { ?program aut:category ?category . }
  OPTIONAL { ?program aut:installedDateTime ?installedDateTime . }
  OPTIONAL { ?program aut:sourceFile ?sourceFile . }
  OPTIONAL {
    ?program aut:sourceHost ?host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q26
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
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
         aut:sourceHost ?host .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?email rdf:type aut:EmailMessage ;
         aut-email:subject ?subject .

  FILTER(CONTAINS(LCASE(STR(?subject)), "spreadsheet"))

  OPTIONAL { ?email aut-email:emailFrom ?emailFrom . }
  OPTIONAL { ?email aut-email:emailTo ?emailTo . }
  OPTIONAL { ?email aut-email:messageId ?messageId . }
  OPTIONAL { ?email aut-email:path ?path . }
  OPTIONAL { ?email aut-email:receivedDateTime ?receivedDateTime . }
  OPTIONAL { ?email aut-email:threadId ?threadId . }
  OPTIONAL { ?email aut:category ?category . }
  OPTIONAL { ?email aut:sourceFile ?sourceFile . }
  OPTIONAL {
    ?email aut:sourceHost ?host .
    ?host rdf:type aut:Host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q27
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?item rdf:type aut:RecycleBin ;
        aut:userName ?userName ;
        aut:category ?category ;
        aut:sourceFile ?sourceFile ;
        aut:timeDeleted ?timeDeleted ;
        aut:sourceHost ?host .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  VALUES ?userName { "SPECIFIC_USER" }

  ?item rdf:type aut:RecycleBin ;
        aut:userName ?userName .

  OPTIONAL { ?item aut:category ?category . }
  OPTIONAL { ?item aut:sourceFile ?sourceFile . }
  OPTIONAL { ?item aut:timeDeleted ?timeDeleted . }
  OPTIONAL {
    ?item aut:sourceHost ?host .
    ?host rdf:type aut:Host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q28
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
  ?artefact rdf:type ?artefactType ;
            aut:sourceHost ?host .
  ?artefact ?artefactLiteralProperty ?artefactLiteral .

  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?hostSha1 .
}
WHERE {
  VALUES ?artefactType {
    aut:Account
    aut:EmailMessage
    aut:ExtensionMismatch
    aut:InstalledProgram
    aut:Metadata
    aut:OperatingSystemInformation
    aut:RecentDocument
    aut:RecycleBin
    aut:USBDeviceAttached
    aut:WebBookmark
    aut:WebCookie
    aut:WebHistory
    aut:WebSearch
  }

  ?artefact rdf:type ?artefactType ;
            aut:sourceHost ?host .

  ?host rdf:type aut:Host .

  OPTIONAL {
    VALUES ?artefactLiteralProperty {
      aut-email:emailFrom
      aut-email:emailTo
      aut-email:messageId
      aut-email:path
      aut-email:receivedDateTime
      aut-email:subject
      aut-email:threadId
      aut:accessedDateTime
      aut:accountType
      aut:attachedDateTime
      aut:category
      aut:createdDateTime
      aut:deviceID
      aut:deviceMake
      aut:deviceModel
      aut:domain
      aut:id
      aut:installedDateTime
      aut:modifiedDateTime
      aut:name
      aut:owner
      aut:path
      aut:processorArchitecture
      aut:productID
      aut:programName
      aut:sourceFile
      aut:sourceFileMd5
      aut:sourceMime
      aut:temporaryFilesDirectory
      aut:text
      aut:timeDeleted
      aut:title
      aut:url
      aut:userID
      aut:userName
    }
    ?artefact ?artefactLiteralProperty ?artefactLiteral .
  }

  OPTIONAL {
    ?host aut:hostSha1 ?hostSha1 .
  }
}
```

## Q29
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .

  ?entity rdf:type ?entityType ;
          aut:sourceHost ?host ;
          ?literalProperty ?literal .
}
WHERE {
  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .

  FILTER(LCASE(STR(?hostSha1)) = LCASE("REPLACE_WITH_SHA1_HASH"))

  ?entity rdf:type ?entityType ;
          aut:sourceHost ?host .

  VALUES ?entityType {
    aut:Account
    aut:EmailMessage
    aut:ExtensionMismatch
    aut:InstalledProgram
    aut:Metadata
    aut:OperatingSystemInformation
    aut:RecentDocument
    aut:RecycleBin
    aut:USBDeviceAttached
    aut:WebBookmark
    aut:WebCookie
    aut:WebHistory
    aut:WebSearch
  }

  OPTIONAL {
    VALUES ?literalProperty {
      aut-email:emailFrom
      aut-email:emailTo
      aut-email:messageId
      aut-email:path
      aut-email:receivedDateTime
      aut-email:subject
      aut-email:threadId
      aut:accessedDateTime
      aut:accountType
      aut:attachedDateTime
      aut:category
      aut:createdDateTime
      aut:deviceID
      aut:deviceMake
      aut:deviceModel
      aut:domain
      aut:id
      aut:installedDateTime
      aut:modifiedDateTime
      aut:name
      aut:owner
      aut:path
      aut:processorArchitecture
      aut:productID
      aut:programName
      aut:sourceFile
      aut:sourceFileMd5
      aut:sourceMime
      aut:temporaryFilesDirectory
      aut:text
      aut:timeDeleted
      aut:title
      aut:url
      aut:userID
      aut:userName
    }

    ?entity ?literalProperty ?literal .
    FILTER(ISLITERAL(?literal))
  }
}
```

## Q30
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?entity rdf:type ?entityType ;
          aut:sourceFile ?sourceFile ;
          aut:sourceHost ?host .
  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?hostSha1 .
}
WHERE {
  VALUES ?sourceFile {
    "REPLACE_WITH_PARTICULAR_FILE"
  }

  ?entity rdf:type ?entityType ;
          aut:sourceFile ?sourceFile ;
          aut:sourceHost ?host .

  VALUES ?entityType {
    aut:WebBookmark
    aut:WebSearch
    aut:EmailMessage
    aut:USBDeviceAttached
    aut:ExtensionMismatch
    aut:WebCookie
    aut:Account
    aut:InstalledProgram
    aut:Metadata
    aut:WebHistory
    aut:RecycleBin
    aut:RecentDocument
    aut:OperatingSystemInformation
  }

  ?host rdf:type aut:Host .
  OPTIONAL {
    ?host aut:hostSha1 ?hostSha1 .
  }
}
```

## Q31
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .

  ?account rdf:type aut:Account ;
           aut:sourceHost ?host ;
           aut:id ?accountId ;
           aut:accountType ?accountType ;
           aut:category ?category ;
           aut:sourceFile ?sourceFile .
}
WHERE {
  ?host rdf:type aut:Host .
  ?account rdf:type aut:Account ;
           aut:sourceHost ?host .

  OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  OPTIONAL { ?account aut:id ?accountId . }
  OPTIONAL { ?account aut:accountType ?accountType . }
  OPTIONAL { ?account aut:category ?category . }
  OPTIONAL { ?account aut:sourceFile ?sourceFile . }
}
```

## Q32
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .

  ?operatingSystem rdf:type aut:OperatingSystemInformation ;
                   aut:sourceHost ?host ;
                   aut:name ?operatingSystemName .

  ?account rdf:type aut:Account ;
           aut:sourceHost ?host ;
           aut:id ?accountId ;
           aut:accountType ?accountType ;
           aut:category ?accountCategory ;
           aut:sourceFile ?accountSourceFile .
}
WHERE {
  ?host rdf:type aut:Host .

  ?operatingSystem rdf:type aut:OperatingSystemInformation ;
                   aut:sourceHost ?host ;
                   aut:name ?operatingSystemName .

  ?account rdf:type aut:Account ;
           aut:sourceHost ?host .

  OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  OPTIONAL { ?account aut:id ?accountId . }
  OPTIONAL { ?account aut:accountType ?accountType . }
  OPTIONAL { ?account aut:category ?accountCategory . }
  OPTIONAL { ?account aut:sourceFile ?accountSourceFile . }
}
```

## Q33
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?bookmark rdf:type aut:WebBookmark ;
            aut:domain ?domain ;
            aut:url ?bookmarkUrl ;
            aut:title ?bookmarkTitle ;
            aut:category ?bookmarkCategory ;
            aut:createdDateTime ?bookmarkCreatedDateTime ;
            aut:sourceFile ?bookmarkSourceFile ;
            aut:sourceHost ?bookmarkHost .

  ?bookmarkHost rdf:type aut:Host ;
                aut:hostSha1 ?bookmarkHostSha1 .

  ?history rdf:type aut:WebHistory ;
           aut:domain ?domain ;
           aut:url ?historyUrl ;
           aut:accessedDateTime ?historyAccessedDateTime ;
           aut:category ?historyCategory ;
           aut:sourceFile ?historySourceFile ;
           aut:sourceHost ?historyHost .

  ?historyHost rdf:type aut:Host ;
               aut:hostSha1 ?historyHostSha1 .
}
WHERE {
  ?bookmark rdf:type aut:WebBookmark ;
            aut:domain ?domain .

  ?history rdf:type aut:WebHistory ;
           aut:domain ?domain .

  OPTIONAL { ?bookmark aut:url ?bookmarkUrl . }
  OPTIONAL { ?bookmark aut:title ?bookmarkTitle . }
  OPTIONAL { ?bookmark aut:category ?bookmarkCategory . }
  OPTIONAL { ?bookmark aut:createdDateTime ?bookmarkCreatedDateTime . }
  OPTIONAL { ?bookmark aut:sourceFile ?bookmarkSourceFile . }
  OPTIONAL {
    ?bookmark aut:sourceHost ?bookmarkHost .
    OPTIONAL { ?bookmarkHost aut:hostSha1 ?bookmarkHostSha1 . }
  }

  OPTIONAL { ?history aut:url ?historyUrl . }
  OPTIONAL { ?history aut:accessedDateTime ?historyAccessedDateTime . }
  OPTIONAL { ?history aut:category ?historyCategory . }
  OPTIONAL { ?history aut:sourceFile ?historySourceFile . }
  OPTIONAL {
    ?history aut:sourceHost ?historyHost .
    OPTIONAL { ?historyHost aut:hostSha1 ?historyHostSha1 . }
  }
}
```

## Q34
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?domainSummary rdf:type aut:WebHistory ;
                 aut:domain ?domain ;
                 aut:category ?visitCount .
}
WHERE {
  {
    SELECT ?domain (COUNT(DISTINCT ?visit) AS ?count)
    WHERE {
      ?visit rdf:type aut:WebHistory ;
             aut:domain ?domain .
    }
    GROUP BY ?domain
  }
  BIND(
    IRI(CONCAT("urn:web-history-domain:", ENCODE_FOR_URI(STR(?domain))))
    AS ?domainSummary
  )
  BIND(xsd:string(?count) AS ?visitCount)
}
```

## Q35
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?history rdf:type aut:WebHistory ;
           aut:domain ?domain ;
           aut:url ?url ;
           aut:accessedDateTime ?accessedDateTime ;
           aut:category ?category ;
           aut:sourceFile ?sourceFile ;
           aut:sourceHost ?host .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  {
    SELECT ?domain
    WHERE {
      ?visit rdf:type aut:WebHistory ;
             aut:domain ?domain .
    }
    GROUP BY ?domain
    ORDER BY DESC(COUNT(DISTINCT ?visit)) ?domain
    LIMIT 5
  }

  ?history rdf:type aut:WebHistory ;
           aut:domain ?domain .

  OPTIONAL { ?history aut:url ?url . }
  OPTIONAL { ?history aut:accessedDateTime ?accessedDateTime . }
  OPTIONAL { ?history aut:category ?category . }
  OPTIONAL { ?history aut:sourceFile ?sourceFile . }
  OPTIONAL {
    ?history aut:sourceHost ?host .
    ?host rdf:type aut:Host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q36
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?connection rdf:type aut:WebHistory ;
              aut:url ?url ;
              aut:domain ?address ;
              aut:accessedDateTime ?accessedDateTime ;
              aut:category ?category ;
              aut:sourceFile ?sourceFile ;
              aut:sourceHost ?host .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?connection rdf:type aut:WebHistory .

  OPTIONAL { ?connection aut:url ?url . }
  OPTIONAL { ?connection aut:domain ?address . }
  OPTIONAL { ?connection aut:accessedDateTime ?accessedDateTime . }
  OPTIONAL { ?connection aut:category ?category . }
  OPTIONAL { ?connection aut:sourceFile ?sourceFile . }

  OPTIONAL {
    ?connection aut:sourceHost ?host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q37
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?host rdf:type aut:Host .
  OPTIONAL {
    ?host aut:hostSha1 ?hostSha1 .
  }
}
```

## Q38
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?recycleBin rdf:type aut:RecycleBin ;
              aut:sourceFile ?file ;
              aut:userName ?userName ;
              aut:timeDeleted ?deletionTime ;
              aut:sourceHost ?host .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?recycleBin rdf:type aut:RecycleBin ;
              aut:sourceFile ?file ;
              aut:userName ?userName ;
              aut:timeDeleted ?deletionTime .

  OPTIONAL {
    ?recycleBin aut:sourceHost ?host .
    OPTIONAL {
      ?host aut:hostSha1 ?hostSha1 .
    }
  }
}
```

## Q39
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
  ?alert rdf:type ?alertType ;
         aut:category ?category ;
         ?literalPredicate ?literal .

  ?alert aut:sourceHost ?host .
  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?alert rdf:type ?alertType ;
         aut:category ?category .

  VALUES ?alertType {
    aut:Account
    aut:EmailMessage
    aut:ExtensionMismatch
    aut:InstalledProgram
    aut:Metadata
    aut:OperatingSystemInformation
    aut:RecentDocument
    aut:RecycleBin
    aut:USBDeviceAttached
    aut:WebBookmark
    aut:WebCookie
    aut:WebHistory
    aut:WebSearch
  }

  FILTER(CONTAINS(LCASE(STR(?category)), "antivirus"))

  ?alert ?literalPredicate ?literal .

  VALUES ?literalPredicate {
    aut:accessedDateTime
    aut:accountType
    aut:attachedDateTime
    aut:category
    aut:createdDateTime
    aut:deviceID
    aut:deviceMake
    aut:deviceModel
    aut:domain
    aut:id
    aut:installedDateTime
    aut:modifiedDateTime
    aut:name
    aut:owner
    aut:path
    aut:processorArchitecture
    aut:productID
    aut:programName
    aut:sourceFile
    aut:sourceFileMd5
    aut:sourceMime
    aut:temporaryFilesDirectory
    aut:text
    aut:timeDeleted
    aut:title
    aut:url
    aut:userID
    aut:userName
    aut-email:emailFrom
    aut-email:emailTo
    aut-email:messageId
    aut-email:path
    aut-email:receivedDateTime
    aut-email:subject
    aut-email:threadId
  }

  FILTER(ISLITERAL(?literal))

  OPTIONAL {
    ?alert aut:sourceHost ?host .
    OPTIONAL {
      ?host aut:hostSha1 ?hostSha1 .
    }
  }
}
```

## Q40
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

# The ontology defines no password property, so no password data can be queried.
CONSTRUCT {
}
WHERE {
  ?account rdf:type aut:Account .
  FILTER(false)
}
```

## Q41
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?program rdf:type aut:InstalledProgram ;
           aut:programName ?programName ;
           aut:installedDateTime ?installedDateTime ;
           aut:category ?category ;
           aut:sourceFile ?sourceFile ;
           aut:sourceHost ?host .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?program rdf:type aut:InstalledProgram .

  OPTIONAL { ?program aut:programName ?programName . }
  OPTIONAL { ?program aut:installedDateTime ?installedDateTime . }
  OPTIONAL { ?program aut:category ?category . }
  OPTIONAL { ?program aut:sourceFile ?sourceFile . }
  OPTIONAL {
    ?program aut:sourceHost ?host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q42
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?program rdf:type aut:InstalledProgram ;
           aut:programName ?programName ;
           aut:installedDateTime ?installedDateTime ;
           aut:category ?category ;
           aut:sourceFile ?sourceFile ;
           aut:sourceHost ?host .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?program rdf:type aut:InstalledProgram ;
           aut:sourceHost ?host .

  OPTIONAL { ?program aut:programName ?programName . }
  OPTIONAL { ?program aut:installedDateTime ?installedDateTime . }
  OPTIONAL { ?program aut:category ?category . }
  OPTIONAL { ?program aut:sourceFile ?sourceFile . }
  OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
}
```

## Q43
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?application rdf:type aut:InstalledProgram ;
               aut:programName ?programName ;
               aut:installedDateTime ?installedDateTime ;
               aut:category ?category ;
               aut:sourceFile ?sourceFile ;
               aut:sourceHost ?host .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?application rdf:type aut:InstalledProgram .

  OPTIONAL { ?application aut:programName ?programName . }
  OPTIONAL { ?application aut:installedDateTime ?installedDateTime . }
  OPTIONAL { ?application aut:category ?category . }
  OPTIONAL { ?application aut:sourceFile ?sourceFile . }
  OPTIONAL {
    ?application aut:sourceHost ?host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q44
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?usb rdf:type aut:USBDeviceAttached ;
       aut:attachedDateTime ?attachedDateTime ;
       aut:deviceID ?deviceID ;
       aut:deviceMake ?deviceMake ;
       aut:deviceModel ?deviceModel ;
       aut:category ?category ;
       aut:sourceFile ?sourceFile ;
       aut:sourceHost ?host .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?usb rdf:type aut:USBDeviceAttached .

  OPTIONAL { ?usb aut:attachedDateTime ?attachedDateTime . }
  OPTIONAL { ?usb aut:deviceID ?deviceID . }
  OPTIONAL { ?usb aut:deviceMake ?deviceMake . }
  OPTIONAL { ?usb aut:deviceModel ?deviceModel . }
  OPTIONAL { ?usb aut:category ?category . }
  OPTIONAL { ?usb aut:sourceFile ?sourceFile . }
  OPTIONAL {
    ?usb aut:sourceHost ?host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q45
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?device rdf:type aut:USBDeviceAttached ;
          aut:sourceHost ?host ;
          aut:attachedDateTime ?attachedDateTime ;
          aut:deviceID ?deviceID ;
          aut:deviceMake ?deviceMake ;
          aut:deviceModel ?deviceModel ;
          aut:category ?category ;
          aut:sourceFile ?sourceFile .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?device rdf:type aut:USBDeviceAttached ;
          aut:sourceHost ?host .

  ?host rdf:type aut:Host .

  OPTIONAL { ?device aut:attachedDateTime ?attachedDateTime . }
  OPTIONAL { ?device aut:deviceID ?deviceID . }
  OPTIONAL { ?device aut:deviceMake ?deviceMake . }
  OPTIONAL { ?device aut:deviceModel ?deviceModel . }
  OPTIONAL { ?device aut:category ?category . }
  OPTIONAL { ?device aut:sourceFile ?sourceFile . }
  OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
}
```

## Q46
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?bookmark rdf:type aut:WebBookmark ;
            aut:title ?title ;
            aut:url ?url ;
            aut:domain ?domain ;
            aut:createdDateTime ?createdDateTime ;
            aut:category ?category ;
            aut:sourceFile ?sourceFile ;
            aut:sourceHost ?host .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?bookmark rdf:type aut:WebBookmark .

  OPTIONAL { ?bookmark aut:title ?title . }
  OPTIONAL { ?bookmark aut:url ?url . }
  OPTIONAL { ?bookmark aut:domain ?domain . }
  OPTIONAL { ?bookmark aut:createdDateTime ?createdDateTime . }
  OPTIONAL { ?bookmark aut:category ?category . }
  OPTIONAL { ?bookmark aut:sourceFile ?sourceFile . }
  OPTIONAL {
    ?bookmark aut:sourceHost ?host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q47
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?bookmark rdf:type aut:WebBookmark ;
            aut:title ?title ;
            aut:url ?url ;
            aut:domain ?domain ;
            aut:createdDateTime ?createdDateTime ;
            aut:category ?category ;
            aut:sourceFile ?sourceFile ;
            aut:sourceHost ?host .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?bookmark rdf:type aut:WebBookmark .

  OPTIONAL { ?bookmark aut:title ?title . }
  OPTIONAL { ?bookmark aut:url ?url . }
  OPTIONAL { ?bookmark aut:domain ?domain . }
  OPTIONAL { ?bookmark aut:createdDateTime ?createdDateTime . }
  OPTIONAL { ?bookmark aut:category ?category . }
  OPTIONAL { ?bookmark aut:sourceFile ?sourceFile . }
  OPTIONAL {
    ?bookmark aut:sourceHost ?host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q48
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?search rdf:type aut:WebSearch ;
          aut:text ?text ;
          aut:domain ?domain ;
          aut:category ?category ;
          aut:sourceFile ?sourceFile ;
          aut:sourceHost ?host .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?search rdf:type aut:WebSearch .

  OPTIONAL { ?search aut:text ?text . }
  OPTIONAL { ?search aut:domain ?domain . }
  OPTIONAL { ?search aut:category ?category . }
  OPTIONAL { ?search aut:sourceFile ?sourceFile . }
  OPTIONAL {
    ?search aut:sourceHost ?host .
    ?host rdf:type aut:Host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q49
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?search rdf:type aut:WebSearch ;
          aut:text ?text ;
          aut:domain ?domain ;
          aut:category ?category ;
          aut:sourceFile ?sourceFile ;
          aut:sourceHost ?host .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?search rdf:type aut:WebSearch .

  OPTIONAL { ?search aut:text ?text . }
  OPTIONAL { ?search aut:domain ?domain . }
  OPTIONAL { ?search aut:category ?category . }
  OPTIONAL { ?search aut:sourceFile ?sourceFile . }
  OPTIONAL {
    ?search aut:sourceHost ?host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q50
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
  ?email rdf:type aut:EmailMessage ;
         aut-email:emailFrom ?emailFrom ;
         aut-email:emailTo ?emailTo ;
         aut-email:messageId ?messageId ;
         aut-email:path ?path ;
         aut-email:receivedDateTime ?receivedDateTime ;
         aut-email:subject ?subject ;
         aut-email:threadId ?threadId ;
         aut:category ?category ;
         aut:sourceFile ?sourceFile ;
         aut:sourceHost ?host .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?email rdf:type aut:EmailMessage .

  OPTIONAL { ?email aut-email:emailFrom ?emailFrom . }
  OPTIONAL { ?email aut-email:emailTo ?emailTo . }
  OPTIONAL { ?email aut-email:messageId ?messageId . }
  OPTIONAL { ?email aut-email:path ?path . }
  OPTIONAL { ?email aut-email:receivedDateTime ?receivedDateTime . }
  OPTIONAL { ?email aut-email:subject ?subject . }
  OPTIONAL { ?email aut-email:threadId ?threadId . }
  OPTIONAL { ?email aut:category ?category . }
  OPTIONAL { ?email aut:sourceFile ?sourceFile . }
  OPTIONAL {
    ?email aut:sourceHost ?host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q51
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
  ?message rdf:type aut:EmailMessage ;
           aut-email:emailFrom ?emailFrom ;
           aut-email:emailTo ?emailTo ;
           aut-email:messageId ?messageId ;
           aut-email:path ?emailPath ;
           aut-email:receivedDateTime ?receivedDateTime ;
           aut-email:subject ?subject ;
           aut-email:threadId ?threadId ;
           aut:category ?category ;
           aut:sourceFile ?sourceFile ;
           aut:sourceHost ?host .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?message rdf:type aut:EmailMessage .

  OPTIONAL { ?message aut-email:emailFrom ?emailFrom . }
  OPTIONAL { ?message aut-email:emailTo ?emailTo . }
  OPTIONAL { ?message aut-email:messageId ?messageId . }
  OPTIONAL { ?message aut-email:path ?emailPath . }
  OPTIONAL { ?message aut-email:receivedDateTime ?receivedDateTime . }
  OPTIONAL { ?message aut-email:subject ?subject . }
  OPTIONAL { ?message aut-email:threadId ?threadId . }
  OPTIONAL { ?message aut:category ?category . }
  OPTIONAL { ?message aut:sourceFile ?sourceFile . }
  OPTIONAL {
    ?message aut:sourceHost ?host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```
