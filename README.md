# Index of Place Names 2012

This is a cache (with CSV version) of the Office for National Statistics [Index of Place Names](https://geoportal.statistics.gov.uk/geoportal/catalog/search/resource/details.page?uuid=%7BCDE30768-6419-4730-B434-B8B46BF9CBB1%7D)

## Converting the .accdb file

For reference, this is how I converted the accdb file to CSV:

```
brew install mdbtools
mdb-tables IPN2012.accdb #=> "IPN 2012"
mdb-export IPN2012.accdb IPN\ 2012 > IPN2012.CSV
```

## Table Structure

| Field Headings | Field Description                                                                     | Field Length | Field Type | Field Values                                                                |
|----------------|---------------------------------------------------------------------------------------|--------------|------------|-----------------------------------------------------------------------------|
| PLACE12NM      | Place name                                                                            | 57           | Text       | Full textual name                                                           |
| POPCNT         | Population count (based on 2011 OA ‘bestfit’ population)                              | 8            | Numeric    | Numeric or blank                                                            |
| DESCNM         | Record description                                                                    | 5            | Text       | COM, CTY, GOR, LOC, LONB, MD, NMD, NPARK, PAR, SETT, UA, URB, URBSD, WD,    |
| CTY12CD        | County code                                                                           | 9            | Character  | E10XXXXXX or blank                                                          |
| CTY12CDO       | ‘Old’ style county code                                                               | 2            | Numeric    | 2 numeric or blank                                                          |
| CTY12NM        | County name                                                                           | 30           | Character  | Full textual name or blank                                                  |
| NMD12CD        | Non metropolitan district code                                                        | 9            | Character  | E07XXXXXX or blank                                                          |
| NMD12CDO       | ‘Old’ style non metropolitan district code                                            | 4            | Character  | 2 numeric, 2 alpha or blank                                                 |
| NMD12NM        | Non metropolitan district name                                                        | 30           | Character  | Full textual name or blank                                                  |
| UA12CD         | Unitary authority code (England)                                                      | 9            | Character  | E06XXXXXX or blank                                                          |
| UA12CD         | Unitary authority code (Wales)                                                        | 9            | Character  | W06XXXXXX or blank                                                          |
| UA12CDO        | ‘Old’ style unitary authority code                                                    | 4            | Character  | 00 and 2 alpha or blank                                                     |
| UA12NM         | Unitary authority name                                                                | 30           | Character  | Full textual name or blank                                                  |
| MD12CD         | Metropolitan district code                                                            | 9            | Character  | E08XXXXXX or blank                                                          |
| MD12CDO        | ‘Old’ style metropolitan district code                                                | 4            | Character  | 00 and 2 alpha or blank                                                     |
| MD12NM         | Metropolitan district name                                                            | 20           | Character  | Full textual name or blank                                                  |
| LONB12CD       | London borough code                                                                   | 9            | Character  | E09XXXXXX                                                                   |
| LONB12CDO      | ‘Old’ style London borough code                                                       | 4            | Character  | 00 and 2 alpha or blank                                                     |
| LONB12NM       | London borough name                                                                   | 23           | Character  | Full textual name or blank                                                  |
| WD12CD         | Ward/electoral division code (England)                                                | 9            | Character  | E05XXXXXX or blank                                                          |
| WD12CD         | Electoral division code (Wales)                                                       | 9            | Character  | W05XXXXXX or blank                                                          |
| WD12CDO        | ‘Old’ style ward/electoral division code                                              | 6            | Character  | 2 numeric, 4 alpha or blank                                                 |
| HLTH12CD       | Strategic health authority code (England)                                             | 9            | Character  | E18XXXXXX or blank                                                          |
| HLTH12CD       | Local health board code (Wales)                                                       | 9            | Character  | W11XXXXXX or blank                                                          |
| HLTH12CDO      | ‘Old’ style strategic health authority code (England) local health board code (Wales) | 3            | Character  | SHA - Q and 2 numeric or blank LHB - 1 numeric, 1 alpha, 1 numeric or blank |
| HLTH12NM       | Strategic health authority name (England) local health board name (Wales)             | 30           | Character  | Full textual name or blank                                                  |
| REGD12CD       | Registration district code (England)                                                  | 9            | Character  | E28XXXXXX or blank                                                          |
| REGD12CD       | Registration district code (Wales)                                                    | 9            | Character  | W20XXXXXX or blank                                                          |
| REGD12CDO      | ‘Old’ style registration district code (England and Wales)                            | 3            | Character  | 3 numeric or blank                                                          |
| REGD12NM       | Registration district name                                                            | 35           | Character  | Full textual name or blank                                                  |
| GOR10CD        | Government office region code (England)                                               | 9            | Character  | E12XXXXXX or blank                                                          |
| GOR10CDO       | ‘Old’ style government office region code (England)                                   | 1            | Character  | 1 alpha or blank                                                            |
| GOR10CDO       | ‘Old’ style government office region code (Wales)                                     | 1            | Character  | ‘Pseudo’ code – W or blank                                                  |
| GOR10NM        | Government office region name                                                         | 25           | Character  | Full textual name or blank                                                  |
| NPARK12CD      | National park code (England)                                                          | 9            | Character  | E26XXXXXX or blank                                                          |
| NPARK12CD      | National park code (Wales)                                                            | 9            | Character  | W18XXXXXX or blank                                                          |
| NPARK12CDO     | ‘Old’ style national park code (England and Wales)                                    | 2            | Character  | 2 numeric or blank                                                          |
| NPARK12NM      | National park name                                                                    | 33           | Character  | Full textual name or blank                                                  |
| BUA11CD        | Built up area code                                                                    | 9            | Character  | E34XXXXXX or blank                                                          |
| PCON12CD       | Parliamentary constituency code (England)                                             | 9            | Character  | E14XXXXXX or blank                                                          |
| PCON12CD       | Parliamentary constituency code (Wales)                                               | 9            | Character  | W07XXXXXX or blank                                                          |
| PCON12CDO      | ‘Old’ style parliamentary constituency code (England and Wales)                       | 3            | Character  | 1 alpha and 2 numeric or blank                                              |
| PCON12NM       | Parliamentary constituency name                                                       | 39           | Character  | Full textual name or blank                                                  |
| EER12CD        | European electoral region code (England)                                              | 9            | Character  | E15XXXXXX or blank                                                          |
| EER12CD        | European electoral region code (Wales)                                                | 9            | Character  | W08XXXXXX or blank                                                          |
| EER12CDO       | ‘Old’ style European electoral region code (England and Wales)                        | 2            | Character  | 2 numeric or blank                                                          |
| EER12NM        | European electoral region name                                                        | 25           | Character  | Full textual name or blank                                                  |
| GRIDGB1        | 1metre grid reference                                                                 | 12           | Numeric    | 12 numeric or blank                                                         |
| GRIDGB1E       | 1 metre Easting grid reference                                                        | 6            | Numeric    | 6 numeric or blank                                                          |
| GRIDGB1N       | 1 metre Northing grid reference                                                       | 6            | Numeric    | 6 numeric or blank                                                          |
| GRID1KM        | 1 kilometre grid reference                                                            | 6            | Character  | 2 numeric, 4 alpha or blank                                                 |
| PAR12CD        | Civil parish code (England)                                                           | 9            | Character  | E04XXXXXX or blank                                                          |
| PAR12CD        | Community code (Wales)                                                                | 9            | Character  | W04XXXXXX or blank                                                          |
| PAR12CDO       | ‘Old’ style civil parish / community code (England and Wales)                         | 7            | Character  | 2 numeric, 2 alpha, 3 numeric or blank                                      |
