# DatiRespingimentoModel

Respingimento

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tipo** | [**TipiRespingimento**](TipiRespingimento.md) | Tipologia di respingimento  Vedi API di codifica: &lt;i&gt;GET /codifiche/v1.0/tipi-respingimento&lt;/i&gt;&lt;p&gt;Valori ammessi:&lt;ul style&#x3D;\&quot;margin:0\&quot;&gt;&lt;li&gt;&lt;i&gt;T&lt;/i&gt; - Totale&lt;/li&gt;&lt;li&gt;&lt;i&gt;P&lt;/i&gt; - Parziale&lt;/li&gt;&lt;/ul&gt;&lt;/p&gt; | 
**quantita** | [**UnitaMisuraQuantitaModel**](UnitaMisuraQuantitaModel.md) | Quantità respinta | [optional] 
**causale** | [**CausaliRespingimento**](CausaliRespingimento.md) | Causale del respingimento  Vedi API di codifica: &lt;i&gt;GET /codifiche/v1.0/causali-respingimento&lt;/i&gt;&lt;p&gt;Valori ammessi:&lt;ul style&#x3D;\&quot;margin:0\&quot;&gt;&lt;li&gt;&lt;i&gt;NC&lt;/i&gt; - Non Conformità, a titolo esemplificativo e non esaustivo, si riporta: rifiuti diverso da quello descritto dal formulario o da quanto dichiarato ai fini della pratica di conferimento all&#39;impianto, rifiuto confezionato in modo non conforme da quanto previsto per la specifica destinazione o dalle norme applicabili, di stato fisico diverso da quello previsto)&lt;/li&gt;&lt;li&gt;&lt;i&gt;IR&lt;/i&gt; - Irricevibile, (a titolo esemplificativo e non esaustivo, si riporta: rifiuto non previsto dall&#39;autorizzazione / iscrizione dell&#39;impianto di destino, mancanza dei requisiti per l&#39;ammissibilità all&#39;impianto quali caratterizzazione di base, analisi di classificazione o di ammissibilità…)&lt;/li&gt;&lt;li&gt;&lt;i&gt;A&lt;/i&gt; - Indicare motivazione. A titolo esemplificativo e non esaustivo, si riporta: esaurimento volumetria disponibile per conferimento rifiuto, chiusura impianto per manutenzione straordinaria, ecc.&lt;/li&gt;&lt;/ul&gt;&lt;/p&gt; | [optional] 
**causale_altro** | **str** | Altra tipologia di causale non prevista.  Richiesto solamente se causale è uguale a \&quot;A\&quot;. | [optional] 

## Example

```python
from rentri_dati_registri.models.dati_respingimento_model import DatiRespingimentoModel

# TODO update the JSON string below
json = "{}"
# create an instance of DatiRespingimentoModel from a JSON string
dati_respingimento_model_instance = DatiRespingimentoModel.from_json(json)
# print the JSON string representation of the object
print DatiRespingimentoModel.to_json()

# convert the object into a dict
dati_respingimento_model_dict = dati_respingimento_model_instance.to_dict()
# create an instance of DatiRespingimentoModel from a dict
dati_respingimento_model_from_dict = DatiRespingimentoModel.from_dict(dati_respingimento_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


