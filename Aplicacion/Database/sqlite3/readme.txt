para compilar usar el comando
gcc -o sqlite3 sqlite3.c main.c -ldl -lpthread -lm

flujo de comandos
co/Aplicacion/Database/sqlite3$ gcc -o sqlite3 sqlite3.c ../db/db.c -ldl -lpthread -lm
samotlqq@samotlqq-HP-250-G7-Notebook-PC:/media/samotlqq/1TB/My/App-Taller-Mecanico/Aplicacion/Database/sqlite3$ ./sqlite3 
Usage: ./sqlite3 DATABASE SQL-STATEMENT
/App-Taller-Mecanico/Aplicacion/Database/sqlite3$ ./sqlite3 ../DatosHuguis "CREATE TABLE usuarios (id INTEGER PRIMARY KEY, nombre TEXT);"
/App-Taller-Mecanico/Aplicacion/Database/sqlite3$ ./sqlite3 ../DatosHuguis "SELECT * FROM usuarios"
/App-Taller-Mecanico/Aplicacion/Database/sqlite3$ ./sqlite3 ../DatosHuguis "INSERT INTO usuarios (id, nombre) VALUES (1, 'Juan');"
/App-Taller-Mecanico/Aplicacion/Database/sqlite3$ ./sqlite3 ../DatosHuguis "SELECT * FROM usuarios"
id = 1
nombre = Juan

samotlqq@samotlqq-HP-250-G7-Notebook-PC:/media/samotlqq/1TB/My/App-Taller-Mecanico/Aplicacion/Database/sqlite3$ ./sqlite3 ../DatosHuguis "DROP TABLE usuarios"
samotlqq@samotlqq-HP-250-G7-Notebook-PC:/media/samotlqq/1TB/My/App-Taller-Mecanico/Aplicacion/Database/sqlite3$ ./sqlite3 ../DatosHuguis "SELECT name FROM sqlite_master WHERE type='table';"
name = Auto

name = sqlite_sequence

name = Trabajo

samotlqq@samotlqq-HP-250-G7-Notebook-PC:/media/samotlqq/1TB/My/App-Taller-Mecanico/Aplicacion/Database/sqlite3$ ./sqlite3 ../DatosHuguis "PRAGMA table_info(Auto);"
cid = 0
name = Patente
type = TEXT
notnull = 1
dflt_value = NULL
pk = 0

cid = 1
name = Duenio
type = TEXT
notnull = 1
dflt_value = NULL
pk = 0

cid = 2
name = Modelo
type = TEXT
notnull = 1
dflt_value = NULL
pk = 0

cid = 3
name = Id
type = INTEGER
notnull = 1
dflt_value = 1
pk = 1

samotlqq@samotlqq-HP-250-G7-Notebook-PC:/media/samotlqq/1TB/My/App-Taller-Mecanico/Aplicacion/Database/sqlite3$ ./sqlite3 ../DatosHuguis "PRAGMA table_info(Trabajo);"
cid = 0
name = Id
type = INTEGER
notnull = 1
dflt_value = 1
pk = 1

cid = 1
name = Descripcion
type = TEXT
notnull = 0
dflt_value = NULL
pk = 0

cid = 2
name = Fecha
type = TEXT
notnull = 0
dflt_value = NULL
pk = 0

cid = 3
name = Km
type = INTEGER
notnull = 0
dflt_value = NULL
pk = 0

cid = 4
name = FkAuto
type = INTEGER
notnull = 0
dflt_value = NULL
pk = 0

cid = 5
name = trabajoN
type = INTEGER
notnull = 0
dflt_value = NULL
pk = 0

co/Aplicacion/Database/sqlite3$ ./sqlite3 ../DatosHuguis "SELECT * FROM Auto"
Patente = AB
Duenio = TOMAS
Modelo = FIAT
Id = 1

Patente = ABC
Duenio = TOMAS
Modelo = FIAT
Id = 2

Patente = ABCD
Duenio = TOMAS
Modelo = FIAT
Id = 3

Patente = ABCDE
Duenio = TOMAS
Modelo = FIAT
Id = 4

Patente = ABCDEF
Duenio = TOMAS
Modelo = FIAT
Id = 5

Patente = ABCDEFG
Duenio = TOMAS
Modelo = FIAT
Id = 6

Patente = ABC 123
Duenio = Tomas
Modelo = Chevrolet meriva 2006
Id = 7

samotlqq@samotlqq-HP-250-G7-Notebook-PC:/media/samotlqq/1TB/My/App-Taller-Mecanico/Aplicacion/Database/sqlite3$ ./sqlite3 ../DatosHuguis "SELECT * FROM Trabajo"Id = 1
Descripcion = Descripcion 1
Fecha = Fecha 1
Km = 0
FkAuto = 1
trabajoN = 1

Id = 2
Descripcion = Descripcion 2
Fecha = Fecha 2
Km = 100
FkAuto = 1
trabajoN = 2

Id = 3
Descripcion = Descripcion 3
Fecha = Fecha 3
Km = 300
FkAuto = 1
trabajoN = 3

Id = 4
Descripcion = Descripcion 1 prima
Fecha = Fecha 1 prima
Km = 1600
FkAuto = 3
trabajoN = 1

Id = 5
Descripcion = Descripcion 2 prima
Fecha = Fecha 2 prima
Km = 3600
FkAuto = 3
trabajoN = 2

Id = 6
Descripcion = Servi completo
Fecha = 29-08-2001
Km = 800
FkAuto = 7
trabajoN = 1
