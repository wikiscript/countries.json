#  `countries.json` - World Country Profiles Sourced from Wikipedia's Country Page Infoboxes Converted into JSON


What are Wikipedia's Country Page Infoboxes?

Every country page on Wikipedia has on the
right-hand side a "floating" infobox about
facts. Example in original Wikitext/script source
(simplified w/o references):

```
{{Infobox country
| conventional_long_name = Republic of Austria
| common_name            = Austria
| native_name            = Republik Österreich (German)
| image_flag             = Flag of Austria.svg
| image_coat             = Austria Bundesadler.svg
| national_motto         =
| national_anthem        = [[National anthem of Austria|Bundeshymne der Republik Österreich]] (German)
                           (English "National Anthem of the Republic of Austria")
                           Land der Berge Land am Strome instrumental.ogg
| image_map              = EU-Austria.svg
| map_caption            = {{map ... EU-Austria.svg}}
| capital                = [[Vienna]]
| coordinates            = {{Coord|48|12|N|16|21|E}}
| largest_city           = capital
| languages              = [[German language|German]]
| languages_type         = [[Official language]] and [[national language]]
| languages2             = [[Hungarian language|Hungarian]],
                           [[Slovene language|Slovene]]
                           [[Burgenland Croatian]]
| languages2_type        = Recognised languages
| ethnic_groups          = 81.1% [[Austrians]]
                            6.3% Ex-[[Yugoslavs]]
                            2.7% [[Germans]]
                            2.2% [[Turks in Austria|Turks]]
                            8.7% Other
| ethnic_groups_year     = 2012
| religion_year          = 2018
| religion               = 69.0% [[Christianity]]
                            —57.0% [[Catholic Church in Austria|Catholicism]]
                            —8.7% [[Eastern Orthodox Church|Eastern Orthodoxy]]
                            —3.3% Other [[List of Christian denominations|Christian]]
                           22.0% [[Irreligion|No religion]]
                            7.9% [[Islam in Austria|Islam]]
                            1.1% [[Religion in Austria|Other]]
| demonym                  = [[Austrians|Austrian]]
| government_type          = [[Federal republic|Federal]] [[parliamentary republic]]
| leader_title1            = [[President of Austria|President]]
| leader_name1             = [[Alexander Van der Bellen]]
| leader_title2            = [[Chancellor of Austria|Chancellor]]
| leader_name2             = [[Sebastian Kurz]]
| leader_title3            = [[Vice Chancellor of Austria|Vice Chancellor]]
| leader_name3             = [[Werner Kogler]]
| legislature              = [[Austrian Parliament|Parliament]]
| upper_house              = [[Federal Council (Austria)|Federal Council]]
| lower_house              = [[National Council (Austria)|National Council]]
| sovereignty_type         = Establishment history
| established_event1       = [[Margraviate of Austria]]
| established_date1        = 976
| established_event2       = [[Duchy of Austria]]
| established_date2        = 1156
| established_event3       = [[Archduchy of Austria]]
| established_date3        = 1453
| established_event4       = [[Austrian Empire]]
| established_date4        = 1804
| established_event5       = [[Austria-Hungary|Austro-Hungarian Empire]]
| established_date5        = 1867
| established_event6       = [[First Republic of Austria|First Republic]]
| established_date6        = 1918
| established_event7       = [[Federal State of Austria|Federal State]]
| established_date7        = 1934
| established_event8       = [[Anschluss]]
| established_date8        = 1938
| established_event9       = [[Second Austrian Republic|Second Republic]]
| established_date9        = since 1945
| established_event10      = [[Austrian State Treaty|State Treaty]] in effect
| established_date10       = 27 July 1955
| established_event11      = [[United Nations Security Council Resolution 109|Admitted to the]] [[United Nations]]
| established_date11       = 14 December 1955
| established_event12      = [[1995 enlargement of the European Union|Joined]] the [[European Union]]
| established_date12       = 1 January 1995
| area_km2                 = 83,879
| area_rank                = 113th
| area_sq_mi               = 32,385.86
| percent_water            = 0.84 (as of 2015)
| population_estimate      = {{increase}} 8,902,600
| population_estimate_year = January 2020
| population_estimate_rank = 98th
| population_density_km2   = 106
| population_density_sq_mi = 262.6
| population_density_rank  = 106th
| GDP_PPP                  = $461.432 billion
| GDP_PPP_year             = 2018
| GDP_PPP_rank             =
| GDP_PPP_per_capita       = $51,936
| GDP_PPP_per_capita_rank  = 17th
| GDP_nominal              = $446,315 billion
| GDP_nominal_year         = 2019
| GDP_nominal_rank         = 27th
| GDP_nominal_per_capita   = $50,277
| GDP_nominal_per_capita_rank = 15th
| Gini                     = 27.5
| Gini_year                = 2019
| Gini_change              = increase
| Gini_rank = 14th
| HDI                      = 0.914
| HDI_year = 2018
| HDI_change               = increase
| HDI_rank                 = 20th
| currency                 = [[Euro]] ([[Euro sign|€]])
| currency_code            = EUR
| time_zone                = [[Central European Time|CET]]
| utc_offset               = +1
| utc_offset_DST           = +2
| time_zone_DST            = [[Central European Summer Time|CEST]]
| drives_on                = right
| calling_code             = [[Telephone numbers in Austria|+43]]
| cctld                    = [[.at]]
}}
```

