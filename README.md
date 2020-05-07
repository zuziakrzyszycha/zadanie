# zadanie
zadanie z prezentacji na programowanie
import random
lista3=[]
alfabet="abcdefghijklmnoprstuwyz"
def dlugosc(lista, suma=0):
    if len(lista) >0:
        return dlugosc(lista[1:],suma+1)
    return suma

print("Witaj w programie do mierzenia list! Poproszę Cię, abyś wpisał dowolne słowo, zdanie.")
slowo=input()
lista_slowo=list(slowo)
wynik_slowo=dlugosc(lista_slowo)
print("Długość Twojej listy wynosi:",wynik_slowo)
print("Teraz program sam wylosuje pewną listę i sam sprawdzi, czy funkcja długości poprawnie działa.")
wylosowana=random.randint(0,20)
for i in range(wylosowana):
    wylosowane=random.choice(alfabet)
    lista3.append(wylosowane)
print("Oto lista jaką wylosował program:", lista3)
wynik_lista3=dlugosc(lista3)
print("Ilość elementów w tej liście wynosi:",wynik_lista3)
print("Teraz ja sama wpiszę listę, a program sprawdzi ile zawiera ona elemntów. Oto moja lista: [1,2,3,4,5,6]")
lista2=[1,2,3,4,5,6]
wynik=dlugosc(lista2)
print("Długość tej listy wynosi:",wynik)
