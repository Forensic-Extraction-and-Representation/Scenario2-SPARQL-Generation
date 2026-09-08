# Generated queries --- grounded / gpt-oss-20b-local

## Q1
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
  ?account a aut:Account ;
           aut:id ?id ;
           aut:accountType ?accType ;
           aut:category ?cat ;
           aut:sourceFile ?srcFile ;
           aut:sourceHost ?host .

  ?host a aut:Host ;
        aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?account a aut:Account .

  OPTIONAL { ?account aut:id ?id } .
  OPTIONAL { ?account aut:accountType ?accType } .
  OPTIONAL { ?account aut:category ?cat } .
  OPTIONAL { ?account aut:sourceFile ?srcFile } .
  OPTIONAL {
    ?account aut:sourceHost ?host .
    ?host a aut:Host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 } .
  } .
}
```

## Q2
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
  ?acct rdf:type aut:Account ;
        aut:accountType ?atype ;
        aut:id ?aid .
}
WHERE {
  ?acct rdf:type aut:Account .
  OPTIONAL { ?acct aut:accountType ?atype } .
  OPTIONAL { ?acct aut:id ?aid } .
}
```

## Q3
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?program rdf:type aut:InstalledProgram .
  ?program aut:installedDateTime ?instDt .
  ?program aut:programName ?progName .
  ?program aut:category ?cat .
  ?program aut:sourceFile ?srcFile .
  ?program aut:sourceHost ?host .
  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?program a aut:InstalledProgram .
  OPTIONAL { ?program aut:installedDateTime ?instDt . }
  OPTIONAL { ?program aut:programName ?progName . }
  OPTIONAL { ?program aut:category ?cat . }
  OPTIONAL { ?program aut:sourceFile ?srcFile . }
  OPTIONAL {
    ?program aut:sourceHost ?host .
    ?host a aut:Host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q4
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>.
PREFIX owl: <http://www.w3.org/2002/07/owl#>.
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>.

CONSTRUCT {
  ?prog a aut:InstalledProgram ;
        aut:programName ?name ;
        aut:installedDateTime ?instDate .
}
WHERE {
  ?prog a aut:InstalledProgram ;
        aut:programName ?name ;
        aut:installedDateTime ?instDate .
}
```

## Q5
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?usb rdf:type aut:USBDeviceAttached .
  ?usb aut:deviceID ?deviceID .
  ?usb aut:deviceMake ?deviceMake .
  ?usb aut:deviceModel ?deviceModel .
  ?usb aut:attachedDateTime ?attachedDateTime .
  ?usb aut:category ?category .
  ?usb aut:sourceFile ?sourceFile .
  ?usb aut:sourceHost ?host .
  
  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?usb rdf:type aut:USBDeviceAttached .
  
  OPTIONAL { ?usb aut:deviceID ?deviceID } .
  OPTIONAL { ?usb aut:deviceMake ?deviceMake } .
  OPTIONAL { ?usb aut:deviceModel ?deviceModel } .
  OPTIONAL { ?usb aut:attachedDateTime ?attachedDateTime } .
  OPTIONAL { ?usb aut:category ?category } .
  OPTIONAL { ?usb aut:sourceFile ?sourceFile } .
  OPTIONAL {
    ?usb aut:sourceHost ?host .
    ?host rdf:type aut:Host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 } .
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
PREFIX xml: <http://www.w3.org/XML/1998/namespace>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
  ?device rdf:type aut:USBDeviceAttached ;
          aut:deviceID ?deviceID ;
          aut:deviceMake ?deviceMake ;
          aut:deviceModel ?deviceModel .
}
WHERE {
  ?device rdf:type aut:USBDeviceAttached ;
          aut:deviceID ?deviceID ;
          aut:deviceMake ?deviceMake ;
          aut:deviceModel ?deviceModel .
}
```

## Q7
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX xml: <http://www.w3.org/XML/1998/namespace>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
  ?os rdf:type aut:OperatingSystemInformation .
  ?os aut:name ?name .
  ?os aut:owner ?owner .
  ?os aut:path ?path .
  ?os aut:processorArchitecture ?processorArch .
  ?os aut:productID ?productID .
  ?os aut:temporaryFilesDirectory ?tmpDir .
  ?os aut:programName ?programName .
  ?os aut:sourceFile ?srcFile .
  ?os aut:sourceHost ?host .

  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?sha1 .
}
WHERE {
  ?os rdf:type aut:OperatingSystemInformation .

  OPTIONAL { ?os aut:name ?name . }
  OPTIONAL { ?os aut:owner ?owner . }
  OPTIONAL { ?os aut:path ?path . }
  OPTIONAL { ?os aut:processorArchitecture ?processorArch . }
  OPTIONAL { ?os aut:productID ?productID . }
  OPTIONAL { ?os aut:temporaryFilesDirectory ?tmpDir . }
  OPTIONAL { ?os aut:programName ?programName . }
  OPTIONAL { ?os aut:sourceFile ?srcFile . }
  OPTIONAL { ?os aut:sourceHost ?host . }
  OPTIONAL { ?host rdf:type aut:Host . }
  OPTIONAL { ?host aut:hostSha1 ?sha1 . }
}
```

## Q8
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX xml: <http://www.w3.org/XML/1998/namespace>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
  ?os rdf:type aut:OperatingSystemInformation .
  ?os aut:name ?name .
  ?os aut:productID ?pid .
  ?os aut:processorArchitecture ?arch .
  ?os aut:owner ?owner .
}
WHERE {
  ?os a aut:OperatingSystemInformation .
  OPTIONAL { ?os aut:name ?name . }
  OPTIONAL { ?os aut:productID ?pid . }
  OPTIONAL { ?os aut:processorArchitecture ?arch . }
  OPTIONAL { ?os aut:owner ?owner . }
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
  ?doc rdf:type aut:RecentDocument .
  ?doc aut:accessedDateTime ?accessedDateTime .
  ?doc aut:category ?category .
  ?doc aut:path ?path .
  ?doc aut:sourceFile ?sourceFile .
  ?doc aut:sourceMime ?sourceMime .
  ?doc aut:sourceFileMd5 ?sourceFileMd5 .
  ?doc aut:sourceHost ?host .
  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?doc rdf:type aut:RecentDocument .
  OPTIONAL { ?doc aut:accessedDateTime ?accessedDateTime . }
  OPTIONAL { ?doc aut:category ?category . }
  OPTIONAL { ?doc aut:path ?path . }
  OPTIONAL { ?doc aut:sourceFile ?sourceFile . }
  OPTIONAL { ?doc aut:sourceMime ?sourceMime . }
  OPTIONAL { ?doc aut:sourceFileMd5 ?sourceFileMd5 . }
  OPTIONAL {
    ?doc aut:sourceHost ?host .
    ?host rdf:type aut:Host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q10
```sparql
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>

