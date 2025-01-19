# TransazioneRequestDataModel


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**claims** | **str** |  | [optional] 
**headers** | **str** |  | [optional] 
**body** | **str** |  | [optional] 

## Example

```python
from rentri_dati_registri.models.transazione_request_data_model import TransazioneRequestDataModel

# TODO update the JSON string below
json = "{}"
# create an instance of TransazioneRequestDataModel from a JSON string
transazione_request_data_model_instance = TransazioneRequestDataModel.from_json(json)
# print the JSON string representation of the object
print(TransazioneRequestDataModel.to_json())

# convert the object into a dict
transazione_request_data_model_dict = transazione_request_data_model_instance.to_dict()
# create an instance of TransazioneRequestDataModel from a dict
transazione_request_data_model_from_dict = TransazioneRequestDataModel.from_dict(transazione_request_data_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