(Source: [Austria's "Raw" Page Source @ Wikipedia ](https://en.wikipedia.org/w/index.php?title=Austria&action=raw))


That gets via the [wikiscript/text parser](https://github.com/wikiscript/wikiscript) turned
into a JSON datasets for easy (re)use
resulting in:

```json
{
  "conventional_long_name": "Republic of Austria",
  "common_name": "Austria",
  "native_name": "Republik Österreich (German)",
  "image_flag": "Flag of Austria.svg",
  "image_coat": "Austria Bundesadler.svg",
  "national_anthem": "Bundeshymne der Republik Österreich (German),
                      (English: \"National Anthem of the Republic of Austria\")",
  "image_map": "EU-Austria.svg",
  "map_caption": "Europe",
  "capital": "Vienna",
  "coordinates": "48°12'N, 16°21'E",
  "largest_city": "capital",
  "languages": "German",
  "languages_type": "Official language and national language",
  "languages2": "Hungarian, Slovene, Burgenland Croatian",
  "languages2_type": "Recognised languages",
  "ethnic_groups": "81.1% Austrians,
                     6.3% Ex-Yugoslavs,
                     2.7% Germans,
                     2.2% Turks,
                     8.7% Other",
  "ethnic_groups_year": "2012",
  "religion_year": "2018",
  "religion": "69.0% Christianity,
                —57.0% Catholicism,
                —8.7% Eastern Orthodoxy,
                —3.3% Other Christian,
               22.0% No religion,
                7.9% Islam,
                1.1% Other",
  "demonym": "Austrian",
  "government_type": "Federal parliamentary republic",
  "leader_title1": "President",
  "leader_name1": "Alexander Van der Bellen",
  "leader_title2": "Chancellor",
  "leader_name2": "Sebastian Kurz",
  "leader_title3": "Vice Chancellor",
  "leader_name3": "Werner Kogler",
  "legislature": "Parliament",
  "upper_house": "Federal Council",
  "lower_house": "National Council",
  "sovereignty_type": "Establishment history",
  "established_event1": "Margraviate of Austria",
  "established_date1": "976",
  "established_event2": "Duchy of Austria",
  "established_date2": "1156",
  "established_event3": "Archduchy of Austria",
  "established_date3": "1453",
  "established_event4": "Austrian Empire",
  "established_date4": "1804",
  "established_event5": "Austro-Hungarian Empire",
  "established_date5": "1867",
  "established_event6": "First Republic",
  "established_date6": "1918",
  "established_event7": "Federal State",
  "established_date7": "1934",
  "established_event8": "Anschluss",
  "established_date8": "1938",
  "established_event9": "Second Republic",
  "established_date9": "since 1945",
  "established_event10": "State Treaty in effect",
  "established_date10": "27 July 1955",
  "established_event11": "Admitted to the United Nations",
  "established_date11": "14 December 1955",
  "established_event12": "Joined the European Union",
  "established_date12": "1 January 1995",
  "area_km2": "83,879",
  "area_rank": "113th",
  "area_sq_mi": "32,385.86",
  "percent_water": "0.84 (as of 2015)",
  "population_estimate": "(increase) 8,902,600",
  "population_estimate_year": "January 2020",
  "population_estimate_rank": "98th",
  "population_density_km2": "106",
  "population_density_sq_mi": "262.6",
  "population_density_rank": "106th",
  "GDP_PPP": "$461.432 billion",
  "GDP_PPP_year": "2018",
  "GDP_PPP_per_capita": "$51,936",
  "GDP_PPP_per_capita_rank": "17th",
  "GDP_nominal": "$446,315 billion",
  "GDP_nominal_year": "2019",
  "GDP_nominal_rank": "27th",
  "GDP_nominal_per_capita": "$50,277",
  "GDP_nominal_per_capita_rank": "15th",
  "Gini": "27.5",
  "Gini_year": "2019",
  "Gini_change": "increase",
  "Gini_rank": "14th",
  "HDI": "0.914",
  "HDI_year": "2018",
  "HDI_change": "increase",
  "HDI_rank": "20th",
  "currency": "Euro (€)",
  "currency_code": "EUR",
  "time_zone": "CET",
  "utc_offset": "+1",
  "utc_offset_DST": "+2",
  "time_zone_DST": "CEST",
  "drives_on": "right",
  "calling_code": "+43",
  "cctld": ".at"
}
```


Note: All country profiles always use the original wikipedia
page name - most of the time that's the name you kind of expect BUT
beware of some "outliers" with qualifiers (e.g. (country)) 
or with official names (e.g. Republic of ...) or even island collectives with commas (,) e.g.:


| Page     |  Dataset  |
|----------|-----------|
| [Austria](https://en.wikipedia.org/wiki/Austria) | => `Austria.json`  |
| [Belgium](https://en.wikipedia.org/wiki/Belgium) | => `Belgium.json` |
| [Georgia (country)](https://en.wikipedia.org/wiki/Georgia_(country)) | => `Georgia_(country).json` |
| [Republic of Ireland](https://en.wikipedia.org/wiki/Republic_of_Ireland) | => `Republic_of_Ireland.json` |
| [Archipelago of San Andrés, Providencia and Santa Catalina](https://en.wikipedia.org/wiki/Archipelago_of_San_Andrés,_Providencia_and_Santa_Catalina) | => `Archipelago_of_San_Andrés,_Providencia_and_Santa_Catalina.json` |

and so on.


...


## Build Your Own Up-to-Date Country Profiles

See the [`wikiscript`](https://github.com/wikiscript/wikiscript)
command line tool and scripts for details.



## Real-World Usage

Q: Anybody using these datasets?  I don't know really.

Add your project here - yes, you can!



## License

![](https://publicdomainworks.github.io/buttons/zero88x31.png)

The datasets and scripts are dedicated to the public domain. Use it as you please with no restrictions whatsoever.


## Questions? Comments?

Send them along to the [Open World Database (world.db) and Friends Forum/Mailing List](http://groups.google.com/group/openmundi).
Thanks!