CONSTRUCT {
  ?doc rdf:type aut:RecentDocument .
  ?doc aut:path ?path .
  ?doc aut:accessedDateTime ?access .
}
WHERE {
  ?doc rdf:type aut:RecentDocument .
  ?doc aut:path ?path .
  ?doc aut:accessedDateTime ?access .
}
```

## Q11
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?b rdf:type aut:WebBookmark .
  ?b aut:title ?t .
  ?b aut:url ?u .
}
WHERE {
  ?b rdf:type aut:WebBookmark .
  OPTIONAL { ?b aut:title ?t . }
  OPTIONAL { ?b aut:url ?u . }
}
```

## Q12
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?cookie rdf:type aut:WebCookie .
  ?cookie aut:name ?name .
  ?cookie aut:domain ?domain .
  ?cookie aut:url ?url .
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
  ?history a aut:WebHistory ;
           aut:url ?url ;
           aut:accessedDateTime ?accessed ;
           aut:domain ?domain ;
           aut:sourceHost ?host .
  ?host a aut:Host ;
        aut:hostSha1 ?sha1 .
}
WHERE {
  ?history a aut:WebHistory ;
           aut:url ?url ;
           aut:accessedDateTime ?accessed .
  OPTIONAL { ?history aut:domain ?domain . }
  OPTIONAL {
    ?history aut:sourceHost ?host .
    ?host a aut:Host ;
          aut:hostSha1 ?sha1 .
  }
}
```

## Q14
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX xml: <http://www.w3.org/XML/1998/namespace>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
  ?search a aut:WebSearch ;
          aut:text ?text ;
          aut:sourceFile ?srcFile ;
          aut:sourceHost ?host .
  ?host a aut:Host .
}
WHERE {
  ?search a aut:WebSearch .
  ?search aut:text ?text .
  OPTIONAL { ?search aut:sourceFile ?srcFile } .
  OPTIONAL { ?search aut:sourceHost ?host } .
}
```

## Q15
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
  ?rb rdf:type aut:RecycleBin .
  ?rb aut:userName ?userName .
  ?rb aut:timeDeleted ?timeDeleted .
  ?rb aut:category ?category .
  ?rb aut:sourceFile ?sourceFile .
  ?rb aut:sourceHost ?host .
  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?rb a aut:RecycleBin .
  OPTIONAL { ?rb aut:userName ?userName . }
  OPTIONAL { ?rb aut:timeDeleted ?timeDeleted . }
  OPTIONAL { ?rb aut:category ?category . }
  OPTIONAL { ?rb aut:sourceFile ?sourceFile . }
  OPTIONAL {
    ?rb aut:sourceHost ?host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
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
  ?msg a aut:EmailMessage .
  ?msg aut-email:emailFrom ?from .
  ?msg aut-email:emailTo ?to .
  ?msg aut-email:subject ?subj .
}
WHERE {
  ?msg a aut:EmailMessage .
  OPTIONAL { ?msg aut-email:emailFrom ?from . }
  OPTIONAL { ?msg aut-email:emailTo ?to . }
  OPTIONAL { ?msg aut-email:subject ?subj . }
}
```

## Q17
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#> .

CONSTRUCT {
  ?ext a aut:ExtensionMismatch ;
       aut:category ?cat ;
       aut:sourceFile ?srcFile ;
       aut:sourceFileMd5 ?srcMd5 ;
       aut:sourceHost ?host .

  ?host a aut:Host ;
        aut:hostSha1 ?sha1 .
}
WHERE {
  ?ext a aut:ExtensionMismatch .
  OPTIONAL { ?ext aut:category ?cat . }
  OPTIONAL { ?ext aut:sourceFile ?srcFile . }
  OPTIONAL { ?ext aut:sourceFileMd5 ?srcMd5 . }
  OPTIONAL {
    ?ext aut:sourceHost ?host .
    ?host a aut:Host .
    OPTIONAL { ?host aut:hostSha1 ?sha1 . }
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
PREFIX xml: <http://www.w3.org/XML/1998/namespace>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
  ?meta rdf:type aut:Metadata ;
        aut:sourceFile ?src ;
        aut:createdDateTime ?created ;
        aut:modifiedDateTime ?modified .
}
WHERE {
  ?meta a aut:Metadata ;
        aut:sourceFile ?src ;
        aut:createdDateTime ?created ;
        aut:modifiedDateTime ?modified .
}
```

