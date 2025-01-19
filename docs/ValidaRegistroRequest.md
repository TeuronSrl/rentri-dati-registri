# ValidaRegistroRequest

Richiesta per la validazione strutturale del registro cronologico di carico e scarico digitale in formato XML

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**file_content** | **bytearray** | Contenuto in Base64 del file XML, o del file ZIP contenente il file XML, del registro cronologico di carico e scarico digitale | 
**nome_file** | **str** | Nome del file | 
**mime** | **str** | Tipo MIME del file da caricare | 

## Example

```python
from rentri_dati_registri.models.valida_registro_request import ValidaRegistroRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ValidaRegistroRequest from a JSON string
valida_registro_request_instance = ValidaRegistroRequest.from_json(json)
# print the JSON string representation of the object
print(ValidaRegistroRequest.to_json())

# convert the object into a dict
valida_registro_request_dict = valida_registro_request_instance.to_dict()
# create an instance of ValidaRegistroRequest from a dict
valida_registro_request_from_dict = ValidaRegistroRequest.from_dict(valida_registro_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


