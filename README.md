# mwk-helper-currency
===============================

### Dokumentation
-----------------------------

Anleitung:

im DCA-File oberhalb Globals einbinden:

\System::loadLanguageFile('currency_short'); (wird das File geladen)

Bei einem SELECT Menü im DCA unter Fields:

'name' => array
		(
			'label'                 => &$GLOBALS['TL_LANG']['tl_mwk_test_currency']['name'],
			'exclude'               => true,
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



-----------------------------

### Systeminformationen
-----------------------------

Contao 3.2.x oder höher.

-----------------------------

Lizenz: LGPL