## Q19
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

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
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
  ?doc rdf:type aut:RecentDocument .
  ?doc aut:accessedDateTime ?dt .
  ?doc aut:path ?path .
  ?doc aut:sourceFile ?srcFile .
  ?doc aut:sourceFileMd5 ?srcMd5 .
  ?doc aut:sourceMime ?mime .
  ?doc aut:category ?cat .
  ?doc aut:sourceHost ?host .

  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?sha .
}
WHERE {
  ?doc rdf:type aut:RecentDocument .
  ?doc aut:accessedDateTime ?dt .
  FILTER( ?dt > "2008-07-01T00:00:00"^^xsd:dateTime ) .

  OPTIONAL { ?doc aut:path ?path . }
  OPTIONAL { ?doc aut:sourceFile ?srcFile . }
  OPTIONAL { ?doc aut:sourceFileMd5 ?srcMd5 . }
  OPTIONAL { ?doc aut:sourceMime ?mime . }
  OPTIONAL { ?doc aut:category ?cat . }
  OPTIONAL { 
    ?doc aut:sourceHost ?host .
    ?host rdf:type aut:Host .
    OPTIONAL { ?host aut:hostSha1 ?sha . }
  }
}
```

## Q21
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
  ?wh a aut:WebHistory .
  ?wh aut:url ?url .
  ?wh aut:domain ?domain .
  ?wh aut:accessedDateTime ?accessed .
  ?wh aut:sourceFile ?sourceFile .
  ?wh aut:sourceHost ?host .
  ?wh aut:category ?category .
  ?host a aut:Host .
  ?host aut:hostSha1 ?sha1 .
}
WHERE {
  ?wh a aut:WebHistory .
  ?wh aut:domain "mail.google.com" .
  OPTIONAL { ?wh aut:url ?url } .
  OPTIONAL { ?wh aut:accessedDateTime ?accessed } .
  OPTIONAL { ?wh aut:sourceFile ?sourceFile } .
  OPTIONAL { ?wh aut:sourceHost ?host } .
  OPTIONAL { ?wh aut:category ?category } .
  OPTIONAL { ?host a aut:Host } .
  OPTIONAL { ?host aut:hostSha1 ?sha1 } .
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
  ?search a aut:WebSearch ;
          aut:text ?txt ;
          aut:category ?cat ;
          aut:sourceFile ?sf ;
          aut:sourceHost ?host .
  
  ?host a aut:Host ;
        aut:hostSha1 ?sha .
}
WHERE {
  ?search a aut:WebSearch ;
          aut:text ?txt .
  
  OPTIONAL { ?search aut:category ?cat . }
  OPTIONAL { ?search aut:sourceFile ?sf . }
  
  OPTIONAL {
    ?search aut:sourceHost ?host .
    ?host a aut:Host ;
          aut:hostSha1 ?sha .
  }
  
  FILTER regex(?txt, "spreadsheet", "i") .
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
  ?doc rdf:type aut:RecentDocument ;
       aut:path ?path ;
       aut:accessedDateTime ?at ;
       aut:sourceFile ?srcFile ;
       aut:sourceFileMd5 ?srcMd5 ;
       aut:sourceMime ?srcMime ;
       aut:sourceHost ?host .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?sha1 .
}
WHERE {
  ?doc rdf:type aut:RecentDocument ;
       aut:path ?path .
  OPTIONAL { ?doc aut:accessedDateTime ?at . }
  OPTIONAL { ?doc aut:sourceFile ?srcFile . }
  OPTIONAL { ?doc aut:sourceFileMd5 ?srcMd5 . }
  OPTIONAL { ?doc aut:sourceMime ?srcMime . }
  OPTIONAL {
    ?doc aut:sourceHost ?host .
    ?host rdf:type aut:Host .
    OPTIONAL { ?host aut:hostSha1 ?sha1 . }
  }
  FILTER regex(?path, "Downloads", "i") .
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
  ?usb rdf:type aut:USBDeviceAttached ;
       aut:attachedDateTime ?attached ;
       aut:deviceID ?id ;
       aut:deviceMake ?make ;
       aut:deviceModel ?model ;
       aut:sourceHost ?host ;
       aut:sourceFile ?srcFile .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?sha1 .
}
WHERE {
  ?usb rdf:type aut:USBDeviceAttached ;
       aut:attachedDateTime ?attached ;
       aut:deviceID ?id ;
       aut:deviceMake ?make ;
       aut:deviceModel ?model ;
       aut:sourceHost ?host ;
       aut:sourceFile ?srcFile .

  ?host rdf:type aut:Host ;
        aut:hostSha1 ?sha1 .

  FILTER ( ?attached > "2008-07-01T00:00:00"^^xsd:dateTime )
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
  ?p rdf:type aut:InstalledProgram .
  ?p aut:programName ?name .
  ?p aut:installedDateTime ?installDate .
  ?p aut:sourceHost ?host .
  ?host rdf:type aut:Host .
}
WHERE {
  ?p a aut:InstalledProgram .
  ?p aut:programName ?name .
  OPTIONAL { ?p aut:installedDateTime ?installDate . }
  OPTIONAL { ?p aut:sourceHost ?host . }
  OPTIONAL { ?host a aut:Host . }
  FILTER regex(?name, "Chrome", "i")
}
```

