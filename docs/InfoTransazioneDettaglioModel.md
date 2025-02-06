# InfoTransazioneDettaglioModel


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identificativo** | **str** |  | [optional] 
**tipo** | [**TipoTransazione**](TipoTransazione.md) |  | [optional] 
**identificativo_precedente** | **str** |  | [optional] 
**data_trasmissione** | **datetime** |  | [optional] 
**identificativo_entita** | **str** |  | [optional] 
**data_inizio_elaborazione** | **datetime** |  | [optional] 
**data_fine_elaborazione** | **datetime** |  | [optional] 
**status_code_push** | **int** |  | [optional] 
**data_push** | **datetime** |  | [optional] 
**data_ultimo_pull** | **datetime** |  | [optional] 
**stato** | [**StatoTransazione**](StatoTransazione.md) |  | [optional] 
**sorgente** | [**SorgenteTransazione**](SorgenteTransazione.md) |  | [optional] 
**endpoint** | **str** |  | [optional] 
**identificativo_firmatario** | **str** |  | [optional] 
**num_iscr_operatore** | **str** |  | [optional] 
**identificativo_operatore** | **str** |  | [optional] 
**denominazione_operatore** | **str** |  | [optional] 
**num_iscr_sito** | **str** |  | [optional] 
**sito_comune_id** | **str** |  | [optional] 
**sito_provincia_id** | **str** |  | [optional] 
**sito_indirizzo** | **str** |  | [optional] 
**sito_civico** | **str** |  | [optional] 
**movimenti_info** | [**List[MovimentoInfoModel]**](MovimentoInfoModel.md) |  | [optional] 

## Example

```python
from rentri_dati_registri.models.info_transazione_dettaglio_model import InfoTransazioneDettaglioModel

# TODO update the JSON string below
json = "{}"
# create an instance of InfoTransazioneDettaglioModel from a JSON string
info_transazione_dettaglio_model_instance = InfoTransazioneDettaglioModel.from_json(json)
# print the JSON string representation of the object
print InfoTransazioneDettaglioModel.to_json()

# convert the object into a dict
info_transazione_dettaglio_model_dict = info_transazione_dettaglio_model_instance.to_dict()
# create an instance of InfoTransazioneDettaglioModel from a dict
info_transazione_dettaglio_model_from_dict = InfoTransazioneDettaglioModel.from_dict(info_transazione_dettaglio_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


