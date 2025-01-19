# DatiRiferimentiBaseModelNumeroRegistrazione

Numero registrazione della registrazione tramite anno e progressivo oppure identificativo rilasciato dal RENTRI

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**anno** | **int** | Anno di riferimento della registrazione | 
**progressivo** | **int** | Progressivo della registrazione | 
**identificativo** | **str** | Identificativo RENTRI | 

## Example

```python
from rentri_dati_registri.models.dati_riferimenti_base_model_numero_registrazione import DatiRiferimentiBaseModelNumeroRegistrazione

# TODO update the JSON string below
json = "{}"
# create an instance of DatiRiferimentiBaseModelNumeroRegistrazione from a JSON string
dati_riferimenti_base_model_numero_registrazione_instance = DatiRiferimentiBaseModelNumeroRegistrazione.from_json(json)
# print the JSON string representation of the object
print(DatiRiferimentiBaseModelNumeroRegistrazione.to_json())

# convert the object into a dict
dati_riferimenti_base_model_numero_registrazione_dict = dati_riferimenti_base_model_numero_registrazione_instance.to_dict()
# create an instance of DatiRiferimentiBaseModelNumeroRegistrazione from a dict
dati_riferimenti_base_model_numero_registrazione_from_dict = DatiRiferimentiBaseModelNumeroRegistrazione.from_dict(dati_riferimenti_base_model_numero_registrazione_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


