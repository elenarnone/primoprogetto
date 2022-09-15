# Pos Retail Standard

## Metodi

nella verticalizzazione di **pos retail standard** esistino dei metodi di caricamento del punto cassa all'interno di questa app.

I metodi sono sia **python** che **javascript**.

in questa classe di **python**  --> **src/user/pos_retail_standard/models/pos/PosCacheDatabase.py**
ci sono metodi che il punto cassa uitlizza per caricare sia i prodotti che l'anagrafica contatti.

1. il metodo che carica sia i prodotti che le anagrafiche nel punto cassa è **def install_data(self, model_name=None, min_id=0, max_id=1999)**, il quale fa una query su una tabella che si chiama **pos.call.log**
  

2. il metodo **js** è  **api_install_datas** e fa un query sul methodo **python** --> **install_data**

    da questo metodo passa sia il modello  **product.product** che **res.partner**

    è presente nel file **pos_retail_standard/static/src/js/Core/BigData.js** e viene richiamato da vari punti per caricare i dati nel punto di cassa