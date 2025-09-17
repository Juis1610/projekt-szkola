# projekt szkola

import math

def main():
    print("Witaj w kalkulatorze geometrii!")
    while True:
        print("\nWybierz kategorię:")
        print("1 - Bryły 3D")
        print("2 - Figury płaskie")
        print("3 - Przekątne")
        print("4 - Twierdzenie Pitagorasa")
        print("0 - Wyjście")
        
        choice = input("--- ")
        if choice == "1":
            bryly()
        elif choice == "2":
            figury_plaskie()
        elif choice == "3":
            przekatne()
        elif choice == "4":
            pitagoras()
        elif choice == "0":
            print("Do widzenia!")
            break
        else:
            print("Nie ma takiej opcji")

# Podmenu dla brył 3D
def bryly():
    print("\nBryły 3D:")
    print("a - Sześcian")
    print("b - Prostopadłościan")
    print("c - Graniastosłup prosty")
    print("d - Ostrosłup")
    print("e - Walec")
    print("f - Stożek")
    print("g - Kula")
    
    choice = input("--- ")
    
    if choice == "a":
        a = float(input("Podaj bok sześcianu a: "))
        print(f"Pole powierzchni: {6*a**2}")
        print(f"Objętość: {a**3}")
    elif choice == "b":
        a = float(input("Podaj bok a: "))
        b = float(input("Podaj bok b: "))
        c = float(input("Podaj wysokość c: "))
        print(f"Pole powierzchni: {2*(a*b + a*c + b*c)}")
        print(f"Objętość: {a*b*c}")
    elif choice == "c":
        a = float(input("Podaj pole podstawy: "))
        h = float(input("Podaj wysokość: "))
        print(f"Objętość graniastosłupa: {a*h}")
    elif choice == "d":
        a = float(input("Podaj pole podstawy: "))
        h = float(input("Podaj wysokość: "))
        print(f"Objętość ostrosłupa: {a*h/3}")
    elif choice == "e":
        r = float(input("Podaj promień walca: "))
        h = float(input("Podaj wysokość walca: "))
        print(f"Pole powierzchni: {2*math.pi*r*(r+h)}")
        print(f"Objętość: {math.pi*r**2*h}")
    elif choice == "f":
        r = float(input("Podaj promień stożka: "))
        h = float(input("Podaj wysokość stożka: "))
        l = math.sqrt(r**2 + h**2)
        print(f"Pole powierzchni: {math.pi*r*(r+l)}")
        print(f"Objętość: {math.pi*r**2*h/3}")
    elif choice == "g":
        r = float(input("Podaj promień kuli: "))
        print(f"Pole powierzchni: {4*math.pi*r**2}")
        print(f"Objętość: {4/3*math.pi*r**3}")
    else:
        print("Nie ma takiej opcji")

# Podmenu dla figur płaskich
def figury_plaskie():
    print("\nFigury płaskie:")
    print("a - Prostokąt")
    print("b - Kwadrat")
    print("c - Równoległobok")
    print("d - Trapez")
    print("e - Trójkąt")
    print("f - Trójkąt równoboczny")
    print("g - Koło")
    print("h - Romb")
    
    choice = input("--- ")
    
    if choice == "a":
        a = float(input("Podaj bok a: "))
        b = float(input("Podaj bok b: "))
        print(f"Pole: {a*b}")
        print(f"Obwód: {2*(a+b)}")
    elif choice == "b":
        a = float(input("Podaj bok kwadratu: "))
        print(f"Pole: {a**2}")
        print(f"Obwód: {4*a}")
    elif choice == "c":
        a = float(input("Podaj podstawę: "))
        h = float(input("Podaj wysokość: "))
        b = float(input("Podaj bok równoległoboku: "))
        print(f"Pole: {a*h}")
        print(f"Obwód: {2*(a+b)}")
    elif choice == "d":
        a = float(input("Podaj podstawę a: "))
        b = float(input("Podaj podstawę b: "))
        h = float(input("Podaj wysokość: "))
        c = float(input("Podaj bok c: "))
        d = float(input("Podaj bok d: "))
        print(f"Pole: {(a+b)/2*h}")
        print(f"Obwód: {a+b+c+d}")
    elif choice == "e":
        a = float(input("Podaj bok a: "))
        h = float(input("Podaj wysokość: "))
        print(f"Pole: {a*h/2}")
        print(f"Obwód: {3*a}")  # zakładamy trójkąt równoboczny dla uproszczenia
    elif choice == "f":
        a = float(input("Podaj bok trójkąta równobocznego: "))
        print(f"Pole: {math.sqrt(3)/4*a**2}")
        print(f"Obwód: {3*a}")
    elif choice == "g":
        r = float(input("Podaj promień: "))
        print(f"Pole: {math.pi*r**2}")
        print(f"Obwód: {2*math.pi*r}")
    elif choice == "h":
        a = float(input("Podaj bok rombu: "))
        h = float(input("Podaj wysokość: "))
        print(f"Pole: {a*h}")
        print(f"Obwód: {4*a}")
    else:
        print("Nie ma takiej opcji")

# Podmenu dla przekątnych
def przekatne():
    print("\nPrzekątne:")
    print("a - Trójkąt równoboczny")
    print("b - Kwadrat")
    
    choice = input("--- ")
    
    if choice == "a":
        a = float(input("Podaj bok trójkąta równobocznego: "))
        d = a*math.sqrt(3)/2
        print(f"Przekątna (wysokość) trójkąta równobocznego: {d}")
    elif choice == "b":
        a = float(input("Podaj bok kwadratu: "))
        d = a*math.sqrt(2)
        print(f"Przekątna kwadratu: {d}")
    else:
        print("Nie ma takiej opcji")

# Twierdzenie Pitagorasa
def pitagoras():
    print("\nTwierdzenie Pitagorasa")
    a = float(input("Podaj bok a: "))
    b = float(input("Podaj bok b: "))
    c = math.sqrt(a**2 + b**2)
    print(f"Przeciwprostokątna = {c}")

# uruchomienie programu
main()