## Q26
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
  ?e a aut:EmailMessage .
  ?e aut-email:emailFrom ?from .
  ?e aut-email:emailTo ?to .
  ?e aut-email:messageId ?mid .
  ?e aut-email:path ?path .
  ?e aut-email:receivedDateTime ?rdt .
  ?e aut-email:subject ?subj .
  ?e aut-email:threadId ?tid .
  ?e aut-email:sourceFile ?src .
  ?e aut:sourceHost ?host .
}
WHERE {
  ?e a aut:EmailMessage .
  OPTIONAL { ?e aut-email:emailFrom ?from } .
  OPTIONAL { ?e aut-email:emailTo ?to } .
  OPTIONAL { ?e aut-email:messageId ?mid } .
  OPTIONAL { ?e aut-email:path ?path } .
  OPTIONAL { ?e aut-email:receivedDateTime ?rdt } .
  OPTIONAL { ?e aut-email:subject ?subj } .
  OPTIONAL { ?e aut-email:threadId ?tid } .
  OPTIONAL { ?e aut-email:sourceFile ?src } .
  OPTIONAL { ?e aut:sourceHost ?host } .
  FILTER regex(?subj, "spreadsheet", "i") .
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
  ?item rdf:type aut:RecycleBin .
  ?item aut:timeDeleted ?timeDeleted .
  ?item aut:userName ?userName .
  ?item aut:sourceFile ?srcFile .
  ?item aut:sourceHost ?host .
  
  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?sha1 .
  ?host aut:sourceFile ?hostSrcFile .
}
WHERE {
  ?item rdf:type aut:RecycleBin .
  ?item aut:timeDeleted ?timeDeleted .
  ?item aut:userName ?userName .
  OPTIONAL { ?item aut:sourceFile ?srcFile . }
  OPTIONAL {
    ?item aut:sourceHost ?host .
    ?host rdf:type aut:Host .
    OPTIONAL { ?host aut:hostSha1 ?sha1 . }
    OPTIONAL { ?host aut:sourceFile ?hostSrcFile . }
  }
  FILTER (?userName = "specificUser") .
}
```

## Q28
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>.
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>.
PREFIX owl: <http://www.w3.org/2002/07/owl#>.
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>.
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>.

CONSTRUCT {
  # Artefact entity
  ?artefact a ?type .
  ?artefact aut:sourceHost ?host .

  # Artefact literals
  ?artefact aut:category ?category .
  ?artefact aut:createdDateTime ?created .
  ?artefact aut:deviceID ?deviceID .
  ?artefact aut:deviceMake ?deviceMake .
  ?artefact aut:deviceModel ?deviceModel .
  ?artefact aut:domain ?domain .
  ?artefact aut:id ?id .
  ?artefact aut:installedDateTime ?instDate .
  ?artefact aut:modifiedDateTime ?modDate .
  ?artefact aut:name ?name .
  ?artefact aut:owner ?owner .
  ?artefact aut:path ?path .
  ?artefact aut:processorArchitecture ?procArch .
  ?artefact aut:productID ?prodID .
  ?artefact aut:programName ?progName .
  ?artefact aut:sourceFile ?srcFile .
  ?artefact aut:sourceFileMd5 ?srcMd5 .
  ?artefact aut:sourceMime ?srcMime .
  ?artefact aut:temporaryFilesDirectory ?tempDir .
  ?artefact aut:text ?text .
  ?artefact aut:timeDeleted ?timeDel .
  ?artefact aut:title ?title .
  ?artefact aut:url ?url .
  ?artefact aut:userID ?userID .
  ?artefact aut:userName ?userName .
  ?artefact aut:accessedDateTime ?accessDT .
  ?artefact aut:attachedDateTime ?attachDT .

  # Email-specific literals
  ?artefact aut-email:emailFrom ?emailFrom .
  ?artefact aut-email:emailTo ?emailTo .
  ?artefact aut-email:messageId ?msgId .
  ?artefact aut-email:path ?emailPath .
  ?artefact aut-email:receivedDateTime ?recDate .
  ?artefact aut-email:subject ?subject .
  ?artefact aut-email:threadId ?threadId .

  # Host entity
  ?host a aut:Host .
  ?host aut:hostSha1 ?hostSha1 .
} WHERE {
  ?artefact a ?type .
  ?artefact aut:sourceHost ?host .
  ?host a aut:Host .

  OPTIONAL { ?artefact aut:category ?category . }
  OPTIONAL { ?artefact aut:createdDateTime ?created . }
  OPTIONAL { ?artefact aut:deviceID ?deviceID . }
  OPTIONAL { ?artefact aut:deviceMake ?deviceMake . }
  OPTIONAL { ?artefact aut:deviceModel ?deviceModel . }
  OPTIONAL { ?artefact aut:domain ?domain . }
  OPTIONAL { ?artefact aut:id ?id . }
  OPTIONAL { ?artefact aut:installedDateTime ?instDate . }
  OPTIONAL { ?artefact aut:modifiedDateTime ?modDate . }
  OPTIONAL { ?artefact aut:name ?name . }
  OPTIONAL { ?artefact aut:owner ?owner . }
  OPTIONAL { ?artefact aut:path ?path . }
  OPTIONAL { ?artefact aut:processorArchitecture ?procArch . }
  OPTIONAL { ?artefact aut:productID ?prodID . }
  OPTIONAL { ?artefact aut:programName ?progName . }
  OPTIONAL { ?artefact aut:sourceFile ?srcFile . }
  OPTIONAL { ?artefact aut:sourceFileMd5 ?srcMd5 . }
  OPTIONAL { ?artefact aut:sourceMime ?srcMime . }
  OPTIONAL { ?artefact aut:temporaryFilesDirectory ?tempDir . }
  OPTIONAL { ?artefact aut:text ?text . }
  OPTIONAL { ?artefact aut:timeDeleted ?timeDel . }
  OPTIONAL { ?artefact aut:title ?title . }
  OPTIONAL { ?artefact aut:url ?url . }
  OPTIONAL { ?artefact aut:userID ?userID . }
  OPTIONAL { ?artefact aut:userName ?userName . }
  OPTIONAL { ?artefact aut:accessedDateTime ?accessDT . }
  OPTIONAL { ?artefact aut:attachedDateTime ?attachDT . }

  OPTIONAL { ?artefact aut-email:emailFrom ?emailFrom . }
  OPTIONAL { ?artefact aut-email:emailTo ?emailTo . }
  OPTIONAL { ?artefact aut-email:messageId ?msgId . }
  OPTIONAL { ?artefact aut-email:path ?emailPath . }
  OPTIONAL { ?artefact aut-email:receivedDateTime ?recDate . }
  OPTIONAL { ?artefact aut-email:subject ?subject . }
  OPTIONAL { ?artefact aut-email:threadId ?threadId . }

  OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
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
  # Host itself
  ?host rdf:type aut:Host ;
        aut:hostSha1 ?sha1 ;
        rdf:type aut:Host .

  # All entities found on the host
  ?e rdf:type ?etype ;
     aut:sourceHost ?host ;
     aut:accountType ?accountType ;
     aut:accessedDateTime ?accessedDateTime ;
     aut:attachedDateTime ?attachedDateTime ;
     aut:category ?category ;
     aut:createdDateTime ?createdDateTime ;
     aut:deviceID ?deviceID ;
     aut:deviceMake ?deviceMake ;
     aut:deviceModel ?deviceModel ;
     aut:domain ?domain ;
     aut:hostSha1 ?hostSha1 ;
     aut:id ?id ;
     aut:installedDateTime ?installedDateTime ;
     aut:modifiedDateTime ?modifiedDateTime ;
     aut:name ?name ;
     aut:owner ?owner ;
     aut:path ?path ;
     aut:processorArchitecture ?processorArchitecture ;
     aut:productID ?productID ;
     aut:programName ?programName ;
     aut:sourceFile ?sourceFile ;
     aut:sourceFileMd5 ?sourceFileMd5 ;
     aut:sourceMime ?sourceMime ;
     aut:temporaryFilesDirectory ?temporaryFilesDirectory ;
     aut:text ?text ;
     aut:timeDeleted ?timeDeleted ;
     aut:title ?title ;
     aut:url ?url ;
     aut:userID ?userID ;
     aut:userName ?userName ;
     aut-email:emailFrom ?emailFrom ;
     aut-email:emailTo ?emailTo ;
     aut-email:messageId ?messageId ;
     aut-email:path ?emailPath ;
     aut-email:receivedDateTime ?receivedDateTime ;
     aut-email:subject ?subject ;
     aut-email:threadId ?threadId .
}
WHERE {
  # Identify the host by its SHA‑1 hash
  ?host rdf:type aut:Host ;
        aut:hostSha1 ?sha1 .
  FILTER (?sha1 = "HASHVALUE") .

  # Find all entities that were sourced from this host
  ?e aut:sourceHost ?host ;
     rdf:type ?etype .

  OPTIONAL { ?e aut:accountType ?accountType } .
  OPTIONAL { ?e aut:accessedDateTime ?accessedDateTime } .
  OPTIONAL { ?e aut:attachedDateTime ?attachedDateTime } .
  OPTIONAL { ?e aut:category ?category } .
  OPTIONAL { ?e aut:createdDateTime ?createdDateTime } .
  OPTIONAL { ?e aut:deviceID ?deviceID } .
  OPTIONAL { ?e aut:deviceMake ?deviceMake } .
  OPTIONAL { ?e aut:deviceModel ?deviceModel } .
  OPTIONAL { ?e aut:domain ?domain } .
  OPTIONAL { ?e aut:hostSha1 ?hostSha1 } .
  OPTIONAL { ?e aut:id ?id } .
  OPTIONAL { ?e aut:installedDateTime ?installedDateTime } .
  OPTIONAL { ?e aut:modifiedDateTime ?modifiedDateTime } .
  OPTIONAL { ?e aut:name ?name } .
  OPTIONAL { ?e aut:owner ?owner } .
  OPTIONAL { ?e aut:path ?path } .
  OPTIONAL { ?e aut:processorArchitecture ?processorArchitecture } .
  OPTIONAL { ?e aut:productID ?productID } .
  OPTIONAL { ?e aut:programName ?programName } .
  OPTIONAL { ?e aut:sourceFile ?sourceFile } .
  OPTIONAL { ?e aut:sourceFileMd5 ?sourceFileMd5 } .
  OPTIONAL { ?e aut:sourceMime ?sourceMime } .
  OPTIONAL { ?e aut:temporaryFilesDirectory ?temporaryFilesDirectory } .
  OPTIONAL { ?e aut:text ?text } .
  OPTIONAL { ?e aut:timeDeleted ?timeDeleted } .
  OPTIONAL { ?e aut:title ?title } .
  OPTIONAL { ?e aut:url ?url } .
  OPTIONAL { ?e aut:userID ?userID } .
  OPTIONAL { ?e aut:userName ?userName } .
  OPTIONAL { ?e aut-email:emailFrom ?emailFrom } .
  OPTIONAL { ?e aut-email:emailTo ?emailTo } .
  OPTIONAL { ?e aut-email:messageId ?messageId } .
  OPTIONAL { ?e aut-email:path ?emailPath } .
  OPTIONAL { ?e aut-email:receivedDateTime ?receivedDateTime } .
  OPTIONAL { ?e aut-email:subject ?subject } .
  OPTIONAL { ?e aut-email:threadId ?threadId } .
}
```

