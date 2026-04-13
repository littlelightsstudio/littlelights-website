# Claude Code Skills Setup
**Kuratierte Skill-Liste für Web-Projekte | Stand: April 2026**

---

## Installation (alle auf einmal)

```bash
npx skills add anthropics/claude-code --skill frontend-design --yes
npx skills add https://github.com/coreyhaines31/marketingskills --yes
npx skills add https://github.com/browser-use/browser-use --skill browser-use --yes
npx skills add https://github.com/valyuai/skills --skill valyu-best-practices --yes
npx skills add https://github.com/coleam00/excalidraw-diagram-skill --skill excalidraw-diagram --yes
npx skills add vercel-labs/agent-skills --yes
npx skills add nextlevelbuilder/ui-ux-pro-max-skill --yes
```

## Aufräumen (irrelevante Skills entfernen)

Das Marketing-Paket installiert viele Skills die nicht für jedes Projekt relevant sind. Folgende entfernen:

```bash
for skill in ab-test-setup ad-creative churn-prevention cold-email competitor-alternatives email-sequence free-tool-strategy launch-strategy marketing-ideas marketing-psychology onboarding-cro paid-ads paywall-upgrade-cro popup-cro pricing-strategy product-marketing-context programmatic-seo referral-program revops sales-enablement signup-flow-cro deploy-to-vercel vercel-cli-with-tokens vercel-react-native-skills; do
  rm -rf ".agents/skills/$skill"
done
```

Nach Installation: **Claude Code neu starten.**

---

## 28 Skills nach Kategorie

### Design & UI
| Skill | Quelle | Funktion |
|-------|--------|----------|
| frontend-design | anthropics/claude-code | Prototyping, UI-Komponenten, Design-System |
| ui-ux-pro-max | nextlevelbuilder | UX-Entscheidungen, Interaktionsdesign |
| ckm:design | nextlevelbuilder | Design-Prinzipien und Patterns |
| ckm:design-system | nextlevelbuilder | Konsistentes Design-System aufbauen |
| ckm:ui-styling | nextlevelbuilder | CSS/Tailwind Styling Best Practices |
| ckm:brand | nextlevelbuilder | Brand Identity Guidelines |
| ckm:banner-design | nextlevelbuilder | Banner und Hero Design |
| ckm:slides | nextlevelbuilder | Präsentations-Design |
| web-design-guidelines | vercel-labs | Web Design Standards und Patterns |
| excalidraw-diagram | coleam00 | Wireframes und Architektur-Diagramme |

### SEO & Analytics
| Skill | Quelle | Funktion |
|-------|--------|----------|
| ai-seo | coreyhaines31 | GEO-Optimierung (AI Search) |
| seo-audit | coreyhaines31 | SEO-Check und Audit |
| schema-markup | coreyhaines31 | Strukturierte Daten (JSON-LD) |
| analytics-tracking | coreyhaines31 | Analytics Setup und Tracking |
| site-architecture | coreyhaines31 | Seitenstruktur und Informationsarchitektur |

### Content & Copy
| Skill | Quelle | Funktion |
|-------|--------|----------|
| copywriting | coreyhaines31 | Texte schreiben (Headlines, Body, CTAs) |
| copy-editing | coreyhaines31 | Texte reviewen und verbessern |
| content-strategy | coreyhaines31 | Content-Planung und Strategie |
| social-content | coreyhaines31 | Social Media Content erstellen |
| lead-magnets | coreyhaines31 | Lead-Magnet Konzeption |
| customer-research | coreyhaines31 | Zielgruppen-Analyse |

### CRO (Conversion Rate Optimization)
| Skill | Quelle | Funktion |
|-------|--------|----------|
| page-cro | coreyhaines31 | Seiten-Conversion optimieren |
| form-cro | coreyhaines31 | Formulare optimieren |

### Development
| Skill | Quelle | Funktion |
|-------|--------|----------|
| vercel-react-best-practices | vercel-labs | Next.js/React Best Practices |
| vercel-composition-patterns | vercel-labs | Komponenten-Architektur |
| vercel-react-view-transitions | vercel-labs | Seitenübergänge und Animationen |
| valyu-best-practices | valyuai | Code-Qualität und Best Practices |
| browser-use | browser-use | Automatisiertes Browser-Testing |