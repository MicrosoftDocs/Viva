---
ROBOTS: NOINDEX,FOLLOW
title: Microsoft Viva Insights API
description: Learn how to use the Microsoft Viva Insights API to secure moving data for more advanced analysis
author: madehmer
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: helayne
audience: Admin
---

# Microsoft Viva Insights API

*This experience is only available through private preview.*

The Microsoft Viva Insights API enables you to provision unique customer keys to secure data in transit between Viva Insights and your application. Additionally, you can use the API to retrieve decryption keys for the data received by your application.

## Decryption Key

Use the following to create a Decryption key for the given copy activity/request ID. The copy activity ID is in the metadata.json file contained in the data drop.

The response will include a decryption key that can be used to decrypt the file contents. Depending on the level of consent granted to your application by the customer, you might also receive a second key for decrypting personally identifiable data within the file, such as the ObjectId of a user.

>[!Note]
>During the private preview release, your application will always receive this key.

Your application must first decrypt the **Value** of the decryption key using the private key of the RSA-2048 key pair that you assigned to the customer with the [Partner key](#partner-key). You can then use the resulting value to decrypt the file or column data.

### Path and parameters

Use the following path:

```POST 
https://api.orginsights.viva.office.com/v{version}/egressDecryptionKey

```

With the following required parameters for the path:

* **Version** - The version of the API. Currently, the only supported version is 1.0.

### Sample request

```http
{
 "requestId": "5c90fd79-6c11-40c7-a66d-f5af65e2b974",
 "scopeId": "dbd9447b-405c-4946-ac5a-492d6e9bfecb" 

}
```

### Sample response

```http
{
   "DecryptionKeys": [
   {
      "DecryptionKeyType": "Column",
      "Value": oF8xFGjrhxC2LsrsrUA3eTCWDl2fYlBkUe886jRLnKFwdbH/9SRA+55ekL42JCcL+iXsQNZdMWmy3LnLgk2nSfZ96ecU/++sOM7QB/6kWrS2Wmg+5XCW5FErodnyBZKCbOo1RETgrxTH8YlcoLX5319VCmBleSMxgitn0Jl+VCM+NjfE87oPWyLo+vifaBtFnIgSOkzKh20dZm/Ue1AxXQlYQ/WptHBRa4LMza/oXgbTpqk9Y+Mw+4IhVtHbCdcEt0DqQ0FRb/qjlwMPaYqOlZ5GxFTiQFsAtYVTpnvcffkDBp1gzlOL2iLhudc66PP4h6v4cBxHx6RTz8bO4KIaQg==",
      "IV": "vLvaqqAN8GaYI9gGuX1bsQ=="
    },
    {
      "DecryptionKeyType": "File",
      "Value": "Hv4OtwCacGJ3mgetOpRS6rx2jC65vWfjCDNCIebYpTe2DFgDlZbxLJ6l3ZETH5Oss6NlLYbWIgTiBwuQxN/a7eZBE5ZYuiG3Gk72lH0Egy7BeSN7dlyV7ryn1nC7eEpYsjOLwSdIs79JP77yvIlkNohCXgP/BVp612kL1/atxITyN2kxWO4RaMhct3izvdjreOJoxUABEAAaqCGagrgsWL1AS+5X5fduspsE8zmPJ78cm67Qt5ZbdZ+N+ilXEclSIUeVrp9iXjh94mLCn9hra8e97SXVquyAnWG5F0Wy/tjS6+pNyM/EVI/QrBCgSW7HsOJp1sQvq7u+/ZJln4zS3w==",
      "IV": "X8G/1lYE9URXyBfQVUGC+A=="
    }
]
}
```

### Request body

```DecryptionKeyCreateRequest``` 

[Model](#decryptionkeycreaterequest)

### Return type

```DecryptionKeyCreateResponse```

[Model](#decryptionkeycreateresponse)
### Responses

* **200** - Returns the created decryption keys as: ```DecryptionKeyCreateResponse```
* **400** - Request has a missing or invalid value.
* **500** - An error occurred when creating the decryption keys.

#### Sample response

```http
{
  "decryptionKeys" : [{
    "type" : "File",
    "value" : "oF8xFGjrhxC2LsrsrUA3eTCWDl2fYlBkUe886jRLnKFwdbH/9SRA+55ekL42JCcL+iXsQNZdMWmy3LnLgk2nSfZ96ecU/++sOM7QB/6kWrS2Wmg+5XCW5FErodnyBZKCbOo1RETgrxTH8YlcoLX5319VCmBleSMxgitn0Jl+VCM+NjfE87oPWyLo+vifaBtFnIgSOkzKh20dZm/Ue1AxXQlYQ/WptHBRa4LMza/oXgbTpqk9Y+Mw+4IhVtHbCdcEt0DqQ0FRb/qjlwMPaYqOlZ5GxFTiQFsAtYVTpnvcffkDBp1gzlOL2iLhudc66PP4h6v4cBxHx6RTz8bO4KIaQg==.",
    "iv" : "vLvaqqAN8GaYI9gGuX1bsQ=="
  }, {
    "type" : "File",
    "value" : "oF8xFGjrhxC2LsrsrUA3eTCWDl2fYlBkUe886jRLnKFwdbH/9SRA+55ekL42JCcL+iXsQNZdMWmy3LnLgk2nSfZ96ecU/++sOM7QB/6kWrS2Wmg+5XCW5FErodnyBZKCbOo1RETgrxTH8YlcoLX5319VCmBleSMxgitn0Jl+VCM+NjfE87oPWyLo+vifaBtFnIgSOkzKh20dZm/Ue1AxXQlYQ/WptHBRa4LMza/oXgbTpqk9Y+Mw+4IhVtHbCdcEt0DqQ0FRb/qjlwMPaYqOlZ5GxFTiQFsAtYVTpnvcffkDBp1gzlOL2iLhudc66PP4h6v4cBxHx6RTz8bO4KIaQg==.",
    "iv" : "vLvaqqAN8GaYI9gGuX1bsQ=="
  }]
}
```

## Partner key

A unique RSA-2048 key pair must be created for each customer that installs your application. This key cannot be reused across multiple customers. Your application can securely generate and store RSA-2048 certificates (containing such a key pair) using Azure KeyVault, or you may use a custom solution.

### Path and parameters

Use the following path:

```POST
 https://api.orginsights.viva.office.com/v1.0/egressPartnerKey
```

With the following required parameters for the path:

* **Version** - The version of the API. Currently, the only supported version is 1.0.

### Request body

```PartnerKeyInfoCreateRequest```

[Model](#partnerkeyinfocreaterequest)

### Return type

```PartnerKeyInfoCreateResponse```

[Model](#partnerkeyinfocreateresponse)

### Response

**200** - Returns the Partner key as: ```PartnerKeyInfoCreateResponse```

#### Sample response

```http
{
  "scopeId" : {
    "id" : "2b13482-357g-dh58-6j34-d2832fee24b8"
  },
  "createdDate" : "2022-04-25T17:44:10.1935639Z",
  "partnerAppId" : "8d067740-790e-be50-6e54-d2832fee24b8",
  "encryptionAlgorithm" : "RSA2048",
  "expirationDate" : "2023-04-25T17:44:10.1935639Z"
}
```

## Models

The following models are used within this API:

* [DecryptionKey](#decryptionkey)
* [DecryptionKeyCreateRequest](#decryptionkeycreaterequest)
* [DecryptionKeyCreateResponse](#decryptionkeycreateresponse)
* [DecryptionKeyType](#decryptionkeytype)
* [EncryptionAlgorithm](#encryptionalgorithm)
* [ScopeId](#scopeid)
* [PartnerKeyInfoCreateRequest](#partnerkeyinfocreaterequest)
* [PartnerKeyInfoCreateResponse](#partnerkeyinfocreateresponse)
* [RsaKey](#rsakey)

### DecryptionKey

Decryption keys consist of the following components:

* **type** – Indicates whether the decryption key is intended to be used to decrypt an entire file, or personally identifiable column data.

  ```DecryptionKeyType```

* **value** – The Base-64 representation of the decryption key’s value. For example:

  ```oF8xFGjrhxC2LsrsrUA3eTCWDl2fYlBkUe886jRLnKFwdbH/9SRA+55ekL42JCcL+iXsQNZdMWmy3LnLgk2nSfZ96ecU/++sOM7QB/6kWrS2Wmg+5XCW5FErodnyBZKCbOo1RETgrxTH8YlcoLX5319VCmBleSMxgitn0Jl+VCM+NjfE87oPWyLo+vifaBtFnIgSOkzKh20dZm/Ue1AxXQlYQ/WptHBRa4LMza/oXgbTpqk9Y+Mw+4IhVtHbCdcEt0DqQ0FRb/qjlwMPaYqOlZ5GxFTiQFsAtYVTpnvcffkDBp1gzlOL2iLhudc66PP4h6v4cBxHx6RTz8bO4KIaQg==```

* **iv** – The Base-64 representation of the initialization vector used to create the decryption key. For example:

  ```vLvaqqAN8GaYI9gGuX1bsQ==```

### DecryptionKeyCreateRequest

**requestId** - The request that gets the decryption keys for a data drop, which is the string value for the unique identifier of the copy activity.

### DecryptionKeyCreateResponse

**decryptionKeys** - The response with the decryption keys, which is an array containing the decryption keys available to your application.

### DecryptionKeyType

The type of decryption key, which might be either **File** or **Column**.

### EncryptionAlgorithm

Types of supported encryption algorithms. For symmetrical keys, the only supported type is **AES256**. For asymmetric key pairs, the only supported type is **RSA2048**.

### ScopeId

**id** - The string value that represents the Viva Insights scope ID. Currently, this is the same as the Azure Active Directory tenant ID for the Viva Insights user.

### PartnerKeyInfoCreateRequest

The request object that uploads the partner key information.

* **partnerAppId** - The string value for the application (client) ID of the application that you are integrating with Viva Insights.
* **tenantId** - The string value for the application’s Azure tenant ID for the application that you are integrating with Viva Insights.
* **rsaKey** - The object that contains the parameters describing the public key of the RSA-2048 key pair.
* **encryptionAlgorithm** - The enum that represents the encryption algorithm used for the key pair. The only supported value is RSA2048.
* **scopeId** – A string value that represents the Viva Insights customer scope ID. Currently, this value must be the same as the customer’s Azure Active Directory tenant ID.

### PartnerKeyInfoCreateResponse

Information about the public key that's used to encrypt data drops for the integration.

* **partnerAppId** - A string value for the application id of the application that you’re integrating with Viva Insights. For example:

  ```8d067740-790e-be50-6e54-d2832fee24b8```

* **createdDate** - A UTC date value for when the key was generated that’s formatted as date-time. For example:

  ```2022-04-25T17:44:10.1935639Z```

* **expirationDate** - A UTC date value for when the key expires that’s formatted as date-time. For example:

  ```2023-04-25T17:44:10.1935639Z```

* **encryptionAlgorithm** - An **enum** that represents the encryption algorithm used for the partner key.
* **scopeId** - The Viva Insights customer scope ID. Currently, this value must be the same as the customer’s Azure Active Directory tenant ID.

### RsaKey

Information about the RSA key.

* **kty** - A string that identifies the cryptographic algorithm family used with the key. The only supported value is:

  ```RSA```

* **e** - A string containing the Base-64 representation of the RSA public key’s exponent. For example:

  ```AQAB```

* **n** - A string containing the Base-64 representation of the RSA public key’s modulus. For example:

  ```s1AkmPGpge25/QiOUIUzKmXpO2pcoZ7yWYkc0RWpV2jjRozXALlyg/2ydCZVjhyuWhduQGFPZTcwyErz1wsA6AtKKYPPxwlLaD1zuG8rUpCPJT1HXqROFUyIADu4VTzjCX32Dv55upPk1VnrRwDPB/cekfBCwhDGiYvLBedXfbRLBqvub5XrfVeeeAc1Whi9m2fyGbxcnW/E0B9kSh5JUd05o39scKupkI0oeILEnLKC0xGGo+M+PK5Cx+u939CsONL+wq0db6ar7uC7l47D7aib5yzNKyp2cYNgdJ3hNFMZLmI4phMXWowZhqqchCJrYHiQGUhszlEyNhDhlfQApQ==```

## Related topics

* [Viva Insights integration](partner-integration.md)
* [Advanced insights metrics](../metrics.md)