## Q30
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
  ?file a ?fileType .
  ?file aut:sourceFile ?srcFile .
  OPTIONAL { ?file aut:path ?path . }
  OPTIONAL { ?file aut:sourceMime ?mime . }
  ?file aut:sourceHost ?host .
  ?host a aut:Host .
  ?host aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?file a ?fileType .
  FILTER (?fileType IN (aut:WebBookmark, aut:WebSearch, aut:EmailMessage, aut:USBDeviceAttached, aut:ExtensionMismatch, aut:WebCookie, aut:Account, aut:InstalledProgram, aut:Metadata, aut:WebHistory, aut:RecycleBin, aut:RecentDocument, aut:OperatingSystemInformation)) .
  ?file aut:sourceFile ?srcFile .
  OPTIONAL { ?file aut:path ?path . }
  OPTIONAL { ?file aut:sourceMime ?mime . }
  ?file aut:sourceHost ?host .
  ?host a aut:Host .
  ?host aut:hostSha1 ?hostSha1 .
}
```

## Q31
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
  # Host entity and its literals
  ?host a aut:Host .
  ?host aut:hostSha1 ?hostSha1 .
  ?host aut:sourceFile ?hostSource .

  # Account entity and its literals
  ?account a aut:Account .
  ?account aut:id ?accountId .
  ?account aut:accountType ?accountType .
  # Relationship between account and host
  ?account aut:sourceHost ?host .
}
WHERE {
  # Find all hosts
  ?host a aut:Host .
  OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  OPTIONAL { ?host aut:sourceFile ?hostSource . }

  # Find all accounts linked to those hosts
  ?account a aut:Account .
  ?account aut:sourceHost ?host .
  OPTIONAL { ?account aut:id ?accountId . }
  OPTIONAL { ?account aut:accountType ?accountType . }
}
```

