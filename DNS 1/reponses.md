# Réponses DNS NSI 1.

---
Q1: 
`n = len(tab)` | `tab[n-1] = 9`

--
Q2:
```py
def filtre_0_100(tab):
    """ list[int] -> list[int]
    Renvoie les éléments de tab compris entre 0 et 100
    """
    return [i for i in tab if i >= 0 and i <= 100 ]
```

--
Q3:
```py
def nbr_de_neuf(tab):
    """ list[int] -> int
    Renvoie le nombre de 9 dans tab
    """
    neufs = [i for i in tab if i == 9]
    return len(neufs)
```

-- 
Q4:
```py
def nbr_de(k, tab):
    """ int, list[int] -> int
    Renvoie le nombre d'occurence du nombre k dans tab
    """

    neufs = [i for i in tab if i == k]
    return len(neufs)
```

--
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

--
Q6: