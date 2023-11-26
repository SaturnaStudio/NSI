# Réponses DNS NSI 1.

---
Q1: 
`n = len(tab)` | `tab[n-1] = 9`

---
Q2:
```py
def filtre_0_100(tab):
    """ list[int] -> list[int]
    Renvoie les éléments de tab compris entre 0 et 100
    """
    return [i for i in tab if i >= 0 and i <= 100 ]
```

---
Q3:
```py
def nbr_de_neuf(tab):
    """ list[int] -> int
    Renvoie le nombre de 9 dans tab
    """
    neufs = [i for i in tab if i == 9]
    return len(neufs)
```

--- 
Q4:
```py
def nbr_de(k, tab):
    """ int, list[int] -> int
    Renvoie le nombre d'occurence du nombre k dans tab
    """

    neufs = [i for i in tab if i == k]
    return len(neufs)
```

---
Q5:
```py
def cree_tableau(n):
    """ int -> list[int]
    préconditions: n >= 0
    Renvoie un tableau de taille n ne contenant que des 0
    """
    tableau = [0 for _ in range(n)]
    return tableau
```

---
Q6:
- [x] A. compteurs[k] = nbr_de(k, tab)
- [] B. compteurs[nbr_de(k, tab)] = k
- [] C. compteurs[k] = k
- [] D. compteurs[k] = tab[k]
- [] E. compteurs[tab[k]] = nbr_de(k, tab)

---
Q7:
```py
def nbr_de_nbr(tab):
    """ list[int] -> list[int]
    precondition: tab ne contient que des nombres entre 0 et 100
    """
    compteurs = cree_tableau(101)
    for i in range(len(tab)+1):
        compteurs[i] = nbr_de(i, tab)
    return compteurs
```

---
Q8:
```py
def nbr_de_nbr(tab):
    """ list[int] -> list[int]
    precondition: tab ne contient que des nombres entre 0 et 100
    """
    compteurs = cree_tableau(101)
    for i in tab:
        compteurs[i] += 1
    return compteurs
```

---
Q9:
```py
def tri_croissant_unique(tab):
    """ list[int] -> list[int]
    precondition: tab ne contient que des nombres entre 0 et 100
    """
    t2 = nbr_de_nbr(tab)
    return [i for i in range(len(t2)) if t2[i] > 0]
```

---
Q10:
```py
def existes_dans(tab):
    """ list[int] -> list[bool]
    precondition: tab ne contient que des nombres entre 0 et 100
    """
    checked = list([False for _ in range(0, 101)])
    for i in range(0,101):
        if i in tab:
            checked[i] = True

    return checked
```