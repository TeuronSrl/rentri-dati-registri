# TransazioneRequestModel


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identificativo_transazione** | **str** |  | [optional] 
**jti** | **str** |  | [optional] 
**issuer** | **str** |  | [optional] 
**date_time** | **datetime** |  | [optional] 
**endpoint** | **str** |  | [optional] 
**data** | [**TransazioneRequestDataModel**](TransazioneRequestDataModel.md) |  | [optional] 

## Example

```python
from rentri_dati_registri.models.transazione_request_model import TransazioneRequestModel

# TODO update the JSON string below
json = "{}"
# create an instance of TransazioneRequestModel from a JSON string
transazione_request_model_instance = TransazioneRequestModel.from_json(json)
# print the JSON string representation of the object
print TransazioneRequestModel.to_json()

# convert the object into a dict
transazione_request_model_dict = transazione_request_model_instance.to_dict()
# create an instance of TransazioneRequestModel from a dict
transazione_request_model_from_dict = TransazioneRequestModel.from_dict(transazione_request_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