## Q32
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?hostSha1 .

  ?os rdf:type aut:OperatingSystemInformation .
  ?os aut:name ?osName .
  ?os aut:sourceHost ?host .

  ?account rdf:type aut:Account .
  ?account aut:id ?accountId .
  ?account aut:accountType ?accountType .
  ?account aut:sourceHost ?host .
}
WHERE {
  ?host a aut:Host ;
        aut:hostSha1 ?hostSha1 .

  ?os a aut:OperatingSystemInformation ;
      aut:name ?osName ;
      aut:sourceHost ?host .

  ?account a aut:Account ;
           aut:id ?accountId ;
           aut:accountType ?accountType ;
           aut:sourceHost ?host .
}
```

## Q33
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?b rdf:type aut:WebBookmark ;
     aut:domain ?d ;
     aut:url ?urlB ;
     aut:createdDateTime ?createdB .
  ?h rdf:type aut:WebHistory ;
     aut:domain ?d ;
     aut:url ?urlH ;
     aut:accessedDateTime ?accessedH .
}
WHERE {
  ?b rdf:type aut:WebBookmark ;
     aut:domain ?d ;
     aut:url ?urlB .
  OPTIONAL { ?b aut:createdDateTime ?createdB . }
  ?h rdf:type aut:WebHistory ;
     aut:domain ?d ;
     aut:url ?urlH .
  OPTIONAL { ?h aut:accessedDateTime ?accessedH . }
}
```

## Q34
```sparql
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>

CONSTRUCT {
  ?domainRes a aut:WebHistory ;
             aut:domain ?domain ;
             aut:category ?count .
}
WHERE {
  {
    SELECT ?domain (COUNT(?wh) AS ?count)
    WHERE {
      ?wh a aut:WebHistory ;
          aut:domain ?domain .
    }
    GROUP BY ?domain
  }
  BIND (BNODE() AS ?domainRes)
}
```

## Q35
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?d rdf:type aut:WebHistory .
  ?d aut:domain ?domain .
}
WHERE {
  {
    SELECT ?domain (COUNT(?wh) AS ?cnt)
    WHERE {
      ?wh a aut:WebHistory .
      ?wh aut:domain ?domain .
    }
    GROUP BY ?domain
    ORDER BY DESC(?cnt)
    LIMIT 5
  }
  BIND (BNODE() AS ?d)
}
```

## Q36
```sparql
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>

CONSTRUCT {
  # Host entity and its identifying literal
  ?host a aut:Host .
  OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }

  # Web history entity (representing a network contact)
  ?entity a aut:WebHistory .
  ?entity aut:url ?url .
  OPTIONAL { ?entity aut:domain ?domain . }

  # Link the host to the URL it contacted
  ?entity aut:sourceHost ?host .
}
WHERE {
  ?entity a aut:WebHistory .
  ?entity aut:url ?url .
  ?entity aut:sourceHost ?host .
  ?host a aut:Host .
}
```

## Q37
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

## Q38
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>

CONSTRUCT {
  ?rb rdf:type aut:RecycleBin .
  ?rb aut:sourceFile ?file .
  ?rb aut:userName ?user .
  ?rb aut:timeDeleted ?time .
}
WHERE {
  ?rb a aut:RecycleBin .
  ?rb aut:sourceFile ?file .
  ?rb aut:userName ?user .
  ?rb aut:timeDeleted ?time .
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
  ?alert a aut:ExtensionMismatch .
  ?alert aut:category ?cat .
  ?alert aut:sourceFile ?srcFile .
  ?alert aut:sourceFileMd5 ?srcMd5 .
  ?alert aut:sourceHost ?host .
  ?host a aut:Host .
  ?host aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?alert a aut:ExtensionMismatch .
  OPTIONAL { ?alert aut:category ?cat . }
  OPTIONAL { ?alert aut:sourceFile ?srcFile . }
  OPTIONAL { ?alert aut:sourceFileMd5 ?srcMd5 . }
  OPTIONAL {
    ?alert aut:sourceHost ?host .
    ?host a aut:Host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```

