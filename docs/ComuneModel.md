# ComuneModel

Comune Italiano

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**comune_id** | **str** | Comune ISTAT del comune.  Non vengono accettati codici non corrispondenti a codici ISTAT di comuni italiani.  Vedi API di codifica: &lt;i&gt;GET /codifiche/v1.0/comuni&lt;/i&gt; | 

## Example

```python
from rentri_dati_registri.models.comune_model import ComuneModel

# TODO update the JSON string below
json = "{}"
# create an instance of ComuneModel from a JSON string
comune_model_instance = ComuneModel.from_json(json)
# print the JSON string representation of the object
print(ComuneModel.to_json())

# convert the object into a dict
comune_model_dict = comune_model_instance.to_dict()
# create an instance of ComuneModel from a dict
comune_model_from_dict = ComuneModel.from_dict(comune_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


