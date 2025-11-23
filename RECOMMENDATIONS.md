# Recommandations pour la présentation "Projection de contenu avec Angular"

## Corrections prioritaires

### 1. Slide "Quand utiliser chaque approche" (ligne 743)
- Compléter la section "Préférer Projection quand" avec :
  - Structure du contenu variable selon le contexte
  - Besoin d'imbriquer plusieurs composants

### 2. Slide "Pattern hybride" (ligne 812)
- Ajouter le template avec `<ng-content />` pour montrer les deux aspects

### 3. Durée incohérente
- Agenda : "~30 minutes"
- Frontmatter : `duration: 35min`
- Harmoniser sur une seule valeur

### 4. Syntaxe contentChild incorrecte (ligne 933)
```typescript
// Actuel
itemTemplate = contentChild.required(TemplateRef);

// Correct
itemTemplate = contentChild.required(TemplateRef<{ $implicit: T }>);
```

---

## Améliorations de forme

### 1. Formatage des blocs de code
- Uniformiser l'affichage du décorateur `@Component` (parfois présent, parfois non)

### 2. Slide "Les 5 problèmes majeurs" (ligne 400)
- Le titre est dans un `<v-clicks>` séparé des problèmes
- Regrouper pour que le titre apparaisse avec le premier problème

### 3. Images
- Vérifier l'existence de `/img/UC1-SimpleCardButton.png` et `/img/UC2-IconCardButton.png`
- Revoir le positionnement (`scale-50 -mt-8`)

### 4. Slide ng-template + Context (ligne 908)
- Mélange syntaxe ancienne (`*ngTemplateOutlet`) et moderne (signals)
- Uniformiser vers la syntaxe moderne

---

## Suggestions bonus

1. **Démo interactive** - Ajouter un lien vers StackBlitz ou le projet local
2. **QR Code** - Sur la slide finale vers le repo GitHub
3. **Slide récapitulative** - 3 takeaways clés avant les questions
4. **Contenu additionnel potentiel** :
   - `ngProjectAs` pour sélecteurs complexes
   - Limitations (pas de lazy rendering du contenu projeté)

---

## Lien GitHub
- Vérifier que `https://github.com/sbruno/ng-content` est le bon repository
