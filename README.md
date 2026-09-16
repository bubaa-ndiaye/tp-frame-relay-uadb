# TP Réseaux Étendus — Frame Relay (GNS3)

**Filière :** L3 SRT — UFR des Sciences Appliquées et TIC, Université Alioune Diop de Bambey (UADB)
**Cours :** Réseaux Étendus
**Prof :** Dr OUESSE Mohamed El-Amine
**Année universitaire :** 2025-2026
**Réalisé par :** Boubacar Ndiaye

## 📖 Contexte

Ce TP couvre la configuration de liaisons **Frame Relay** sous GNS3, une technologie WAN historique permettant de faire transiter plusieurs connexions virtuelles (PVC) sur une même ligne physique via un identifiant appelé **DLCI** (Data Link Connection Identifier).

Chaque exercice explore une topologie différente : simple point-à-point, multipoint, avec ou sans switch Frame Relay dédié, avec RIP comme protocole de routage dynamique.

## 🛠️ Environnement

- **Simulateur :** GNS3 2.2.61
- **Image routeur :** Cisco c3725, IOS 12.4(7) `adventerprisek9-mz`
- **Switch Frame Relay :** module natif GNS3

## 📂 Structure du dépôt

```
tp-frame-relay-uadb/
├── README.md
├── docs/
│   └── notions-frame-relay.md    # Rappels théoriques (DLCI, PVC, LMI...)
├── exercice1/
│   ├── README.md                 # Topologie, objectifs, configs
│   ├── R1-config.txt
│   ├── R2-config.txt
│   └── captures/
├── exercice2/  (à venir)
├── exercice3/  (à venir)
...
```

## ✅ Avancement

| Exercice | Description | Statut |
|---|---|---|
| 1 | Simple configuration avec Switch FR | ✅ Terminé |
| 2 | Point-à-point (2 routeurs) via Switch | ⏳ À venir |
| 3 | Point-à-point (3 routeurs) avec RIP | ⏳ À venir |
| 4 | Point-à-point (4 routeurs) avec RIP | ⏳ À venir |
| 5 | Simple configuration sans Switch | ⏳ À venir |
| 6 | frame-relay map ip | ⏳ À venir |
| 7 | frame-relay interface-dlci | ⏳ À venir |
| 8 | Configuration multipoint | ⏳ À venir |
| 9 | Point-à-point et multipoint combinés | ⏳ À venir |

## 📚 Ressources

- Cours : Dr OUESSE Mohamed El-Amine, UADB