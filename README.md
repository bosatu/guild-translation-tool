# guild-translation-tool
A little helper that converts .loo files for Guild 3 localization to xlsx files and back.

## Usage

`GTT.Terminal.exe <filename> <codepage> [formatFile]`

The program will automatically detect if the supplied file is .loo or .xlsx. 
Make sure to provide the correct code page. In most cases this will be 1252, for Russian translations it is 1251.
The format file is optional and is used to truncate texts that are too long. An up to date version can always be found in `/Resources` in the repository.
The tool will create the converted version in the same directory the source file was found in. 
It will not overwrite existing files, instead create copies with _1, _2, etc appended.



**IMPORTANT**: Do not modify the column headers in the spreadsheet, nor should you modify the .loo files manually to avoid syntax errors that might lead to problems in parsing with either this tool or the game.

### Editing
If you do not own a copy of Microsoft Office you can use Google Sheets ( https://docs.google.com/spreadsheets/u/0/ ) to import and export the files.

* Import files using File -> Import -> Upload
* Export files by using File -> Download As -> Microsoft Excel

## Community Translations
You can find all information about the community translation effort in our steam thread: http://steamcommunity.com/app/311260/discussions/0/1520386297685072772/ 

## Dependencies
This project uses https://github.com/ClosedXML/ClosedXML to handle xlsx files.