## Q40
```sparql
CONSTRUCT` query could be written to return the password. Until such a property is defined, the request cannot be fulfilled.
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
  ?program a aut:InstalledProgram ;  
           aut:programName ?pName ;  
           aut:installedDateTime ?iDate ;  
           aut:category ?cat ;  
           aut:sourceFile ?srcFile ;  
           aut:sourceHost ?host .  
  ?host a aut:Host ;  
        aut:hostSha1 ?sha .  
}  
WHERE {  
  ?program a aut:InstalledProgram .  
  OPTIONAL { ?program aut:programName ?pName . }  
  OPTIONAL { ?program aut:installedDateTime ?iDate . }  
  OPTIONAL { ?program aut:category ?cat . }  
  OPTIONAL { ?program aut:sourceFile ?srcFile . }  
  OPTIONAL { ?program aut:sourceHost ?host . }  
  OPTIONAL { ?host aut:hostSha1 ?sha . }  
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
  ?prog rdf:type aut:InstalledProgram .
  ?prog aut:programName ?pname .
  ?prog aut:installedDateTime ?idtime .
  ?prog aut:sourceFile ?sfile .
  ?prog aut:sourceHost ?host .

  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?sha1 .
}
WHERE {
  ?prog rdf:type aut:InstalledProgram .
  OPTIONAL { ?prog aut:programName ?pname } .
  OPTIONAL { ?prog aut:installedDateTime ?idtime } .
  OPTIONAL { ?prog aut:sourceFile ?sfile } .
  OPTIONAL { ?prog aut:sourceHost ?host } .
  OPTIONAL { ?host rdf:type aut:Host } .
  OPTIONAL { ?host aut:hostSha1 ?sha1 } .
}
```

## Q43
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX xml: <http://www.w3.org/XML/1998/namespace>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
  ?prog a aut:InstalledProgram .
  ?prog aut:programName ?progName .
  ?prog aut:installedDateTime ?instDate .
  ?prog aut:category ?cat .
  ?prog aut:sourceFile ?srcFile .
  ?prog aut:sourceFileMd5 ?srcMd5 .
  ?prog aut:sourceHost ?host .

  ?host a aut:Host .
  ?host aut:hostSha1 ?sha .
  ?host aut:sourceFile ?hostSrc .
  ?host aut:sourceFileMd5 ?hostMd5 .
  ?host aut:sourceHost ?hostHost .
}
WHERE {
  ?prog a aut:InstalledProgram .
  OPTIONAL { ?prog aut:programName ?progName } .
  OPTIONAL { ?prog aut:installedDateTime ?instDate } .
  OPTIONAL { ?prog aut:category ?cat } .
  OPTIONAL { ?prog aut:sourceFile ?srcFile } .
  OPTIONAL { ?prog aut:sourceFileMd5 ?srcMd5 } .
  OPTIONAL { ?prog aut:sourceHost ?host } .

  OPTIONAL { ?host a aut:Host } .
  OPTIONAL { ?host aut:hostSha1 ?sha } .
  OPTIONAL { ?host aut:sourceFile ?hostSrc } .
  OPTIONAL { ?host aut:sourceFileMd5 ?hostMd5 } .
  OPTIONAL { ?host aut:sourceHost ?hostHost } .
}
```

