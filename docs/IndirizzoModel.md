# IndirizzoModel

Indirizzo

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**citta** | [**IndirizzoModelCitta**](IndirizzoModelCitta.md) |  | 
**indirizzo** | **str** | Indirizzo | 
**civico** | **str** | Civico | [optional] 
**cap** | **str** | CAP (se indirizzo italiano 5 cifre, altrimenti da 2 a 20 caratteri) | [optional] 

## Example

```python
from rentri_dati_registri.models.indirizzo_model import IndirizzoModel

# TODO update the JSON string below
json = "{}"
# create an instance of IndirizzoModel from a JSON string
indirizzo_model_instance = IndirizzoModel.from_json(json)
# print the JSON string representation of the object
print(IndirizzoModel.to_json())

# convert the object into a dict
indirizzo_model_dict = indirizzo_model_instance.to_dict()
# create an instance of IndirizzoModel from a dict
indirizzo_model_from_dict = IndirizzoModel.from_dict(indirizzo_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


