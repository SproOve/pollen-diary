# Pollen Diary

Track your hay fever and other symptoms and check the given pollen data, which is surrounding you. The purpose of this is, that even if there are a lot of Pollen-Apps or Weather-Apps containing pollen data, there is no real diary type of this data where you can track, how severe your symptoms were and compare it to the given data. By tracking the symptoms we can get to a conclusion, which type of pollen is the most to fear individually - basically a self diagnosis, what you are allergic to.
Everyone taking cetirizin or loratadin knows, that you have to take it usually 24 hours before this medicine actually helps, plus there are some of us, who actually dont want to take it from March to November every day or sometimes forget to take them.

## Setup

1. Edit your config depending on the region, you're living in (see below).
2. Get this service to run at least daily. There are several ways to achive this. Here are some examples :
   - use pyinstaller and run the executable as a service
   - use pyinstaller and add it to autostart (Windows) on a computer, you start (nearly) daily
   - start it on a alltime-online raspberry-pi or other linux server
3. Open the .xlsx file every time, you get symptoms and type the severity of it and if you've taken medicine like cetirizin or loratadin in the corresponding fields
4. After some time you can maybe find a pattern, which pollen is the most conspicuous and prepare yourself by taking the medicine only in the time-frames, where you need it

## `region_id` and `partregion_id`

Available Region ids. If issues occur, compare the original list from the API owner on

https://github.com/ekeih/dwdpollen

| Region                         | `region_id` | Partregion                                         | `partregion_id` |
| ------------------------------ | ----------- | -------------------------------------------------- | --------------- |
| Schleswig-Holstein und Hamburg | 10          | Inseln und Marschen                                | 11              |
|                                |             | Geest, Schleswig-Holstein und Hamburg              | 12              |
| Mecklenburg-Vorpommern         | 20          |                                                    | -1              |
| Niedersachsen und Bremen       | 30          | Westl. Niedersachsen/Bremen                        | 31              |
|                                |             | Östl. Niedersachsen                                | 32              |
| Nordrhein-Westfalen            | 40          | Rhein.-Westfäl. Tiefland                           | 41              |
|                                |             | Ostwestfalen                                       | 42              |
|                                |             | Mittelgebirge NRW                                  | 43              |
| Brandenburg und Berlin         | 50          |                                                    | -1              |
| Sachsen-Anhalt                 | 60          | Tiefland Sachsen-Anhalt                            | 61              |
|                                |             | Harz                                               | 62              |
| Thüringen                      | 70          | Tiefland Thüringen                                 | 71              |
|                                |             | Mittelgebirge Thüringen                            | 72              |
| Sachsen                        | 80          | Tiefland Sachsen                                   | 81              |
|                                |             | Mittelgebirge Sachsen                              | 82              |
| Hessen                         | 90          | Nordhessen und hess. Mittelgebirge                 | 91              |
|                                |             | Rhein-Main                                         | 92              |
| Rheinland-Pfalz und Saarland   | 100         | Saarland                                           | 103             |
|                                |             | Rhein, Pfalz, Nahe und Mosel                       | 101             |
|                                |             | Mittelgebirgsbereich Rheinland-Pfalz               | 102             |
| Baden-Württemberg              | 110         | Oberrhein und unteres Neckartal                    | 111             |
|                                |             | Hohenlohe/mittlerer Neckar/Oberschwaben            | 112             |
|                                |             | Mittelgebirge Baden-Württemberg                    | 113             |
| Bayern                         | 120         | Allgäu/Oberbayern/Bay. Wald                        | 121             |
|                                |             | Donauniederungen                                   | 122             |
|                                |             | Bayern n. der Donau, o. Bayr. Wald, o. Mainfranken | 123             |
|                                |             | Mainfranken                                        | 124             |
