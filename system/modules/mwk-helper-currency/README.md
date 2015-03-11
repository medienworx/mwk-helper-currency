# mwk-helper-currency
===============================

### Dokumentation
-----------------------------

**Anleitung:**

In deiner DCA-Datei oberhalb von ```$GLOBALS ['TL_DCA]...``` wird der Pfad zur Lang-Datei ```\System::loadLanguageFile('currency_short');``` eingefügt:


Bei einem z.B. **SELECT Menü** im DCA-File unter Fields bei ```'options' ``` 
wird als Wert ```&$GLOBALS['TL_LANG']['CUR_SHORT'],``` eingebunden, 
die Währungen werden jetzt über die Lang-Datei geladen.


BEISPIEL:
```
'name' => array
		(
			'label'                 => &$GLOBALS['TL_LANG']['tabellenname']['name'],
			'inputType'             => 'select',
			'options'               => &$GLOBALS['TL_LANG']['CUR_SHORT'],
			'eval'                  => array
			(
				'includeBlankOption'=>true,
				'mandatory'=>true,
				'chosen'=>true,
				'tl_class'=>'w50',
			),
			'sql'                   => "varchar(3) NOT NULL default ''",
		),
```
		
-----------------------------

### Systeminformationen
-----------------------------

Contao 3.2.x oder höher.

-----------------------------

Lizenz: LGPL