# Listen
Eine Liste ist eine Sammlung von Elementen, die in einer festen Reihenfolge
abgelegt werden. Der Datentyp der Elemente kann beliebig sein. Der Zugriff erfolgt 
über den Index, der die Position des Elements in der Liste bestimmt. Indizes 
beginnen mit 0 und nicht mit 1!

## Anlegen einer Liste
Man kann entweder ein leere Liste anlegen

    liste = []

oder die Liste gleich mit Inhalt anlegen

    liste = ["val1", "val2"]

## Zugriff auf einen Wert in einer Liste
Auf die Werte in Liste wird mit dem Index zugegriffen:

    value1 = liste[0] # erstes Element
    value2 = liste[1] # zweites Element

## Zugriff auf das letzte/vorletzte/... Element einer Liste:

    value = liste[-1] # letztes Element
    value = liste[-2] # vorletztes Element
    ...

## Zugriff auf eine (Index-) Bereich in einer Liste
Hier einige Beispiele:

    >>> liste = [i for i in range(1, 11)]
    >>> print(liste)
    [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
    >>> print(liste[1:3])
    [2, 3]
    >>> print(liste[1:])
    [2, 3, 4, 5, 6, 7, 8, 9, 10]
    >>> print(liste[5:-1])
    [6, 7, 8, 9]
    [2, 3, 4, 5, 6, 7, 8, 9, 10]

## Ein Wert am Ende der Liste hinzufügen

    liste.append("val3")

## Einen Wert in eine Liste einfügen:

    liste.insert(idx, value)

## Einen Wert Liste löschen

    liste.remove(idx)

## Einen Wert lesen und aus der Liste löschen

    value = liste.pop(idx)

## Eine Liste an eine Liste anhängen:

    liste.extend(liste2)

## Ein Wert aus einer Liste löschen

    del(liste[idx])

## Anzahl der Werte in einer Liste

    len(liste)

## Abfragen ob ein Wert in einer Liste enthalten ist

    if "val1" in liste:
        print("gefunden")

## Abfragen ob ein Wert nicht in einer Liste enthalten ist

    if "val1" not in liste:
        print("nicht gefunden")

## Alle Werte aus einer Liste lesen

    for value in liste:
        print(value)

## Alle Werte aus einer Liste lesen und löschen
Mit dieser naheliegenden for Schleife lässt sich das Problem leider nicht lösen :-(

    for value in liste:
        print(value)
        liste.pop(0)

Denn: es wird einerseits implizit ein Iterator benutzt, um alle Elemente der Liste 
nacheinander zu bekommen und zum anderen wird direkt auf der Liste operiert.

Man kann hierzu eine while Schleife verwenden:

    while (len(liste) > 0):
        print(liste.pop(0))

Alternativ kann man auch die folgende for Schleife verwenden:

    for i in range(len(liste)):
        print(liste.pop(0))

## Umkehr der Reihenfolge in einer Liste

    liste.reverse()

## Werte in einer Liste sortieren

    liste.sort()

### Sortierreihenfolge umkehren

    liste.sort(reverse=True)

---

## Weiterführende Links

* [Python-Kurs: Listen](https://www.python-kurs.eu/python3_listen.php)
* [Python's list Data Type: A Deep Dive With Examples](https://realpython.com/python-list/)
