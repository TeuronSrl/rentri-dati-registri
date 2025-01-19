# EsitoValidaRegistroModel

Esito validazione strutturale del registro cronologico di carico e scarico digitale in formato XML.   L'array ```validazione``` contiene i codici di errore e/o avvertimento relativi alla validazione del file XML.  I messaggi relativi ai codici di errori sono recuperabili dall'API di codifica ```GET /codifiche/v1.0/codici-errore```  E' presente anche l'array ```parametri``` personalizzato in base al ```codice_messaggio```:  - ```xmlRegistro.fileXmlNonValidoDettaglio```    - 1️⃣ stringa con il dettaglio dell'errore riscontrato nel file XML    - 2️⃣ array di oggetti con le seguenti proprietà:      - ```linea```: numero di riga del file XML      - ```posizione```: posizione all'interno della riga del file XML      - ```tipo```: tipo di errore riscontrato (```Errore, Avviso```)      - ```messaggio```: messaggio di errore riscontrato  - ```xmlRegistro.firmaVidimazioneRegistroNonValidaDettaglio``` o ```xmlRegistro.firmaNonValidaDettaglio```    - 1️⃣ stringa con il dettaglio dell'errore riscontrato nella firma    - 2️⃣ array di oggetti con le seguenti proprietà:      - ```codice```: codice dell'errore riscontrato nella firma (```ErroreNonDefinito, CertificatoScaduto, CertificatoRevocato, CertificatoAuthorityScaduto, AuthorityNonRiconosciuta, CertificatoNonAbilitato, FirmaCertificatoNonValida, CRLNonDisponibile, ErroreInterno, FirmaFileNonValida, AuthorityListNonDisponibile, CertificatoNonRiconosciuto, CertificatoNonDiFirma, FileNonFirmatoConSHA256, AuthoritySenzaCountryName```)      - ```messaggio```: messaggio di errore riscontrato nella firma  - ```xmlRegistro.datiMovimentoNonValidi```    - 1️⃣ stringa contenente l'anno e il progressivo del movimento non valido    - 2️⃣ oggetto con le seguenti proprietà:      - ```anno```: anno del movimento non valido      - ```progressivo```: progressivo del movimento non valido      - ```validazione```: array di oggetti con le seguenti proprietà:        - ```campo```: campo del movimento non valido        - ```messaggio```: codice del messaggio di errore riscontrato  - ```xmlRegistro.numeroRegistrazioniNonCorrispondente```, ```xmlRegistro.progressivoDaNonCorrispondente```, ```xmlRegistro.progressivoANonCorrispondente```, ```xmlRegistro.presentiSaltiNeiProgressivi```    - 1️⃣ numero dell'elemento \"Registrazioni\" dove si riscontra la problematica.  - ```xmlRegistro.datiMovimentoNonCorrispondenti```    - 1️⃣ stringa contenente l'anno e il progressivo del movimento non corrispondente    - 2️⃣ oggetto con le seguenti proprietà:      - ```anno```: anno del movimento non corrispondente      - ```progressivo```: progressivo del movimento non corrispondente      - ```campi_non_corrispondenti```: lista di stringhe corrispondenti a campi relativi agli elementi XML dove si riscontra la non corrispondenza dei dati  - ```xmlRegistro.registrazioniDaEsportare``` o ```xmlRegistro.registrazioniNonInRentri```    - 1️⃣ stringa contenente l'anno e il progressivo iniziale    - 2️⃣ stringa contenente l'anno e il progressivo finale    - 3️⃣ oggetto con le seguenti proprietà:      - ```anno```: anno del movimento      - ```progressivo_da```: progressivo iniziale del movimento      - ```progressivo_a```: progressivo finale del movimento 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**esito** | [**EsitoValidaRegistroDataModel**](EsitoValidaRegistroDataModel.md) | Dati dell&#39;esito validazione | [optional] 
**transazione_id** | **str** | Identificativo della transazione asincrona | [optional] 
**validazione** | [**List[EsitoMessaggioModel]**](EsitoMessaggioModel.md) | Messaggi di validazione | [optional] 
**errore** | **bool** |  | [optional] [readonly] 
**tempo_elaborazione** | **str** |  | [optional] 

## Example

```python
from rentri_dati_registri.models.esito_valida_registro_model import EsitoValidaRegistroModel

# TODO update the JSON string below
json = "{}"
# create an instance of EsitoValidaRegistroModel from a JSON string
esito_valida_registro_model_instance = EsitoValidaRegistroModel.from_json(json)
# print the JSON string representation of the object
print(EsitoValidaRegistroModel.to_json())

# convert the object into a dict
esito_valida_registro_model_dict = esito_valida_registro_model_instance.to_dict()
# create an instance of EsitoValidaRegistroModel from a dict
esito_valida_registro_model_from_dict = EsitoValidaRegistroModel.from_dict(esito_valida_registro_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


