# EsitoValidaRegistroDataModel


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identificativo_registro** | **str** | Identificativo del registro | [optional] 
**num_iscr_operatore** | **str** | Numero di iscrizione dell&#39;operatore | [optional] 
**codice_fiscale_operatore** | **str** | Codice fiscale dell&#39;operatore | [optional] 
**denominazione_operatore** | **str** | Ragione sociale dell&#39;operatore | [optional] 
**num_iscr_soggetto_delegato** | **str** | Numero di iscrizione del soggetto delegato | [optional] 
**codice_fiscale_soggetto_delegato** | **str** | Codice fiscale del soggetto delegato | [optional] 
**denominazione_soggetto_delegato** | **str** | Ragione sociale del soggetto delegato | [optional] 
**num_iscr_sito** | **str** | Numero di iscrizione dell&#39;unità locale | [optional] 
**indirizzo_sito** | **str** | Indirizzo dell&#39;unità locale | [optional] 
**data_vidimazione** | **datetime** | Data di vidimazione del registro informatico | [optional] 
**cciaa** | **str** | Camera di commercio di appartenenza del registro informatico | [optional] 
**identificativo_firma** | **str** | Identificativo del soggetto che ha firmato il registro informatico | [optional] 
**denominazione_firma** | **str** | Denominazione del soggetto che ha firmato il registro informatico | [optional] 
**ca_firma** | **str** | CA della firma del soggetto che ha firmato il registro informatico | [optional] 
**firma_non_etsi** | **bool** | True se la firma non è XAdES | [optional] 
**numero_esportazioni_totali** | **int** | Numero totale di esportazioni effettuate | [optional] 
**numero_esportazioni_file** | **int** | Numero di esportazioni presenti nel file | [optional] 
**numero_registrazioni_file** | **int** | Numero di registrazioni presenti nel file | [optional] 
**numero_registrazioni_rentri** | **int** | Numero di registrazioni presenti in RENTRI | [optional] 
**numero_registrazioni_ultima_esportazione** | **int** | Numero di registrazioni presenti nell&#39;ultima esportazione | [optional] 
**data_ultima_esportazione** | **datetime** | Data dell&#39;ultima esportazione effettuata | [optional] 
**ultimo_anno_progressivo_esportato** | **str** | Ultimo progressivo esportato | [optional] 

## Example

```python
from rentri_dati_registri.models.esito_valida_registro_data_model import EsitoValidaRegistroDataModel

# TODO update the JSON string below
json = "{}"
# create an instance of EsitoValidaRegistroDataModel from a JSON string
esito_valida_registro_data_model_instance = EsitoValidaRegistroDataModel.from_json(json)
# print the JSON string representation of the object
print EsitoValidaRegistroDataModel.to_json()

# convert the object into a dict
esito_valida_registro_data_model_dict = esito_valida_registro_data_model_instance.to_dict()
# create an instance of EsitoValidaRegistroDataModel from a dict
esito_valida_registro_data_model_from_dict = EsitoValidaRegistroDataModel.from_dict(esito_valida_registro_data_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


