# DatiDestinatarioModel

Destinatario

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**denominazione** | **str** | Denominazione del soggetto | 
**codice_fiscale** | **str** | Codice fiscale | 
**nazione_id** | **str** | Codice ISO 3166-1 alpha-2 della nazione, in caso di \&quot;IT\&quot; è possibile omettere.  Vengono accettati solo codici previsti dallo standard ISO 3166-1 alpha-2.  Vedi API di codifica: &lt;i&gt;GET /codifiche/v1.0/nazioni&lt;/i&gt;  &lt;i&gt;Questo campo viene utilizzato esclusivamente per validare i dati di input in base alla nazione di appartenenza (non viene memorizzato e quindi restituito in output).&lt;/i&gt; | [optional] 
**num_autorizzazione** | **str** | Numero autorizzazione. Non obbligatorio nel caso di destinatario estero, richiesto in caso contrario | [optional] 

## Example

```python
from rentri_dati_registri.models.dati_destinatario_model import DatiDestinatarioModel

# TODO update the JSON string below
json = "{}"
# create an instance of DatiDestinatarioModel from a JSON string
dati_destinatario_model_instance = DatiDestinatarioModel.from_json(json)
# print the JSON string representation of the object
print DatiDestinatarioModel.to_json()

# convert the object into a dict
dati_destinatario_model_dict = dati_destinatario_model_instance.to_dict()
# create an instance of DatiDestinatarioModel from a dict
dati_destinatario_model_from_dict = DatiDestinatarioModel.from_dict(dati_destinatario_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


