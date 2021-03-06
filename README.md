## README

## Data

Data is public-use, but requires login at ICPSR. 

Data can be downloaded from https://doi.org/10.3886/ICPSR13568.v1
Data should extracted from zip file and placed into folder "data". Note that the files structure of the downloaded data is maintained but only subfolder DS0002 (Alaska) is used.


## Requirements

Runtime: approximatly 1.6s on  Windows 64-bit, PC (64-bit x86-64) with Processors: 8.

Stata Packages: `latab` available in SSC.

## Code

There are 5 Stata program files:

- `master.do` : will run all programs in the right sequence
- `00_setup_stata.do`: will set up directory structure, and install any required packages
- `01_dataclean.do`: reads in downloaded data, saves person and household files, and creates a clean merged dataset, for Alaska only
- `02_table1.do`: Creates Table 1
- `config.do`: sets up the environment. Called by `master.do`. If running programs individually, must be called before running each program within the same Stata session.

## Running code

Run the `master.do`. Suggested batch command:
```
stata -b do master.do
```
A log file will be created.

## Tables

All table output is in folder `tables`:

| Table | Programs | 
|-------|----------|
| Table 1 | 02_table1.do | 

