# Notions théoriques — Frame Relay

## Qu'est-ce que Frame Relay ?

Frame Relay est une technologie de réseau étendu (WAN) qui permet de connecter plusieurs sites distants en partageant une même infrastructure physique via des **circuits virtuels** plutôt que des lignes dédiées coûteuses. C'est l'ancêtre conceptuel des VPN/MPLS modernes.

## DLCI (Data Link Connection Identifier)

Le **DLCI** identifie un circuit virtuel (PVC) sur une liaison Frame Relay. Il a une **signification locale** : le même circuit peut porter un numéro différent à chaque extrémité (ex: DLCI 100 côté R1, DLCI 200 côté R2 pour le même lien).

Analogie : comme un numéro de quai de gare — chaque gare a sa propre numérotation, mais le système d'aiguillage (le switch Frame Relay) fait la correspondance entre les deux numéros pour le même train.

## PVC (Permanent Virtual Circuit)

Un circuit virtuel permanent établi entre deux points du réseau Frame Relay. Son état peut être :
- **ACTIVE** : le circuit fonctionne des deux côtés
- **INACTIVE** : le circuit est connu localement mais l'autre extrémité n'est pas joignable
- **DELETED** : le DLCI n'est pas reconnu par le switch

## Frame Relay Map

Table de correspondance entre une **adresse IP** et un **DLCI**. Peut être :
- **dynamic** : découverte automatique via Inverse ARP
- **static** : configurée manuellement avec `frame-relay map ip <adresse> <dlci> broadcast`

## Commandes de vérification essentielles

| Commande | Ce qu'elle montre |
|---|---|
| `show frame-relay pvc` | État des circuits virtuels (ACTIVE/INACTIVE/DELETED) |
| `show frame-relay map` | Correspondance IP ↔ DLCI |
| `show ip route` | Table de routage |
| `show interfaces serial x/x` | État physique et protocole de la liaison |

## Configuration type d'une interface Frame Relay

```
interface serial 0/0
encapsulation frame-relay
ip address <adresse> <masque>
frame-relay interface-dlci <dlci>
no shutdown
```