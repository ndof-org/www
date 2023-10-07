# [NDOF - Newline Delimited Objects Format - www.ndof.org](http://www.ndof.org)

NDOF - Newline Delimited Objects Format

+ StreamLine
+ MultiObjects
+ JSONL
+ NDJSON
+ Newline-Delimited XML

Welcome to NDOF (Newline Delimited Objects Format)

## About the Project

NDOF is a revolutionary data format that supports the seamless streaming of JSON, XML, and other newline delimited objects. 
Our innovative solution allows for writing, reading, and searching separated formats like JSON, XML, and others in each line without the need for decoding.


## Why NDOF?

With NDOF, you no longer need to worry about the complexities and inefficiencies that come with the traditional approaches to handling streaming data formats. Our easy-to-use and flexible approach make streaming data easier and faster than ever.
Get Started

To start using NDOF in your projects, download our open-source library from the official repository and follow the instructions in our comprehensive guide. Join the NDOF community today and transform the way you handle streaming data.


Powstaje coraz więcej oprogramowania, mamy coraz więcej wyspecjalizowanych bibliotek, języków programowania, DSL.
Naturalnym rezultatem jest modularyzacja orpogramowania, atomizacja logiki do poziomu funkcji i zmiany struktury danych do pojedynczych tabel z tysiącami, milionami wierszy

W celu wykorzystania potencjalu leżącego w modularyzacji konieczne są specjalizowane funkcje i formaty danych. Jedno z możliwości to wykorzystanie format pliku: multipart 
format NDOF jest w tej sytuacji mniej kosztowny przy odczycie i zapisie.




# Separators Delimeter

Characters - Newline - End of Line ( EOL ) - Line Separators - Line Break

## OS
To mark line endings in text files, the following characters are used:

+ Unix/Linux file systems use newlines (**\n**).
+ MacOS uses carriage-returns (**\r**).
+ Windows uses a carriage-return followed by a newline (**\r\n**).

The line separator used by the in-memory representation of file contents is always the newline character. When a file is being loaded, the line separator used in the file on disk is stored in a per-buffer property, and all line-endings are converted to newline characters for the in-memory representation. When the buffer is consequently saved, the value of the property replaces newline characters when the buffer is saved to disk. 


