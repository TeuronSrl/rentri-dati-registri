# IndirizzoModelCitta

Città estera o comune Italiano

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**comune_id** | **str** | Comune ISTAT del comune.  Non vengono accettati codici non corrispondenti a codici ISTAT di comuni italiani.  Vedi API di codifica: &lt;i&gt;GET /codifiche/v1.0/comuni&lt;/i&gt; | 
**nazione_id** | **str** | Codice ISO 3166-1 alpha-2 della nazione, in caso di \&quot;IT\&quot; è possibile omettere.  Vengono accettati solo codici previsti dallo standard ISO 3166-1 alpha-2.  Vedi API di codifica: &lt;i&gt;GET /codifiche/v1.0/nazioni&lt;/i&gt; | 
**nome_citta** | **str** | Città estera | 

## Example

```python
from rentri_dati_registri.models.indirizzo_model_citta import IndirizzoModelCitta

# TODO update the JSON string below
json = "{}"
# create an instance of IndirizzoModelCitta from a JSON string
indirizzo_model_citta_instance = IndirizzoModelCitta.from_json(json)
# print the JSON string representation of the object
print IndirizzoModelCitta.to_json()

# convert the object into a dict
indirizzo_model_citta_dict = indirizzo_model_citta_instance.to_dict()
# create an instance of IndirizzoModelCitta from a dict
indirizzo_model_citta_from_dict = IndirizzoModelCitta.from_dict(indirizzo_model_citta_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


