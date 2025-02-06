# CittaEsteraModel

Città estera

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**nazione_id** | **str** | Codice ISO 3166-1 alpha-2 della nazione, in caso di \&quot;IT\&quot; è possibile omettere.  Vengono accettati solo codici previsti dallo standard ISO 3166-1 alpha-2.  Vedi API di codifica: &lt;i&gt;GET /codifiche/v1.0/nazioni&lt;/i&gt; | 
**nome_citta** | **str** | Città estera | 

## Example

```python
from rentri_dati_registri.models.citta_estera_model import CittaEsteraModel

# TODO update the JSON string below
json = "{}"
# create an instance of CittaEsteraModel from a JSON string
citta_estera_model_instance = CittaEsteraModel.from_json(json)
# print the JSON string representation of the object
print CittaEsteraModel.to_json()

# convert the object into a dict
citta_estera_model_dict = citta_estera_model_instance.to_dict()
# create an instance of CittaEsteraModel from a dict
citta_estera_model_from_dict = CittaEsteraModel.from_dict(citta_estera_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