## Q44
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX xml: <http://www.w3.org/XML/1998/namespace>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
  ?usb rdf:type aut:USBDeviceAttached .
  ?usb aut:deviceID ?deviceID .
  ?usb aut:deviceMake ?deviceMake .
  ?usb aut:deviceModel ?deviceModel .
  ?usb aut:attachedDateTime ?attached .
  ?usb aut:category ?cat .
  ?usb aut:sourceFile ?srcFile .
  OPTIONAL {
    ?usb aut:sourceHost ?host .
    ?host rdf:type aut:Host .
    ?host aut:hostSha1 ?sha .
  }
}
WHERE {
  ?usb rdf:type aut:USBDeviceAttached .
  ?usb aut:deviceID ?deviceID .
  ?usb aut:deviceMake ?deviceMake .
  ?usb aut:deviceModel ?deviceModel .
  ?usb aut:attachedDateTime ?attached .
  ?usb aut:category ?cat .
  OPTIONAL { ?usb aut:sourceFile ?srcFile . }
  OPTIONAL {
    ?usb aut:sourceHost ?host .
    ?host rdf:type aut:Host .
    OPTIONAL { ?host aut:hostSha1 ?sha . }
  }
}
```

## Q45
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#> .
PREFIX owl: <http://www.w3.org/2002/07/owl#> .
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#> .
PREFIX xml: <http://www.w3.org/XML/1998/namespace> .
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#> .

CONSTRUCT {
  ?usb rdf:type aut:USBDeviceAttached .
  ?usb aut:deviceID ?deviceID .
  ?usb aut:deviceMake ?deviceMake .
  ?usb aut:deviceModel ?deviceModel .
  ?usb aut:attachedDateTime ?attachedDateTime .
  ?usb aut:category ?category .
  ?usb aut:sourceHost ?host .

  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?usb rdf:type aut:USBDeviceAttached .
  OPTIONAL { ?usb aut:deviceID ?deviceID } .
  OPTIONAL { ?usb aut:deviceMake ?deviceMake } .
  OPTIONAL { ?usb aut:deviceModel ?deviceModel } .
  OPTIONAL { ?usb aut:attachedDateTime ?attachedDateTime } .
  OPTIONAL { ?usb aut:category ?category } .
  OPTIONAL { ?usb aut:sourceHost ?host } .
  OPTIONAL { ?host rdf:type aut:Host } .
  OPTIONAL { ?host aut:hostSha1 ?hostSha1 } .
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
  ?b rdf:type aut:WebBookmark .
  ?b aut:url ?url .
  ?b aut:title ?title .
  ?b aut:createdDateTime ?created .
  ?b aut:category ?cat .
  ?b aut:domain ?dom .
  ?b aut:sourceHost ?host .

  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?sha .
}
WHERE {
  ?b rdf:type aut:WebBookmark .
  OPTIONAL { ?b aut:url ?url . }
  OPTIONAL { ?b aut:title ?title . }
  OPTIONAL { ?b aut:createdDateTime ?created . }
  OPTIONAL { ?b aut:category ?cat . }
  OPTIONAL { ?b aut:domain ?dom . }
  OPTIONAL {
    ?b aut:sourceHost ?host .
    ?host rdf:type aut:Host .
    OPTIONAL { ?host aut:hostSha1 ?sha . }
  }
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
  ?bm rdf:type aut:WebBookmark .
  ?bm aut:title ?title .
  ?bm aut:url ?url .
  ?bm aut:category ?cat .
  ?bm aut:sourceFile ?sourceFile .
  ?bm aut:createdDateTime ?created .
  ?bm aut:sourceHost ?host .
  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?sha1 .
}
WHERE {
  ?bm rdf:type aut:WebBookmark .
  ?bm aut:category ?cat .
  FILTER( regex(?cat, "fav", "i") )
  OPTIONAL { ?bm aut:title ?title } .
  OPTIONAL { ?bm aut:url ?url } .
  OPTIONAL { ?bm aut:sourceFile ?sourceFile } .
  OPTIONAL { ?bm aut:createdDateTime ?created } .
  OPTIONAL {
    ?bm aut:sourceHost ?host .
    ?host rdf:type aut:Host .
    OPTIONAL { ?host aut:hostSha1 ?sha1 } .
  }
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
  ?search a aut:WebSearch .
  ?search aut:text ?text .
  ?search aut:domain ?domain .
  ?search aut:accessedDateTime ?accessed .
  ?search aut:category ?cat .
  ?search aut:sourceFile ?srcFile .
  ?search aut:sourceHost ?host .
  ?host a aut:Host .
  ?host aut:hostSha1 ?hostSha .
}
WHERE {
  ?search a aut:WebSearch .
  OPTIONAL { ?search aut:text ?text } .
  OPTIONAL { ?search aut:domain ?domain } .
  OPTIONAL { ?search aut:accessedDateTime ?accessed } .
  OPTIONAL { ?search aut:category ?cat } .
  OPTIONAL { ?search aut:sourceFile ?srcFile } .
  OPTIONAL { ?search aut:sourceHost ?host } .
  OPTIONAL {
    ?host a aut:Host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha } .
  }
}
```

## Q49
```sparql
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX aut: <https://github.com/owlontology/digitalforensics/blob/main/autopsy.owl#>
PREFIX aut-email: <https://github.com/owlontology/digitalforensics/blob/main/autopsy-email.owl#>

CONSTRUCT {
  ?ws rdf:type aut:WebSearch .
  ?ws aut:text ?text .
  ?ws aut:category ?cat .
  ?ws aut:sourceFile ?srcFile .
  ?ws aut:sourceHost ?host .
  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?sha1 .
}
WHERE {
  ?ws a aut:WebSearch .
  OPTIONAL { ?ws aut:text ?text } .
  OPTIONAL { ?ws aut:category ?cat } .
  OPTIONAL { ?ws aut:sourceFile ?srcFile } .
  OPTIONAL {
    ?ws aut:sourceHost ?host .
    ?host a aut:Host .
    OPTIONAL { ?host aut:hostSha1 ?sha1 } .
  }
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
  ?e a aut:EmailMessage ;
     aut-email:emailFrom ?from ;
     aut-email:emailTo ?to .
}
WHERE {
  ?e a aut:EmailMessage .
  OPTIONAL { ?e aut-email:emailFrom ?from }
  OPTIONAL { ?e aut-email:emailTo ?to }
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
  ?msg rdf:type aut:EmailMessage .
  ?msg aut-email:emailFrom ?emailFrom .
  ?msg aut-email:emailTo ?emailTo .
  ?msg aut-email:messageId ?messageId .
  ?msg aut-email:path ?path .
  ?msg aut-email:receivedDateTime ?receivedDateTime .
  ?msg aut-email:subject ?subject .
  ?msg aut-email:threadId ?threadId .
  ?msg aut:sourceHost ?host .
  ?host rdf:type aut:Host .
  ?host aut:hostSha1 ?hostSha1 .
}
WHERE {
  ?msg rdf:type aut:EmailMessage .
  OPTIONAL { ?msg aut-email:emailFrom ?emailFrom . }
  OPTIONAL { ?msg aut-email:emailTo ?emailTo . }
  OPTIONAL { ?msg aut-email:messageId ?messageId . }
  OPTIONAL { ?msg aut-email:path ?path . }
  OPTIONAL { ?msg aut-email:receivedDateTime ?receivedDateTime . }
  OPTIONAL { ?msg aut-email:subject ?subject . }
  OPTIONAL { ?msg aut-email:threadId ?threadId . }
  OPTIONAL {
    ?msg aut:sourceHost ?host .
    ?host rdf:type aut:Host .
    OPTIONAL { ?host aut:hostSha1 ?hostSha1 . }
  }
}
```
