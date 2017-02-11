# Currencies

Currencies supported by Paylike

- AED (United Arab Emirates dirham)
- AFN (Afghan afghani)
- ALL (Albanian lek)
- AMD (Armenian dram)
- ANG (Netherlands Antillean guilder)
- AOA (Angolan kwanza)
- ARS (Argentine peso)
- AUD (Australian dollar)
- AWG (Aruban florin)
- AZN (Azerbaijani manat)
- BAM (Bosnia and Herzegovina convertible mark)
- BBD (Barbados dollar)
- BDT (Bangladeshi taka)
- BGN (Bulgarian lev)
- BHD (Bahraini dinar)
- BIF (Burundian franc)
- BMD (Bermudian dollar)
- BND (Brunei dollar)
- BOB (Boliviano)
- BRL (Brazilian real)
- BSD (Bahamian dollar)
- BTN (Bhutanese ngultrum)
- BWP (Botswana pula)
- BYR (Belarusian ruble)
- BZD (Belize dollar)
- CAD (Canadian dollar)
- CDF (Congolese franc)
- CHF (Swiss franc)
- CLP (Chilean peso)
- CNY (Chinese yuan)
- COP (Colombian peso)
- CRC (Costa Rican colon)
- CUP (Cuban peso)
- CVE (Cape Verde escudo)
- CZK (Czech koruna)
- DJF (Djiboutian franc)
- DKK (Danish krone)
- DOP (Dominican peso)
- DZD (Algerian dinar)
- EGP (Egyptian pound)
- ERN (Eritrean nakfa)
- ETB (Ethiopian birr)
- EUR (Euro)
- FJD (Fiji dollar)
- FKP (Falkland Islands pound)
- GBP (Pound sterling)
- GEL (Georgian lari)
- GHS (Ghanaian cedi)
- GIP (Gibraltar pound)
- GMD (Gambian dalasi)
- GNF (Guinean franc)
- GTQ (Guatemalan quetzal)
- GYD (Guyanese dollar)
- HKD (Hong Kong dollar)
- HNL (Honduran lempira)
- HRK (Croatian kuna)
- HTG (Haitian gourde)
- HUF (Hungarian forint)
- IDR (Indonesian rupiah)
- ILS (Israeli new shekel)
- INR (Indian rupee)
- IQD (Iraqi dinar)
- IRR (Iranian rial)
- ISK (Icelandic króna)
- JMD (Jamaican dollar)
- JOD (Jordanian dinar)
- JPY (Japanese yen)
- KES (Kenyan shilling)
- KGS (Kyrgyzstani som)
- KHR (Cambodian riel)
- KMF (Comoro franc)
- KPW (North Korean won)
- KRW (South Korean won)
- KWD (Kuwaiti dinar)
- KYD (Cayman Islands dollar)
- KZT (Kazakhstani tenge)
- LAK (Lao kip)
- LBP (Lebanese pound)
- LKR (Sri Lankan rupee)
- LRD (Liberian dollar)
- LSL (Lesotho loti)
- MAD (Moroccan dirham)
- MDL (Moldovan leu)
- MGA (Malagasy ariary)
- MKD (Macedonian denar)
- MMK (Myanmar kyat)
- MNT (Mongolian tögrög)
- MOP (Macanese pataca)
- MRO (Mauritanian ouguiya)
- MUR (Mauritian rupee)
- MVR (Maldivian rufiyaa)
- MWK (Malawian kwacha)
- MXN (Mexican peso)
- MYR (Malaysian ringgit)
- MZN (Mozambican metical)
- NAD (Namibian dollar)
- NGN (Nigerian naira)
- NIO (Nicaraguan córdoba)
- NOK (Norwegian krone)
- NPR (Nepalese rupee)
- NZD (New Zealand dollar)
- OMR (Omani rial)
- PAB (Panamanian balboa)
- PEN (Peruvian Sol)
- PGK (Papua New Guinean kina)
- PHP (Philippine peso)
- PKR (Pakistani rupee)
- PLN (Polish złoty)
- PYG (Paraguayan guaraní)
- QAR (Qatari riyal)
- RON (Romanian leu)
- RSD (Serbian dinar)
- RUB (Russian ruble)
- RWF (Rwandan franc)
- SAR (Saudi riyal)
- SBD (Solomon Islands dollar)
- SCR (Seychelles rupee)
- SDG (Sudanese pound)
- SEK (Swedish krona)
- SGD (Singapore dollar)
- SHP (Saint Helena pound)
- SLL (Sierra Leonean leone)
- SOS (Somali shilling)
- SRD (Surinamese dollar)
- STD (São Tomé and Príncipe dobra)
- SYP (Syrian pound)
- SZL (Swazi lilangeni)
- THB (Thai baht)
- TJS (Tajikistani somoni)
- TMT (Turkmenistani manat)
- TND (Tunisian dinar)
- TOP (Tongan paʻanga)
- TRY (Turkish lira)
- TTD (Trinidad and Tobago dollar)
- TWD (New Taiwan dollar)
- TZS (Tanzanian shilling)
- UAH (Ukrainian hryvnia)
- UGX (Ugandan shilling)
- USD (United States dollar)
- UYU (Uruguayan peso)
- UZS (Uzbekistan som)
- VEF (Venezuelan bolívar)
- VND (Vietnamese dong)
- VUV (Vanuatu vatu)
- WST (Samoan tala)
- XAF (CFA franc BEAC)
- XCD (East Caribbean dollar)
- XOF (CFA franc BCEAO)
- XPF (CFP franc)
- YER (Yemeni rial)
- ZAR (South African rand)
- ZMK (Zambian kwacha)
- ZWL (Zimbabwean dollar)

## Funding currencies

These are the currencies you can use as a base for your account, the so called
funding currency.

### Global

- EUR (Euro)
- USD (United States dollar)
- GBP (British pound sterling)

### Nordic

- DKK (Danish krone)
- NOK (Norwegian krone)
- SEK (Swedish krona)

## Usage

Pin the dependency to the current version branch to ensure future installs of
your application will work. Like so:

```json
"dependencies": {
	"@paylike/currencies": "^1.0.0"
}
```

```js
var currencies = require('@paylike/currencies');

currencies;
/*
[
	{
		code: 'AED',
		currency: 'United Arab Emirates dirham',
		numeric: '784',
		exponent: 2,
	},
	...
	{
		code: 'DKK',
		currency: 'Danish krone',
		numeric: '208',
		exponent: 2,
		funding: true,
	},
	...
]
*/

// lookup by code
var currencies = require('@paylike/currencies');

currencies.byCode('AED');
// { code: 'AED', currency: 'United Arab Emirates dirham', numeric: '784' }

currencies.byCode();
	// Map()

// list supported funding currencies
currencies
	.filter(x => x.funding)
	.map(x => x.currency);
/*
[
	'Danish krone',
	'Euro',
	'Pound sterling',
	'Norwegian krone',
	'Swedish krona',
	'United States dollar',
]
*/
```
