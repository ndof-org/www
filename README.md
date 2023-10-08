# [NDOF - Newline Delimited Objects Format - www.ndof.org](http://www.ndof.org)

NDOF is a newline delimited objects format that supports the seamless streaming of JSON, XML and other data formats

+ [examples](https://examples.ndof.org/)
+ [roadmap](https://roadmap.ndof.org/)
+ [identity](https://identity.ndof.org/)
+ [docs](https://docs.ndof.org/)
+ [logo](https://logo.ndof.org/)

## About the Project

Newline Delimited Objects Format supports the seamless streaming of JSON, XML, and other newline delimited objects in a single file.
Our innovative solution allows for writing, reading, and searching separated formats like JSON, XML, and others in each line without the need for parsing and decoding whole file or object.


    
## Why NDOF?

With NDOF, you no longer need to worry about the complexities and inefficiencies that come with the traditional approaches to handling streaming data formats. Our easy-to-use and flexible approach make streaming data easier and faster than ever.
Get Started

To start using NDOF in your projects, download our open-source library from the official repository and follow the instructions in our comprehensive guide. Join the NDOF community today and transform the way you handle streaming data.


Powstaje coraz więcej oprogramowania, mamy coraz więcej wyspecjalizowanych bibliotek, języków programowania, DSL.


### Modularyzacja
Naturalnym rezultatem jest modularyzacja orpogramowania, atomizacja logiki do poziomu funkcji i zmiany struktury danych do pojedynczych tabel z tysiącami, milionami wierszy
W celu wykorzystania potencjalu leżącego w modularyzacji konieczne są specjalizowane funkcje i formaty danych. Jedno z możliwości to wykorzystanie format pliku: multipart 
format NDOF jest w tej sytuacji mniej kosztowny przy odczycie i zapisie.

### Struktura
Utrzymanie struktury w formatach baz danych czy plikach w systemie operacyjnym i usługach wirtualizacji kosztuje,
w przypadku dysków NVME z prędkościami przekraczającymi możliwości sieci, mamy zdolność do dostępu do danych bez potrzeby ich przetwarzania, cache-owania, bezpośrednio ze źródła.
W takiej sytuacji koszt pozyskania danych w przypadku usług sieciowych jest zerowy w momencie gdy dane nie są potrzebne, Cache jest kosztem, niezależnie od tego czy dane są potrzebne, bo są one przechowywane w pamięci operacyjnej.

### Korzyśći
w przypadku rozwiązań JSONL, NDJSON mamy do czynienia z plikiem przeznaczonym do jednego typu formatu danych na plik.
NDOF zdejmuje to ograniczenie z pliku i pozwala przechowywać inne formaty jak XML, JSON, CSV, a nawet kod programu (tekst funkcji, serialized objects) pod warunkiem, że separatory wewnątrz obiektu nie zawierają znaku końca linii EOL 

### Format danych w jednej linii
Dozwolone jest przechowywanie każdego formatu danych w odseparowanych liniach znakiem EOL, kwestią drugorzędną pozostaje format tych danych.
Dopiero na poziomie przeczytania formatu dochodzi do detekcji formatu danych, z racji tego, że każdy sensowny zapis będzie w minimalnej formie odzwierciedlał zapis konkretnego formatu, można przyjąć, że format ten nie wymaga opisu, dodatkowego parametru, top pozwala w przyszłości na utworzenie dodatkowych informacji, jeśli było by to konieczne, np. co druga linia, poprzedzająca linię danych zawierałałaby meta dane takie jak format pliku.


### Alternatywa dla baz danych

Koszt utrzymania bazy danych zwiększa się wraz z jej obiętością,
poza tym konieczne są drivery, w świecie streamowania danych, gdzie dostępd o pojedynczych rekordów wymaga osbługi zaawansowanych zapytań kosztuje niewspółmiernie do korzyści.

### Przykładowy zasotosowania

Streamowanie danych może odbywac się bezposredni z pliku danych, który można modyfikować a także udostępniać tylko część danych, np 2 linijki 102-104 w formacie JSON.
aby tego dokonać wystarczy udostępnić te dane przez funkcję kontrolującą prawa do odczytu i przeprowadzić konwersję do wybranego formatu.

### Przykłady użycia standardu

NDOF został wykorzystany w zdalnym dostępie poprzez RPC, In distributed computing, a remote procedure call (RPC) is when a computer program causes a procedure (subroutine) to execute in a different address space (commonly on another computer on a shared network), which is written as if it were a normal (local) procedure call, without the programmer explicitly writing the details for the remote interaction. 

apirpc - [www.apirpc.com](https://www.apirpc.com/)



### NDOF Requirements

The NDOF Lines format has 5 requirements:

### UTF-8 Encoding

NDOF allows encoding Unicode strings with only ASCII escape sequences, however those escapes will be hard to read when viewed in a text editor. 
The author of the NDOF Lines file may choose to escape characters to work with plain ASCII files.

Encodings other than UTF-8 are very unlikely to be valid when decoded as UTF-8 so the chance of accidentally misinterpreting characters in NDOF Lines files is low.


### Values

Each Line is a Valid NDOF Value
The most common values will be objects or arrays, but any JSON, XML, serialized value is permitted.



### Separators Delimeter

Line Separator is '\n'

This means '\r\n' is also supported because surrounding white space is implicitly ignored when parsing NDOF values.

The last character in the file may be a line separator, and it will be treated the same as if there was no line separator present.


Characters - Newline - End of Line ( EOL ) - Line Separators - Line Break

### OS

To mark line endings in text files, the following characters are used:

+ Unix/Linux file systems use newlines (**\n**).
+ MacOS uses carriage-returns (**\r**).
+ Windows uses a carriage-return followed by a newline (**\r\n**).

The line separator used by the in-memory representation of file contents is always the newline character. When a file is being loaded, the line separator used in the file on disk is stored in a per-buffer property, and all line-endings are converted to newline characters for the in-memory representation. When the buffer is consequently saved, the value of the property replaces newline characters when the buffer is saved to disk. 



### Suggested Conventions

NDOF Lines files may be saved with the file extension .ndof.

Stream compressors like gzip or bzip2 are recommended for saving space, resulting in .ndof.gz or .ndof.bz2 files.

MIME type may be application/ndof, but this is not yet standardized; any help writing the RFC would be greatly appreciated (see issue).

Text editing programs call the first line of a text file "line 1". The first value in a NDOF Lines file should also be called "value 1". 




---

## keywords: 

+ NDOF
+ Newline Delimited
+ Data Format
+ JSON
+ XML
+ Streaming Data
+ Data Objects
+ File Format
+ StreamLine
+ MultiObjects
+ JSONL
+ NDJSON
+ Newline-Delimited XML    
+ Delimiter separated values
+ Delimiterless
+ delimeter free
+ Stream Object Format
+ StreamSweep
+ Newline Delimeted Objects File Format
+ Objects Lines File Format
+ Newline Delimeted File
+ NdOff
+ multipart objects
+ multipart

---

+ [edit](https://github.com/ndof-org/www/edit/main/README.md)
  

