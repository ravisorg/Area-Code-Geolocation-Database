# Area-Code-Geolocation-Database

Area Codes for North America with city, state, latitude and longitude in easy to read CSV format.

This data pairs up NPA (area) codes with one or more cities, as well as a latitude / longitude pair. 

There have been a number of times where I wanted to be able to map (roughly) where a phone number was, or to find "nearby" numbers. This seems to be a fairly rare thing to do, as it's much harder to find area code data than it is to find (eg) zip code data. There are commercial versions out there that cost anywhere from a hundred dollars to well over a thousand, on an ongoing/subscription basis. It seemed silly to pay that much money for for public data, so I finally sat down and used that public data to compile a list that could be shared. No commercial products were used when compiling these documents, all sources are listed below if you wish to verify that. A fair amount of data cleansing was done to match everything up and (hopefully) end up with useful / authoritative city and state/province names.

Keep in mind that area codes do not guarantee a location, since numbers can easily be ported across the country. It does give a good indication of where the number was originally assigned, however, and in most cases probably indicates the rough location of the number.

I am, of course, trusting that the sources I used were "accurate". It's possible (likely even) that there are errors. Please do not use this data to dispatch ambulances and fire trucks.

## File Formats

Files begin with the country code (currently the United States and Canada) and are all UTF-8 encoded CSVs. Pretty much anything should be able to open them, including random text editors and your favorite programming language.

### Field Lists

#### xx-area-code-cities.csv

1. Area Code
2. City Name
3. Province/State Name
4. Country Code
5. Latitude (of the city)
6. Longitude (of the city)

#### xx-area-code-geo.csv

1. Area Code
2. Latitude (average of the cities using this code)
3. Longitude (average of the cities using this code)

## Sources

US/American area code listings were pulled from NANPA (North American Numbering Plan) at http://www.nationalnanpa.com/reports/area_code_relief_planning.html, field definitions can be found at http://www.nationalnanpa.com/area_codes/AreaCodeDatabaseDefinitions.xls. More information on these files is available at http://www.nationalnanpa.com/area_codes/index.html. The cities in each area code were queried from the form at http://www.nanpa.com/enas/npa_city_query.do.

Canadian area codes were pulled from the CNA (Canadian Numbering Administrator) at http://www.cnac.ca/data/COCodeStatus_ALL.zip. More information on this file is available at http://www.cnac.ca/co_codes/co_code_status.htm.

Geolocation data (specifically, the coordinates of each city) was pulled from Geonames at http://download.geonames.org/export/dump/cities5000.zip. More information on that file is available at http://download.geonames.org/export/dump/.

Proper (accented) state and province data is somehow unavailble from Geonames. Fortunately Tony Showoff compiled a list at http://tonyshowoff.com/files/supplement/geonames/admin1Codes.txt. More information is available at http://tonyshowoff.com/articles/geonames-the-only-terrible-choice-we-have/.

Alternate province / state short names / codes pulled from http://englishplus.com/grammar/00000057.htm.

## License

You are free to use this compilation for any purpose (commercial or not). I believe (although cannot provide a legal guarantee) that the data used while compiling these files is public domain.
