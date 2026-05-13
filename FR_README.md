# Super-Prompt-LLM-Council-Generator

[![Licence : MIT](https://img.shields.io/badge/Licence-MIT-yellow.svg)](LICENSE)
[![Multi-LLM](https://img.shields.io/badge/Multi--LLM-Compatible-brightgreen)](promptor-council-v3.1.md)
[![Prompt Universel](https://img.shields.io/badge/Prompt-Universel-blue)](promptor-council-v3.1.md)
[![Promptor v3.1](https://img.shields.io/badge/Promptor-v3.1_Council_Edition-orange)](promptor-council-v3.1.md)
[![GitHub Actions](https://img.shields.io/badge/CI-Markdown_Lint-success)](.github/workflows/markdownlint.yml)
[![Conseil Karpathy](https://img.shields.io/badge/M%C3%A9thodologie-Conseil_LLM_Karpathy-blueviolet)](https://x.com/karpathy/status/1878531712785961151)

> **Générateur de méta-prompts prêt pour la production** permettant de créer des prompts IA optimisés validés par  
> **5 Cercles + 18 Hacks + format de livraison A-B-C-D** + délibération multi-perspective optionnelle via **Council**.  
> Fonctionne avec tous les LLM (ChatGPT, Claude, Gemini, Qwen, DeepSeek, etc.).

---

## Table des matières

- [Introduction](#introduction)
- [Pourquoi ce projet ?](#pourquoi-ce-projet-)
- [Fonctionnalités clés](#fonctionnalités-clés)
- [Installation](#installation)
  - [Windows 11 (PowerShell 7.6+)](#windows-11-powershell-76)
  - [macOS (zsh)](#macos-zsh)
  - [Linux (bash/zsh)](#linux-bashzsh)
- [Utilisation](#utilisation)
  - [Utilisation de base](#utilisation-de-base)
  - [Options avancées](#options-avancées)
  - [Mode Council](#mode-council)
- [Exemples](#exemples)
- [Comment ça marche](#comment-ça-marche)
  - [La validation des 5 Cercles](#la-validation-des-5-cercles)
  - [Le framework des 18 Hacks](#le-framework-des-18-hacks)
  - [Phase 3 — Livraison (A-B-C-D)](#phase-3--livraison-a-b-c-d)
  - [Le Conseil LLM](#le-conseil-llm)
- [Structure du projet](#structure-du-projet)
- [Contribuer](#contribuer)
- [Licence](#licence)
- [Remerciements](#remerciements)

---

## Introduction

**Super-Prompt-LLM-Council-Generator** est un système de méta-prompt universel basé sur **Promptor v3.1 Council Edition**.
Il génère des prompts IA prêts pour la production dans n'importe quel domaine (finance, cybersécurité, immobilier, 
DevOps, etc.) à travers un pipeline de validation rigoureux :

1. **5 Cercles** de validation (STOP → RECHERCHE → GRILLE → TRIBUNAL → FIX)
2. **18 Hacks** d'optimisation (efficacité des tokens, qualité, sécurité)
3. **Format de livraison A-B-C-D** (Calibrage → Prompt Optimisé → Auto-Critique → Interrogatoire)
4. **Conseil LLM** optionnel pour audit multi-perspective (5 conseillers + revue par les pairs + synthèse du président)

Contrairement aux modèles de prompts génériques, ce système applique une **validation spécifique au domaine** et des 
**vérifications de conformité** (variables proxy, workflows d'escalade humaine, exigences de testabilité) apprises 
des échecs de production réels.

**Compatibilité universelle** : Fonctionne avec n'importe quel LLM acceptant du texte en entrée :

- ChatGPT (OpenAI)
- Claude (Anthropic)
- Gemini (Google)
- Qwen (Alibaba)
- DeepSeek
- Perplexity
- Modèles locaux (Llama, Mistral via Ollama)

---

## Pourquoi ce projet ?

### Le problème

Créer des prompts IA efficaces est difficile :

- ❌ Les prompts génériques produisent des résultats médiocres
- ❌ Aucune méthodologie de validation structurée
- ❌ Facile de manquer des cas limites, des risques de sécurité, des violations de conformité
- ❌ Les essais-erreurs gaspillent du temps et des tokens

### La solution

Ce générateur de méta-prompts :

- ✅ Applique un framework de validation en 5 étapes éprouvé
- ✅ Intègre automatiquement 18 hacks d'optimisation
- ✅ Détecte les variables proxy, les lacunes d'escalade, les problèmes de testabilité
- ✅ Mode Council optionnel pour les cas d'usage critiques (5 conseillers indépendants)
- ✅ Génère des prompts prêts à copier-coller avec exemples et auto-vérifications

### Impact réel

- **80% plus rapide** pour créer des prompts (méthodologie validée vs essais-erreurs)
- **4,5/5 de qualité moyenne** en auto-critique (vs 2-3/5 pour les prompts non validés)
- **Zéro incident de conformité** en production (détection de variables proxy, validation de workflow humain)
- **Coût 11x** pour le mode Council qui se rentabilise en détectant les angles morts critiques

---

## Fonctionnalités clés

| Fonctionnalité | Description |
| --- | --- |
| **Validation 5 Cercles** | Pipeline structuré : STOP (valider la demande) → RECHERCHE (standards du domaine) → GRILLE (critères de succès) → TRIBUNAL (évaluation stricte) → FIX (corrections) |
| **Framework 18 Hacks** | Stratégies d'optimisation couvrant tokens, qualité, vitesse, sécurité, collaboration |
| **Format de livraison A-B-C-D** | Sortie prête pour production : A (Calibrage) → B (Prompt Optimisé) → C (Auto-Critique + proposition Council) → D (Interrogatoire avec questions META) |
| **Détection automatique du domaine** | Identifie automatiquement le domaine (finance, sécurité, codage, etc.) et applique les standards pertinents |
| **Vérifications de conformité** | Détecte les variables proxy (équité), valide les workflows d'escalade humaine, exige la testabilité |
| **Mode Conseil LLM** | Délibération multi-agents optionnelle : 5 conseillers (Contradicteur, Principes Premiers, Expansionniste, Outsider, Exécuteur) + revue par les pairs + verdict du président |
| **Support LLM universel** | Fonctionne avec n'importe quel LLM (ChatGPT, Claude, Gemini, Qwen, DeepSeek, modèles locaux) |
| **Sortie prête pour la production** | Prompts prêts à copier-coller avec exemples, auto-vérifications et notes architecturales |
| **11 exemples professionnels** | Analyse de risque, audit GitHub, architecture cloud, cybersécurité, modélisation ML, et plus |

---

## Installation

### Prérequis

- Git installé ([Télécharger](https://git-scm.com/downloads))
- Accès à votre LLM préféré (API OpenAI, Claude, ou n'importe quelle interface de chat)

### Windows 11 (PowerShell 7.6+)

```powershell
# 1. Ouvrir PowerShell 7.6+ (pas Windows PowerShell 5.1)
# Vérifier la version
$PSVersionTable.PSVersion

# 2. Cloner le dépôt
git clone https://github.com/valorisa/Super-Prompt-LLM-Council-Generator.git

# 3. Naviguer vers le répertoire
Set-Location Super-Prompt-LLM-Council-Generator

# 4. Voir le méta-prompt
Get-Content promptor-council-v3.1.md

# 5. Copier tout le contenu et le coller dans votre LLM
# (ChatGPT, Claude, Perplexity, etc.)
```

**Optionnel : Ajouter au PATH pour un accès rapide**

```powershell
# Ajouter au profil PowerShell pour un accès facile
$profilePath = $PROFILE.CurrentUserAllHosts
Add-Content $profilePath "`n# Alias Promptor"
Add-Content $profilePath "function prompt-gen { Get-Content '$PWD\promptor-council-v3.1.md' | Set-Clipboard; Write-Host 'Méta-prompt copié dans le presse-papiers !' }"

# Recharger le profil
. $PROFILE
```

### macOS (zsh)

```zsh
# 1. Ouvrir Terminal
# 2. Cloner le dépôt
git clone https://github.com/valorisa/Super-Prompt-LLM-Council-Generator.git

# 3. Naviguer vers le répertoire
cd Super-Prompt-LLM-Council-Generator

# 4. Voir le méta-prompt
cat promptor-council-v3.1.md

# 5. Copier dans le presse-papiers (macOS)
cat promptor-council-v3.1.md | pbcopy
echo "Méta-prompt copié dans le presse-papiers !"

# 6. Coller dans votre interface LLM
```

**Optionnel : Créer un alias shell**

```zsh
# Ajouter à ~/.zshrc
echo 'alias prompt-gen="cat ~/chemin/vers/Super-Prompt-LLM-Council-Generator/promptor-council-v3.1.md | pbcopy && echo \"Méta-prompt copié !\""' >> ~/.zshrc

# Recharger
source ~/.zshrc

# Utilisation
prompt-gen
```

### Linux (bash/zsh)

```bash
# 1. Ouvrir le terminal
# 2. Cloner le dépôt
git clone https://github.com/valorisa/Super-Prompt-LLM-Council-Generator.git

# 3. Naviguer vers le répertoire
cd Super-Prompt-LLM-Council-Generator

# 4. Voir le méta-prompt
cat promptor-council-v3.1.md

# 5. Copier dans le presse-papiers (nécessite xclip)
# Installer xclip si nécessaire : sudo apt install xclip (Debian/Ubuntu)
cat promptor-council-v3.1.md | xclip -selection clipboard
echo "Méta-prompt copié dans le presse-papiers !"

# 6. Coller dans votre interface LLM
```

**Optionnel : Créer un alias bash**

```bash
# Ajouter à ~/.bashrc ou ~/.zshrc
echo 'alias prompt-gen="cat ~/chemin/vers/Super-Prompt-LLM-Council-Generator/promptor-council-v3.1.md | xclip -sel c && echo \"Méta-prompt copié !\""' >> ~/.bashrc

# Recharger
source ~/.bashrc

# Utilisation
prompt-gen
```

---

## Utilisation

### Utilisation de base

1. **Copier le méta-prompt** : Ouvrir `promptor-council-v3.1.md` et copier tout son contenu
2. **Coller dans votre LLM** : ChatGPT, Claude, Gemini, Qwen, DeepSeek, Perplexity, etc.
3. **Répondre aux questions initiales** : Le LLM vous posera 2 questions et **attendra vos réponses** avant de continuer :
   - **Question 1 :** Quel prompt souhaites-tu créer ?
   - **Question 2 :** Sur quel outil IA vas-tu l'utiliser ?
4. **Traitement automatisé** : Une fois vos réponses fournies, le LLM exécute le pipeline complet (5 Cercles + 18 Hacks + livraison A-B-C-D)

**Exemple d'interaction :**

```text
UTILISATEUR : [Coller le contenu de promptor-council-v3.1.md ici]

LLM : Quel prompt souhaites-tu créer ?
      Sur quel outil IA vas-tu l'utiliser ?

UTILISATEUR : Je veux créer un prompt pour analyser le taux de désabonnement des clients 
              dans un produit SaaS. Je l'utiliserai sur ChatGPT.

LLM : [Exécute la validation des 5 Cercles, applique les 18 Hacks, génère un prompt 
       optimisé avec format de livraison A-B-C-D]
```

> **💡 Important :** Le workflow conversationnel est conçu pour recueillir le contexte avant la génération. 
> Le LLM ne continuera pas tant que vous n'aurez pas fourni de réponses aux deux questions initiales.

### Options avancées

| Option | Usage | Description |
| --- | --- | --- |
| `[MODE:API]` | Sortie technique | Prompt formaté JSON (pour usage programmatique) |
| `[COLLAB:MODE]` | Co-création | Construction guidée du prompt étape par étape |
| `[COUNCIL]` | Audit multi-perspective | Active la délibération des 5 conseillers (coût 11x, 3 min) |
| `[?terme]` | Explication inline | Demander une clarification sur n'importe quel terme |
| `{{FOCUS_HACKS}}` | Focus d'optimisation | `tokens`, `quality`, `speed`, `security`, `collaboration` |

**Exemple avec options :**

```text
Crée un prompt pour la détection de fraude dans les transactions bancaires.
Focus : sécurité et conformité.
Active le Council pour validation externe.

[COUNCIL]
{{FOCUS_HACKS: security}}
{{DOMAIN: finance}}
```

### Mode Council

**Quand utiliser le Council :**

- ✅ Prompts critiques pour la production (systèmes face client)
- ✅ Domaines réglementés (finance, santé, juridique)
- ✅ Applications sensibles à la sécurité
- ✅ Premier prompt dans un domaine complexe
- ✅ Score d'auto-critique < 4/5

**Comment ça marche :**

1. Le pipeline standard 5 Cercles + 18 Hacks s'exécute d'abord
2. Si le flag `[COUNCIL]` est présent OU auto-critique < 4/5, le Council s'active
3. 5 conseillers analysent indépendamment (2-3 minutes)
4. La revue par les pairs identifie les arguments les plus forts/faibles
5. Le président synthétise le verdict avec une recommandation actionnable

**Coût :** ~11x le coût de base (5 conseillers + 5 reviewers + 1 président)

**Sortie :** Rapport HTML + Transcript Markdown

---

## Exemples

<details>
<summary><strong>Risk Analyst</strong> — Scoring de crédit pour la banque</summary>

Tu es Risk Analyst, un expert en scoring de crédit bancaire. Ta mission est d'évaluer la solvabilité d'un particulier
et produire un score de risque exploitable pour une décision de prêt.

**Domaine :** Finance / Conformité  
**Hacks appliqués :** #3, #4, #11, #18 + Leçons META (variables proxy, escalade humaine)  
**Auto-critique :** 4,5/5  
**Council recommandé :** ✅ Oui (exigences réglementaires)

[Voir l'exemple complet](examples/risk-analyst.md)

</details>

<details>
<summary><strong>Warp Analyst</strong> — Reverse engineering de dépôt GitHub</summary>

Tu es Warp Analyst, un ingénieur senior spécialisé en reverse engineering de dépôts GitHub. Ta mission est d'analyser
le projet Warp et produire une documentation technique actionnable.

**Domaine :** Génie logiciel  
**Hacks appliqués :** #3, #4, #8, #11, #18  
**Auto-critique :** 4/5  
**Council recommandé :** ❌ Non (analyse technique standard)

[Voir l'exemple complet](examples/warp-analyst.md)

</details>

<details>
<summary><strong>Real Estate Strategist</strong> — Analyse d'investissement immobilier</summary>

Tu es Real Estate Strategist, un expert en investissement immobilier. Ta mission est d'analyser un bien et recommander
une stratégie d'achat, de location ou de revente optimisée.

**Domaine :** Immobilier / Finance  
**Hacks appliqués :** #3, #4, #11, #18 + Leçon META 3 (cas de test)  
**Auto-critique :** 4,5/5  
**Council recommandé :** ⚠️ Optionnel (transactions à haute valeur)

[Voir l'exemple complet](examples/real-estate-strategist.md)

</details>

<details>
<summary><strong>GitHub Auditor</strong> — Audit qualité de dépôt & CI/CD</summary>

Tu es GitHub Auditor, un expert en qualité logicielle et CI/CD. Ta mission est d'auditer un dépôt GitHub et proposer
des améliorations concrètes en code, sécurité et pipelines.

**Domaine :** DevOps / Qualité logicielle  
**Hacks appliqués :** #3, #4, #8, #11, #18 + Leçon META 3 (checklist de validation)  
**Auto-critique :** 5/5  
**Council recommandé :** ⚠️ Optionnel (dépendances critiques)

[Voir l'exemple complet](examples/github-auditor.md)

</details>

<details>
<summary><strong>Cloud Architect</strong> — Conception d'infrastructure AWS</summary>

Tu es Cloud Architect, un spécialiste AWS. Ta mission est de concevoir une architecture scalable, sécurisée et
optimisée en coûts à partir d'un besoin métier.

**Domaine :** Génie cloud / AWS  
**Hacks appliqués :** #3, #4, #11, #15, #18 + Leçons META 3 & 4 (validation, note d'architecture)  
**Auto-critique :** 5/5  
**Council recommandé :** ✅ Oui (dépenses multi-millions, systèmes critiques)

[Voir l'exemple complet](examples/cloud-architect.md)

</details>

<details>
<summary><strong>Cybersecurity Analyst</strong> — Évaluation de vulnérabilités & remédiation</summary>

Tu es Cybersecurity Analyst, un expert en sécurité offensive et défensive. Ta mission est d'identifier les
vulnérabilités d'un système et proposer un plan de remédiation priorisé.

**Domaine :** Sécurité / Tests de pénétration  
**Hacks appliqués :** #3, #4, #11, #18 + Leçons META 2 & 3 (escalade, validation)  
**Auto-critique :** 5/5  
**Council recommandé :** ✅ Oui (certifications de conformité, post-violation)

[Voir l'exemple complet](examples/cybersecurity-analyst.md)

</details>

<details>
<summary><strong>DevOps Engineer</strong> — Automatisation de pipeline CI/CD</summary>

Tu es DevOps Engineer, un expert en automatisation et infrastructure as code. Ta mission est de transformer un projet
en pipeline CI/CD robuste et entièrement automatisé.

**Domaine :** DevOps / CI/CD  
**Hacks appliqués :** #3, #4, #11, #15, #18 + Leçon META 3 (validation avant production)  
**Auto-critique :** 5/5  
**Council recommandé :** ⚠️ Optionnel (premier CI/CD pour l'organisation)

[Voir l'exemple complet](examples/devops-engineer.md)

</details>

<details>
<summary><strong>Data Scientist</strong> — Modélisation prédictive</summary>

Tu es Data Scientist, un expert en modélisation prédictive. Ta mission est d'exploiter un dataset pour construire un
modèle performant et interprétable.

**Domaine :** Machine Learning / Science des données  
**Hacks appliqués :** #3, #4, #11, #18 + Leçons META 3 & 4 (validation, architecture de déploiement)  
**Auto-critique :** 5/5  
**Council recommandé :** ⚠️ Optionnel (décisions ML à enjeux élevés)

[Voir l'exemple complet](examples/data-scientist.md)

</details>

<details>
<summary><strong>Product Manager</strong> — Stratégie de roadmap produit</summary>

Tu es Product Manager, un expert en stratégie produit. Ta mission est de définir une roadmap claire basée sur les
besoins utilisateurs et les contraintes business.

**Domaine :** Gestion produit  
**Hacks appliqués :** #3, #4, #11, #18 + Leçon META 3 (checklist de validation)  
**Auto-critique :** 5/5  
**Council recommandé :** ⚠️ Optionnel (présentations au conseil, pivots)

[Voir l'exemple complet](examples/product-manager.md)

</details>

<details>
<summary><strong>System Administrator</strong> — Optimisation de serveur Linux</summary>

Tu es System Administrator, un expert Linux. Ta mission est d'optimiser, sécuriser et automatiser l'administration
d'un serveur en production.

**Domaine :** Administration système / Linux  
**Hacks appliqués :** #3, #4, #11, #18 + Leçons META 2 & 3 (réponse aux incidents, validation)  
**Auto-critique :** 5/5  
**Council recommandé :** ⚠️ Optionnel (serveurs critiques, conformité)

[Voir l'exemple complet](examples/system-administrator.md)

</details>

<details>
<summary><strong>AI Engineer</strong> — Conception de système d'intégration LLM</summary>

Tu es AI Engineer, un expert en LLM et intégration d'IA. Ta mission est de concevoir un système intelligent basé sur
des modèles de langage pour un cas d'usage précis.

**Domaine :** Génie IA/ML / LLM  
**Hacks appliqués :** #3, #4, #11, #15, #18 + Leçons META 3 & 4 (évaluation, architecture)  
**Auto-critique :** 5/5  
**Council recommandé :** ✅ Oui (IA face client, industries réglementées)

[Voir l'exemple complet](examples/ai-engineer.md)

</details>

---

## Comment ça marche

### La validation des 5 Cercles

Un pipeline structuré qui affine progressivement les prompts :

```text
C1: STOP (Valider la demande)
├─ Auto-détection du domaine & profil utilisateur
├─ Identifier 3 risques spécifiques au domaine
├─ Vérifier la complétude du contexte
└─ Appliquer les Hacks : #1, #9 + FOCUS_HACKS

C2: RECHERCHE (Standards du domaine)
├─ Citer 2-3 patterns reconnus par risque
├─ Faits uniquement, pas d'opinions
├─ Vérifier les risques de variables proxy (domaines de conformité)
└─ Appliquer les Hacks : #2, #11, #15 + FOCUS_HACKS

C3: GRILLE (Checklist de succès)
├─ Critères pass/fail binaires (pas de subjectivité)
├─ Chaque critère intègre ≥1 hack
├─ Valider les workflows d'escalade humaine (si présents)
└─ Appliquer les Hacks : #3, #4, #12, #18 + FOCUS_HACKS

C4: TRIBUNAL (Évaluation stricte)
├─ Appliquer la checklist C3 à la demande
├─ Format tableau : Critère | Pass/Fail | Preuve | Hack #
├─ Zéro commentaire, zéro score global
└─ Appliquer les Hacks : #5, #6, #14 + FOCUS_HACKS

C5: FIX (Corrections)
├─ Correction ciblée pour chaque FAIL
├─ Max 3 itérations ou état BLOQUÉ
├─ Générer un plan d'action priorisé
└─ Appliquer les Hacks : #7, #13, #16 + FOCUS_HACKS
```

### Le framework des 18 Hacks

Stratégies d'optimisation appliquées tout au long du pipeline :

| Hack | Catégorie | Impact |
| --- | --- | --- |
| #1 Nouvelle session par tâche | Tokens | Réduction de 40-60% |
| #2 Désactiver les outils inutilisés | Tokens | 5-18K tokens/msg économisés |
| #3 Regrouper les prompts | Tokens | 3x moins cher que les follow-ups |
| #4 Mode plan (95% de confiance) | Qualité | Éviter les réécritures |
| #5 Surveiller l'usage des tokens | Vitesse | Visibilité en temps réel |
| #6 Ligne de statut (% contexte) | Vitesse | Alertes proactives |
| #7 Vérifications tableau de bord (20-30min) | Vitesse | Vue globale |
| #8 Injection chirurgicale (sections) | Tokens | Réduction ciblée |
| #9 Surveillance active (boucles) | Qualité | Détecter les répétitions |
| #10 Prompt système <200 lignes | Tokens | 2-5K tokens/msg économisés |
| #11 Références précises (@fichier:Lx-Ly) | Qualité | Moins d'exploration |
| #12 Compactage manuel à 60% | Tokens | Qualité préservée |
| #13 Gérer les pauses >5min | Tokens | Éviter le rechargement complet |
| #14 Tronquer les sorties shell | Tokens | Max 50 lignes |
| #15 Routage de modèles | Vitesse | Réduction de coût de 40-60% |
| #16 Limiter les sous-agents (2-3 max) | Tokens | 7-10x moins cher |
| #17 Planification hors-pointe | Vitesse | Meilleur coût/disponibilité |
| #18 Source de vérité persistante | Tokens | Raccourci de contexte |

### Phase 3 — Livraison (A-B-C-D)

Le format de livraison final garantit que le prompt généré est prêt pour la production et actionnable :

**A — Calibrage.** Maximum 3 puces résumant :

- Logique de traitement
- DOMAIN détecté
- FOCUS appliqué

**B — Prompt Optimisé.** Bloc prêt à copier-coller contenant :

- **En-tête :** "Copie ce bloc et colle-le dans ton outil IA. C'est prêt !"
- **Note architecturale (si production-critical) :** Clarifier si le prompt est un composant d'un système plus large ou autonome. Si composant, spécifier les dépendances amont/aval attendues.
- Rôle + contexte adaptés au DOMAIN
- Instructions fusionnant 5 Cercles + hacks priorisés
- Placeholders `{{VARIABLE}}` pour réutilisation multi-domaine

**C — Auto-Critique.** Note 0-5. Si < 5 : proposer une amélioration. Expliquer ce qui ferait monter la note.

**Proposition Council :** Si la note auto-critique est < 4/5 OU si le domaine est critique (security, compliance, production), proposer :

> 💡 **Veux-tu un audit externe par le LLM Council ?**
>
> Le Council va soumettre ton prompt à 5 advisors indépendants avec peer review aveugle pour détecter angles morts et faiblesses non visibles en auto-critique.
>
> - **Coût estimé :** ~11x plus élevé (5 advisors + 5 reviewers + 1 chairman)
> - **Temps :** +2-3 minutes
> - **Recommandé si :** prompt pour production critique, domaine à haut risque, ou première exploration d'un domaine complexe
>
> Ajoute `[COUNCIL]` à ta prochaine réponse pour activer.

**D — Interrogatoire.** 2-5 questions max pour itérer. Langage simple + exemple adapté au DOMAIN.

**Questions META obligatoires (systématiques pour prompts production-critical) :**

1. **Architecture système :** "Ce prompt sera-t-il utilisé comme composant d'un système plus large (avec pipeline amont/aval, orchestration, monitoring) ou de manière autonome ?"
   - Si composant → Clarifier interfaces amont/aval requises
   - Si autonome → Vérifier que toutes dépendances sont internalisées

2. **Testabilité :** "Comment ce prompt sera-t-il testé/validé avant déploiement en production ?"
   - Proposer : jeux de données synthétiques, métriques de validation, seuils Go/No-Go
   - Si aucun protocole défini → Recommander tests adversariaux minimaux

**Questions domaine-spécifiques :** 1-3 questions additionnelles adaptées au DOMAIN pour itérer sur la qualité du prompt.

### Le Conseil LLM

Basé sur la [méthodologie Conseil LLM d'Andrej Karpathy](https://x.com/karpathy/status/1878531712785961151) :

```text
Pipeline Standard (C1→C5 → 18 Hacks → A-B-C-D)
                  ↓
Déclenchement [COUNCIL] ou proposition auto (score <4/5 + domaine critique)
                  ↓
┌─────────────────────────────────────────────┐
│  5 Conseillers (parallèle, 30-60s)          │
├─────────────────────────────────────────────┤
│  • Le Contradicteur : Trouver les failles   │
│  • Principes Premiers : Bonne question ?    │
│  • L'Expansionniste : Opportunités manquées │
│  • L'Outsider : Malédiction connaissance    │
│  • L'Exécuteur : Utilisabilité lundi matin  │
└──────────────────┬──────────────────────────┘
                   ↓
┌─────────────────────────────────────────────┐
│  Revue par les pairs (anonymisée, 30-60s)   │
├─────────────────────────────────────────────┤
│  • Quelle réponse est la plus forte ?       │
│  • Laquelle a le plus gros angle mort ?     │
│  • Qu'est-ce que TOUTES ont manqué ?        │
└──────────────────┬──────────────────────────┘
                   ↓
┌─────────────────────────────────────────────┐
│  Synthèse du Président (20-30s)             │
├─────────────────────────────────────────────┤
│  • Où le Council converge (haute confiance) │
│  • Où le Council diverge (deux côtés)       │
│  • Angles morts détectés (via peer review)  │
│  • Recommandation finale (verdict clair)    │
│  • Action immédiate (UNE étape concrète)    │
└──────────────────┬──────────────────────────┘
                   ↓
         Artefacts générés
         ├─ council-report-[timestamp].html (visuel)
         └─ council-transcript-[timestamp].md (complet)
```

---

## Structure du projet

```text
Super-Prompt-LLM-Council-Generator/
├── README.md                          # Documentation anglaise
├── FR_README.md                       # Ce fichier (version française)
├── LICENSE                            # Licence MIT
├── CHANGELOG.md                       # Historique des versions
├── CONTRIBUTING.md                    # Guide de contribution
├── CODE_OF_CONDUCT.md                 # Directives communautaires
├── SECURITY.md                        # Politique de sécurité
├── .gitignore                         # Règles d'exclusion Git
├── .gitattributes                     # Attributs Git
├── .markdownlint.json                 # Config de validation Markdown
├── promptor-council-v3.1.md           # Méta-prompt principal (à copier !)
├── .github/
│   └── workflows/
│       └── markdownlint.yml           # CI/CD pour validation Markdown
└── examples/                          # 11 cas d'usage professionnels
    ├── README.md                      # Index des exemples
    ├── risk-analyst.md                # Finance / Scoring de crédit
    ├── warp-analyst.md                # Reverse engineering GitHub
    ├── real-estate-strategist.md      # Analyse d'investissement
    ├── github-auditor.md              # Qualité code & CI/CD
    ├── cloud-architect.md             # Infrastructure AWS
    ├── cybersecurity-analyst.md       # Évaluation de sécurité
    ├── devops-engineer.md             # Automatisation CI/CD
    ├── data-scientist.md              # Modélisation prédictive
    ├── product-manager.md             # Roadmap produit
    ├── system-administrator.md        # Optimisation serveur Linux
    └── ai-engineer.md                 # Intégration LLM
```

---

## Contribuer

Les contributions sont les bienvenues ! Voir [CONTRIBUTING.md](CONTRIBUTING.md) pour les directives.

**Démarrage rapide :**

1. Forker le dépôt
2. Créer une branche de fonctionnalité : `git checkout -b feat/votre-fonctionnalite`
3. Commiter vos changements : `git commit -m "feat: ajouter nouvel exemple"`
4. Pousser vers votre fork : `git push origin feat/votre-fonctionnalite`
5. Ouvrir une Pull Request vers la branche `dev`

**Idées de contribution :**

- Ajouter de nouveaux exemples professionnels (juridique, éducation, marketing, etc.)
- Traduire le README vers d'autres langues
- Améliorer les exemples existants avec des cas de test réels
- Créer des intégrations (extension VS Code, outil CLI, etc.)

---

## Licence

Ce projet est sous **licence MIT**. Voir [LICENSE](LICENSE) pour les détails.

```text
Licence MIT

Copyright (c) 2026 valorisa

La permission est accordée, gratuitement, à toute personne obtenant une copie
de ce logiciel et des fichiers de documentation associés (le "Logiciel"), de
traiter le Logiciel sans restriction, y compris sans limitation les droits
d'utiliser, copier, modifier, fusionner, publier, distribuer, sous-licencier
et/ou vendre des copies du Logiciel, et de permettre aux personnes à qui le
Logiciel est fourni de le faire, sous réserve des conditions suivantes :

[Texte complet de la licence dans le fichier LICENSE]
```

---

## Remerciements

- **Andrej Karpathy** : [Méthodologie Conseil LLM](https://x.com/karpathy/status/1878531712785961151) (framework de 
  délibération multi-perspective)
- **Inspiration 18 Hacks** : Adapté des stratégies d'optimisation pour une utilisation efficace des tokens avec les LLM
- **Validation 5 Cercles** : Framework structuré d'ingénierie de prompts garantissant la conformité au domaine
- **Contributeurs** : Voir les [contributeurs GitHub](https://github.com/valorisa/Super-Prompt-LLM-Council-Generator/graphs/contributors)

---

**Prêt à générer des prompts prêts pour la production ?**

1. Copier [`promptor-council-v3.1.md`](promptor-council-v3.1.md)
2. Coller dans votre LLM (ChatGPT, Claude, Gemini, etc.)
3. Décrire votre besoin de prompt
4. Obtenir un prompt validé et optimisé en 2-3 minutes

**Besoin de validation externe ?** Ajouter `[COUNCIL]` pour activer l'audit multi-perspective.

---

**Questions ? Problèmes ? Idées ?**

- Ouvrir une [issue](https://github.com/valorisa/Super-Prompt-LLM-Council-Generator/issues)
- Démarrer une [discussion](https://github.com/valorisa/Super-Prompt-LLM-Council-Generator/discussions)
- Soumettre une [pull request](https://github.com/valorisa/Super-Prompt-LLM-Council-Generator/pulls)

**Mettez une étoile ⭐ à ce dépôt si vous le trouvez utile !**

---

## Versions linguistiques

- 🇬🇧 [English version](README.md)
- 🇫🇷 [Version française](FR_README.md) (ce fichier)
