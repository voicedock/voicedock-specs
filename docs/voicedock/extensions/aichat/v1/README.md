# Protocol Documentation
<a name="top"></a>

## Table of Contents

- [voicedock/extensions/aichat/v1/aichat.proto](#voicedock_extensions_aichat_v1_aichat-proto)
    - [Model](#voicedock-extensions-aichat-v1-Model)
  
- [voicedock/extensions/aichat/v1/aichat_api.proto](#voicedock_extensions_aichat_v1_aichat_api-proto)
    - [DownloadModelRequest](#voicedock-extensions-aichat-v1-DownloadModelRequest)
    - [DownloadModelResponse](#voicedock-extensions-aichat-v1-DownloadModelResponse)
    - [GenerateRequest](#voicedock-extensions-aichat-v1-GenerateRequest)
    - [GenerateResponse](#voicedock-extensions-aichat-v1-GenerateResponse)
    - [GetModelsRequest](#voicedock-extensions-aichat-v1-GetModelsRequest)
    - [GetModelsResponse](#voicedock-extensions-aichat-v1-GetModelsResponse)
  
    - [AichatAPI](#voicedock-extensions-aichat-v1-AichatAPI)
  
- [Scalar Value Types](#scalar-value-types)



<a name="voicedock_extensions_aichat_v1_aichat-proto"></a>
<p align="right"><a href="#top">Top</a></p>

## voicedock/extensions/aichat/v1/aichat.proto



<a name="voicedock-extensions-aichat-v1-Model"></a>

### Model
AI Chat model info.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | Model name |
| downloaded | [bool](#bool) |  | Is downloaded |
| downloadable | [bool](#bool) |  | Can be downloaded |
| license | [string](#string) |  | License text to accept |





 

 

 

 



<a name="voicedock_extensions_aichat_v1_aichat_api-proto"></a>
<p align="right"><a href="#top">Top</a></p>

## voicedock/extensions/aichat/v1/aichat_api.proto



<a name="voicedock-extensions-aichat-v1-DownloadModelRequest"></a>

### DownloadModelRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | Model name. |






<a name="voicedock-extensions-aichat-v1-DownloadModelResponse"></a>

### DownloadModelResponse







<a name="voicedock-extensions-aichat-v1-GenerateRequest"></a>

### GenerateRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| prompt | [string](#string) |  | Text prompt |






<a name="voicedock-extensions-aichat-v1-GenerateResponse"></a>

### GenerateResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| token_text | [string](#string) |  | Text token |






<a name="voicedock-extensions-aichat-v1-GetModelsRequest"></a>

### GetModelsRequest







<a name="voicedock-extensions-aichat-v1-GetModelsResponse"></a>

### GetModelsResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| models | [Model](#voicedock-extensions-aichat-v1-Model) | repeated |  |





 

 

 


<a name="voicedock-extensions-aichat-v1-AichatAPI"></a>

### AichatAPI
Speech-to-text service.

| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| Generate | [GenerateRequest](#voicedock-extensions-aichat-v1-GenerateRequest) | [GenerateResponse](#voicedock-extensions-aichat-v1-GenerateResponse) stream | Generate response text by prompt. |
| GetModels | [GetModelsRequest](#voicedock-extensions-aichat-v1-GetModelsRequest) | [GetModelsResponse](#voicedock-extensions-aichat-v1-GetModelsResponse) | Returns available ai chat models. |
| DownloadModel | [DownloadModelRequest](#voicedock-extensions-aichat-v1-DownloadModelRequest) | [DownloadModelResponse](#voicedock-extensions-aichat-v1-DownloadModelResponse) | Downloads selected ai model. |

 



## Scalar Value Types

| .proto Type | Notes | C++ | Java | Python | Go | C# | PHP | Ruby |
| ----------- | ----- | --- | ---- | ------ | -- | -- | --- | ---- |
| <a name="double" /> double |  | double | double | float | float64 | double | float | Float |
| <a name="float" /> float |  | float | float | float | float32 | float | float | Float |
| <a name="int32" /> int32 | Uses variable-length encoding. Inefficient for encoding negative numbers – if your field is likely to have negative values, use sint32 instead. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="int64" /> int64 | Uses variable-length encoding. Inefficient for encoding negative numbers – if your field is likely to have negative values, use sint64 instead. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="uint32" /> uint32 | Uses variable-length encoding. | uint32 | int | int/long | uint32 | uint | integer | Bignum or Fixnum (as required) |
| <a name="uint64" /> uint64 | Uses variable-length encoding. | uint64 | long | int/long | uint64 | ulong | integer/string | Bignum or Fixnum (as required) |
| <a name="sint32" /> sint32 | Uses variable-length encoding. Signed int value. These more efficiently encode negative numbers than regular int32s. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="sint64" /> sint64 | Uses variable-length encoding. Signed int value. These more efficiently encode negative numbers than regular int64s. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="fixed32" /> fixed32 | Always four bytes. More efficient than uint32 if values are often greater than 2^28. | uint32 | int | int | uint32 | uint | integer | Bignum or Fixnum (as required) |
| <a name="fixed64" /> fixed64 | Always eight bytes. More efficient than uint64 if values are often greater than 2^56. | uint64 | long | int/long | uint64 | ulong | integer/string | Bignum |
| <a name="sfixed32" /> sfixed32 | Always four bytes. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="sfixed64" /> sfixed64 | Always eight bytes. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="bool" /> bool |  | bool | boolean | boolean | bool | bool | boolean | TrueClass/FalseClass |
| <a name="string" /> string | A string must always contain UTF-8 encoded or 7-bit ASCII text. | string | String | str/unicode | string | string | string | String (UTF-8) |
| <a name="bytes" /> bytes | May contain any arbitrary sequence of bytes. | string | ByteString | str | []byte | ByteString | string | String (ASCII-8BIT) |

