# MovimentoInfoModel


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**anno** | **int** |  | [optional] 
**progressivo** | **int** |  | [optional] 
**identificativo** | **str** |  | [optional] 
**data_ora_registrazione** | **datetime** |  | [optional] 

## Example

```python
from rentri_dati_registri.models.movimento_info_model import MovimentoInfoModel

# TODO update the JSON string below
json = "{}"
# create an instance of MovimentoInfoModel from a JSON string
movimento_info_model_instance = MovimentoInfoModel.from_json(json)
# print the JSON string representation of the object
print(MovimentoInfoModel.to_json())

# convert the object into a dict
movimento_info_model_dict = movimento_info_model_instance.to_dict()
# create an instance of MovimentoInfoModel from a dict
movimento_info_model_from_dict = MovimentoInfoModel.from_dict(movimento_info_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


