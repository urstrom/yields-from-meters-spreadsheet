# yields-from-meters-spreadsheet

Spreadsheet to calculate annual yields from meter readings

*Intention: this spreadsheet serves to share practices for calculation of annual meter values, to be commented or copied or adapted by other users.*

UrStrom uses a spreadsheet with annual meter readings to calculate on-site power consumption for individual sites, as well as to create overall reports (see e.g.  https://www.urstrom.de/wordpress/wp-content/uploads/2026/09/UrStrom_Projektbericht_2025.pdf).

This repository holds an appropriately anonymized spreadsheet of accounting of yearly data is done at UrStrom. UrStrom currently operates 30+ PV plants, this is just a glimpse of how we do it at the moment.

All text is in English followed by German. 

The spreadsheet contains two worksheets, one of them is "Meter readings", the other is "Systems".
For illustration, the "Systems" spreadsheet shows 5 plants, and the "Meter readings" spreadsheet just shows the data of 1 plant. Data has been partially anonymized, except for plant size and yields, which in this case are public anyway.

# Worksheet "Meter readings"

In worksheet "Meter readings", the columns are

* "No.": system number, 
* "system": system name, always 6 here, as we only illustrate with the data of system 6,
* "Meter": number of the meter,
* "Register": this is the register of the meter, the OBIS value "1.8.0" is consumption and "2.8.0" is feed-in,
* "Function" is what is read from the meter: real meter values by convention are at the lower part of the rows for each plan, and written in __bold__. Derived values are in the upper part, and not in bold.
* "Transformer factor": this is the factor the raw register value read out from the meter has to be multiplied with to obtain the actual energy value. 
* "End of 2025 (meter) / 2025 total (other values) (Ende 2025 (Zähler) / 2025 gesamt (andere Werte)": for meter readings (in __bold__), these are the values of the meter, for other values, these are derived values for (in this case) 2025.

The calculation of values is illustrated by the formulas that typically act on the values in the same column or adjacent column, examples: 

* "Yield": calculated from meter reading of current year - meter reading of previous year, both values multiplied by transformer factor, using OBIS 2.8.* values
* "Forecast": initial forecast with 0.5% degression annually
* "Feed-in", current year - previous year, using OBIS 1.8.* values and also transformer factor.

Generally it is possible to add columns also for ad-hoc calculations. 

# Worksheet "Systems"

In worksheet "Systems", the columns are: 

* No. (Nr.) – Sequential row number identifying each PV unit within the list.
* Name – Name/label of the installation, often the site or owner designation of the PV system.
* Grid operator (VNB) – The local distribution grid operator (Verteilnetzbetreiber) in whose grid area the unit feeds in power.
Contract account (Vertragskonto) – The account number for the grid/metering contract with the VNB; groups one or more units under a customer relationship.
* Unit MaStR number (EinheitMastrNummer) – Unique identifier of the installation in the Marktstammdatenregister (German federal register for energy installations); format typically "SEE" followed by digits.
EEG – Flag/identifier indicating the unit receives support under the German Renewable Energy Sources Act (Erneuerbare-Energien-Gesetz).
EEG commissioning (Inbetriebnahme EEG) – Date when the unit was first commissioned for EEG purposes; determines the applicable feed-in tariff regime.
* End of EEG remuneration (Ende EEG Vergütung) – Date the 20-year EEG feed-in remuneration period ends, after which feed-in is no longer tariff-supported.
Nominal power (kWp) (Nennleistung) – Rated peak DC capacity of the PV installation in kilowatt-peak.
* Forecast kWh/kWp at commissioning (Prognose kWh/kWp bei Betriebnahme)
* Specific yield forecast at commissioning, i.e., expected annual production per installed kWp (site quality indicator).
Forecast kWh at commissioning (Prognose kWh bei Betriebnahme) – Total expected annual production in kWh for the unit at commissioning (specific yield × nominal power).
* Feed-in tariff (Einspeisevergütung) – EEG remuneration in €/kWh paid for electricity fed into the grid, fixed at commissioning for 20 years.

Contact: holger.blasum@urstrom.de




