# VeicoloFuoriUsoRegPubblicaSicurezzaModel

Registro pubblica sicurezza

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**numero** | **str** | Numero reg. pubblica sicurezza | 
**data** | **datetime** | Data reg. pubblica sicurezza (formato ISO 8601 UTC) | [optional] 

## Example

```python
from rentri_dati_registri.models.veicolo_fuori_uso_reg_pubblica_sicurezza_model import VeicoloFuoriUsoRegPubblicaSicurezzaModel

# TODO update the JSON string below
json = "{}"
# create an instance of VeicoloFuoriUsoRegPubblicaSicurezzaModel from a JSON string
veicolo_fuori_uso_reg_pubblica_sicurezza_model_instance = VeicoloFuoriUsoRegPubblicaSicurezzaModel.from_json(json)
# print the JSON string representation of the object
print(VeicoloFuoriUsoRegPubblicaSicurezzaModel.to_json())

# convert the object into a dict
veicolo_fuori_uso_reg_pubblica_sicurezza_model_dict = veicolo_fuori_uso_reg_pubblica_sicurezza_model_instance.to_dict()
# create an instance of VeicoloFuoriUsoRegPubblicaSicurezzaModel from a dict
veicolo_fuori_uso_reg_pubblica_sicurezza_model_from_dict = VeicoloFuoriUsoRegPubblicaSicurezzaModel.from_dict(veicolo_fuori_uso_reg_pubblica_sicurezza_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


