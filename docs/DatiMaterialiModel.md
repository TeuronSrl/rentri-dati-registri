# DatiMaterialiModel

Materiali (solo Impianti)

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**materiale** | [**Materiali**](Materiali.md) | Materiale  Vedi API di codifica: &lt;i&gt;GET /codifiche/v1.0/materiali&lt;/i&gt;&lt;p&gt;Valori ammessi:&lt;ul style&#x3D;\&quot;margin:0\&quot;&gt;&lt;li&gt;&lt;i&gt;ACV&lt;/i&gt; - 1 - Ammendante compostato verde&lt;/li&gt;&lt;li&gt;&lt;i&gt;ACM&lt;/i&gt; - 2 - Ammendante compostato misto&lt;/li&gt;&lt;li&gt;&lt;i&gt;AA&lt;/i&gt; - 3 - Altri Ammendanti&lt;/li&gt;&lt;li&gt;&lt;i&gt;DIG&lt;/i&gt; - 4 - Digestato&lt;/li&gt;&lt;li&gt;&lt;i&gt;AGG&lt;/i&gt; - 5 - Aggregati riciclati&lt;/li&gt;&lt;li&gt;&lt;i&gt;RA&lt;/i&gt; - 6 - Rottami di alluminio&lt;/li&gt;&lt;li&gt;&lt;i&gt;RV&lt;/i&gt; - 7 - Rottami di vetro&lt;/li&gt;&lt;li&gt;&lt;i&gt;RFA&lt;/i&gt; - 8 - Rottami di ferro e acciaio&lt;/li&gt;&lt;li&gt;&lt;i&gt;RR&lt;/i&gt; - 9 - Rottami di rame&lt;/li&gt;&lt;li&gt;&lt;i&gt;CC&lt;/i&gt; - 10 - Carta e cartone&lt;/li&gt;&lt;li&gt;&lt;i&gt;PLA&lt;/i&gt; - 11 - Plastica&lt;/li&gt;&lt;li&gt;&lt;i&gt;LS&lt;/i&gt; - 12 - Legno e sughero&lt;/li&gt;&lt;li&gt;&lt;i&gt;CSS&lt;/i&gt; - 13 - CSS – combustibile&lt;/li&gt;&lt;li&gt;&lt;i&gt;TE&lt;/i&gt; - 14 - Tessili&lt;/li&gt;&lt;li&gt;&lt;i&gt;GOM&lt;/i&gt; - 15 - Gomma&lt;/li&gt;&lt;li&gt;&lt;i&gt;CU&lt;/i&gt; - 16 - Cuoio&lt;/li&gt;&lt;li&gt;&lt;i&gt;MC&lt;/i&gt; - 17 - Materiali ceramici&lt;/li&gt;&lt;li&gt;&lt;i&gt;CF&lt;/i&gt; - 18 - Correttivi da Fanghi&lt;/li&gt;&lt;li&gt;&lt;i&gt;AF&lt;/i&gt; - 19 - Altri Fertilizzanti&lt;/li&gt;&lt;li&gt;&lt;i&gt;GCB&lt;/i&gt; - 20 - Granulato di Conglomerato bituminoso&lt;/li&gt;&lt;li&gt;&lt;i&gt;ASS&lt;/i&gt; - 21 - Materiali secondari derivanti dal recupero di prodotti assorbenti per la persona&lt;/li&gt;&lt;li&gt;&lt;i&gt;GMV&lt;/i&gt; - 22 - Gomma vulcanizzata da PFU&lt;/li&gt;&lt;li&gt;&lt;i&gt;A&lt;/i&gt; - 23 - Altro&lt;/li&gt;&lt;/ul&gt;&lt;/p&gt; | 
**descrizione_materiale** | **str** | Descrizione materiale | [optional] 
**quantita** | [**UnitaMisuraPesoQuantitaModel**](UnitaMisuraPesoQuantitaModel.md) | Quantità | [optional] 

## Example

```python
from rentri_dati_registri.models.dati_materiali_model import DatiMaterialiModel

# TODO update the JSON string below
json = "{}"
# create an instance of DatiMaterialiModel from a JSON string
dati_materiali_model_instance = DatiMaterialiModel.from_json(json)
# print the JSON string representation of the object
print(DatiMaterialiModel.to_json())

# convert the object into a dict
dati_materiali_model_dict = dati_materiali_model_instance.to_dict()
# create an instance of DatiMaterialiModel from a dict
dati_materiali_model_from_dict = DatiMaterialiModel.from_dict(dati_materiali_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


