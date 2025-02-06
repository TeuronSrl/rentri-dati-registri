# DatiIntegrazioneFirModel

Integrazione FIR - Registro C/S

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**numero_fir** | **str** | Numero formulario | [optional] 
**trasporto_transfrontaliero** | **bool** | Trasporto transfrontaliero | [optional] 
**tipo_trasporto_transfrontaliero** | [**TipiTrasportoTransfrontaliero**](TipiTrasportoTransfrontaliero.md) | Tipo trasporto transfrontaliero.  Richiesto solamente se trasporto_transfrontaliero è uguale a true. Vedi API di codifica: &lt;i&gt;GET /codifiche/v1.0/tipi-trasporto-transfrontaliero&lt;/i&gt;&lt;p&gt;Valori ammessi:&lt;ul style&#x3D;\&quot;margin:0\&quot;&gt;&lt;li&gt;&lt;i&gt;DM&lt;/i&gt; - Documento di movimento (Allegato I-B  al Regolamento 1013/06)&lt;/li&gt;&lt;li&gt;&lt;i&gt;DA&lt;/i&gt; - Documento di accompagnamento (Allegato VII – al Regolamento 1013/06)&lt;/li&gt;&lt;/ul&gt;&lt;/p&gt; | [optional] 
**data_inizio_trasporto** | **datetime** | Data inizio trasporto (formato ISO 8601 UTC) | [optional] 

## Example

```python
from rentri_dati_registri.models.dati_integrazione_fir_model import DatiIntegrazioneFirModel

# TODO update the JSON string below
json = "{}"
# create an instance of DatiIntegrazioneFirModel from a JSON string
dati_integrazione_fir_model_instance = DatiIntegrazioneFirModel.from_json(json)
# print the JSON string representation of the object
print DatiIntegrazioneFirModel.to_json()

# convert the object into a dict
dati_integrazione_fir_model_dict = dati_integrazione_fir_model_instance.to_dict()
# create an instance of DatiIntegrazioneFirModel from a dict
dati_integrazione_fir_model_from_dict = DatiIntegrazioneFirModel.from_dict(dati_integrazione_fir_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


