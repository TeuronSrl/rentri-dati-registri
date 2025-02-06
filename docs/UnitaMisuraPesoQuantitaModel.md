# UnitaMisuraPesoQuantitaModel


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**valore** | **float** | Quantità (parte intera: 10, parte decimale: 4) compresa tra 0.0000 e 9999999999.9999. | 
**unita_misura** | [**UnitaMisuraPeso**](UnitaMisuraPeso.md) | Unità di misura della quantità  Vedi API di codifica: &lt;i&gt;GET /codifiche/v1.0/unita-misura&lt;/i&gt;&lt;p&gt;Valori ammessi:&lt;ul style&#x3D;\&quot;margin:0\&quot;&gt;&lt;li&gt;&lt;i&gt;kg&lt;/i&gt; - Chilogrammi&lt;/li&gt;&lt;/ul&gt;&lt;/p&gt; | 

## Example

```python
from rentri_dati_registri.models.unita_misura_peso_quantita_model import UnitaMisuraPesoQuantitaModel

# TODO update the JSON string below
json = "{}"
# create an instance of UnitaMisuraPesoQuantitaModel from a JSON string
unita_misura_peso_quantita_model_instance = UnitaMisuraPesoQuantitaModel.from_json(json)
# print the JSON string representation of the object
print UnitaMisuraPesoQuantitaModel.to_json()

# convert the object into a dict
unita_misura_peso_quantita_model_dict = unita_misura_peso_quantita_model_instance.to_dict()
# create an instance of UnitaMisuraPesoQuantitaModel from a dict
unita_misura_peso_quantita_model_from_dict = UnitaMisuraPesoQuantitaModel.from_dict(unita_misura_peso_quantita_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


