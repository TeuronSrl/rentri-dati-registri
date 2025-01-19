# TransazioneModel


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**transazione_id** | **str** |  | [optional] 

## Example

```python
from rentri_dati_registri.models.transazione_model import TransazioneModel

# TODO update the JSON string below
json = "{}"
# create an instance of TransazioneModel from a JSON string
transazione_model_instance = TransazioneModel.from_json(json)
# print the JSON string representation of the object
print(TransazioneModel.to_json())

# convert the object into a dict
transazione_model_dict = transazione_model_instance.to_dict()
# create an instance of TransazioneModel from a dict
transazione_model_from_dict = TransazioneModel.from_dict(transazione_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


