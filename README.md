# APBD_Zadanie_6
W niniejszym zadaniu przygotuj aplikację w oparciu o podejście EF
code first.
Zaimplementuj następujące końcówki:
Dodawanie nowej recepty
Przykład żądania:
Końcówkę pozwalającą na wystawienie nowej recepty.
Końcówka powinna przyjmować jako element żądania informacje
o pacjencie, recepcie i informacje o lekarz wystawionych na
danej recepcie.
Jeśli pacjent przekazany w żądaniu nie istnieje, wstawiamy
nowego pacjenta do tabeli Pacjent.
Jeśli lek podany na recepcie nie istnieje, zwracamy błąd.
Recepta może obejmować maksymalnie 10 leków. W innym
wypadku zwracamy błąd.
Musimy sprawdzić czy DueData>=Date
Dane na temat pacjenta:**
Przygotuj końcówkę pozwalającą na wyświetlenie wszystkich danych
na temat konkretnego pacjenta, wraz z listę recept i leków, które
pobrał. Chcielibyśmy, żeby odpowiedź uwzględniała wszystkie
informacje na temat leków i lekarzy. Dane na temat recept powinny
być posortowane po polu DueDate.
Przykład:
{
"patient": {
"IdPatient": 1,
"FirstName": "Jan",
//...
},
"medicaments": [
{"idMedicament": 1, "Dose": 3, "Description":
"Some desc..." }
],
"Date": "2012-01-01",
"DueDate": "2012-01-01"
}
{
"IdPatient": 1,
"FirstName": "Jan",
//...
"Prescriptions": [
{
"IdPrescription": 1,
. "Date": "2012-01-01",
"DueDate": "2012-01-01",
"Medicaments": [
{
"IdMedicament": 1,
"Name": "AAA",
Spróbuj przygotować testy jednostkowe sprawdzające twoje końcówki.
Upewnij się, że:
"Dose": 10,
"Description": "AAA"
}
]
"Doctor": {
"IdDoctor": 1,
"FirstName": "AAA"
}
}
]
}
nazewnictwo jest poprawne
kod został podzielony na osobne warstwy i jest testowalny
pamiętaj o zasadach REST, SOLID, DRY, YAGNI, KIS
