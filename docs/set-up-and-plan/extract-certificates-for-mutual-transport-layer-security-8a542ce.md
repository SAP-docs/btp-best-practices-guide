<!-- loio8a542ce870714550a3e70dc50bd453e6 -->

# Extract Certificates for Mutual Transport Layer Security

Some SAP BTP services such as the SAP Destination service need an X.509 certificate and private key for mutual transport layer security \(mTLS\) in a single privacy enhanced mail \(PEM\) file. Extract this information from the service key of the service that needs to authenticate with the authentication server.



<a name="loio8a542ce870714550a3e70dc50bd453e6__steps_sf1_nyn_kxb"/>

## Procedure

1.  In the SAP BTP cockpit, select the service instance you've created and navigate to the service key.

    The service key contains a JSON structure that has the credential information.

    Find the client certificate under the `certificate` attribute. The private key is present under the `key` attribute.

    Check that the `credential-type` is ***x509***.

      
      
    **Form View of a Service Key with Credential Type X509**

    ![](images/Service_Key_mTLS_8b110f5.png "Form View of a Service Key with Credential Type X509")

    > ### Note:  
    > Some service keys put the `certificate` and `key` attributes directly in the root JSON object.
    > 
    > Both the certificate and the private key are Base64 encoded with the appropriate prefix and postfix.

2.  Copy the values of the `key` and `certificate` attributes to two separate text files in a text editor, such as Notepad.

    > ### Restriction:  
    > Certificate files have strict formatting requirements, such as line length and the use of line breaks. For more information, see [RFC 7468](https://datatracker.ietf.org/doc/html/rfc7468). There are third-party tools to help handle such characters.

3.  Save the files with the `.pem` extension.

    `my-private-key.pem`

    `my-certificate.pem`

4.  Create the final PEM file with both certificate and key.

    Formatting restrictions of RFC 7468 still apply.

    1.  From your private key file, copy and paste the contents to a new text file.

    2.  From your certificate file, add the certificate **after** the private key.

    3.  Save the new file with the `.pem` extension.

        `my-keypair.pem`


    The result resembles the following example.

    ```
    -----BEGIN RSA PRIVATE KEY-----
    MB2NmLWV1MjAxDzANBgNVBAoMBlNBUCBTRTEYMBYGA1UECwwPU0FQIEJUUCBDbG
    llbnRzMS4wLAYDVQQDDCVTQVAgUEtJIENlcnRpZmljYXRlIFNlcnZpY2UgQ2xpZ
    -----END RSA PRIVATE KEY-----
    
    -----BEGIN CERTIFICATE-----
    MIIGaTCCBFGgAwIBAgIQND4V8+sFquk7Lndu82bZ9jANBgkqhkiG9w0BAQsFADB
    jMQswCQYDVQQGEwJERTENMAsGA1UEBwwERVUxMDEPMA0GA1UECgwGU0FQIFNFMR
    -----END CERTIFICATE-----
    -----BEGIN CERTIFICATE-----
    MIIGSjCCBDKgAwIBAgITcAAAAApMdyh1162sZgAAAAAACjANBgkqhkiG9w0BAQs
    FADBNMQswCQYDVQQGEwJERTERMA8GA1UEBwwIV2FsbGRvcmYxDzANBgNVBAoMBl
    -----END CERTIFICATE-----
    -----BEGIN CERTIFICATE-----
    MIIGSjCCBDKgAwIBAgITcAAAAApMdyh1162sZgAAAAAACjANBgkqhkiG9w0BAQs
    FADBNMQswCQYDVQQGEwJERTERMA8GA1UEBwwIV2FsbGRvcmYxDzANBgNVBAoMBl
    -----END CERTIFICATE-----
    ```




<a name="loio8a542ce870714550a3e70dc50bd453e6__postreq_ftg_v22_4xb"/>

## Next Steps

To create other file formats for certificates, such as `.cer`, `.jks`, and `.p12`, use third-party tools.

**Related Information**  


[OAuth with X.509 Client Certificates](https://help.sap.com/docs/CP_CONNECTIVITY/14ad6e76ba9b44f682154bb90686ae84/2c162aaa9e464480b2307879d1b865f5.html)

