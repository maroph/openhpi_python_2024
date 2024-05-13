# Dictionary
Ein Dictionary speichert seinen Inhalt in Key/Value (Schlüssel/Wert) Paaren ab. Der 
Datentyp der Werte kann beliebig sein. Ähnliches gilt für die Schlüssel, jedoch
muss der Datentyp unveränderbar sein (int, float, String, Tuple, ...).  Der 
Zugriff auf die Values erfolgt dabei über den Key und nicht, wie bei Listen,
über einen Index.

Bis einschließlich der Python Version 3.6 gab es für die Key/Value Paare eines Dictionaries
keine feste Reihenfolge. D.h.: hat man in einer for Schleife (Beispiele siehe weiter unten) über die Keys eines Dictionaries iteriert, hing die Reihenfolge der Keys von der
verwendeten Python Implementierung ab. Seit der Python Version 3.7 sind Dictionaries
ordered, d.h. die Key/Value Paare werden in einer festen Reihenfolge ausgegeben. Die 
Reihenfolge richtet sich nach dem Zeitpunkt, zu dem sie in das Dictionary eingestellt 
wurden.

## Anlegen eines Dictionaries
Man kann entweder ein leeres Dictionary anlegen

    dict = {}

oder das Dictionary gleich mit Inhalt anlegen

    dict = {"key1": "val1", "key2": "val2"}

## Zugriff auf einen Wert im Dicitonary
Auf die Werte im Dictionary wird mit dem Schlüssel zugegriffen:

    value = dict["key"]

### Zugriff auf einen Wert im Dictionary - auch wenn der Key nicht existiert
Greift man auf einen Key zu, den es im Dictionary nicht gibt, kommte es im
Python Runtime System zu einem KeyError. Dieses Problem kann man mit der
Methode get vermeiden

    value = dict.get(key, default_value)

Ist der Key nicht im Dictionary, wird der angegebene Defaultwert zurückgegeben.

    value = dict.get(key)

Ist der Key nicht im Dictionary, wird None zurückgegeben.

### defaultdict
Statt jedes Mal beim Aufruf von _get_ einen Defaultwert
mitzuübergeben, kann man auch die Klasse 
[defaultdict](https://docs.python.org/3/library/collections.html?highlight=defaultdict#collections.defaultdict)
verwenden.

    from collections import defaultdict

    def default_value():
        return None

    d = defaultdict(default_value, dict)
    value = d.get(key)

Wir jetzt beim Aufruf von _get_ ein Key verwendet, der
nicht im Dictionary abgelegt ist, wird kein KeyError
erzeugt, sondern es wird der Wert, den die Funktion
_default_value_ zurückgibt (im Beispiel __None__)
zurückgegeben.

## Ein Key/Value Paar zum Dictionary hinzufügen:

    dict["key"] = "value"

## Ein Key/Value Paar auf einem Dictionray löschen

    del(dict["key2"])

### Löschen und lesen

    value = dict.pop("key2")

## Anzahl der Key/Value Paare in einem Dictionary

    len(dict)

## Abfragen ob ein Key in einem Dictionary enthalten ist

    if "key1" in dict:
        print("gefunden, Wert: ", dict["key1"])

## Abfragen ob ein Key nicht in einem Dictionary enthalten ist

    if "key1" not in dict:
        print("nicht gefunden")

## Alle Keys aus einem Dictionary lesen

    for key in dict:
        print(key)

Oder

    for key in dict.keys():
        print(key)

### Alle Keys in einer Liste speichern

    liste = list(dict.keys())

## Alle Values aus einem Dictionary lesen

    for key in dict:
        print(dict[key])

Oder 

    for value in dict.values():
        print(value)

### Alle Values in einer Liste speichern

    liste = list(dict.values())

## Alle Key/Value Paare aus einem Dictionary lesen

### Jedes Paar als Tuple

    for item in dict.items():
        print(item[0], item[1])

### Alles Paare in einer Liste speichern

    liste = list(dict.items())

### Jedes Paar als einzelne Werte: key, value

    for key, value in dict.items():
        print(key, value)

## Inhalt eines Dictionaries löschen

    dict.clear()

## Dictionary kopieren

    dict_copy = dict.copy()


## Einfügen eines Dictionaries

    dict.update(dict2)

Alle Key/Value Paare aus dem Dictionary dict2 werden in
das Dictionay dict eingefügt. Ist der Key bereits in 
dict enthalten, wird der Wert durch den Wert aus
dem Dictionary dict2 ersetzt.

---

## Weiterführende Links

* [Defaultdict in Python](https://www.geeksforgeeks.org/defaultdict-in-python/)
* [How to Iterate Through a Dictionary in Python](https://realpython.com/iterate-through-dictionary-python/)
* [Python-Kurs: Dictionaries](https://www.python-kurs.eu/python3_dictionaries.php)
